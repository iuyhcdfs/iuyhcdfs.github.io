---  
title: "Making a game engine [8]"
categories:
  - Blog
---

Besides playing system shock 2, other things happened. Lets talk productivity.

<b>[The balancing act]</b>

I have to pace myself. Theres got to be a good way to constantly decide the next goal and finish it.

I've found a great technique. It's called "playing the game". Each time I build I ask, whats the next missing thing? And the first thing that occurs to me is what i'll do.

Right now: I want to make 3d objects get drawn. With a working camera.

And even simpler than that, I want some generic spheres. Once those spheres are done, I'll focus on what to do next.

Thinking ahead is helpful, but it must be balanced with actually making something.

<i>This balance is everything, isn't it. Planning prevents disaster, but creation is what rewards time spent.</i>

I have to remind myself that the engine shouldn't just be copying others, it should just be calmly implementing whatever is necessary for a game.
 
That being said, I spent lots of time making realisations as to why at least Unity, Godot and Unreal are the way they are. 

I shouldn't IMMEDIATELY copy those engines, but when I consider a system where everything is an object and "components" don't exist, you can do silly things like daisy chain unrelated subobjects and have something unmanagable.

The reality is that subobjects are for anchoring relative position and rotation. I could make any object an anchor of another object in a myriad of ways.

But if I continue the idea of only using C++ next to the engine, we don't really need objects at all! We just need the appropriate interfaces to inherit from and you can make your own giant mess of an object as long as it can update and if need be, render.

This would make badly created objects not easily updatable. And it could make for one massive update function, which again, is something to consider for multithreading.

ANYWAY IMPLEMENTING SPHERES DOES NOT REQUIRE A DECISION ON SUBOBJECTS.

I'll think more about that once after I make a million spheres play together on screen.


<b>Have fun out there, won't ya?</b>
