---
# title: "<i>nutzen.guard@2.0.6</i> - .this points to instance."
archiveTitle: "<i>nutzen@2.0.6</i> - <i>.guard's</i> .this points to object data."
date: "2023-06-27"
tags: ["nutzen","algebraic data types","livescript"]
author: "sourcevault"
# author: ["Me", "You"] # multiple authors
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
# description:
# disableHLJS: false # to disable highlightjs
disableShare: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: false
---

# `nutzen@2.0.6` 
- **`nutzen.guard` `.this` variable now points to object instance.**

All functions defined within `nutzen.guard` now have the `.this` point to the calling instance's value, this has special usecase when we are dealing with object models that require handling large number of state values.

A simple vanilla javascript example will make things clear:

```js
var tank = {}

tank.move = function(x,y)
{
 this.x  = this.x + x
 this.y  = this.y + y
}

tank.shoot = function(round_type = "apcr")
{
  internal_shell = this.shell

  if (internal_shell[round_type] <= 0)
  {
    console.log("no more " + round_type + ", tank has run out of ammo !")
  }
  else
  {
    internal_shell[round_type] = internal_shell[round_type] - 1
  }
}

var ins_bare  = Object.create(tank)

var self_data = {
    x:0,
    y:0,
    shell:
        heat: 10,
        apcr: 10 // armour piercing rounds
    }

var tank_1 = Object.assign(ins_bare,self_data)

```
In our example we have a tank object class with two prototype function describing the behavior `move` and `shoot`.

The issue with the code above is error handling is tied together with application logic, the reason for introducing guards and pattern matching in the first place is so that we can keep these concerns seperate to one another.

We are now going to now add guards to refactor the code to put error handling in a seperate function:

```js
var nutzen = require("nutzen")

hop = nutzen.guard


var move = {}

var shoot = {}

// 1. move methods

move.main = function(x,y)
{
 this.x  = this.x + x
 this.y  = this.y + y
}

move.err = function()
{
  console.log("Argument Error (move) : requires mininum of 2 arguments (x,y).")
}

shoot.check_arg = function(rt)
{

  if ((rt == "aprc") || (rt == "heat"))
    return true
  else
    return false
}

// 2. shoot methods

shoot.main = function(round_type = "apcr")
{
  internal_shell = this.shell

  if (internal_shell[round_type] <= 0)
  {
    console.log("no more " + round_type + ", tank has run out of ammo !")
  }
  else
  {
    internal_shell[round_type] = internal_shell[round_type] - 1
  }
}

shoot.err = function()
{
  console.log("Argument Error (shoot): incorrect value.")
}

// bringing everything together

var tank = {}

tank.move = hop.ar(2,move.main).def(move.err)

tank.shoot = hop.arwh(1,shoot.check_arg,shoot.main).def(shoot.err)

var instance_bare  = Object.create(tank)

var mutating_data = {
    x:0,
    y:0,
    shell:
        heat: 10,
        apcr: 10 // armour piercing rounds
    }

var tank_1 = Object.assign(instance_bare,mutating_data)

```

In the code using `nutzen.guard` the application logic and error handling is cleanly seperated.

As the complexity of our object grows, we can even move the application logic and error handling into two seperate files (e.g `core.ls` and `error.ls`).

Using guards removes all the error-handling clutter from the main part of our code.