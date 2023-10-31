## Quick compilation

The third requirement for quick compilation lies solely on the side of build tooling.
Compile time has an even more signifianct impact on the developer experience and iteration cycle length than the previous requirement of fast app startup.

It is difficult to set an absolute value for this metric, as compilation is heavily affected by the nature of the application content.
However, we can establish a target that is more relative: compiling the Robius frameworks shall not constitute an unbearable addition to the overall compilation time of the application.
While this is unrealistic for simple applications, we can revise this into the following:

***Incremental* compilation must be fast enough to be interactive.**

This means that a quick code change should be compilable within a few seconds, such that the developer does not suffer loss of mental focus or context while waiting for compilation to complete.


One major challenge is the pervasive notion across online communities that the Rust compiler is slow.
Although this is a contentious issue, it is true that `rustc` must do more compile-time actions than other languages with fewer static safety guarantees.
While the compiler team has taken [significant action to improve compiler performance](https://nnethercote.github.io/2023/08/25/how-to-speed-up-the-rust-compiler-in-august-2023.html), Robius must be careful to explicitly subvert this negative expectation.


Robius makes several design choices to combat high compilation times.
First and foremost, both the Makepad and Dioxus UI toolkits support **hot reloading**, in which an application can be live updated without restarting it.
This enables developers to instantly observe changes to an application's UI without needing to re-compile at all.
Makepad also provides a minimal set of in-house dependencies for very fast compilation, which helps speed up iterative rebuilding of application components that cannot yet be hot-reloaded.
Another contributing aspect is the desired project structure of many small crates, which enables Robius to benefit from parallelization of distinct compilation units.
