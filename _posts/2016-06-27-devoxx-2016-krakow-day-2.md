---
categories: conferences
---

Devoxx 2016 Krakow - Day 2
===

On the second day I found just one presentation to be worth mentioning here.

[Understanding Microservice performance (Rob Harrop)](http://cfp.devoxx.pl/2016/talk/WDX-9109/Understanding_Microservice_performance)
---

Very inspiring and deep overview of concepts related to measuring performance. This resembled a lot what Gil Tene talks about in his [How NOT to Measure Latency](https://www.youtube.com/watch?v=lJ8ydIuPFeU) but with a bit more theorems and perhaps more interaction.

Concepts like Little's Law, Amdahl's Law and Universal Scalability Law are easily searchable, so do look them up.

Some tools recommended:

- [PDQ](http://www.perfdynamics.com/Tools/PDQ.html)
- [Guesstimate](https://github.com/getguesstimate/guesstimate-app)
- [R](https://www.r-project.org/) for visualising measurements

Also, Rob gave some useful book recommendations:

- ["Release it!" by Michael T. Nygard](https://pragprog.com/book/mnee/release-it)
- ["Systems Performance" by Brendan Gregg](http://www.brendangregg.com/sysperfbook.html)
- ["Practical Scalability Analysis With The Universal Scalability Law"](https://www.vividcortex.com/resources/universal-scalability-law/)
- ["Guerilla Capacity Planning" by Neil J. Gunther](http://www.perfdynamics.com/iBook/gcap.html)

And a final tip was given: Monitor latency per user, not just per request.
