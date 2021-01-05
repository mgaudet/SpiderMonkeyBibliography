A collection of links to published articles, blog posts, talks, and other important pieces of history of the SpiderMonkey JavaScript engine.

The goal is try to collect together much of what has been written about SpiderMonkey across the internet. This includes research done atop SpiderMonkey, as well as techniques and advances within the engine.


#### Annotations

* 🏚 Obsolete: Code removed from today's SpiderMonkey codebase.
* 🎓 Academic Source
* 📄 Link to PDF
* 📽 Video

## History

General history of the SpiderMonkey JavaScript engine: 

* [JavaScript: The First 20 Years](https://zenodo.org/record/3710954), _Allen Wirfs-Brock and Brendan Eich_ (2020)  (Especially Part 1, Section 5: From Mocha to SpiderMonkey) 

## VM

Information about the SpiderMonkey Engine

* [Compiler Compiler](https://hacks.mozilla.org/2020/06/compiler-compiler-working-on-a-javascript-engine/), _Yulia Startsev_ (2020) 📽 [Playlist](https://www.youtube.com/playlist?list=PLo3w8EB99pqJVPhmYbYdInBvAGarDavh-)
* [How do Generators... Generate, in SpiderMonkey?](https://www.mgaudet.ca/technical/2020/9/1/how-do-generators-generate-in-spidermonkey), _Matthew Gaudet_ (2020)
* [A Brief note on Environments and Scopes in SpiderMonkey](https://www.mgaudet.ca/technical/2020/9/10/a-brief-note-on-environments-and-scopes-in-spidermonkey), _Matthew Gaudet_ (2020)

### Debugger

* [Making SpiderMonkey's Debugger Just-in-Time](https://rfrn.org/~shu/2014/11/20/speeding-up-debugger.html), _Shu-yu Guo_ (2014)

### Embedding

SpiderMonkey is designed to be embedded in other programs. This section covers this embedding, and people talking about it

* [SpiderMonkey Embedding Examples](https://github.com/spidermonkey-embedders/spidermonkey-embedding-examples)
* [Code-generating Away the Boilerplate in Our Migration Back to Spidermonkey](https://engineering.mongodb.com/post/code-generating-away-the-boilerplate-in-our-migration-back-to-spidermonkey), _Jason Carey_ (2016)


### Garbage Collection

* [Garbage collection](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/SpiderMonkey/Internals/Garbage_collection) - _MDN_
* [GC Rooting Guide](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/SpiderMonkey/GC_Rooting_Guide) - _MDN_
* [Compacting Garbage Collection in SpiderMonkey](https://hacks.mozilla.org/2015/07/compacting-garbage-collection-in-spidermonkey/), _Jon Coppeard_ (2015)
* [Generational Garbage Collection in Firefox](https://hacks.mozilla.org/2014/09/generational-garbage-collection-in-firefox/), _Steve Fink_ (2014)
* [Incremental GC in Firefox 16!](https://blog.mozilla.org/javascript/2012/08/28/incremental-gc-in-firefox-16/), _Bill McCloskey_ (2012)


### Compiler Technology

SpiderMonkey has a lot of compiler technology, and has had many different JIT compilers embedded within it. 

* [Debugging in the Time of JITs](https://rfrn.org/~shu/2014/05/14/debugging-in-the-time-of-jits.html), _Shu-yu Guo_ (2014)
* [A Beginners Guide to SpiderMonkey's MacroAssembler](https://www.mgaudet.ca/technical/2019/4/9/a-beginners-guide-to-spidermonkeys-macroassembler), _Matthew Gaudet_ (2019)

#### Tracemonkey 🏚

TraceMonkey was the first JIT compiler added to SpiderMonkey, and [removed in Mozilla 11](https://bugzilla.mozilla.org/show_bug.cgi?id=698201).

* [Trace-based just-in-time type specialization for dynamic languages](https://dl.acm.org/citation.cfm?id=1542528), _Brendan Eich, Andreas Gal, Mike Shaver, David Anderson, David Mandelin, Mohammad R. Haghighat, Blake Kaplan, Graydon Hoare, Boris Zbarsky, Jason Orendorff, Jesse Ruderman, Edwin W. Smith, Rick Reitmaier, Michael Bebenita, Mason Chang, Michael Franz_, PDLI (2009) 🎓

* [An Overview of TraceMonkey](https://hacks.mozilla.org/2009/07/tracemonkey-overview/), _David Mandelin_ (2009)

#### JaegerMonkey 🏚

The first method compiler added to SpiderMonkey.

* [Improving JavaScript performance with JägerMonkey](https://hacks.mozilla.org/2010/03/improving-javascript-performance-with-jagermonkey/), ? (2010)
* [Starting JägerMonkey](http://web.archive.org/web/20120420011230/https://blog.mozilla.org/dmandelin/2010/02/26/starting-jagermonkey/), _Dave Mandelin_ (2010)
* [Land Ho, Fast JavaScript](http://www.bailopan.net/blog/?p=768), _David Anderson_ (2010)
* [JaegerMonkey development diary - shaping up THE JavaScript engine for Firefox 4.0](https://www.digit.in/features/general/jaegermonkey-development-diary-shaping-up-the-javascript-engine-for-firefox-4-0-5151.html), _Soumya Deb_ (2010)

#### IonMonkey 

The second method JIT compiler in SpiderMonkey. Warp, [enabled by default in Firefox 83](https://mozilla-spidermonkey.github.io/blog/2020/12/18/newsletter-8.html), has replaced the graph construction (IonBuilder) portion of Ion. 

* [IonMonkey in Firefox 18](https://blog.mozilla.org/javascript/2012/09/12/ionmonkey-in-firefox-18/), _David Anderson_ (2012)
* [Just-in-Time Value specialization](https://ieeexplore.ieee.org/document/6495006), _Igor Costa, Péricles Alves, Henrique Nazaré Santos, Fernando Magno Quintão Pereira_, CGO (2013) 🎓 [📄](https://homepages.dcc.ufmg.br/~fernando/publications/papers/CGO13_igor.pdf)
* [Recover Instructions](https://nbp.github.io/slides/RInstruction/), _Nicolas B. Pierron_ (2014)
* [Optimizing Away](https://blog.mozilla.org/javascript/2014/07/15/ionmonkey-optimizing-away/), _Nicolas B. Pierron_ (2014)

#### WarpBuilder

A new compiler frontend, creating MIR from bytecode, replacing the previous IonBuilder and Type Inference system. 

* [Warp: Improved JS performance in Firefox 83](https://hacks.mozilla.org/2020/11/warp-improved-js-performance-in-firefox-83/), _Jan de Mooij_ (2020) 

##### Exploitation Reports
* [A journey into IonMonkey: root-causing CVE-2019-9810](https://doar-e.github.io/blog/2019/06/17/a-journey-into-ionmonkey-root-causing-cve-2019-9810/), _Axel "0vercl0k" Souchet_ (2019)
* [Exploiting CVE-2019-17026 - A Firefox JIT Bug](https://labs.f-secure.com/blog/exploiting-cve-2019-17026-a-firefox-jit-bug/), _Max Van Amerongen_ (2020)

#### OdinMonkey (asm.js)

* [asm.js in Firefox Nightly](https://blog.mozilla.org/luke/2013/03/21/asm-js-in-firefox-nightly/), _Luke Wagner_ (2013)
* [asm.js AOT compilation and startup performance](https://blog.mozilla.org/luke/2014/01/14/asm-js-aot-compilation-and-startup-performance/), _Luke Wagner_ (2014)

#### Rabaldr (wasm baseline compiler)

* [Making WebAssembly even faster: Firefox’s new streaming and tiering compiler](https://hacks.mozilla.org/2018/01/making-webassembly-even-faster-firefoxs-new-streaming-and-tiering-compiler/), _Lin Clark_ (2018)
* [firefox's low-latency webassembly compiler](https://wingolog.org/archives/2020/03/25/firefoxs-low-latency-webassembly-compiler), _Andy Wingo_ (2020) 


#### BaldrMonkey (WebAssembly)

* [Making asm.js/WebAssembly compilation more parallel in Firefox](https://blog.benj.me/2016/04/22/making-asmjs-webassembly-compilation-more-parallel), _Benjamin Bouvier_ (2016) (story of the refactoring of Odin into Baldr + parallel compilation)
* [Calls between JavaScript and WebAssembly are finally fast 🎉](https://hacks.mozilla.org/2018/10/calls-between-javascript-and-webassembly-are-finally-fast-%f0%9f%8e%89/), _Lin Clark_ (2018) (fast calls between JIT and WebAssembly in both ways)

#### Baseline

* [The Baseline Compiler Has Landed](https://blog.mozilla.org/javascript/2013/04/05/the-baseline-compiler-has-landed/), _Kannan Vijayan_ (2013)
* [The Baseline Interpreter: a faster JS interpreter in Firefox 70](https://hacks.mozilla.org/2019/08/the-baseline-interpreter-a-faster-js-interpreter-in-firefox-70/), _Jan de Mooij_ (2019)

#### CacheIR

* [CacheIR: A new approach to Inline Caching in Firefox](https://jandemooij.nl/blog/2017/01/25/cacheir/), _Jan de Mooij_ (2017)

#### Type Inference 🏚

([Removed in Firefox 84](https://bugzilla.mozilla.org/show_bug.cgi?id=1673553)) 

* [Fast and precise hybrid type inference for JavaScript](https://dl.acm.org/citation.cfm?id=2254094), _Brian Hackett, Shu-yu Guo_ (2012) 🎓 [📄](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.365.9413&rep=rep1&type=pdf)


#### Optimization Tracking 🎓 🏚

* [Optimization Coaching for JavaScript](https://2015.ecoop.org/event/research-track-optimization-coaching-for-javascript), _Vincent St-Amour, Shu-yu Guo_, ECOOP (2015) [📄](http://www.ccs.neu.edu/home/stamourv/papers/optimization-coaching-js.pdf)
    * [Presentation 📽](https://www.youtube.com/watch?v=ZBYj9UHoml0)
