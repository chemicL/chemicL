---
categories: conferences
---

Devoxx 2016 Krakow - Day 1
===

Here's a short summary of the best talks I attended at Devoxx 2016 Poland in Krakow.

[The good monolith - bounded contexts in practice (Łukasz Szydło)](http://cfp.devoxx.pl/2016/talk/BLZ-7878/The_good_monolith_-_bounded_contexts_in_practice)
---

Interesting perspective on properly architecting a monolith application with use of Bounded Context from Domain Driven Design methodology.

In short: if you have a user, you don't need to store that users' data in a single entity. View the user in context (e.g. as a client with delivery address vs as a user with logging credentials) and design the modules with different contextual entities instead of a single blown up one. Then apply CQRS (Command and Query Responsibility Segregation) to clearly define where a particular context can be modified.

This talk could have been delivered in 10 minutes though and some code samples could have been presented for clarity.

[Blockchain and distributed ledgers for developers (Mark Van Cuijk)](http://cfp.devoxx.pl/2016/talk/WRV-3066/Blockchain_and_distributed_ledgers_for_developers)
---

A concise introduction to Blockchain, the underlying protocol for Bitcoin. No deep dive into implementation details, but a thorough overview of problems and involved components:

1. State machine with a validation function
2. Distributed Network
3. Consensus algorithm (e.g. lottery, voting)
4. Chain of blocks with immutable history and hashing
5. Authorization

Mark gave reasons when this approach can be useful:

- a distributed database needed
- multiple writers
- not fully trusted behaviour of agents

In conclusion Mark suggested Blockchain is usually not a viable solution for most systems, which proved this was a pragmatic talk.

[Building common libraries and not failing at it (Piotr Betkier)](http://cfp.devoxx.pl/2016/talk/FHE-5810/Building_common_libraries_and_not_failing_at_it)
---

An excellent talk delivered by my teammate. Thoughts derived from experience of providing commonly used libaries and frameworks for multiple teams across Allegro.

Piotr suggested building reusable and composable libraries vs a big framework in a catch all cases style. At Allegro, a common Spring Boot Starter libary has been created, where particular features can be enabled or disabled when needed.

Minimal dependencies and runtime dependencies were advised.

I think Piotr covered it all in this talk.

[JVM dive for mere mortals (Jakub Kubryński)](http://cfp.devoxx.pl/2016/talk/HPE-0572/JVM_dive_for_mere_mortals)
---

Wonderful and extremely concise overview of the bits and pieces that a JVM does. I'd say Jakub has not said any unnecessary word, or that no sentence could have been more compacted. Things were pretty clear with his explanatations.

Things explained:

- what javac produces
- classloaders
- interpreter
- JIT techniques and tiered compilation
- memory layout
- object layout
- gc
- generics and type erasure myth (mostly the type info remains at runtime)
- dispatch types in bytecode
- why throwing exceptions is expensive (@Override fillStackTrace and it's not expensive any more)

Recommended book: Optimizing Java (Not out yet)

A great hint: when debugging in IntelliJ Idea, there's no need to run again if you dived inside the stack too much. You can right-click on the call stack and select "Drop Frame" to get to the interesting context.

There's also a github repo with examples from the presentation: https://github.com/jkubrynski/jvm-dive-benchmarks
