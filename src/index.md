# Introduction to Robius

Robius is a fully open-source, decentralized, community-driven effort to enable multi-platform application development in Rust.

The Robius organization also acts as an informal[^1] working group: a welcoming, public space to collect and discuss resources related to improving and furthering the app dev experience in Rust.

> Got a question? Want to get involved? Interested in contributing?    
> Come join our friendly community on the [Matrix chat Robius space](https://matrix.to/#/#robius:matrix.org).


## Our vision

We believe that the Rust programming language is the right choice for the next generation of application developers,
but that the language ecosystem needs a bit more love and attention to make it a first-class citizen in the world of application development, particularly on mobile platforms.

We envision a future in which:
1. Rust developers can create safe, beautiful, and robust applications that execute efficiently and performantly on a wide variety of platforms, especially mobile.
2. Frontend developers using other languages are encouraged to come over to the ~~dark side~~ wonderful world of Rust and give it a try, with a seamless transition experience that helps overcome the steep learning curve commonly associated with Rust.
3. The Rust ecosystem is broadened and strengthened, demonstrating to existing Rust experts in other domains that Rust is a great fit for application development, not just low-level systems and embedded programming.


### What's in a name?
The name *Robius* comes from the Latin word [robius](http://latin-dictionary.net/definition/33662/robius-robia-robium), meaning red in color, as in oxen, wheat, rust, etc.
This makes for a nice color-based connection to Rust, our programming language of choice.

Robius rhymes with Mobius, and our logo/icons take inspiration from the wordplay combination of "Rust" and "Mobius strip". 

> Yes, *technically*, the original German name is Möbius, but we use an Americanized pronunciation with a long "o" sounds: "Roe-bee-us" / ˈɹoʊˈbiəs.


## Key Community Projects
The Robius ecosystem consists of several independent projects that can be composed into a complete system stack to realize fast, painless application development across multiple platforms in pure Rust.
Components are loosely coupled, allowing a developer (in the future) to customize which components are used to comprise the underlying system, such as choosing 

* [Makepad] is a cross-platform UI toolkit currently under active development that offers a hybrid retained-mode and immediate-mode UI model.
  * Rapid development cycle: *very* fast compile times due to a custom minimal dependency set, plus a custom DSL for live design that enables hot reloading of UI elements.
  * Makepad Studio: an IDE prototype built using Makepad itself with unique features like cross-process shared textures for live reload of an in-window UI app, docking tabs for file/window views, hyper-smooth code folding, and more.
  * Makepad framework: a (growing) collection of highly-performant widgets and minimal, zero/low-overhead platform abstractions.

* [Dioxus] is a cross-platform, production-ready UI toolkit that is inspired by React, with a custom metalanguage called RSX that is used to declare UI elements/layout in an HTML-like style.
  * Supports *many* platforms with a set of interchangeable target renderers, including desktop, webapps, static sites, text UIs, liveview, and mobile.
  * Fast and memory-efficient, with perfect lighthouse scores and performance orders of magnitude better than Node or Python.
  * Excellent built-in abstractions for state management.
  * Easy, familiar styling using vanilla CSS or the CSS framework of your choice, e.g., Tailwind.

* [Osiris] is a set of Rust interfaces for developing immersive applications atop a diverse set of operating systems services and platform-specific functionality.
  * Osiris aims to provide Rust apps with an easy canonical way to access platform features like storage, networking, multimedia (video, audio, camera), geolocation, device orientation (accelerometer, gyro), timers & alarms, notifications, clipboard, drag-n-drop, and more. 
  * `osi`: the primary Rust package that exposes direct access to OS interfaces. Higher-level Rust abstractions are coming soon, after raw interfaces for more platforms are complete.
  * Osiris offers build tooling that can:
    1. Set up new project directories with auto-generated scaffolding for platform-specific integration components that can be customized post-creation.
    2. Generate application artifacts that adhere to the policies of each platform, i.e., packages that can be published to common app stores (Google Play, Apple App Store, Microsoft Store, etc).

* [ylong] is an async runtime for Rust that includes:
  * *Priority*-based scheduling of tasks.
  * Abstractions for auto-parallelizing computation, offering parallel iterators over data in a manner similar to [rayon], but for *async tasks* rather than native (OS-level) threads.
  * Standard primitives for non-blocking async I/O, async synchronization, and async timers.
  * An executor and reactor to schedule tasks and respond to system events, respectively.



## Repositories of Interest

Robius aims to provide a fully-functional *reference design* of the entire system stack beneath the application, for which an architectural overview and detailed documentation will be available.

We also intend to provide two classes of actual applications:
1. Flagships: complete, fully-featured apps with a clean UI design, polished UX, and functional business logic. These apps will be publishable to platform app stores.
2. Simple demos: a series of basic example apps that exhibit a few key features, with mock components underneath and elsewhere.

#### Flagship apps
* Robrix: the Robius Matrix chat client.  Coming soon!
  * The needs of this app will be the primary driver for Robius development.

#### Simple demo apps
* [`makepad_social_media_feed`]: a mobile UI demo of a social media feed.
  * Also see Makepad's more recent example: [Makepad news feed](https://github.com/makepad/makepad/tree/master/examples/news_feed).
* [`makepad_taobao`]: a UI demo for an online shopping app, similar to eBay or Taobao.
* [`todo_makepad`]: a basic to-do list app.
* [`makepad_wechat`]: a demo of a chat-like app UI, like WeChat, WhatsApp, Signal, etc.
* [`makepad_tiktok`]: a UI demo for a TikTok-style short video browsing app.
* [`makepad_widgets_sample`]: an app showcasing various widgets offered by Makepad.
* [`makepad_image_manipulation`]: a demo of Makepad's ability to do funky transformations on images with high performance.
* 7 GUIs: select implementations of the 7 GUIs benchmark, atop both [Makepad](https://github.com/project-robius/makepad_7guis) and [Dioxus](https://github.com/project-robius/dioxus_7guis).


For more examples, check out the extensive set of [Dioxus example apps](https://github.com/DioxusLabs/example-projects) and [Makepad example apps](https://github.com/makepad/makepad/tree/master/examples). 
Osiris-specific examples are coming soon.



## Contributing
We welcome contributions, ideas, and suggestions from anyone! We're also open to help you host and maintain your project under the umbrella of the Robius organization.

As mentioned at the top, please feel free to reach out to our friendly community of devs on the [Robius space on Matrix chat](https://matrix.to/#/#robius:matrix.org).


<!-- Links below -->
[robius_book]: #
[Makepad]: https://makepad.nl/
[Makepad_github]: https://github.com/makepad/makepad
[Dioxus]: https://dioxuslabs.com/
[Dioxus_github]: https://github.com/DioxusLabs/dioxus
[Osiris]: https://github.com/osiris-apis
[ylong]: https://gitee.com/openharmony/commonlibrary_rust_ylong_runtime
[rayon]: https://crates.io/crates/rayon


[`makepad_social_media_feed`]: https://github.com/project-robius/makepad_social_media_feed
[`makepad_widgets_sample`]: https://github.com/project-robius/makepad_widgets_sample
[`makepad_taobao`]: https://github.com/project-robius/makepad_taobao
[`makepad_wechat`]: https://github.com/project-robius/makepad_wechat
[`todo_makepad`]: https://github.com/project-robius/todo_makepad
[`makepad_tiktok`]: https://github.com/project-robius/makepad_tiktok
[`makepad_image_manipulation`]: https://github.com/project-robius/makepad_image_manipulation

[^1]: Robius is not officially affiliated with the Rust project or Rust foundation.


<!-- cspell:ignore Mobius, Möbius, ˈɹoʊˈbiəs -->
