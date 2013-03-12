Background
==========

This Kata was originally created by Terry Hughes (http://twitter.com/#!/TerryHughes).

Pre-requisites
==============

1. Install GIT (http://git-scm.com/)
2. Create directory where to keep local copy of your project
3. Sync down the code.
    $> git clone https://github.com/jonolo6/GildedRose.git
4. Import the project into your IDE
5. Install an Automatic test runner
	- http://infinitest.github.com/ or http://junitmax.com/

How to use this Kata
====================

You have to follow the TDD rules below to the best of your ability when working on this project:

1. You are not allowed to write any production code (anything under /src) unless it is to make a failing unit test pass.
2. You are not allowed to write any more of a unit test than is sufficient to fail; and compilation failures are failures.
3. You are not allowed to write any more production code (anything under /src) than is sufficient to pass the one failing unit test.

You have to follow the TDD flow below to the best of your ability when working on this project:

1. Write a failing test
2. Write code to make the test pass
3. Refactor the code.

The idea of the exercise is to do some deliberate practice, and improve your Refactoring skills. The idea is not to re-write the code from scratch, but rather to practice taking small steps, running the tests often, and incrementally improving the design.

Before you start
================

Tips: 

* Let the IDEA do the work for you - creating tests (CMD - Shift - T in IntelliJ for instance)
* Refactor is the most important step to allow the code to grow well and nicely. 
	Take the time to refactor both source and test code in the TDD cycle.
* A Unit test should only test the class - mock all other dependencies using Mockito, etc.

Gilded Rose Requirements
========================

Hi and welcome to team Gilded Rose. As you know, we are a small inn with a prime location in a prominent city ran by a friendly innkeeper named Allison. We also buy and sell only the finest goods. Unfortunately, our goods are constantly degrading in quality as they approach their sell by date. We have a system in place that updates our inventory for us. It was developed by a no-nonsense type named Leeroy, who has moved on to new adventures. Your task is to add the new feature to our system so that we can begin selling a new category of items. First an introduction to our system:

    All items have a SellIn value which denotes the number of days we have to sell the item
    All items have a Quality value which denotes how valuable the item is
    At the end of each day our system lowers both values for every item

Pretty simple, right? Well this is where it gets interesting:

    Once the sell by date has passed, Quality degrades twice as fast
    The Quality of an item is never negative
    "Aged Brie" actually increases in Quality the older it gets
    The Quality of an item is never more than 50
    "Sulfuras", being a legendary item, never has to be sold or decreases in Quality
    "Backstage passes", like aged brie, increases in Quality as it's SellIn value approaches; Quality increases by 2 when there are 10 days or less and by 3 when there are 5 days or less but Quality drops to 0 after the concert

We have recently signed a supplier of conjured items. This requires an update to our system:

    "Conjured" items degrade in Quality twice as fast as normal items

Feel free to make any changes to the UpdateQuality method and add any new code as long as everything still works correctly. However, do not alter the Item class or Items property as those belong to the goblin in the corner who will insta-rage and one-shot you as he doesn't believe in shared code ownership (you can make the UpdateQuality method and Items property static if you like, we'll cover for you). Your work needs to be completed by Friday, February 18, 2011 08:00:00 AM PST.

Just for clarification, an item can never have its Quality increase above 50, however "Sulfuras" is a legendary item and as such its Quality is 80 and it never alters.



