---  
title: "Making a game engine [3]"
categories:
  - Blog
---

Game engine dev log part 3: Further reflection and "target audiences"

I decided to do this with the *intention* of learning c++.

Now, real game engines are made with the *intention* of enabling other users to create games.

<b>[In terms of abstraction]</b>

This clear things up in terms of planning the whole library abstraction.

When building a game engine the focus is on "who is using it" and "what does it build".

Appropriate functions that make THOSE tasks easy should be decided first, then everything else can be built around it.

This way of thinking is intuitive when *designing* a game, but I didn't see planning the engine as another *design* task.

Honestly almost everything is a design task. This was a pretty big mistake!

<b>[In terms of scope]</b>

I wanted to practice planning for how the code could scale up. Thats no mistake. The intent here was to fail and learn.

<b>[In terms of learning]</b>

I want to learn c++ via this and that's fine.

What ended up happening is that I *designed* this project for people who are learning c++.

The folders aren't too deep, the threading system is simple, and the engine is small in scope.

Not only that, when deciding how files were included, I kept in mind someone who uses a simple Makefile. (If i switch back to linux, I want to be able to comfortably continue using my code).

Although really I should learn CMake because I can.

My weird namespace approach however does pay off when it comes to keeping code reasonably short. My use of NON-struct/class enums is quite convenient as long as im only wreaking havoc in "namespace amaneshi::input". As long as it's readable, right? Ahahaha.

<b>[Should I keep going]</b>

In that case, until I don't need to learn anymore (never), I can always come back here.

It's my c++ sandbox. I can learn things here, I can read source code elsewhere.

I'll use it as long as some concepts are more appropriate to learn by coding.


<b><a href="https://github.com/iuyhcdfs/amaneshi">Have fun out there, won't ya?</a></b>
