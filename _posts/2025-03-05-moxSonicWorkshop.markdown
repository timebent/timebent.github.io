---
layout: post
title:  "MoxSonic Workshop"
subtitle: live coding
date:   2025-03-05 16:56:52 -0400
categories: live_coding
tags: live_coding
image: /assets/images/algorave.png
---

<h2>
Strudel Live Coding Environment<br> 
</h2> 

<ol>
  <h3>Introduction to live coding.</h3>
    <ul>
      <li>A general overview of live coding and its history</li>
      <li>A brief discussion well-known options for live coding</li>
      <li>A bit of how Tidalcycles and Strudel function</li>
      <li>Strudel as a starting point for live coding</li>
    </ul>


<p>An overview of the entire ecosystem live coding environments is impossible here. Instead, I will focus on the set of environments that form the backbone of Tidalcycles or branch from it.  </p>

<p> <strong> SuperCollider </strong> - SuperCollider now has a long and storied history as a powerful variant of the Music N languages. It was designed to run efficiently in real time. Learning the language of SuperCollider and the manner in which the language and server function is a large endeavor. SuperCollider features the Just In Time Programming Library. From the SuperCollider help files:</p>

<blockquote> Here, a program is not taken as a tool that is made first to be productive later, but instead as a dynamic construction process of description and conversation. Writing code becomes an integral part of musical or experimental practice.</blockquote> 

<p> <strong> Estuary </strong> - Collaborative browser based coding. Long distance coding worked quite well with Estuary. We used Estuary to create a performance between Les P (special thanks to Pablo Tobar) in Colombia and the electronic ensemble at Georgia Southern in the fall of 2022. 36 minutes in 
https://www.youtube.com/watch?v=sMfLMXDw_eM </p?>

<p> Estuary can run several different live coding languages, including those meant for visual performance. Estuary's excellent collaborative capabilities are due in part to it being entirely web based. Estuary uses the web audio engine "WebDirt" to play back samples, which must be available online so that every participant can hear them. So, adding samples means adding to a common repository. This process involves forking the repository on github and using git to manage the addition and removal of samples. The process is not intuitive. </p>

<p> For live coding audio, Estuary uses a subset of tidal called mini-tidal. This subset is not fully featured. The Estuary interface contains a way to reference files for different functions with code examples. Additionally, samples are available for use are listed in a separate tab.</p> 

<p> <strong> Tidalcycles </strong> - This coding environment works in conjunction with SuperCollider, and specifically with a third party set of classes and a set of samples called SuperDirt. Running SuperDirt in SuperCollider is simple and allows leveraging SuperCollider's audio engine while using a simplified coding environment for patterning music. One needs to run two programs in order to work using Tidalcycles, SUperCollider and a coding environment. I use Pulsar and VS Code as environments. Tidalcycles in conjunction with SuperCollider creates a strong choice for live coding, </p>

<p>To program in tidal cycles requires using Haskell. The subset of the Haskell that is used for Tidalcyles is small. It isn't necessary to know how to program in Haskell to be successful at making music in Tidalcycles.  Using Haskell provides the live coder with the opportunity to type fewer characters at the expense of ease of understanding. Tidalcycles is not a collaborative live coding environment.</p>

<p> <strong> Strudel </strong> 

<p> <strong> Flok </strong>

<table>
  <thead>
    <tr>
      <th>Live-Coding Environment</th>
      <th>Collaborative</th>
      <th>Easy to Setup</th>
      <th>Easy to Learn</th>
      <th>Easy to Access Reference</th>
      <th>Fully Featured</th>
    </tr>
  </thead>
  <tbody>

  <tr>
      <td><strong>SuperCollider</strong></td>
      <td>❌ No, not natively</td>
      <td>❌and✅ SuperCollider is relatively easy to install, but you won't be live coding right out of the gate</td>
      <td>❌ (Steep learning curve)</td>
      <td>⚠️ (Extensive but complex)</td>
      <td>Best</td>
  </tr>
    <tr>
      <td><strong>TidalCycles</strong></td>
      <td>❌ No</td>
      <td>❌ (Requires a good bit of work also requires SuperCollider and the SuperDirt quark)</td>
      <td>⚠️ (Moderate learning curve)</td>
      <td>⚠️  (Good documentation, but you need to set things up for yourself by adding files to your editor.)</td>
      <td>Best</td>
    </tr>
    <tr>
      <td><strong>Estuary</strong></td>
      <td>✅ Yes</td>
      <td>✅ (Web-based)</td>
      <td>✅ (Beginner-friendly)</td>
      <td>✅ (Built-in docs)</td>
      <td>Good</td>
    </tr>
    <tr>
      <td><strong>Strudel</strong></td>
      <td>❌ No </td>
      <td>✅ (Web-based)</td>
      <td>✅ (Beginner-friendly)</td>
      <td>✅ (Clear documentation)</td>
      <td>Better (especially when paired with SuperDirt)</td>
    </tr>
    <tr>
      <td><strong>Flok</strong></td>
      <td>✅ Yes</td>
      <td>✅ (Web-based)</td>
      <td>✅ (Beginner-friendly)</td>
      <td>❌ (Not in the environment) </td>
      <td>Good</td>
    </tr>
    
  </tbody>
</table>








 <li> Tempo and Rhythm in Strudel
    <ul>
    <li> - An assumption of repeating cycles </li>
    <li> - Cycles per minutes </li>
    <li> - Functions and Patterns Syntax  </li>
    <li> - Euclidean Rhythms </li> 
    </ul>
  </li>


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

<p>How can we explore this exercise using Strudel's rhythmic notation?</p>

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


<p> Again from John Fielder's blog, this time with melody. This is much gnarlier in Strudel due to the shifting meter.


<img src="http://klangnewmusic.weebly.com/uploads/1/2/3/0/12308331/1673883_orig.jpg" alt="John Fielder credit" />

</strudel-repl>

<script src="/assets/embed.js"></script>
<strudel-repl>
  <!--
setcpm (160 / 5)

let measure1 = "< [ [c5]@2 [b4]@1 [gs4 a4 fs4]@2 ] >"
let measure2 = "< [ [c5 b4 ef5]@2  [d5 c5 ef5 f5]@2 [fs5 gs5 a5 b5 c6]@2 ] >"
let measure3 = "< [ [d6 ~*5] ] >"

let melody = note(
  arrange( 
    [1, measure1], 
    [1, measure2], 
    [1, measure3],
    [1/5, "~*5"]
  )
).sound("vibraphone")
// let melody = note(cat(measure1))
//   .sound("vibraphone")
let tick = s(
  arrange(
    [ 1, "[c4*5]" ],
    [ 1, "[c4*5]" ],
    [ 1, "[c4*5]" ],
    [ 1/5, "c4*5" ] 
  )
).sound("hh")

stack(melody, tick)
-->

</strudel-repl>

<br>

<p> Euclidean Rhythms <p>
<p> This link contains not only an explanation of how it works, but also examples of common euclydian patterns  http://cgm.cs.mcgill.ca/~godfried/publications/banff.pdf </p>