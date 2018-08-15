--- 
title: "Making a game engine [5]"
categories:
  - Blog
---

Game engine dev log part 5: Roadmap/Learning OpenGL

<b>[Planning time]</b>

I was originally going to focus on the task queue, but testing a task queue requires enough subtasks to stress the engine.

Theres some paralysis in thinking of what to do next, because there are so many choices.

(also because i've been busy with other things)

I can finish off a super simple game just by drawing graphics primitives.

I can learn more OpenGL and create something prettier. 

I can also think about making the engine accomodate textures and animations.

I have to pick just one though.

So I have to plan a roadmap. The order doesn't matter as much as I sort out what I want to do and just focus on making it happen.

So I'll do this order!

 - Make it easy to render sprites and basic 3d shapes with colors. Textures come later.
 - Make a simple game with collisions, which needs some camera code and colliders
 - Test its performance with different execution models
 - Use other engines for a while.
 
Most things will be implemented as attachable object components because that's how you prevent trouble. It's just a little unoriginal because every other game engine does that.

I just need to be original with the games that come out of an engine.

<b>[Enter OpenGL]</b>

I'll pretend you don't know about OpenGL. Here's what you need to know

 - You should use modern OpenGL, but it's a little more complicated.
 - OpenGL is how you talk to graphics cards
 - Graphics cards can do math VERY QUICKLY.
 - Graphics is just math.
 - Modern OpenGL requires you use shaders.

Shaders? Let me explain.

<b>[Let's meet our friend]</b>

Pretend we are a game engine, we've managed to make game mechanics but we actually can't draw!

Remember how I said graphics card do math quickly? FORGET IT. Graphics cards are Natural Born Artists.

Suppose we have a friend, who happens to be a graphics card. They're a drawing genius. We really need their help, because hardly any great game is made alone.

Our friend wants to make games too, and they're waiting for us to tell them what to draw!

They want to draw pictures perfectly, so they always plan out the drawing with these steps.

 - 1: They first put dots on the paper
 - 2: Then they connect perfect lines between these dots.
 - 3: Then they colour in these outlines. It's finished!
 
You can try this. As a human.

It's a great way to draw complicated shapes that look great, even though you leave a lot of dots on the paper.

Anyway, when our friend works that way, they're No.1 in the world for speed. They're superhumanly fast, and the pictures are drawn perfectly.

This is getting silly. Our friend is just a graphics card, okay?

Lets talk about our "friend" again with computer words.
 - 1: A "Dot" is now called a "Vertex", and we draw to a computer screen instead of paper. We'll tell the graphics card where vertices are on the screen.
 - 2: The lines get drawn between vertices. Some OpenGL functions could decide what order we join our dots.
 - 3: To colour in the screen, we split our screen into little pieces... lets call them "Fragments".

As beginner learners there are 2 main shaders. The vertex shader and the fragment shader.

Clearly they're involved with steps 1 and 3.

We're just making code that tells the graphics card how to dot and colour in.

Theres some functions that let you be specific with how the hardware is doing this under the hood, if you want to make your rendering as fast as possible.

But I am just making an engine. First the code will make sense and be easy to change, and afterwards I'll see if I need to change it.

It's not worth blogging in detail, but I'm just learning the foundation involving GL functions and shaders for now.

<b>[A more specific roadmap]</b>

For personal use. See you next time!

 - Further OpenGL integration. I study more GL/GLSL.
 - Game of spawning colliding objects
 - Stress test mass collision with single/multithread
 - Learn Unreal by making Go
 - Finish Unity project "Poppy"


<b><a href="https://github.com/iuyhcdfs/amaneshi">Have fun out there, won't ya?</a></b>
