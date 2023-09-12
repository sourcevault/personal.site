---
title: regular expression with hoplon.types
date: "2021-08-06"
tags: ["hoplon","algebraic data types","livescript"]
author: "sourcevault"
# author: ["Me", "You"] # multiple authors
showToc: false
TocOpen: false
draft: true
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

Javascript is filled with functions whose return values will always cause you to bang your head against the wall.

The built-in `.exec` found with regular expressions is just one of those functions.

Why you ask ? well let's see an example.

```ls
re = /hello/


re.exec "hello world"

re.exec "world" # returns null

```