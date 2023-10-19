# Robius Whitepaper

This chapter contains an informal whitepaper about the Robius project, including:
* The motivation behind Robius — why we chose to embark upon this journey.
* Project goals — what we want to achieve.
* Technical requirements — qualitative and quantitative metrics we must hit.
* System Architecture — a reference design for the full system stack.

You can also view this whitepaper content as:
* [a PowerPoint slide deck (18MB)](https://github.com/project-robius/files/raw/041e980ec1d14bf325f1fb2ba743f8ed142a70cb/Robius%20-%20A%20Vision%20for%20Multi-platform%20App%20Development%20in%20Rust.pptx), [PDF version (15MB)](https://github.com/project-robius/files/blob/041e980ec1d14bf325f1fb2ba743f8ed142a70cb/Robius%20-%20A%20Vision%20for%20Multi-platform%20App%20Development%20in%20Rust.pdf)
* [a conference talk on YouTube](https://youtu.be/8JfOXfmwotQ?si=kLogqnaApYPNuSq8&t=6802)


## Elevator pitch — Robius in 60 seconds
The Robius project's primary focus is to provide a multi-platform application development toolkit where both the app and the entire system stack are written completely in Rust.
This will enable developers across all layers to leverage the many benefits of Rust: safety, efficiency, fearless concurrency, high performance, and a robust ecosystem of crates spanning many domains.
A Rust-only stack avoids the additional complexity brought on by introducing other languages via FFI interop layers; these "bridges" only facilitate the usage of Rust for business logic, and impose high overhead when crossing the boundary between Rust and the platform-native framework.

Robius's secondary focus is to make the Rust experience on mobile platforms feel like a first-class citizen.
Historically, Rust on mobile has been a neglected area of the ecosystem, missing key components from build tooling to native-like UIs and widgets to platform support crates.
We want to make Rust as enjoyable to use on mobile platforms as it is to use in systems programming environments.


Robius is and always will be fully open-source, decentralized, and community-driven.



## What's in a name?
The name *Robius* comes from the Latin word [robius](http://latin-dictionary.net/definition/33662/robius-robia-robium), meaning red in color, as in oxen, wheat, rust, etc.
This makes for a nice color-based connection to Rust, our programming language of choice.

Robius rhymes with Mobius, and our logo/icons take inspiration from the wordplay combination of "Rust" and "Mobius strip". 

> Yes, *technically*, the original German name is Möbius, but we use an Americanized pronunciation with a long "o" sound: "Roe-bee-us" / ˈɹoʊˈbiəs.


<!-- cspell:ignore Mobius, Möbius, ˈɹoʊˈbiəs -->
