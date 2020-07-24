---  
title: "Making a game engine [7]"
categories:
  - Blog
---

Game engine dev log part 7: Maths/Cameras/Drawables/Collisions 2

I'm rambling about implementations of certain features now. 

This post is probably lower in entertainment value.

<b>[A short selective history of numbers]</b>

Number systems describe what a number means, and how it changes. 

The earliest number systems humans used were based on the real world. I can count the number of fingers on my hands.

We learned to add and subtract. Multiply and divide. Raise to the power or find a root.

There eventually were number systems that described... something else. Something alien.

We had complex numbers. I am incapable of telling you what they describe, but the rules that govern them make them useful for converting one problem into another. For many problems, first you make it an easier problem, then you solve it.

Quaternions are another set of complex numbers, where there are extra "dimensions" of numbers. The rules for quaternions, to keep it short, make quaternions a valid way of representing a rotation.

At this point you should check out a bunch of videos on gimbal lock, which quaternions avoid.

<b>[Cameras]</b>

Cameras let you look at the world. You could say a camera is moving, or the rest of the world moves around it.

Again, there are guides out there that are good at explaining this. I'm just asking myself future questions such as:

"How do I implement multiple cameras projecting onto in-game surfaces?"

Perhaps you're in a surveillance camera room, and you can see into many other rooms. 

Perhaps the surveillance room has it's own camera too, and you can see it project onto itself.

Perhaps as an exercise you want to implement portal/narbaculardrop.

The camera implementation should at least accomodate the potential for this.

<b>[Preventing a coding nightmare]</b>

It's all about thinking of the future!

After I wrap up graphics, I can finally make some concrete game objects.

They'll just rely on a graphics component, but it should be relatively painless to use primitive shapes.

The more I think about this the more I know for sure I'd never surpass Unity for prototyping speed.

I'll just have to keep making more classes and contain more common functionality in a neat way for now.

Is that demoralizing? No. I'm still curious about stress testing this whole thing.

But I want to speed up progress. 

The rendering component of a game object will fetch the necessary opengl objects and adapt to the shape it's been given.

Theres also the idea that the game engine should lend easily to a client-server and peer-to-peer system for multiplayer.

Of course, my game state is pretty bare at the moment. But that entire topic is worth reading into.

<b>[Collisions again]</b>

Splitting the map into subspaces via a data structure is messy business... if we do every combination of dimension.

But we can just do each dimension individually.

I can just make 6 vectors of buckets, for the positive and negative values of the x, y and z axes.

That way if objects go far enough out in the game world, I can just push back more buckets to accomodate them.

<b>[State of the Roadmap]</b>

Now with more detail than ever. 
I have to re-orient to important tasks as necessary.

 - ~~I study more GL/GLSL. (quickly learn an api)~~
 - New folder "Math" for position/rotation and function code (implement quaternions on my own)
 - Basic camera system (revise geometry and linear algebra)
 - Use OpenGL to at least draw spheres and boxes (put everything into practice)
 
 - Collision of many freely moving objects "Not Air Hockey" (implement collision system)
 - Stress test mass collision with single/multithread (fully implement tasks)

 - Make "Go" in Unreal/Amaneshi (both accept c++ classes)
 - Unity project "Poppy"



<b><a href="https://github.com/iuyhcdfs/amaneshi">Have fun out there, won't ya?</a></b>
