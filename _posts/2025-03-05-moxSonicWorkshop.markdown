---
layout: post
title:  "MoxSonic Workshop"
subtitle: live coding
date:   2025-03-05 16:56:52 -0400
categories: live_coding
tags: live_coding
image: /assets/images/algorave.png
---


<ol>
  <li>Introduction to live coding.
    <ul>
      <li>A general overview of live coding and its history</li>
      <li>A brief discussion well-known options for live coding</li>
      <li>A bit of how Tidalcycles and Strudel function</li>
      <li>Strudel as a starting point for live coding</li>
    </ul>
  </li>
<p> </p>

 <li> Tempo and Rhythm in Strudel
    <ul>
    <li> - An assumption of repeating cycles </li>
    <li> - Cycles per minutes </li>
    <li> - Functions and Patterns Syntax  </li>
    </ul>
  </li>
</ol>


<script src="/assets/embed.js"></script>
<strudel-repl>
  <!--
// A simple exambple of how a cycle can be divided in strudel
// Here we divide the cycle into 4 parts using the "." notation


setcpm (110 / 4)

let wordUp = sound("[bd hh] . [rim bd] . [hh -] . [rim -]")
    ._pianoroll({labels: 1})

// or

// let wordup = sound("[bd hh] [rim bd] [hh -] [rim -]")
     ._pianoroll({labels: 1})

// or

// let wordup = sound("bd hh . rim bd . hh - . rim -")
    ._pianoroll({labels: 1})


// let bd = sound("bd:1 . - . - . -!3 bd:1").bank('Linn9000')

stack(wordUp)
-->
</strudel-repl>

Let's take a moment to see how we can explore more difficult rhythmic structures like nested tuplets. 
The following notation is taken from John Fielder's blog post on nested tuplets.
(http://klangnewmusic.weebly.com/direct-sound/lets-talk-rhythm-part-2-nested-tuplets)

<img src="http://klangnewmusic.weebly.com/uploads/1/2/3/0/12308331/1727048_orig.jpg" alt="John Fielder credit" />

How can we explore this exercise using Strudel's rhythmic notation?

<script src="/assets/embed.js"></script>
<strudel-repl>
  <!--
setcpm (40/4)
let hh = sound("[hh hh] [hh hh] [hh*5]@2 [hh hh] [hh hh]")
let bd = sound("bd . bd . bd . bd . bd . bd")
// let hh = sound("[hh hh] [hh hh] [[hh*3]@2 hh hh hh]@2 [hh hh] [hh hh]")
// let hh = sound("[hh hh] [hh hh] [[hh*3]@2 [hh*5]@2 hh]@2 [hh hh] [hh hh]")
stack(hh, bd)
-->
</strudel-repl>

<script src="/assets/embed.js"></script>
<strudel-repl>
  <!--
let hh = sound("[hh hh hh]@2 [hh*5]@2 [hh hh ~ ~]")
let pulse = sound("cp . cp . cp . cp . cp")
let pulse2 = sound("bd . bd . bd . bd").bank('Linn9000')
// http://klangnewmusic.weebly.com/direct-sound/lets-talk-rhythm-part-2-nested-tuplets
  
// stack(wordUp, bd)
stack(hh, pulse, pulse2)

-->
</strudel-repl>

<br>