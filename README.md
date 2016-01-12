# What Now? Rust now.

Are you new to Rust? Have you finished [The Rust Programming Language][trpl] and/or [Rust by Example][rbe] and found yourself asking, "Well, **what now**?" You've come to the right place.

It may not feel like it, but you probably have a good enough grasp of Rust now to venture out on your own. You'll pick up the little things a lot faster once you start writing your own code, as compared to just copying someone else's. Check out one of the following sections for ideas on what you can do next.

####[Ideas for a First Rust Project](ideas/first.md)

Projects that aren't too complex; any given one might take you a couple hours to an afternoon to complete. These should be cleanly implementable in a single file with the standard library, so they shouldn't require detailed knowledge of the module system or Cargo.

####[Advanced Project Ideas](ideas/advanced.md)

More challenging projects which might take a while--maybe a weekend or two. These will probably necessitate some sort of module structure, and you may want to bring in external crates so you don't have to implement everything yourself.

####[Programming Challenges](challenges.md)

Sites and forums which provide generic or domain-specific programming challenges for you to complete. More often than not these are language-agnostic, and Rust is quite often underrepresented in submitted solutions. 

####[Project Walkthroughs](walkthroughs.md)

Blog posts by Rust community members which walk the reader through creating a domain-specific project, like a 2D game. These vary in their levels of hand-holdiness, but may provide additional challenges if they haven't been kept up to date with Rust and the crates they use, or deliberately omit part of their implementation as an exercise for the reader.

####[Contributing to Rust](contrib/rust.md)

How to get started with contributing to Rust itself, the compiler, the standard library, Cargo, or official Rust-Lang crates.

####[Contributing to Servo](contrib/servo.md)

How to get started with contributing to [Servo][servo], Rust's partner-project at Mozilla, as well as related projects managed by [the Servo team][servo-team].

####[Community Projects Open to Collaboration](contrib/community.md)

Rust community projects which are welcoming and supportive of collaborators, and which might be, or are, looking to mentor newcomers to Rust. Organized by problem domain.

#####[Application Development](contrib/community.md#app-development)

General applications development; programs which are meant to run in a common desktop or terminal environment and are meant for an end-user. Includes IDEs, text editors, command-line interface (CLI) utilities, etc.

#####[Game Development](contrib/community.md#game-development)

Projects which are related to or primarily focused on game development; this includes domains like graphics programming, audio libraries, user interface development, physics simulations, maths libraries, realtime network programming, etc.

#####[General Library Development](contrib/community.md#general-library-development)

Projects which don't strictly fall into one of the other categories. These projects are usually crates which provide convenience functions or wrappers around standard library types to make it easier to develop applications or other libraries for some problem domain. Sometimes touches `unsafe` code depending on the problem the project is meant to solve.

#####[Systems Programming](contrib/community.md#systems-programming)

Projects which involve low-level systems programming, like interfacing to C libraries via the Rust Foreign Function Interface (FFI), developing operating systems, or developing applications for embedded platforms. Knowledge of C and how linking and object files work is good to have, but not strictly necessary. A nightly Rust compiler is usually required for its unstable features like syntax extensions and intrinsics. `unsafe` code is very common and programmers need to be very careful to check numerous invariants to avoid undefined behavior.

Recommended reading: [The Rustonomicon](https://doc.rust-lang.org/nightly/nomicon/)

#####[Web Development](contrib/community.md#web-development)

Aside from the previously mentioned Servo project, there are many projects in the Rust ecosystem revolving around web development, usually focused on the server side. These include low-level HTTP libraries, web servers, web application frameworks, database bindings, etc. There are also a few projects focused more on the client side, like HTTP clients and REST bindings to popular web services.

####[Community Involvement](community-other.md)

Perhaps you'd rather write English (or another human language) than Rust, but still might want to exercise your knowledge. There's still loads of things you can do within the Rust community, and this category might give you some ideas.

[trpl]: https://doc.rust-lang.org/nightly/book/
[rbe]: http://rustbyexample.com/
[servo]: https://github.com/servo/servo
[servo-team]: https://github.com/servo
