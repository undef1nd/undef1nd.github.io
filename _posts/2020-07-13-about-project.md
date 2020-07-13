---
layout: post
title: Implementing Structured Headers Parser in Rust
categories: Outreachy
---

It's hard to believe how fast time flies! The second month of my [Outreachy](https://www.outreachy.org/) internship with Mozilla is coming to its end. I guess it's time to tell how my project goes.

In a nutshell, as the title implies, I've been working on a teeny tiny library, "crate" in Rust lingo,  for parsing HTTP headers. It's an implementation of the [existing specification](https://httpwg.org/http-extensions/draft-ietf-httpbis-header-structure.html): the specification "describes a set of data types and associated algorithms that are intended to make it easier and safer to define and handle HTTP header and trailer fields, known as "Structured Fields", "Structured Headers", or "Structured Trailers””. Originally the crate’s name was `structured-headers`, but it has been recently renamed into `sfv` which stands for "structured field values" The ultimate goal is to integrate `sfv` crate into Firefox codebase.

At the very beginning, when my mentor and I talked about the timeline, we didn't set any deadline on per task basis. Instead, we discussed the project phases and agreed that I should have a parser prototype by Week 9. And then I would start working on the wrapper around my library for integration with Firefox. So roughly, my project consists of two phases.

Even though I'm new to Rust, the implementation of the crate itself went more or less smoothly. During the first two weeks, my mentor ran pair programming sessions to help me get started with TDD approach and set up a proper workflow. This well-organized start allowed me to be relatively independent going forward. Of course, I still asked questions, often actually, as I occasionally got stuck or didn't know what was the best approach to use. Sometimes I spent hours on refactoring to see it failing to work eventually. Nevertheless, that time was not wasted, it was rather a part of the learning curve.  I'm quite happy that the library has been built by the expected date. It has some rough edges, it needs improvement, but overall it works and it has a good (IMHO) testing suite. So YAY!

I've also started working on the wrapper code for the crate, which is a part of "integrating crate into Firefox" step. At the very beginning of this chunk of work, I struggled a lot, felt helpless, and needed mentor's help to write even the smallest bit of the code. Most likely, because it requires using thing that is not something one can easily google. I'm talking about writing [XPIDL bindings](https://developer.mozilla.org/en-US/docs/Mozilla/Tech/XPIDL): they will allow using my crate from JS and C++. To my great relief, we've made some significant progress lately. I'm extremely grateful to my mentor Valentin for surviving the never-ending flow of my questions :D

I also maintain the list of nice-to-have things. I used to work on them on those days when I lacked the energy to tackle more complex tasks. Needless to say, there's still plenty of more important work to do, but only one month of the internship is left. So I'm gonna spend this month finishing the planned features.  And, of course, enjoying the rest of my time here at Mozilla.
