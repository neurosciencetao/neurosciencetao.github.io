---
layout: post
title: "A super brief E-prime tutorial"
date: 2017-01-19
---
This is a E-prime tutorial to show you how to build experiments from zero (but assuming you have E-prime 2.0 installed on your computer). Basically I write this tutorial to show my colleagues how to build psychological and linguistic experiments with E-prime and also to tell future me how to do this in case I forget.

# Why another tutorial?

There are a lot of E-prime tutorials out there, so why another tutorial?

I love those simple but informative tutorials. Those tutorials allow you to achieve something immediately and give you nice starting points. I aim to write such an easy to follow instruction, along which you only need to drag and drop the objects (most of the time) to build the experiment.

> NOTES: I will explain some 'critical concepts' for experiment design and program during you reading this tutorial. But these explanations can be safely ignored without prohibiting you accomplish this tutorial. You can always come back later.

I hope you will enjoy : )

# Start up

E-prime is an psychological stimuli presentation software made by [PST](https://www.pstnet.com/).
It has several functional modules, as shown in the program folder.

![folder](/img/EprimeTutorial/folder.png)

Here in this tutorial you will only need the E-studio module.

>NOTES:
E-prime only supports windows system.
E-prime 1.x and 2.x are best supported by windows 7 or earlier.
E-prime 3.0 is released recently and supports windows 10.
If you want to do experiments using linux operation system,
Matlab (Psychtoolbox) and Python (e.g. OpenSesame) are nice choices.

The welcome screen of E-prime will be like this

![start up window](/img/EprimeTutorial/Startup.png)

In the toolbox, there are 11 objects. Here we are going to use the following

  * `TextDisplay`
  * `List`
  * `Procedure`

throughout this tutorial, category names of objects and properties will be shown in `code format`, i.e. white font on grey background. A specific **object or property name** will be shown in bold. the _value of a property_ will shown in italic.

# First, a trial

Here we use a bottom-up method to build the experiment.

As we are replicating the procedure used in this article, we have a well designed procedure already. For a single trial, it includes

  * a fixation presented for 500 ms
  * a prime presented for 270 ms
  * a blank screen presented for 100 ms
  * a target for judgement presented for 2500 ms
  * and a post target blank screen presented for 1000 ms

These five parts of a trial can be realized by the same object, the `TextDisplay` object. We double click the `SessionProc` in the structure window, then another window pop out with a title _SessionProc_ and a line in it. We then click, hold, drag, and drop the `TextDisplay` object onto the line and a `TextDisplay` object appears on the line, with a name _TextDisplay1_. We do it another 4 times until we have _TextDisplay5_. Right click the _TextDisplay1_ and Rename it to _Fixation_. It is important to rename the objects with a meaningful name, so it will be obvious what function it does. Rename the rest four to

  * Prime
  * Blank
  * Target
  * ITI (which stands for inter trial interval)

Now we have a trial built. You should have this

[one trial](/img/EprimeTutorial/OneTrial.png)

We are going to **modify properties of the objects** according to our design.
For the first object, Fixation, we are going to make it showing a fixation, which is

  * a cross
  * in the middle of the screen
  * with a font size of 20
  * for 500 ms

We will modify these properties one by one. By douby and exact informationclicking the **Fixation object**, we access the property page. It looks like these.

[property page](/img/EprimeTutorial/PropertyPage.png)

The property page have several subpages, including

  * font
  * duration
  * etc

In the font page we choose font size 20. The original article used Geneva as the font, however we do not have it installed on our computer, so we choose Courior instead.

Then, we modify the properties of other four objects according to the table.

>make a table Here

As you have modified all the properties, there is still one more modification to make. We have to specify how we will collect the reaction time! Go back to the property page of `target`. In the `Duration` page, we have set the duration to 2500 ms. Now we click add device, and choose Keyboard. On the right side, type in `[correct]` in the correct column. Click the `end action` and choose `terminate`.

>explanations on duration page, data collection, end action, etc.

Great, we have a well made trial. Remember to save what you have frequently. Now we actually can run this program, although it has only one trial. Press `F5` and enter a subject number and session number. If you have followed the previous steps, you should see the five elements shown ordinally on the screen. Next step, we are going to make multi-trials.

# make a list!
As a researcher, we want our participant to do the trial response for, say, 4 times. We have told the computer how to show a single trial. Now we should tell it how to do it for 4 times.

In E-prime, we do this by using `List`. A `List` can be thought as a to-do list. It is well orgnized and contains every infomation the computer needs to do what we want it to do. Because computers are inflexible, you have to tell it all the neccessary and exact information it needs.

1. Drag and drop a `List` object to the front of `SessionProc` line, as we operated the `TextDisplay` object.
2. Rename it *ExpBlock*. (Or any other meaningful names)
3. Double click the object to enter the property page.

You will notice `List` has a quite different property page as `TextDisplay`. On the lower part, it has a table. Each row stands for a trial, so we are going to make it 4. Each column stands for a attribute, which contains information the trials need. On the upper part, it has 5 icons. From left to right, they are

- add one trial
- add one attribute
- add multi-attributes


4. Click `add multi-trials` icon, input 3, and press `Enter`.
5. Click `add multi-attributes` icon, input 3, and press `Enter`.
6. On the lower part table, click attribute 1 and rename it to `prime`.

You might notice, and you are right. This attribute `prime` **is** the `[prime]` we input earlier in the `Prime` object.

7. input the prime words in each column under the `prime` attribute. But in this stage, to make our workflow smoother, we just input numbers 1 to 4 in the columns.
8. rename the rest attributes target and correct.
9. input word one to four for the `target` attribute.
10. input the letter `z` for the `correct` attribute, because we want participants to use z key for a correct response. But you can input another key if you want.

>about special keys and function keys.
about mouse.

Now, we are going to make the most critical modification for the `List`.
11. Click the `Procedure` attribute and input `TrialProc`.

If E-prime ask if you want to make this procedure default, choose yes. If E-prime says `TrialProc` does not exist, and asking for your permittion to create it, choose yes.

12. Drag and drop the five `TextDisplay` objects, `fixation`, `prime`, `blank`, `target`, and `ITI`, accordingly from `SessionProc` to `TrialProc`.
13. Delete the five `TextDisplay` objects on `SessionProc`.

>You may notice the deleted objects at the end of the structure.
They are not permanently deleted, thus can be reused.
The obejects, especially `List`, in the end of the structure may have special usage.
However, delete them from the end of the structure if you want to permanently delete them.

Now you can run the experiment again to see if everything works.

# make the practice session

A linguistic study usually has a practice session. As we have well made the experiment session, it is easy to make a practice session.

Do the same thing as when you make up the `ExpBlock`. The differences are
1. rename the `List` to `PracBlock`;
2. choose `TrialProc` for the `procedure` attribute, but you do not have to make futher modification to the `TrialProc`.

Now save and run the script again. It will go smoothly if you do everything right.

>We have been running the experiment for several times during this tutorial.
Actually it is important to test what you have before you move on.
With the growth of the script it becomes harder to debug.
It is important to make sure the elements are built right.

# a few more modification
I guess you have noticed

# What next?
