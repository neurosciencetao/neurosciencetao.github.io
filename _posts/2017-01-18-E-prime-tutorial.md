---
layout: post
title: "TEST"
date: 2017-01-19
---

# Why another tutorial?
There are a lot of E-prime tutorials out there, so why another tutorial?
Basically I write this tutorial to show my collegues how to build E-prime experiments and also to tell future me how to do this in case I forget. I aim to write an easy to follow instruction, along which you only need to drag and drop the objects (most of the time) to build the experiment. So you can build up an real experiment with reading this tutorial.

>I will explain those 'critical concepts' for experiment design and program during you reading this tutorial. But these explanations can be safely ignored without prohibiting you accomplish this tutorial. You can always come back later.

I hope you will enjoy:)

# Start up
E-prime is an psychological stimuli presentation software made by [PST](https://www.pstnet.com/).
It has several functional modules, as shown in the program folder.
![folder](/img/EprimeTutorial/folder.png)

Here in this tutorial you will only need the E-studio module.

I assume you have installed E-prime 2.0 on your computer. The welcome screen of E-prime will be like this
![start up window](/img/EprimeTutorial/Startup.png)

In the toolbox, there are 11 objects. Here we are going to use the following

  * TextDisplay
  * List
  * Procedure

# First, a trial
Here we use a bottom up method to build the experiment.
As we are replicating the procedure used in this article, we have a well designed procedure already. For a single trial, it includes

  * a fixation presented for 500 ms
  * a prime presented for 270 ms
  * a blank screen presented for 100 ms
  * a target for judgement presented for 2500 ms
  * and a post target blank screen presented for 1000 ms

These five parts of a trial can be realized by the same object, the 'TextDisplay' object. We double click the 'SessionProc' in the structure window, then another window pop out with a title SessionProc and a line in it. We then click, hold, drag, and drop the 'TextDisplay' object onto the line and a 'TextDisplay' object appears on the line, with a name _TextDisplay1_. We do it another 4 times until we have _TextDisplay5_. Right click the _TextDisplay1_ and Rename it to _Fixation_. It is important to rename the objects with a meaningful name, so it will be obvious what function it does. Rename the rest four

  * Prime
  * Blank
  * Target
  * ITI (which stands for inter trial interval)

Great, now we have the trials built. We are going to modify properties of the objects according to our design.
For the first object, Fixation, we are going to make it showing a fixation, which is

  * a cross
  * in the middle of the screen
  * with a font size of 20
  * for 500 ms

We will modify these properties one by one. By clicking the this icon, we access the property page. It looks like these. The property page have several subpages, including
s
  * font
  * duration
  * etc
In the font page we choose font size 20. The original article used Geneva as the font, however we do not have it installed on our computer, so we choose Courior instead.

**modify the properties**

# make a list!

# make the practice session

# run a test

# a few more modification

# What next?
