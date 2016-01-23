---
layout: post
title:  "Seams in code, explained"
date:   2016-01-23 1:35:25
categories: technical post
---

# Seams in code, explained

## Goal

A friend of mine shared that they had never heard an explanation of a seam in the code without someone using the analogy of a clothing seam, thus recursively using the word in its own definition.  

I aim to provide an alternate definition.  

> **History of the term _seam_:**
> 
> It is used in Michael Feather's <a href="http://www.amazon.com/Working-Effectively-Legacy-Michael-Feathers/dp/0131177052">_Working Effectively with Legacy Code_</a>.

## Traditional definition of a seam
So what is a seam?  

It's a convenient place in the code where you can rip out one component and replace it with another component.  

The traditional metaphor is the one of a clothing seam, where you can pry pieces of cloth apart in a place that will not damage the overall structure.  

<a name="clothing-seams" href="http://sewbeitstudio.com/diy-projects/clothing/gatsbytop/">![Clothing seams](/images/seam-clothing.jpg "Clothing seams")</a>

**Clothing Seams** 

However, I like to think of seams differently.  

## A seam as a puzzle

If all of the code is a puzzle (think of one of those 1000 piece puzzles), then a seam is the edges of meeting puzzle pieces.  

<a name="puzzle-seams" href="https://www.flickr.com/photos/bludgeoner86/2137761064/">![Puzzle seams](/images/seam-puzzle-medium.jpg "Puzzle seams")</a>

**Puzzle Seams** 

In this place, you can remove a single puzzle piece (or many pieces) and replace them with completely different implementations that still match the same contract.  The contract being, of course, the same API/ same unwrapped JSON/ generally the same entry points and boundaries. 

Within a single puzzle piece/ a class/ a microservice/ etc, it is the boundary conditions that determine the proper fit into the overall structure.  

Thus, a seam is a convenient location to replace an old implementation with a new one.  

<a name="last-piece-seams" href="https://www.flickr.com/photos/10154402@N03/5362769454/">![Last piece of the puzzle](/images/seam-last-puzzle-piece.jpg "Last piece of the puzzle")</a>

**The last puzzle piece** 

## A seam as tectonic plates

Another way I like to think of seams is like tectonic plates.  

This analogy feels more grand, more epic, and I relate to it more when I think of big refactorings to make, such as replacing a 3rd Party Integration service provider or switching databases.  It feels much... larger of an analogy than a puzzle box & puzzle pieces. 

Anyways, tectonic plates. 

You have a world, a whole landscape sitting on top of tectonic plates.  And for whatever reason, you'd like change out a mountain range that yields poor crops with fields and water.  

<a name="mountains" href="https://www.flickr.com/photos/dfsmith/7884948784/">![Craggy mountains](/images/seam-mountains-medium.jpg "Craggy mountains")</a> 

becomes 

<a name="fields" href="https://www.flickr.com/photos/oneterry/16434200600/">![Fields](/images/seam-fields-medium.jpg "Water and fields")</a>

In order to make this move, this epic, gargantuan move, you want to minimize the resources allocated to do this.  You need to find a convenient place to lift and remove these mountains.  

<a name="crane" href="https://www.flickr.com/photos/jaxport/13084381295/">![Crane](/images/seam-crane-medium.jpg "Crane lifting heavy things")</a>

Enter the seam.  A tectonic plate.  A giant area that is easier than other areas to lift and replace.  

As long as the borders line up, you can lift and replace it with relative ease.  

### Enjoy!








