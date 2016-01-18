#Contributing to Rust

How to get started with contributing to Rust itself, the compiler, the standard library, Cargo, or official Rust-Lang crates.

###Overview - rust-lang/rust (Main Repository)

As every large open-source project seeking contributors should, Rust has a [`CONTRIBUTING`][rust-contrib-md] file as a guide for new contributors. You should have a look through that before continuing. However, the contributing guide is often just a very general overview, and it can still be difficult for new contributors to find something to get them started.

Github's issue labels often come in very handy here, and the Rust repository has many labels configured in its [issue tracker][rust-issues]. You can select one or more labels to filter issues with by using the **Labels** dropdown in the grey bar or appending `label:<label name>` (e.g. `label:E-easy`) to the text box with the magnifying glass and pressing Enter.

* [**E-easy**](https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AE-easy): This is the first label you should check out. These are issues which are considered to have relatively straightforward solutions, and as such, ought to be a good place to start for someone who wants to contribute to Rust.

* [**E-mentor**](https://github.com/rust-lang/rust/labels/E-mentor): Sometimes appearing alongside the **E-easy** label but not always, this label signifies an issue where a Rust team member or an otherwise experienced contributor has offered to mentor on the task at hand, which means they will make themselves available for advice or assistance as the need arises. Preferred methods of communicating varies from person to person, but discussion on the issue itself or in one of the Rust IRC channels is usually preferred.

However, filtering by these labels alone will show issues for all the different areas of Rust, including various components of the compiler, as well as the standard library and documentation. You can include one, or several, of the **A-*** labels to filter for a specific **a**rea of Rust. Most of the A-\* labels are for different areas of the compiler, with a few exceptions:

* [**A-libs**](https://github.com/rust-lang/rust/labels/A-libs): Filters for all issues concerning the libraries in the Rust distribution: `std`, `core`, `alloc`, `collections`, `libc`, and `rustc_unicode`.

* [**A-docs**](https://github.com/rust-lang/rust/labels/A-docs): Filters for all issues concerning documentation. This includes Rust libraries (usually denoted by the inclusion of the **A-libs** label), as well as The Rust Programming Language (sometimes referred to as "The Book").

* Platform-specific labels: A-linux, A-mac-osx, A-windows

There are many others not listed here for various reasons. Have a look at the [full list](https://github.com/rust-lang/rust/labels) if you want to explore the Rust issue tracker further.

[rust-contrib-md]: https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md
[rust-issues]: https://github.com/rust-lang/rust/issues
