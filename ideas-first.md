#Ideas for a First Rust Project

Projects that aren't too complex; any given one might take you a couple hours to an afternoon to complete. These should be cleanly implementable in a single file with the standard library, so they shouldn't require detailed knowledge of the module system or Cargo.

Suggestions are welcome; feel free to open an issue or pull request on this repository. Please follow the style of the existing entries. 

### Reverse Polish Notation (RPN) Calculator

* Reading from standard input and writing to standard output
* Matching on strings and parsing strings as numbers
* Managing a stack datastructure

https://en.wikipedia.org/wiki/Reverse_Polish_notation

A Reverse Polish Notation (RPN) calculator takes expressions in postfix notation, e.g. `6 2 +`, as opposed to the infix notation usually used in maths writing, e.g. `6 + 2`. Postfix notation ties well to a [stack datastructure](https://en.wikipedia.org/wiki/Stack_(abstract_data_type)) (aka a last-in, first-out [LIFO] structure), as operands (numbers) are pushed to the stack in the order they're taken in, and operators (`+ - * /`, etc) pop operands from the stack and push their result.

You can use a standard [`Vec`](http://doc.rust-lang.org/std/vec/struct.Vec.html) as your stack, accessing it only via its `.push()` and `.pop()` methods (and optionally `.peek()` for operators which copy the top of the stack). For simplicity, use `f64` as your number type. Real calculators use number types which have higher precision and lower susceptibility to rounding errors; however, simple floating-point numbers are fine for our purposes.

Your calculator program should read expressions line-by-line from [standard input](http://doc.rust-lang.org/std/io/index.html#standard-input-and-output), split on whitespace, parse numbers (e.g. `"4.0".parse::<f64>()`) and dispatch on operators, and then print the resulting stack after each expression (can just be `println!("{:?}", stack)`). Optionally, you can retain the stack across expressions so the user can build a larger calculation one expression at a time. 

You should at least support four operators:

* Addition (`+`): pop two operands, add them together, and push the result.
* Subtraction(`-`): pop two operands, subtract the first from the second (so `6 2 -` equals 4 and not -4), and push the result.
* Multiplication(`*`): pop two operands, multiply them together, and push the result.
* Division(`/`): pop two operands, divide the second by the first (so `4 2 /` equals 2 and not 0.5), and push the result.

Errors, such as unparseable numbers or operators which need more operands than are available on the stack, should not crash the program; thus, you should not use `.unwrap()` or `.expect()` where a function call returns `Option` or `Result`. Instead, print a message detailing the error and continue to the next expression. If you're preserving the stack across expressions, then you could optionally add code to roll back the stack to its previous state so the user doesn't lose data to a typo.

Additional challenges:

* Implement more operators (see the methods on the [`f64`](http://doc.rust-lang.org/std/primitive.f64.html) type):
    * Modulus/remainder, usually `%`; combined divide and remainder (maybe `/%`)
    * Rounding operators: `round` (round towards nearest integer), `ceil` (round to next larger integer), `floor` (round to next smaller integer), `trunc` (discard decimal component/round towards 0), `fract` (discard integral component)
    * Square root (`sqrt`, or generic nth root `root`), exponentiation (`pow`, should pop the exponent first and then the base)
    * Trigonometric operators, `sin`, `cos`, `tan`, and their inverses `arcsin`, `arccos`, and `arctan`
    * Conversion to degrees or radians (convert whole stack or just top value)
    * Logarithmic operators: `log` (use `.log10()` as that's what most people will expect), `ln`
    * Stack manipulation: pop top of stack and discard (`>`), copy top of stack (use `.peek().cloned()`) and push (`<`)
    * Constants (operators which only push): `pi` and `e`

* Add an overloaded meta-operator, maybe `&`, that copies operands for operators instead of popping them, e.g. `&+`, `&round`, `&sin`, etc.

* Print numbers without the decimal point when they're integral

* Add operators which can store and access variables by-name in a separate datastructure (use `HashMap<String, f64>`)

  * Perhaps `:var` for pop (or copy) and store under "var", `'var` to copy the value of "var" and push it onto the stack.

* Use arbitrary-precision floating point (you'll need to use Cargo and pull in an external crate
    * As of 1/11/2016, it doesn't look like there's any arbitrary-precision crates on Crates.io which support floating-point numbers, because [it's actually kind of hard to get right](https://en.wikipedia.org/wiki/Arbitrary-precision_arithmetic#Implementation_issues).
