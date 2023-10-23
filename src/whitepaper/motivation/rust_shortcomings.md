## Rust does have some relevant shortcomings 

While Rust offers an excellent experience for systems development, it does have some disadvantages from a UI standpoint, many of which represent obstacles for its usage in application development.

### 1. Lack of inheritance
First, Rust doesn't support true type-level inheritance, only interface-level inheritance (at the trait level).
This makes it difficult to realize the object-oriented programming design patterns to which UI developers are typically accustomed, e.g., a base displayable/widget class from which other subclasses can inherit and override functionality as necessary.

### 2. Representing shared mutable state is hard
Second, it can be difficult to implement access to shared mutable state in Rust.
The ownership and borrow-checking semantics are not yet sophisticated enough to support all use cases and programming patterns typically found in UI development and state management frameworks, e.g., updating a state from a background thread that is then read by the main UI thread to re-display it on a widget.
This is because Rust strictly enforces an "aliasing XOR mutability" rule for memory safety, meaning that there cannot be multiple simultaneous mutable aliases to a piece of shared state — only one mutable alias *or* multiple immutable aliases, but not both.

For example, a global static variable can be freely aliased multiple times, but only accessed *mutably* through unsafe code, which is undesirable, or via a wrapper type that offers interior mutability with some sort of mutual exclusion mechanism, e.g., a `Mutex`.
Even for states shared across different parts of a single thread, e.g., among async tasks, mutability still must be separated from aliasing, which is typically realized via the `RefCell` wrapper type (a single-threaded `Mutex` equivalent). 
Also, as Rust lacks runtime garbage collection, the de facto alternative is to wrap states with reference-counter pointer type, e.g., `Rc` or `Arc`, for easy sharing of states whose lifetimes are only determinable at runtime.
The result of these rules and conventions is that code becomes less ergonomic and readable, as it must be littered with `Arc<Mutex<State>>` or `Rc<RefCell<State>>` patterns rather than just direct access to `State`.

### 3. Slow compilation
Third, the Rust compiler has a reputation for being "slow" in that compile times for large Rust projects can be high, at least compared to other languages.
This is primarily due to the need for and the ability of Rust to perform more safety checks at compile time than other languages.
The problem with slow compilation is that it lengthens the iterative development cycle, making it more tedious to test a quick change and reducing the overall productivity of app developers.
The good news is that compilation times are continuously improving thanks to the efforts of [Nick Nethercote and others](https://nnethercote.github.io/), but this still may pose a problem to Rust frameworks that wish to incorporate many features into a project build.

### 4. Steep learning curve
Finally, Rust is known to have a steep learning curve, as the aforementioned rules for memory safety often present a barrier to newcomers, colloquially referred to as ["fighting the borrow checker"](https://www.google.com/search?q=rust+fighting+the+borrow+checker).
While systems programmers and low-level programmers may already possess a deeper understanding of memory models and memory safety restrictions, frontend developers are less likely to be intimately familiar with these topics, as they are accustomed to working in higher-level languages that abstract away and handle memory management implicitly.
A survey from Very Good Ventures found that [frontend developers needed around 3.5 months of retraining](https://verygood.ventures/whitepaper/business-value-of-flutter) to switch from a platform-native framework to the cross-platform Flutter framework before they could be equally productive.
It is possible that switching frontend developers to a Rust-based multi-platform framework like Robius could impose an even steeper barrier to entry.
As framework designers, we must be careful to strike a balance between explicitness, expressiveness, and simplicity in order to not get in the way of app developers' intentions and productivity.


<!-- cspell:ignore Nethercote -->
