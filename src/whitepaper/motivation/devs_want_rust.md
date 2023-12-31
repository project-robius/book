## 1. Developers *really* want to write apps in Rust
<!-- ## 1. Developers express great interest in writing Rust apps -->


Online programming forums are filled with posts asking how to use Rust to develop mobile, desktop, and web applications. 
We have observed this trend for several years in two main flavors:
* Existing Rust systems-level developers that wonder if they can leverage their Rust knowledge for applications too.
* Frontend app developers that currently use other languages, but want to use Rust because they have heard about its benefits. 

The former group of Rust devs is mainly focused on the biggest unknown to them: creating GUI apps and packaging apps up for mobile targets; this is the first group that we wish to support with Robius.
The latter group of frontend devs have deeper expertise in application-level implementation but are not sure how to transition those skills to the world of Rust; this is the second group that we wish to support.
One major commonality is that both groups are unsure how or where to start developing an app in Rust.

### Ecosystem is fractured and incomplete
The first problem that most aspiring devs encounter is the massive collection of projects, mostly GUI libraries, many of which are incomplete proofs-of-concept or simply abandoned.
Though there are many competing UI frameworks in the main `crates.io` registry, it is difficult to discover which ones are most appropriate for a given application's needs, and even harder to determine whether and how these projects can be integrated with others to form a functional app dev toolkit.


For more evidence, look no further than the [`areweguiyet.org`](https://areweguiyet.com/) website, which aims to track the bevy of GUI crates and their progress. Their homepage states:

> As a low level language, Rust is perfectly suitable for making user interfaces the old fashioned way, with native APIs. However, competing in today's world typically means supporting many platforms, and that makes using native APIs an unattractive option for many.
>
> Rust's expressiveness and high level abstractions make it ideal for building intricate and complex user interfaces. Unfortunately, there is little consensus on what the best abstractions are.
>
> There are a number of bindings available today to existing frameworks, but those looking for a mature, easy to use, and completely Rust-based solution will most likely find themselves out of luck.


Due to the relatively young age of the Rust language itself, many of these crates are incomplete, as building a UI toolkit is a lengthy endeavor.
Most are only proofs-of-concept that offer barebones UI primitives; 
even the more mature and fully-developed crates only offer a partial solution for application development, focusing primarily on the UI appearance and fundamental UX behavior. 

As expected, there is not yet a de facto "best" toolkit, nor has the Rust Foundation or Rust project teams made any official recommendation or guidebook concerning this matter.
Although this is good for the sake of both neutrality and healthy competition, it has led to a fractured ecosystem in which nearly every crate has significant overlap with the functionality of several other crates.
This overlap makes it even harder to select a UI toolkit for a new app, as the differences between toolkits are minimal on paper and only become evident after several weeks of development experience with each one.

All in all, there is a noticeable absence of cohesion and coordination in this ecosystem, presenting the most significant barrier of entry to cross-platform application development in Rust.
This is especially evident when compared to app dev frameworks led by a single directing entity, such as React Native or Flutter. 



### Apps need more than just UI + UX
Even if GUI development in Rust was a solved problem, UIs do not tell the whole story — an application still needs to access services and features from the underlying platform or OS.
As with UI works, there are indeed a plethora of crates that offer basic interfaces to access platform-specific features.
Some offer general abstractions of a single feature across multiple platforms, while others or specific features on a single platform.

These features are crucial to developing *immersive* applications that take full advantage of the software and hardware functionality afforded to them by the device platform.
For example, robust applications typically expect an app dev framework to expose the following:
* camera, multimedia (audio and video) capture and playback, 
* geolocation, haptic feedback actuators like vibration motors,
* system services like notifications, drag and drop, a rich clipboard,
* on-device sensors like accelerometers/gyros, barometers, thermometers, proximity and ambient light sensors, etc,
* local communication protocols like WiFi, Bluetooth, NFC, and more,
* typical I/O like storage, cache space, and networking, in a platform-native manner.

While these crates can certainly be used directly by an application, this model places the serious burden of assembling multiple piecemeal crates into a workable platform abstraction on the shoulders of the application developers themselves.
This expectation is not feasible for most application developers, as they are neither sufficiently experienced nor have the time to undertake such an arduous task.

That is why we created the [**Osiris project**](https://github.com/osiris-apis/osi) — to fill in the gaps and offer a fully-integrated, consistent solution for accessing platform-specific functionality in an abstract manner.



### Documentation is paramount

Another reason many newcomers find it so difficult to get started is that there is a distinct lack of documentation, tutorials, and examples for the vast majority of crates in this domain.

If examples exist, they are extraordinarily simple and only cover the basics of setting up a primitive UI or application skeleton.
Holistic tutorials and complete examples are few and hard to come by, which exacerbates the integration problem. 
Without end-to-end sample code, it is challenging for an expert, let alone a newcomer to the worlds of app dev and Rust, to compose a working system stack by integrating multiple disparate crates together. 

One guiding light in this space is Dioxus, which has [recently released high-quality comprehensive documentation](https://dioxuslabs.com/learn/0.4/reference) for both external users and internal contributors along with several well-commented demo apps, making it both easy and enticing to use Dioxus to create new apps.

For a Rust application development framework to gain real traction, it must lead the pack in terms of documentation quality, tutorial thoroughness, and variety and depth of real-world example application code.

