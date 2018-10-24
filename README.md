A collection of links to published articles, blog posts, talks, and other important pieces of history of the SpiderMonkey JavaScript engine. The goal is try to collect together much of what has been written about SpiderMonkey across the internet. 


#### Annotations

* 🏚 Obsolete: Code removed from today's SpiderMonkey codebase. 
* 🎓 Academic Source
* 📄 Link to PDF
* 📽 Video

## Compiler Technology


### Tracemonkey 🏚

TraceMonkey was the first JIT compiler added to SpiderMonkey, and [removed in Mozilla 11](https://bugzilla.mozilla.org/show_bug.cgi?id=698201).

* [Trace-based just-in-time type specialization for dynamic languages](https://dl.acm.org/citation.cfm?id=1542528) - _Brendan Eich, Andreas Gal, Mike Shaver, David Anderson, David Mandelin, Mohammad R. Haghighat, Blake Kaplan, Graydon Hoare, Boris Zbarsky, Jason Orendorff, Jesse Ruderman, Edwin W. Smith, Rick Reitmaier, Michael Bebenita, Mason Chang, Michael Franz_, PDLI '09 🎓

* [An Overview of TraceMonkey](https://hacks.mozilla.org/2009/07/tracemonkey-overview/) - _David Mandelin_

### JaegerMonkey

The first method compiler added to SpiderMonkey ([_More Info Wanted!_](https://github.com/mgaudet/SpiderMonkeyBibliography/issues/1))

### IonMonkey

* [IonMonkey in Firefox 18](https://blog.mozilla.org/javascript/2012/09/12/ionmonkey-in-firefox-18/) - _David Anderson_
* [Recover Instructions](https://nbp.github.io/slides/RInstruction/) - _Nicolas B. Pierron_

### Baseline 

* [The Baseline Compiler Has Landed](https://blog.mozilla.org/javascript/2013/04/05/the-baseline-compiler-has-landed/) - _Kannan Vijayan_

### CacheIR

* [CacheIR: A new approach to Inline Caching in Firefox](https://jandemooij.nl/blog/2017/01/25/cacheir/) - _Jan de Mooij_

### Type Inference

* [Fast and precise hybrid type inference for JavaScript](https://dl.acm.org/citation.cfm?id=2254094) 🎓 [📄](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.365.9413&rep=rep1&type=pdf)

### Optimization Tracking 🎓

* [Optimization Coaching for JavaScript](https://2015.ecoop.org/event/research-track-optimization-coaching-for-javascript) - _Vincent St-Amour, Shu-yu Guo_ ECOOP '15 [📄](http://www.ccs.neu.edu/home/stamourv/papers/optimization-coaching-js.pdf)
    * [Presentation 📽](https://www.youtube.com/watch?v=ZBYj9UHoml0)

## Garbage Collecction 


* [Compacting Garbage Collection in SpiderMonkey](https://hacks.mozilla.org/2015/07/compacting-garbage-collection-in-spidermonkey/) -  Jon Coppeard

## Embedding 

* [Code-generating Away the Boilerplate in Our Migration Back to Spidermonkey](https://engineering.mongodb.com/post/code-generating-away-the-boilerplate-in-our-migration-back-to-spidermonkey) - _Jason Carey_ 
* [SpiderMonkey Embdedding Examples](https://github.com/spidermonkey-embedders/spidermonkey-embedding-examples) 
