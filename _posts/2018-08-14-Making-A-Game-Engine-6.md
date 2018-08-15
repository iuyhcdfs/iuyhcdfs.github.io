--- 
title: "Making a game engine [6]"
categories:
  - Blog
---

Game engine dev log part 6: More Graphics/An Idea/Collisions

<b>[More Graphics]</b>

Learning continues. Here's the main ideas.

There are dots lines and triangles that can be easily drawn. We'll make the most out of using triangles.

Each triangle can be drawn in certain ways, and vertices for adjacent triangles can be re-used to save memory.

Of course, this means we can easily establish convex polygons with GL_TRIANGLE_STRIP. If we have to draw concave polygons its still possible with the right ordering of vertices.

We always. Need. To. Think. About. The. Future.

So if we ever had complex 3d polygons, how do we make sure they get drawn properly? Whatever format a highly detailed model contains, it too must decide vertices in an appropriate order, in order to define what is it's surface. This should already correlate with a triangle strip hopefully.

What about 3d models that warp? Where the relative position between vertices can change? Well, we would like to expect that it does not deform weirdly (like one vertex of a sphere changed to pierce through itself). It should still work out fine.

Mapping textures and lighting? Our abstractions will hopefully accomodate the change. By the time we might need to rewrite code we'll probably have a much better idea on how to do everything.

<b>[An Idea]</b>

I could try to add one further goal to the engine, which would be: Make Amaneshi the fastest option for building a prototype.

If I simply want to test gameplay, multiple platforms and built in functionality is not necessary.

When you're making completely new game mechanics, you'll end up inside code eventually. (At least, if you already can, you don't need blueprints)

But on second thought, the drawback is I decrease my level of experience using a full engine. If I don't save a ridiculous amount of time, I should stick to prototyping in Unity/Unreal and just continue having Amaneshi be my c++ sandbox.

The only way I could make a pure-c++ engine faster for prototyping is if there is already convenient objects at my disposal.

When thinking this way, I could overtake either engine, but I could also just make the appropriate classes for those engines too.

Maybe once I'm done learning all this I'll be fast in every engine.

Anyway, an incredibly smart person said this: "The technical knowledge of today will no longer be useful in ten years. In contrast, we want to hire adapatable people who are looking toward tomorrow’s challenges."

I'll keep thinking about that.

<b>[Collisions]</b>

This is me rambling to myself, which you can skip, because thinking about collisions on your own is a great exercise!

When objects collide, physics happen. I've already had a lot of thoughts about this, long ago. 

Theres 2 immediately easy kinds of hitboxes. We can make spheres/circles and boxes/rectangles. For brevity I'm going to say circles and boxes, but our choice of 2d or 3d is irrelevant.

Boxes overlap when they're within each other's edges. Circles just need their radius applied.

Making circles and boxes interact with each other however, require you to test if the closest point is touching. If the box is not rotated, the closest point depends on the center of the circle. If the center is within the box's edge, the closest point is one of the dimensional axes.

Otherwise if the circle center is outside in all dimensions BUT the center + radius can still fall inside, you have to see if the corners of the box are touching the circle at a non-90-degree-angle. 

Comparing two circles for collision is much easier. The distance between their two centers should not be less than their combined radius.

If you didn't know, computers don't like doing square-root operations. So any time we compare distance to a circle's radius, we actually produce the squared distance, and then deliberately square the radius to compare.

This is going to lead into making the physics system. I'm going to take the typical approach.

 - Every physical object has a mathematical coordinate and rotation. Thus, objects could experience normal velocity and rotational velocity.
 - Each object could be grouped in a different layer (where interaction does not occur between groups)
 - Objects with collision hitboxes will result in reactions. They might stop dead or bounce off each other
 - To properly test collisions, you will need to compare each object in a layer with each other
 - To avoid testing every possible pair of objects if they collided, we could cull based on location.
 - To cull based on location, we must be able to ask the engine to provide every object in a certain part of the world.

So we need to split up the world reasonably nicely. This is another thing we're going to need to stress test later.

Splitting the map however, will be a strange task. We'll need to create a data structure to hold every sub-cube of the map, and each moving object needs to update which sub-cube they're in. Smaller sub-cubes of the map will mean each object has to update this data structure more often, but larger sub-cubes of the map mean we have more pair combinations to compare for nearby collisions.

We'll have to end up testing this to find what a good balance is.

Not only that, we'll have to allow this data to be accesed by more than one thread! Tasks for updating each object could be assigned to a thread!

Perhaps we might need to only create a task for updating whole sub-cubes at a time. Again these are all ideas, but it'll be the most important experience I have in this game engine before returning to commercial ones.

<b>[How's That Roadmap Going?]</b>

Now with more detail than ever. 

 - ~~I study more GL/GLSL.~~
 - New folder "Math" for position/rotation and function code
 - Basic camera system
 - Use OpenGL to at least draw spheres and boxes
 
 - Collision of many freely moving objects "Not Air Hockey"
 - Stress test mass collision with single/multithread

 - Make "Go" in Unreal/Amaneshi (the c++ game logic SHOULD be interchangeable!)
 - Finish Unity project "Poppy", something with actual gameplay

 - Always be ready to switch focus to the most important tasks.


<b><a href="https://github.com/iuyhcdfs/amaneshi">Have fun out there, won't ya?</a></b>
