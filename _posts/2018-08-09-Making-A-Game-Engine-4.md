--- 
title: "Making a game engine [4]"
categories:
  - Blog
---

Game engine dev log part 4: Generalising Graphics.

Tutorial code is great... but if you want to make an engine the code has to handle more than a triangle.

<b>The goal:</b> Just make a nice interface for a polygon with N vertices. How hard can it be?

<b>The challenge:</b> I am using OpenGL4+, which means I can't pretend shaders don't exist and I need to understand a bunch of functions.

<b>The reward:</b> A pretty important part of the engine gets finished. Afterwards I can look into making a camera system.

The great thing about modular code is that you can make each separate part and then revise how they're accessed later.

Theres now files for GLFW (window/input), OpenGL (shaders and gl function calls), and then my original graphics interface (functions for games to use)

And then each has their own namespace. amaneshi::graphics will pluck functions from amaneshi::glfw if it's initialized. amaneshi::opengl is the only namespace that should use GL functions. amaneshi::vulkan is going to remain untouched until I have working games.

I didn't really decide on any fixed order of dependency because its a game engine! For the initial polygon type in amaneshi::graphics, it's important to be able to mix and match shaders. I just need appropriate game engine classes to contain everything relevant to rendering.

Speaking of shaders theres a funny way to include shaders into code with a... cheeky #include. If I end up with a hundred shaders I'll quickly swap over to some file-reading code that stores every loaded shader. Even then, this all serves to help me understand opengl/glsl better. Once that's done, I can divert my thoughts to how a proper company might actually squeeze performance/memory out of their code.

I already took care of input. Abstracting input was just providing another layer of enums. However, once I bring input and graphics together, I can start seeing how to make a multithreaded game run. The short answer is: Task Queues. What could go wrong? I'm looking forward to it!

<b><a href="https://github.com/iuyhcdfs/amaneshi">Have fun out there, won't ya?</a></b>
