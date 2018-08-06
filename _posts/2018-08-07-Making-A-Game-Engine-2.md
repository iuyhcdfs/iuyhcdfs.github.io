--- 
title: "Making a game engine [2]"
categories:
  - Blog
---

Game engine dev log part 2: Planning and coding begins

I have to readily expose my inexperience with c++, so I can stop being inexperienced with c++.

<b>[Issue 1: Organising code]</b>

Ideally you can have folders that go downwards in terms of dependency.

To keep things simple, I'm trying to see if its possible to only have 1 folder depth.

To make a tree-shape out of your dependencies, any time say, the sound library and a game object interact, 
some class in a folder above needs to contain files from two folders.

Of course, what i've ended up is having file names with prefixed catagories. It's almost the same as just having more folder depth.

<b>[What did I learn from planning the engine code]</b>

Magically though, after planning this: Unreal Engine's source code is much easier to navigate. UE has folders for what the code is built for, then it splits into components. The public and private folders are neat since clearly every public folder is added to the include path. If folders were reorganised, none of the #includes get broken as long as the folders are called public.

Unlike Unreal, my engine was just going to be pure c++ with no editor, and no additional programs. 

So the folder layout is fine, given how much i'll probably end up using my engine.

Basically, I've confirmed the only benefit of my engine is that building it will improve my skill. Thats great! Having well defined expectations is the first step to avoiding dissapointment and frustration.

<b>[Issue 2: How to add libraries]</b>

I wanted libraries to be abstracted so I could swap them if I wanted. Seemed like a simple request. 

Hmmmmmmmm here are the lessons learnt.

You can't split graphics and input so easily, since say GLFW needs the window to which input is directed to.
This of course, reveals how window managers direct your input. It's better to just focus on gameplay while the window is active.

If you're going to really make everything swappable, you could also be able to swap between say, OpenGL and DirectX?

Also, I considered classes and a namespace with global function pointers.

<b>[What did I learn from trying to abstract this much]</b>

I've crossed the line where abstraction stops helping me.

Firstly, function pointers not done via an inherited class is extra work for the programmer since you have to assign the function pointer for every new function you needed to abstract. Even if I made hardly any functions, this seems like a future nightmare.

Also, you might as well make whatever functions you want and use the library directly. If I needed to use another library, the function names are still the same.

Many project utilise third party source code, but they typically pick one and use it thoroughly.

What was I thinking? I wanted to try the idea of globals in a namespace compared to using classes. 

I guess that just means I got sidetracked. But the conclusion is useful: Don't do that. For some things, theres a reason why you don't see it in other source code.

I got some extreme deja vu typing this so I'm sure I'm on the right track.

<b>[Issue 3: I want to try multithreading]</b>

To deal with this, I have to make a task system. I did some research of course.

Thanks to the modern c++ concurrency library, I'll be able to stress test my own code with and without splitting threads.

I haven't read into how Unreal does this yet. Can't do everything at once.

<b>[Issue 4: When do I stop?]</b>

When I accomplish the issues already mentioned and these two small games, time is probably better making a game in UE4/Unity.

 - Just adding circles to a screen that bounce around.
 - Go: Adding black and white circles to fixed spots on a grid with certain rules for eliminating them.
 
It'll be nice to get back to making gameplay :)

<b>[Issue 5: Once I stop, will I ever return?]</b>

I can still come back to play with OpenGL, or learn more about processing signals.

Its a sandbox for learning. 

Good thing I laid out my thoughts here, sometimes you start thinking you're wasting time and then you want to give up!

Time isn't being wasted here at least. Until next time,

<b><a href="https://github.com/iuyhcdfs/amaneshi">Have fun out there, won't ya?</a></b>
