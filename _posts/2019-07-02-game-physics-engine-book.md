# Introduction

In this book we’ll cover a representative sample of physics tasks.With a gradually more comprehensive technology suite, our physics enginewill support particle effects, flight simulation, car physics, crates, destructible objects, cloth, and ragdolls, along
with many other effects.

## Advantages of a Physics Engine

 - Portability
 - Quality
 
 A physics engine provides you with the ability to have effects interact in believable ways. Remember themoveable crates inHalf-Life 1? They formed the basis of only one or two puzzles in the game. When it came to Half-Life 2, crate physics was replaced by a full physics engine. This opens up all kinds of new opportunities. The pieces of a shattered crate float on water, objects can be stacked and used as moveable shields, and so on.

## Weaknesses of a Physics Engine

 - The most common reason is speed. A general-purpose physics engine is quite processor-intensive.
 - The need to provide the engine with data can also be a serious issue
 - A final reason to avoid physics engines is scope. If you are a one-person hobbyist working on your game in the evenings, then developing a complete physics solution might take your time away from improving other aspects of your game, such as the graphics or game play. Or worse, it might distract you from finishing, releasing, and promoting your game. On the other hand, even amateur games need to compete with commercial titles for attention, and top-quality physics is a must for a top-quality title of any kind.

# Approaches to Physics Engines

## Types of Objects

 - **Rigid-body** engines treat objects as a whole, and work out the way they move and rotate. A crate is a single object, and can be simulated as a whole.
 - **Mass aggregate** engines treat objects as if they were made up of lots of little masses. A box might be simulated as if it were made up of eight masses, one at each corner, connected by rods.

## Contact Resolution

 - One approach is to handle these contacts one by one, making sure each works well on its own. This is called the **“iterative”** approach and it has the advantage of speed.
 - Amore physically realistic way is to calculate the exact interaction between different contacts and calculate an overall set of effects to apply to all objects at the same time. This is called a **“Jacobian-based”** approach,1 but it is very time consuming.
 - A third option is to calculate a set of equations based on the contacts and constraints between objects. Rather than use Newton’s laws of motion, we can create our own set of laws for the specific configuration of objects we are dealing with. These equations will change from frame to frame, and most of the effort for the physics engine goes into creating them (even though solving them is no picnic either). This is called a **“reduced coordinate”** approach.

## Impulses and Forces

 - **“force-based”** physics engine and it works in the way the real world does
 - **“impulse-based”** physics engine. Each frame of the game, the book receives a little collision that keeps it on the surface of the table until the next frame.

