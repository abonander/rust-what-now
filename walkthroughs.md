#[Project Walkthroughs](walkthroughs.md)

Web series by Rust community members which walk the reader through creating a domain-specific project, like a 2D game. These vary in their levels of hand-holdiness, but may provide additional challenges if they haven't been kept up to date with Rust and the crates they use, or deliberately omit part of their implementation as an exercise for the reader.

Want to add or update an entry? Open an issue or a pull request.

###ArcadeRS

http://jadpole.github.io/arcaders/arcaders-1-0/

A blog series by Jessy Pelletier-Lemire detailing the creation of a 2D side-scrolling sci-fi shoot-em-up game using the [SDL2 bindings for Rust][rust-sdl2].

This series covers intermediate-level concepts such as lifetimes, macros, trait objects, and iterators, all of which are quite common in large Rust projects. The walkthrough does not require much prerequisite knowledge of Rust or game development, but a basic grasp of the former is recommended.

Readers should also be comfortable enough with their computer to install third-party native libraries ([SDL2][sdl2] itself). Readers running Linux should already know their way around their distribution's package manager, but users of OS X or Windows might have to get their hands dirty to get SDL2 installed correctly. The walkthrough currently (as of 17/01/2016) punts on installation instructions for SDL2 to the README of the Rust-SDL2 bindings.

As of January 17, 2016, 12 out of 16 parts of the walkthrough have been posted.

[rust-sdl2]: https://github.com/AngryLawyer/rust-sdl2 
[sdl2]: https://www.libsdl.org/index.php
