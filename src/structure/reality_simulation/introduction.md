# Introduction

In this part of the book we will discuss the many design decisions that went into creating a `Reality` inside of UnnamedEngine. Starting from a `Reality`, we will talk about what goes into the creation of everything in the simulation.

The explanation will have this flow: **Bigger -> Lower**


## Reality
Well, I can't tell you what reality itself is, if its real or not, or other types of affirmations that are outside of the scope of your development, we are game developers and will be ignorig all the details related to what is what. The terminology used inside UE takes inspiration in real life, but is adapted to fit our deign and goals.

`Reality` is the uppermost container, everything that _exist_ is inside of a `Reality`, note that things that don't _exist_ are not contained in a reality!

But what does not exist?

A Graphical User Interface GUI **does not exist**. Well, you can see it, but the world does not, only the player is capable of seeing it, it also does not interact with anything besides the player's input or other GUI elements, and thus it doesn't exist! Sure, it exist on _our_ reality, but not inside the `Reality`.

### Structure
A `Reality` contains two things.

- [`Reality Rules`]()
- [`Dimensions`]()

These two things are responsible for defining our game "world". Note that since UE was born to create a complex and exotic game, why not provide the tools to make these types of games easier to be reused?

Generally speaking, almost all structures related to space and time, contain just _space and time_-related values, but `Reality` is the exception. [`Reality Rules`]() are `Rules` that define how the world works, I will not get into details here, but these exist so we have a way to create and use complex simulations without hardcoding anything.
