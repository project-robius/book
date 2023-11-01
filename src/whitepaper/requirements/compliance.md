## Compliance with platform policies

The sixth and final requirement is for real-world applications developed using Robius to be fully compliant with platform-specific policies.
This concerns both runtime behavior and decisions made at build time, with the ultimate purpose of ensuring that Robius apps can be published to actual app stores, e.g., Google Play Store (Android), Apple's App Store (iOS, macOS), Microsoft Store (Windows), Flatpak's Flathub (Linux), and more. 

Attempting to publish applications that do not comply with these policies results in errors, such as these returned by build tools on iOS:
* > Error: the app references non-public symbols in `<path>`. If method names in your source code match the private Apple APIs listed above, altering your method names will help prevent this app from being flagged in future submissions. In addition, note that one or more of the above APIs may be located in a static library that was included with your app. If so, they must be removed.
* > Error: Invalid Bundle Structure - The binary file `<file>` is not permitted. Your app can't contain standalone executables or libraries.
* > Note: applications must be packaged and submitted using technologies provided in Xcode; no third-party installers allowed. They must also be self-contained, single app installation bundles and cannot install code or resources in shared locations.


The corresponding design-time requirement is that Robius must not depend on private platform APIs to realize higher-level abstractions.
Technically, we can leverage such hidden functionality for "hacky" non-compliant solutions that speed up dev builds, as long as they can be transparently replaced with the official APIs for publishable release builds.
For example, Makepad provides custom, stripped-down versions of Android and iOS SDK modules, which shrinks the size and scope of these dependencies, *significantly* reducing compile times. 
However, publishing an app built against these dependencies may not be compatible with all platform guidelines.



To this end, Osiris build infrastructure ensures that platform requirements are met by always using the native platform toolchain to generate the final package.
This prevents accidental violations of packaging requirements, e.g., including third-party components that are not allowed in the app package.
An additional advantage of this approach is easy integration with other platform-specific tools, such as linters, package checking systems, static analyzers, performance profiling tools, and more.


The corresponding runtime requirement is that Robius must not attempt to download or run third-party code not originally included in the app package, which is mostly a concern on mobile platforms.
Loading said foreign code is expressly forbidden on iOS and implicitly disallowed on Android.
Similarly, just-in-time (JIT) compilation of code is also prohibited on iOS, while Android's ART runtime has deprecated JIT in favor of ahead-of-time (AOT) compilation.
Android also therefore no longer supports loading class files from native code.
These restrictions render certain potential mechanisms for cross-platform abstractions impossible, forcing us to adopt other solutions that comply with these rules.
