---
categories: conferences
---

Devoxx 2016 Krakow - Day 3
===

In the end I think first day was the best in terms of my personal selection of talks, but still there were a couple good ones for the conclusion.

[How to Lie (to Yourself) about Performance (Douglas Hawkins)](http://cfp.devoxx.pl/2016/talk/OSR-7014/How_to_Lie_(to_Yourself)_about_Performance)
---

In his talk Douglas explains many pitfalls that await while attempting to measure performance. A very practical presentation, with live demos and code samples.

A brilliant depiction of coordinated ommission using JMeter with it's default settings: launch the server, hit it with Jmeter continuously and observe the measures. Then kill the server while JMeter is running and observe the stats still don't change much. Bring back the server again and observe how it's back to "normal" - there is no sign of downtime in the graphs. Due to timeouts on JMeter's connections, there's less samples so the measurements are skewed towards when the server was up and JMeter is coordinating with the server.

News to me: hprof was never intended for us, but was a demo of [JVM TI](https://docs.oracle.com/javase/8/docs/technotes/guides/jvmti/) and [will be removed](http://openjdk.java.net/jeps/240)

Some hints regarding sampling profilers:

- they take into account all idle threads, which may be misleading
- sampling is done at safepoints, so even a very intensive math operation can be unseen as there might be no safepoints in the method

Instrumentation based profiling might be better in the end, although slower and can affect the behaviour.

Some profilers:

- [lightweight-java-profiler by Google](https://code.google.com/archive/p/lightweight-java-profiler/)
- [Honest Profiler](https://github.com/RichardWarburton/honest-profiler/wiki)

A post by Netflix was mentioned: http://techblog.netflix.com/2015/07/java-in-flames.html

More tools:

- [JMH for micro benchmarks](http://openjdk.java.net/projects/code-tools/jmh/)
- [jHiccup for pauses and stalls](https://www.azul.com/jhiccup/)
- [HdrHistogram for keeping stats in measurements at different resolution](https://github.com/HdrHistogram/HdrHistogram)

[oDDs & enDs (Vaughn Vernon)](http://cfp.devoxx.pl/2016/talk/OBE-3778/oDDs_&_enDs)
---

This wasn't a very technical talk, however what I'd like to note here is that Vaughn highlighted a frequent problem in many companies:

Business sees software development as a cost center, while the devs see business in terms of the database.

A suggestion is given for people in the tech area to be more focused on the business needs and finding solutions to business problems with comprehension, not ignorance, so that one can:

Be the pesron with business sense. Don't just be a technologist.

This goes along with the term frequently mentioned by Martin Thompson - Resume Driven Development.

A key takeaway is an advice: make the business view development as a profit center instead.

Conway's Law also got mentioned (the company organisation is reflected in the designs it produces).
