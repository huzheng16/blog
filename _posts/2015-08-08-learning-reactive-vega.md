---
layout: post
title: Learning Vega 2.0 a.k.a. Reactive Vega
date: '2015-08-08T18:38:52+02:00'
author: enrico_spinielli
comments: true
tags:
- vega
- Grammar of graphics
- D3.js
- Grammar of interaction
modified_time: '2015-08-08T18:39:13+02:00'
---
<style>
h1 ~ aside {
  font-size: small;
  right: 0;
  position: absolute;
  width: 180px;
}
</style>
# Learning Vega 2.0 #

## A Grammar of Graphics ##
Vega 2.0 adds a _grammar of interaction_ to the _grammar of graphics_ implemented in Vega 1.0.

When you say _grammar of graphics_ all roads bring you to

> Leland Wilkinson
> [The Grammar of Graphics](http://books.google.com/books/about/The_Grammar_of_Graphics.html?id=_kRX4LoFfGQC)
> Springer Science & Business Media, Jul 15, 2005

But given [the price of 100+ USD](http://www.amazon.com/Grammar-Graphics-Statistics-Computing/dp/0387245448/),
I am not even thinking of getting my hands on it.

So the next thing you can look at is who has build upon this conceptual framework.
And then we bump into

> Hadley Wickham.
> A layered grammar of graphics.
> Journal of Computational and Graphical Statistics, vol. 19, no. 1, pp. 3–28, 2010.
> http://vita.had.co.nz/papers/layered-grammar.html

which implements a (layered) grammar of graphics as a package for the excellent
[R language](https://www.r-project.org/).
The article in the "Conclusions" section raises the question of how to add interaction to the `ggplot2` framework.

## ... and a Grammar of Interaction ##
Moving to Vega, from its own site

> Vega is a visualization grammar, a declarative format for creating, saving, and sharing interactive visualization designs


The _interactive_ was not present in the first implementation as of Apr 2014, it has been added and publicly described in

> Arvind Satyanarayan, Kanit Wongsuphasawat, Jeffrey Heer
> Declarative Interaction Design for Data Visualization
> ACM User Interface Software & Technology (UIST), 2014,
http://idl.cs.washington.edu/papers/reactive-vega


## And now let's use it ##
All that reading is ok but without doing I do not fully get it (and even then ... ;-)
I need [examples](http://bost.ocks.org/mike/example/)

So the [Vega tutorial](https://github.com/vega/vega/wiki/Tutorial) is a very good starting point
(and like all tutorials [it can be perfected](https://github.com/vega/vega/issues/308) by
[inspirational minds](https://github.com/vega/vega/issues/308#issuecomment-125266356)),
as well as the interactive and non examples in the [Vega Editor](http://vega.github.io/vega-editor/?spec=bar).

Here of course you have less textual description about the what's and why's.

So for doin my part I implemented what requested as en exercise at the end of the tutorial.
That is

"convert [the (vertical) bar plot](https://bl.ocks.org/espinielli/358d490182efc1beace5)


<p class="slide"><iframe data-src="https://bl.ocks.org/espinielli/358d490182efc1beace5" width="960" height="580" marginwidth="0" marginheight="0" scrolling="no"></iframe>

to [an horizontal one](https://bl.ocks.org/espinielli/64b0be9bc33d1405bc92):

<p class="slide"><iframe data-src="https://bl.ocks.org/espinielli/64b0be9bc33d1405bc92" width="960" height="580" marginwidth="0" marginheight="0" scrolling="no"></iframe>


The interactive bit in both blocks is evident when you hover your mouse on the bars and the relevant amount is textually shown.
Sinple and it renders the concept.