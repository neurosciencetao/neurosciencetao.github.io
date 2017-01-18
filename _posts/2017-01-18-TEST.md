---
layout: post
title: "A super brief tutorial for E-prime"
date: 2017-01-13
---

<h1>Why another tutorial?</h1>
<p>There are a lot of E-prime tutorials out there, so why another tutorial?
Basically I write this tutorial to show my collegues how to build E-prime experiments and also to tell future me how to do this in case I forget. I aim to write an easy to follow instruction, along which you only need to drag and drop the objects (most of the time) to build the experiment. So you can really write up an experiment with reading this tutorial. I will explain those critical concepts for experiment design and program during you reading this tutorial. I hope you will enjoy:)</p>

<h1>Start up</h1>
<p>E-prime is an psychological stimuli presentation software made by PST.
It has several functional modules, including
<img url="">
Here in this tutorial you will only need the E-studio module.

I assume you have installed E-prime 2.0 on your computer. The welcome screen of E-prime will be like this
<img url="">

In the toolbox, there are 11 objects. Here we are going to use the following
<ul>
  <li>TextDisplay</li>
  <li>List</li>
  <li>Procedure</li>
</ul>
</p>
<h1>First, a trial.</h1>
<p>Here we use a bottum up method to build the experiment.
As we are replicating the procedure used in this article, we have a well designed procedure already. For a single trial, it includes
<ul>
  <li>a fixation presented for 500 ms</li>
  <li>a prime presented for 270 ms</li>
  <li>a blank screen presented for 100 ms</li>
  <li>a target for judgement presented for 2500 ms</li>
  <li>and a post target blank screen presented for 1000 ms</li>
</ul>

These five parts of a trial can be realized by the same object, the TextDisplay object. We double click the SessionProc in the structure window, then another window pop out with a title SessionProc and a line in it. We then click, hold, drag, and drop the TextDisplay object onto the line and a TextDisplay object appears on the line, with a name "TextDisplay1". We do it another 4 times until we have "TextDisplay5". Right clike the TextDisplay1 and Rename it to "Fixation". It is important to rename the objects with a meaningful name, so it will be obvious what function it does. Rename the rest four to
<ul>
  <li>Prime</li>
  <li>Blank</li>
  <li>Target</li>
  <li>ITI (which stands for inter trial interval)</li>
</ul>

Great, now we have the trials built. We are going to modify properties of the objects according to our design.
For the first object, Fixation, we are going to make it showing a fixation, a cross, in the middle of the screen, with a font size 20 for 500 ms.
</p>
