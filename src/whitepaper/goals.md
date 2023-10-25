# Project Goals

The Robius project has established and will strive to achieve the following goals:

* Establish a Rust app dev community and drive ecosystem development
* Create reference design of full app + system stack
* Develop flagship apps and simpler demo apps as proofs of concept
* [Future] Give feedback to Rust's lang, libs, and cargo teams


The following sections provide more details on each of these goals.
All in all, we hope that Robius will attract front-end developers to the world of Rust and encourage existing Rust experts to broaden their horizons and explore the application development domain as well.


## Community and ecosystem
Our goal is to establish the Robius project as a collective, communal space for all things related to multi-platform app development in Rust.
As this community doesn't yet exist, we must build it from the ground up.
Thus far, we have the `project-robius` GitHub organization that aims to serve as a starting point, but once the vision has had more time to incubate and grow, we will create a working group related to app dev in Rust.
We also intend to host and maintain an "are we app yet" website that tracks the status and progress of our Rust app dev work in a public and easy-to-follow format.


As part of building this community, we aim to collect and maintain a set of crates related to app dev that are highly functional and actively supported.
In short, this amounts to identifying key projects in the space and inviting their authors, maintainers, and contributors to participate in the larger Robius vision.
Thus far, we have welcomed two major UI frameworks, Makepad and Dioxus, and a platform abstraction framework, Osiris, into the community.
We aim to foster collaboration between these founding projects in order to enable each project to jointly benefit from contributions and improvements to other projects.

> If you are interested in adding your project or suggesting another project to add to Robius, please don't hesitate to reach out to us.
> We're always looking for more projects to include in the Robius ecosystem!


Another major goal of the Robius vision is to drive the *non-code* components of the ecosystem forward, i.e., documentation.
This whitepaper is one example, but we also strive to publish and support holistic (cross-project) docs and detailed tutorials, as well as provide a platform for blogs and discussion forums related to Rust app development.


## Reference design for full-system stack

The central goal of the Robius project is to deliver a complete working solution for multi-platform app development, in which all components in both the application and the systems stack are written in Rust.

We call this a "reference design" because it embodies only *one* incarnation of how the ecosystem of loosely-coupled components can be assembled into a fully-working stack.
The intent is for the reference design to act as a "blessed" systems stack that new developers can use to quickly and easily start building apps, i.e., a pre-integrated combination of components that are known to work well together.
At the same time, we wish to allow expert developers to tailor the stack to meet their more complex needs, e.g., by selecting or building different components to replace individual pieces of the stack.


The goal of the Robius reference design is to support all major platforms and OS environments, with mobile and desktop being the priority targets:
* Mobile: Android, iOS
* Desktop: Linux, macOS, Windows
* Other: OpenHarmony
* Web (plus WebAssembly) 

The following diagram shows the proposed architecture of this reference design, which is described in greater detail in the system architecture section of this whitepaper.

![Robius Reference Design](img/reference_design.png)


## Flagship apps and examples

Coming soon!

## Advertise business value

Coming soon!

<!-- [Long term] Evangelize for usage of Rust + Robius in app dev business cases
[Long term] Drive the development of a stable, robust app dev Rust ecosystem -->

