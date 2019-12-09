A collection of links to published articles, blog posts, talks, and other important pieces of history of the SpiderMonkey JavaScript engine.

The goal is try to collect together much of what has been written about SpiderMonkey across the internet. This includes research done atop SpiderMonkey, as well as techniques and advances within the engine.


#### Annotations

* 🏚 Obsolete: Code removed from today's SpiderMonkey codebase.
* 🎓 Academic Source
* 📄 Link to PDF
* 📽 Video


## Compiler Technology

* [Debugging in the Time of JITs](https://rfrn.org/~shu/2014/05/14/debugging-in-the-time-of-jits.html) - _Shu-yu Guo_

### Tracemonkey 🏚

TraceMonkey was the first JIT compiler added to SpiderMonkey, and [removed in Mozilla 11](https://bugzilla.mozilla.org/show_bug.cgi?id=698201).

* [Trace-based just-in-time type specialization for dynamic languages](https://dl.acm.org/citation.cfm?id=1542528) - _Brendan Eich, Andreas Gal, Mike Shaver, David Anderson, David Mandelin, Mohammad R. Haghighat, Blake Kaplan, Graydon Hoare, Boris Zbarsky, Jason Orendorff, Jesse Ruderman, Edwin W. Smith, Rick Reitmaier, Michael Bebenita, Mason Chang, Michael Franz_, PDLI '09 🎓

* [An Overview of TraceMonkey](https://hacks.mozilla.org/2009/07/tracemonkey-overview/) - _David Mandelin_

### JaegerMonkey 🏚

The first method compiler added to SpiderMonkey ([_More Info Wanted!_](https://github.com/mgaudet/SpiderMonkeyBibliography/issues/1))

### IonMonkey

* [IonMonkey in Firefox 18](https://blog.mozilla.org/javascript/2012/09/12/ionmonkey-in-firefox-18/) - _David Anderson_ (2012)
* [Recover Instructions](https://nbp.github.io/slides/RInstruction/) - _Nicolas B. Pierron_
* [Just-in-Time Value specialization](https://ieeexplore.ieee.org/document/6495006) - _Igor Costa, Péricles Alves, Henrique Nazaré Santos, Fernando Magno Quintão Pereira_, CGO '13, 🎓 [📄](https://homepages.dcc.ufmg.br/~fernando/publications/papers/CGO13_igor.pdf)
* [A journey into IonMonkey: root-causing CVE-2019-9810](https://doar-e.github.io/blog/2019/06/17/a-journey-into-ionmonkey-root-causing-cve-2019-9810/) - _Axel "0vercl0k" Souchet_, (2019)

### OdinMonkey (asm.js)

* [asm.js in Firefox Nightly](https://blog.mozilla.org/luke/2013/03/21/asm-js-in-firefox-nightly/) - _Luke Wagner_
* [asm.js AOT compilation and startup performance](https://blog.mozilla.org/luke/2014/01/14/asm-js-aot-compilation-and-startup-performance/) - _Luke Wagner_

### Rabaldr (wasm baseline compiler)

* [Making WebAssembly even faster: Firefox’s new streaming and tiering compiler](https://hacks.mozilla.org/2018/01/making-webassembly-even-faster-firefoxs-new-streaming-and-tiering-compiler/) - _Lin Clark_

### BaldrMonkey (WebAssembly)

* [Making asm.js/WebAssembly compilation more parallel in Firefox](https://blog.benj.me/2016/04/22/making-asmjs-webassembly-compilation-more-parallel) - _Benjamin Bouvier_ (story of the refactoring of Odin into Baldr + parallel compilation)
* [Calls between JavaScript and WebAssembly are finally fast 🎉](https://hacks.mozilla.org/2018/10/calls-between-javascript-and-webassembly-are-finally-fast-%f0%9f%8e%89/) - _Lin Clark_ (fast calls between JIT and WebAssembly in both ways)

### Baseline

* [The Baseline Compiler Has Landed](https://blog.mozilla.org/javascript/2013/04/05/the-baseline-compiler-has-landed/) - _Kannan Vijayan_

### CacheIR

* [CacheIR: A new approach to Inline Caching in Firefox](https://jandemooij.nl/blog/2017/01/25/cacheir/) - _Jan de Mooij_

### Type Inference

* [Fast and precise hybrid type inference for JavaScript](https://dl.acm.org/citation.cfm?id=2254094) - _Brian Hackett, Shu-yu Guo_ 🎓 [📄](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.365.9413&rep=rep1&type=pdf)

### Optimization Tracking 🎓

* [Optimization Coaching for JavaScript](https://2015.ecoop.org/event/research-track-optimization-coaching-for-javascript) - _Vincent St-Amour, Shu-yu Guo_ ECOOP '15 [📄](http://www.ccs.neu.edu/home/stamourv/papers/optimization-coaching-js.pdf)
    * [Presentation 📽](https://www.youtube.com/watch?v=ZBYj9UHoml0)

## Debugger

* [Making SpiderMonkey's Debugger Just-in-Time](https://rfrn.org/~shu/2014/11/20/speeding-up-debugger.html) - _Shu-yu Guo_

## Embedding

* [Code-generating Away the Boilerplate in Our Migration Back to Spidermonkey](https://engineering.mongodb.com/post/code-generating-away-the-boilerplate-in-our-migration-back-to-spidermonkey) - _Jason Carey_
* [SpiderMonkey Embedding Examples](https://github.com/spidermonkey-embedders/spidermonkey-embedding-examples)

## Garbage Collection

* [Garbage collection](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/SpiderMonkey/Internals/Garbage_collection) - _MDN_
* [GC Rooting Guide](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/SpiderMonkey/GC_Rooting_Guide) - _MDN_
* [Compacting Garbage Collection in SpiderMonkey](https://hacks.mozilla.org/2015/07/compacting-garbage-collection-in-spidermonkey/) - _Jon Coppeard_
* [Generational Garbage Collection in Firefox](https://hacks.mozilla.org/2014/09/generational-garbage-collection-in-firefox/) - _Steve Fink_
* [Incremental GC in Firefox 16!](https://blog.mozilla.org/javascript/2012/08/28/incremental-gc-in-firefox-16/) - _Bill McCloskey_
