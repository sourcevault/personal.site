---
title: symbol lookup performance
date: "2023-01-04"
# weight: 1
tags: [javascript,performance]
author: " "
# author: ["Me", "You"] # multiple authors
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
# description: description
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
js: https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.2.0/languages/livescript.min.js
---

In javascript symbols can be used as keys to store private values like so:

```js
sig = Symbol "self"

ob = {}

ob.self = null

ob[sig] = null

symbol_look = function()
{
  ob[sig] = Math.random()
}
normal_look = function()
{
  ob.self = Math.random()
}
```
The private value `self` is accessible publicly while the one using `sig` is not, I was curious to know if there was significant performance penalty for using symbols.

```
symbol_look x 56,957,738 ops/sec ±1.49% (85 runs sampled)
normal_look x 57,632,100 ops/sec ±1.81% (87 runs sampled)
```

In my tests using [`benchmark.js`](https://benchmarkjs.com/) it seemed there was none, so if you are in a stuck in a situation where you have to choose but are concerned about the performance penalty, you can rest assured it will not be a problem.
