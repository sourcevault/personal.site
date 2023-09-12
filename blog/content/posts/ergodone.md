---
title: "Ergodone"
date: "2023-06-28"
tags: [
    "repetitive strain injury",
    "keyboard",
    "KRepublic.com",
    "ergonomics"
    ]
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

*Keyboard-maxing for coding.*

{{< figure src="./keyboard.jpg#center" width="60%">}}

My current keyboard is an Ergodone with Durock T1 Shrimp switches, the post contains some of my initial thoughts about the Ergodone PCB, using customized layout ([FRU_76](https://github.com/sourcevault/FRU_76),[FRU_68](https://github.com/sourcevault/FRU_68)) and how to build it.

- [Switches](#switches)
   - [Comparison]()
   - [Applying Lube]()
- [Customized Layout](#customized-layout)
    - [(*FRU_76*) - Ergodone](#customized-layout)
    - [(*FRU_68*) - Kinesis Advantage](#customized-layout)
- [Building the Ergodone]()
    - [Components and Tooling]()
    - [Soldering (PCB)](#Soldering)
    - [Desoldering](#Desoldering)
    - [Double Press]()

**TLDR:** Moving to a customized keyboard has a **steep** price in terms of time and money, but worth seriously considering you spend +5 hours a day typing.

I used to use a [Kinesis Advantage 2](https://kinesis-ergo.com/shop/advantage2/) before trying out the Ergodone, I liked the original Kinesis Advantage so much that I have 3 of them. I purchased my first Kinesis Advantage while dealing with RSI and during that time I knew about the [ErgoDox EZ](https://ergodox-ez.com/) ( which was similar to the Ergodone ) but it was too expensive and risky to get your hands on it, the shipping cost alone was prohibitive. Since I considered the ErgoDox EZ a better design, I knew one day when I had enough money and time, the story for the Kinesis Advantage will have to come to an end.

During those days, you could get used Kinesis Advantage at half the price from Ebay. Hence, two of my Kinesis™ are *used* Kinesis Advantage 1. The third one is brand new Advantage 2, which I was forced to buy as some of the keys on the Advantage 1 stopped working, and there was no cheap and fast way to fix it.

The first issue around using the Kinesis Advantage keyboard is that it's too **bulky** to be used on the go. It takes up all the space in your Rucksack. Even for long trips where you have more options for luggage, it still takes up half the space in the largest suitcase you are allowed to check in on an aeroplane.

The Ergodone is a split design keyboard like the Advantage 1 and 2, but unlike them, the left and right side are physically separated. It's actual closest match among the Kinesis family of keyboard is the newer [Advantage 360](https://kinesis-ergo.com/keyboards/advantage360/). The only design difference between them and the Ergodone is that it lacks a more ergonomic dome shape, for that trade off however, it means it gets to be more compact.

The second issue with the Kinesis™ is **repairability**. The Kinesis™ line of keyboards are not created to be easy to repair on your own; this has important implications. If you cannot put up with any interruption in your work, even for a day, then you will need to keep a secondary keyboard *just as a backup*. If you live in areas with poor access to international shipping, then even the wonderful customer service of Kinesis™ will not be able to help you overcome logistical issues. The chance of something going wrong with any electronics device is quite high, as what happened with my first Advantage 1 - granted it was a used one.

With modern electronic device you never know when they go from a luxury to a dependency, and once you reach dependancy it is hard to switch to a different device once you are accustomed to it. The issue around ease of repair does not only apply to the Kinesis™, but is more of a general concern with any electronic device you use ( phones, laptop, etc), so ease of repair should be given priority. Ideally, you should be able to source all it's replacement parts and repair it on your own. *If you live in a country that is heavily sanctioned, or a country with high import tariff on foreign goods, then this point cannot be emphasized enough.*


### Switches

The variety of mechanical switches have exploded over the past half decade, and there is no way for a single person to try them all, even though that would be ideal. For now, you just have buy a couple of switches and try it, which tends to very quickly add up how much money you are spending behind your keyboard, and leaves behind a deep hole in your pocket. 

The best option for now is to find online review of switches you are interested in (if they exist at all). In my own personal trials, I can with certainty only compare **three** switches that I have used as a **full set**, but I will also mention the tester switches I have tried.

Even if you are left behind with a lot of extra switches, there is one way that you can make them useful and that is to scavenge them for parts. In my case, I had issues with double presses due to a poor soldering job on the ouside connector terminals. 

The Cherry MX Brown on the Kinesis Advantage is a good starter switch, *if you have not tried any other switches*. 

### Customized Layout

I have been using customized keyboard layout for half a decade, and once you move to one and experience the level of comfort, it feels barbaric to return to standard layout. I was forced to try and use one due to dealing with RSI 

{{< figure src="./layout_ergodox.png#center" width="95%">}}

<center> › FRU_76 layout used on Ergodone, covers English, French and Russian symbols. </center>

{{< figure src="./layout_kinesis.png#center" width="95%">}}

<center> › Initial FRU design with 68 keys used on the Kinesis Advantage. </center>

{{< figure src="./pano_table.jpg#center" width="95%">}}

<center> › Split keyboard allows you to keep your microphone closet to your face without obstructing your view, but also add a second multi-purpose area on top of your keyboard to be used for keeping your phone, or writing on physical paper. </center>