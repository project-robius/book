## Fast application startup

The second requirement in the runtime behavior category is fast startup for applications, i.e., a short app launch time.
Decades of surveys have revealed the importance of this metric, as it affects the overall responsive feel of the system and can reflect very poorly on consumer opinion of company.
For example, [70% of mobile app users will abandon an app](https://www.appsflyer.com/blog/tips-strategy/app-performance/#:~:text=How%20important%20is%20app%20performance,the%20first%20month%20of%20download.) if it takes too long to load, and between [49%](https://embrace.io/blog/observability-mobile-app-performance/#:~:text=According%20to%20a%20recent%20report,fewer%20chances%20before%20uninstalling%20it.) to [59%](https://www.appdynamics.com/blog/engineering/3-mobile-app-performance-issues-you-cant-ignore) of users expect apps to start in under 2 seconds.
Similarly, [studies of webpage load times](https://www.gigaspaces.com/blog/amazon-found-every-100ms-of-latency-cost-them-1-in-sales) found that an extra 0.5 seconds in Google page generation results in 20% less traffic, every 100ms of additional latency reduces Amazon's sales by 1%, and that ultimately [53% of visitors will leave a website](https://neilpatel.com/blog/loading-time/) if it takes over 3 seconds to load.


Our target is a 2-second cold start, which means that an application being launched for the first time since system boot must display its UI and be interactive within 2 seconds.
The *time to initial display* (TTID) should be far less, in that the application must display at least *something* within 500ms.
We derive these requirements from guidelines published by mobile app publishers (iOS and Android), who recommend cold starts within 3-5 seconds, warm starts within 2 seconds, hot starts within 1.5 seconds, and TTIDs within 250-500ms.
We tend to the lower side of the cold start metric, because fast cold start times benefit not only users but also developers, as it helps to shorten the iterative build-run-test development cycle.


Notably, some of these factors are beyond the control of Robius.
For example, on Android, a cold start requires the following procedures: process creation, class loading, application initialization, activity creation, layout inflation, and rendering.
The first two are completely under the control of the platform, while the other four are at least partially under the domain of Robius components.
Similar procedures are undertaken on iOS and desktop platforms.


That being said, design and implementation choices within Robius can affect all stages of application startup.
The primary directive of writing everything in Rust removes the concern about inconsistent performance due to garbage collection or just-in-time compilation jank at startup, because Rust is a fully ahead-of-time compiled language.
However, Rust binary sizes are notoriously larger than other languages, which may increase loading and dynamic linking time when creating the application process.
In general, Robius will follow other canonical best practices for reducing startup latency:  maximize lazy initialization, avoid synchronous operations, move work off of the main UI thread, etc.

<!-- cspell:ignore TTID, TTIDs -->