# Fractal firsts

This repo acts as a hub of the various languages in which I've implemented an ETF fractal renderer. When I need or want to learn a new language, this is the project I do. It's a fantastic first project, because it forces one to learn various aspects of the language, and is quite satisfying. In a nutshell, the goal of the exercise is to produce a parametric renderer of 𝔸\[X], the set of polynomials over 𝔸, where 𝔸 is some choice of a 2D algebra (complex numbers, perplex numbers, etc).

The core of the exercise is to render various escape-time fractals with the following constraints:
  - render a fractal image to a window (forces one to learn about available libraries, build systems, and some IO),
  - can work with multiple ℝ²-algebras over arbitrary polynomials (forces a minimum of generic, typed architecture, and gives fun renders),
  - can run various dwell protocols and various rendering algorithms (forces one to implement modular code),
  - can zoom up to machine precision,
  - implements a version of the Mariana-Silver algorithm (to learn how to recurse in the language with a non-trivial algorithm).

It's a project that I've done:
  - in C (core done, with a lot of interactivity, but only for complex numbers; though relies on 42's MLX, so annoying to compile; I'll probably update it to work with SDL some day, I've been wanting to learn Vulkan for a while after all...),
  - in React/TypeScript (core done, and even some amount of interactivity, though somewhat buggy and not too UX-friendly, only had about a week),
  - in Rust (only a rudimentary implementation; I didn't have much time, only about a weekend),
  - in Haskell (for now, only steps 1, 2, 3 and 5 of the core are done; I had a couple of weeks).

Depending on the amount of time that I have before needing to use the language professionally, I put more or less care/features into this project. Other features include:
  - saving to file (as a set of parameters, and/or as a picture), loading from file (set of parameters)
  - keyboard and mouse interactivity
  - a togglable debug menu
  - in-app changes to the parameters, including, but not limited to:
    - the anchor position
    - the level of zoom
    - coefficients of the iteration polynomial
    - the dwell protocol
    - the rendering algorithm
    - the color palette
    - the color smoothing algorithm
    - the ℝ²-algebra chosen
    - the escape radius
    - show/unshow axes
    - show/unshow Mariani-Silver boundaries

Features that I'd like to do someday but never got the chance to
  - deep (arbitrary precision) zoom 
  - more Mariani-Silver tilings than just the quadtree version
  - n-dimensional fractals using geometric algebra (cf. Wareham and Lasenby)
  - complex color smoothing algorithms
  - trace the evolving path of a point's iterations when hovering over it
