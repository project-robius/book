## Consistency across platforms
The fourth requirement of cross-platform consistently is relevant to both runtime and build-time behavior, though is primarily focused on the latter.
The key part of this requirement is that developers should never be *required* to touch platform-specific code in their application.
However, they should be able to access platform-specific functionality with relative ease, if desired or needed.
Though challenging, Robius can meet this requirement through careful design of abstractions that easily reveal lower-level features, e.g., downcasting Rust traits to concrete platform-specific types.

The runtime-focused aspect of this requirement is that platform-agnostic abstractions should impose no overhead (or as little as possible) compared to using the underlying platform-native code directly.
Although this is technically more of a design-time requirement, the implementation choices therein will ultimately affect runtime behavior, namely execution efficiency.
To this end, Rust libraries typically strive to offer zero-cost abstractions, and Robius components shall do the same in this regard.


## Flexibility to incorporate other components
The fifth requirement for flexible componentization is primarily a build tooling concern.
This encompasses two subrequirements at varying levels of importance:
1. Developers must be able to easily incorporate arbitrary third-party components (crates) into the system stack. 
2. (Future) Developers should be able to select between one of many choices for various modularization levels, e.g., pick from multiple UI toolkits when setting up an application project environment.
    * Ideally, a default component could be replaced with a drop-in compatible third-party version of that component[^1].

Robius's build infrastructure must be able to support flexible, modular build manifests.
In addition, the constituent individual projects shall not be tightly coupled to one another, but rather loosely coupled via abstract layers that enable compatibility across different projects that inhabit the same role or responsibility, e.g., UI toolkits, platform abstractions, concurrency runtimes, etc.
Currently, we are working with members of the Cargo team to add any required missing features to Cargo, as well as experimenting with higher-level build systems that sit atop and invoke Cargo as needed.
The Osiris project is also developing its own Cargo-compatible build tool for expressing complex build procedures related to packaging applications into publishable units.

[^1]: This is a distant goal of Robius, but initial versions will likely not support arbitrary drop-in replacement components until Robius is more stable and cross-component boundary interfaces have been clearly established.
