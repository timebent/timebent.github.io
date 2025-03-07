---
layout: post
title:  "MoxSonic Workshop"
subtitle: live coding
date:   2025-03-05 16:56:52 -0400
categories: live_coding
tags: live_coding
image: /assets/images/algorave.png
---

I am happy to have the opportunity to share the first few years of my journey into live coding. The workshop will unfold as follows:

1) Introduction to live coding. 
    - A general overview of live coding and its history
    - A brief discussion well-known options for live coding 
    - A bit of how Tidalcycles and Strudel function
    - Strudel as a starting point for live coding

2) Tempo and Rhythm in Strudel
    - An assumption of repeating cycles
    - Cycles per minutes
    - Functions and Patterns Syntax 

<script src="/assets/embed.js"></script>
<strudel-repl>
  <!--
// A simple exambple of how a cycle can be divided in strudel
// Here we divide the cycle into 4 parts using the "." notation


setcpm (110 / 4)

let wordUp = sound("[bd hh] . [rim bd] . [hh -] . [rim -]")
    // ._pianoroll()

// or

// let wordup = sound("[bd hh] [rim bd] [hh -] [rim -]")
    // ._pianoroll()

// or

// let wordup = sound("bd hh . rim bd . hh - . rim -")
    // ._pianoroll()


let bd = sound("bd:1 . - . - . -!3 bd:1")
  .bank('Linn9000')

stack(wordUp, bd)
-->
</strudel-repl>

<script src="https://unpkg.com/@strudel/embed@latest"></script>
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

<script src="https://unpkg.com/@strudel/embed@latest"></script>
<strudel-repl>
  <!--
setcpm (40/4)
let hh = sound("[hh hh] [hh hh] [hh*5]@2 [hh hh] [hh hh]")
// let hh = sound("[hh hh] [hh hh] [[hh*3]@2 hh hh hh]@2 [hh hh] [hh hh]")
//let hh = sound("[hh hh] [hh hh] [hh*5]@2 [hh hh] [hh hh]")
// let hh = sound("[hh hh] [hh hh] [[hh*3]@2 [hh*5]@2 hh]@2 [hh hh] [hh hh]")
stack(hh, bd)
-->
</strudel-repl>

<br>