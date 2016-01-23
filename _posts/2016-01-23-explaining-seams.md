## Seams in code, explained

### Goal

A friend of mine shared that they had never heard an explanation of a seam in the code without someone using the analogy of a clothing seam, thus recursively using the word in its own definition.  

I aim to provide an alternate definition.  

### Traditional definition of a seam
So what is a seam?  

It's a convenient place in the code where you can rip out one component and replace it with another component.  

The traditional metaphor is the one of a clothing seam, where you can pry pieces of cloth apart in a place that will not damage the overall structure. 

[image of seam]

However, I like to think of seams differently.  

### A seam as a puzzle

If all of the code is a puzzle (think of one of those 1000 piece puzzles), then a seam is the edges of meeting puzzle pieces.  

[image of puzzle pieces, sliding in]

In this place, you can remove a single puzzle piece (or many pieces) and replace them with completely different implementations that still match the same contract.  The contract being, of course, the same API/ same unwrapped JSON/ generally the same entry points and boundaries. 

[image of puzzle with new colored piece sliding in]

Within a single puzzle piece/ a class/ a microservice/ etc, it is the boundary conditions that determine the proper fit into the overall structure.  

Thus, a seam is a convenient location to replace an old implementation with a new one.  

### A seam as tectonic plates

Another way I like to think of seams is like tectonic plates.  

This analogy feels more grand, more epic, and I relate to it more when I think of big refactorings to make, such as replacing a 3rd Party Integration service provider or switching databases.  It feels much... larger of an analogy than a puzzle box & puzzle pieces. 

Anyways, tectonic plates. 

You have a world, a whole landscape sitting on top of tectonic plates.  And for whatever reason, you'd like change out a mountain range that yields poor crops with a port city surrounded by fields.  

[imae of mountains] --> [image of fields, port]

In order to make this move, this epic, gargantuan move, you want to minimize the resources allocated to do this.  You need to find a convenient place to lift and remove these mountains.  

[image of crane lifting flat section of land]

Enter the seam.  A tectonic plate.  A giant area that is easier than other areas to lift and replace.  

As long as the borders line up, you can lift and replace it with relative ease.  

### Enjoy!








