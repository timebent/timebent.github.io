---
layout: post
title:  "MoxSonic Workshop"
subtitle: live coding
date:   2025-03-05 16:56:52 -0400
categories: live_coding
tags: live_coding
image: /assets/images/MOXsonic-LOGO.png
---

<h2>
Strudel Live Coding Environment<br> 
</h2> 

<!-- <<ol>
  <h3>Introduction to live coding.</h3>
    <ul>
      <li>A general overview of live coding and its history</li>
      <li>A brief discussion well-known options for live coding</li>
      <li>A bit of how Tidalcycles and Strudel function</li>
      <li>Strudel as a starting point for live coding</li>
    </ul>> -->

<!-- <details>
  <summary>Live coding overview</summary>

<p> </p>
<p>What is live coding? (probably a lot of things qualify)</p>

**comment out
<p>A brief history - Thor Magnussen with iXi Lang on SuperCollider, Charlie Roberts with Gibber on Browser, Tidalcycles with SuperCollider, Strudel with Browser. This workshop will focus on Strudel, which operates as a patterning sequencer for an audio engine. 
***

<p> It has been my experience, that early success provides the most inviting entryway into the creative coding of music. Certain live coding environments can reduce the overhead of learning a larger, less constrained environments. </p>

<p>In this workshop, I suggest that Strudel is a good place to start. Strudel only requires a browser to use. It uses basic Javascript to create patterned sequences, and is easy to learn. It implements a cyclic rhythmic model that provides a simple but deep way to explore rhythm.  It is a fast lane toward thinking algorithmically. For those that are coming from software sequencers, I find it particularly enticing.</p>

<p>The ceiling of the environment is high. The first step is generally providing external samples. This quickly leads to loading samples from disk. Eventually, to send messages to SuperCollider's SuperDirt for a more full featured experience. Soon after, you may find yourself learning a bit of SuperCollider syntax to augment the SuperDirt library with your own Synthesis Definitions.  Next thing you know, you are using the Pattern system in SuperCollider and Just In Time Programming techniques to live code synthesis and patterns in conjunction. </p>

<p> Historically score generation methods are generalized in computer music languages. It is appropriate to have an environment where few assumptions are made about musical paradigms. However, sometimes constraints imposed by certain musical model can be appropriate. There is a gradient here. The more constrained, the more easily the limited territory can be explored. The less constrained, the more vast the territory, and the task of exploration is more involved. For more on this discussion see:</p> <p><cite>  Roberts, Charlie, and Graham Wakefield, 'Tensions and Techniques in Live Coding Performance', in Roger T. Dean, and Alex McLean (eds), The Oxford Handbook of Algorithmic Music, Oxford Handbooks (2018; online edn, Oxford Academic, 5 Feb. 2018), https://doi.org/10.1093/oxfordhb/9780190226992.013.20, accessed 10 Mar. 2025.</cite> </p>

<p> Strudel is unabashedly pattern-based with a cyclic model of rhythm. It lends itself well to music that embraces this cyclical model, which is maybe more broad than one might think. Ambient, minimalist, techno, house, edm, idm, pop, hip hop, etc. </p>

<p> If the cyclical constraint is a bridge too far, then I would recommend live coding in SuperCollider, which take a less constrained approach with regard to musical models. The territory is considerably larger </p>

</details> 
-->

<!-- ***************************************************** -->


<details>
<summary>Well-known options for live coding </summary>

<!-- 
<p>

<p>An overview of the entire ecosystem of live coding environments is impossible here. Instead, I will focus on the set of environments that form the backbone of Strudel, branch from it, or are similar to it.  </p>

<p> <strong> Backbone: </strong> </p>

<p> <strong> SuperCollider </strong> </p>
<p> - SuperCollider now has a long and storied history as a powerful variant of the Music N languages. It was designed to run efficiently in real time. Learning the language of SuperCollider and the manner in which the language and server function is a large endeavor. SuperCollider features the Just In Time Programming Library. From the SuperCollider help files:</p>

<blockquote> Here, a program is not taken as a tool that is made first to be productive later, but instead as a dynamic construction process of description and conversation. Writing code becomes an integral part of musical or experimental practice.</blockquote> 

<p> <strong> Tidalcycles </strong> </p> 
<p> - This coding environment, created by Alex McLean, works in conjunction with SuperCollider, and specifically with a third party set of classes and a set of samples called SuperDirt. Running SuperDirt in SuperCollider is simple and allows leveraging SuperCollider's audio engine while using a simplified coding environment for patterning music. One needs to run two programs in order to work using Tidalcycles, SUperCollider and a coding environment. I use Pulsar and VS Code as environments. Tidalcycles in conjunction with SuperCollider creates a strong choice for live coding, </p>

<p>To program in tidal cycles requires using Haskell. The subset of the Haskell that is used for Tidalcyles is small. It isn't necessary to know how to program in Haskell to be successful at making music in Tidalcycles.  Using Haskell provides the live coder with the opportunity to type fewer characters at the expense of ease of understanding. Tidalcycles is not a collaborative live coding environment.</p>

<p> Of note, the theoretical framework  of Tidalcycles' polymetric structures was inspired by the Bol Processor software (https://bolprocessor.org/misc/bp2intro.htm) </p>

<p> <strong> Similar and also Collaborative </strong> </p>

<p> <strong> Estuary </strong> </p>
<p> - Collaborative browser based coding. Long distance coding worked quite well with Estuary. We used Estuary to create a performance between Les P (special thanks to Pablo Tobar) in Colombia and the electronic ensemble at Georgia Southern in the fall of 2022. 36 minutes in 
https://www.youtube.com/watch?v=sMfLMXDw_eM </p>

<p> Estuary can run several different live coding languages, including those meant for visual performance. Estuary's excellent collaborative capabilities are due in part to it being entirely web based. Estuary uses the web audio engine "WebDirt" to play back samples, which must be available online so that every participant can hear them. So, adding samples means adding to a common repository. This process involves forking the repository on github and using git to manage the addition and removal of samples. The process is not intuitive. </p>

<p> For live coding audio, Estuary uses a subset of tidal called mini-tidal. This subset is not fully featured. The Estuary interface contains a way to reference files for different functions with code examples. Additionally, samples are available for use are listed in a separate tab.</p> 

<p> <strong> Flok </strong> </p>
<p> </p>

<p> <strong> Gibber / Gabber </strong></p>

<p> - Gibber, maintained by Charlie Roberts, runs in the browser and uses javascript. Gibber folds in the minitidal subset of tidal cycles in addition to having its own patterning tools which are apart from tidal's musical model.  The syntaxis moderately more involved that using Strudel, but it is a viable option with some excellent pattern visualization features and a well thought out model.</p> 

<p> Here is an example of the moderately more involved syntax: </p>
<p> In Gibber: </p>
<code> s = Synth() </code>
<p> <code> s.note(0) </code> </p>

<p> In Strudel: </p>
<code> s("sine").note(0) </code>

<p> OR even more similar </p>
<p> In Gibber: </p>
<code>  d = Drums() </code>
<p> <code> d.tidal('kd sd kd sd') </code> </p>

<p> In Strudel: </p>
<code> sound("kd sd kd sd") </code>

<p> </p>
<p> <strong> Strudel </strong> </p>

<p> Strudel is developed by Felix Roos.  </p>

--> 
<p> Here is a chart which compares some basic elements </p>

<table>
  <thead>
    <tr>
      <th>Live-Coding Environment</th>
      <th>Collaborative</th>
      <th>Easy to Setup</th>
      <th>Easy to Learn</th>
      <th>Easy to Access Reference</th>
      <th>Visual Feedback Highlighting Code</th>
      <th>Fully Featured</th>
    </tr>
  </thead>
  <tbody>

  <tr>
      <td><strong>SuperCollider</strong></td>
      <td>⚠️ Not natively. </td>
      <td>❌and✅ SuperCollider is relatively easy to install, but you won't be live coding right out of the gate</td>
      <td>❌ (Steep learning curve, SuperCollider specific language and not singularly focused on live coding)</td>
      <td>⚠️ (Extensive but complex)</td>
      <td>❌ No visual feedback unless you code it yourself</td>
      <td>Best</td>
  </tr>
    <tr>
      <td><strong>TidalCycles</strong></td>
      <td>❌ No</td>
      <td>❌ (Requires a good bit of work also requires SuperCollider and the SuperDirt quark)</td>
      <td>⚠️ (Moderate learning curve, Uses the Haskell language, which can be difficult)</td>
      <td>⚠️  (Good documentation, but you need to set things up for yourself by adding files to your editor.)</td>
      <td>❌ No visual feedback as far as I know</td>
      <td>Best</td>
    </tr>
    <tr>
      <td><strong>Estuary</strong></td>
      <td>✅ Yes</td>
      <td>✅ (Web-based)</td>
      <td>✅ (Beginner-friendly, allows miniTidal which is a reduced subset of tidal)</td>
      <td>✅ (Built-in docs)</td>
      <td>❌ No visual feedback</td>
      <td>Good</td>
    </tr>

      <tr>
      <td><strong>Gibber</strong></td>
      <td>✅ Yes (with gabber) </td>
      <td>✅ (Web-based)</td>
      <td>✅ (Beginner-friendly. Uses javascript. Not as streamlined as Strudel)</td>
      <td>✅ (Clear documentation)</td>
      <td>✅ Visual feedback with highlighting of code and more!</td>
      <td>✅ Good+. The library of possibilities is not quite a full as other programs. </td>
    </tr>

    <tr>
      <td><strong>Strudel</strong></td>
      <td>❌ No </td>
      <td>✅ (Web-based)</td>
      <td>✅ (Beginner-friendly. Uses javascript as an alternative to Haskell. Really simple)</td>
      <td>✅ (Clear documentation)</td>
      <td>✅ Visual feedback with highlighting of code and more!</td>
      <td>Better (especially when paired with SuperDirt)</td>
    </tr>
    <tr>
      <td><strong>Flok</strong></td>
      <td>✅ Yes</td>
      <td>✅ (Web-based)</td>
      <td>✅ (Beginner-friendly. Can use Strudel within this collaborative environment)</td>
      <td>❌ (You have to know what you are doing. You won't get help from the interface) </td>
      <td>✅ Visual feedback with highlighting of code</td>
      <td>Good</td>
    </tr>
    
  </tbody>
</table>

</details>

<!-- Beginning Rhythm-->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->


<!-- <li> Tempo and Rhythm in Strudel
    <ul>
    <li> - Thinking in cycles </li>
    <li> - Functions and Patterns Syntax  </li>
    <li> - Euclidean Rhythms </li> 
    </ul>
  </li> 
-->

<details>
<summary> Tempo and Rhythm in Strudel - Thinking in Cycles (Basic) </summary>
<p>

<img src="https://strudel.cc/img/drumset.png" alt="Drumset Image" />
-- Image from strudel.cc

<p> To begin, we need to provide two things: a function and a pattern. Below a function named "sound" is used. The function requires a pattern.  Patterns are expressed in quotation marks or backticks (useful for writing patterns across multiple lines). </p>

 <script src="https://unpkg.com/@strudel/repl@latest"></script>
<strudel-editor>
  <!--
setcpm (140 / 4)
sound("bd")
-->
</strudel-editor>

<p> This indicates that the sound called bd should be called once a cycle, at the beginning of the cycle. Let's add another item to the pattern. </p>

<strudel-editor>
  <!--
setcpm (140 / 4)
sound("bd sd")
-->
</strudel-editor>


<p>Now the cycle is split in two and the elements of the pattern bd and sd are played at those divisions. Let's experiment a bit with making rhythms with only this much information. </p>

<p> CLick the Strudel REPL Spiral below. Try chaining the "bank" function to end of sound .bank("RolandTR808"). See the side panel under sounds and then drum-machines.  </p>

<script src="/assets/embed.js"></script>
<strudel-repl>

 <!--
setcpm (140 / 4)
sound("bd sd")
-->
</strudel-repl>
 
<p> We eventually find that we need to group elements together to create subdivisions of the cycle. Also, we see the syntax for a rest (either - or ~)</p>

<table>
  <thead>
    <tr>
      <th>Notation</th>
      <th>Function</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>[ ]</code></td>
      <td>Divides the cycle or subdivisions when nested 
<strudel-editor>

 <!--
setcpm (140 / 4)
sound("[ bd sd hh ] [hh hh]") 
// The two enclosures [] and [] divide the cycle into 2. The elements within the enclosures then further divide that part of the cycles into 3 parts and 2 parts respectively. Compare: 
// sound("[ bd sd hh ] [hh hh]") 
// and 
// sound("bd sd hh hh hh")
// In the second of these, the cycle is divided evenly into 5 parts. 
-->
</strudel-editor>

</td>
    </tr>
    <tr>
      <td><code>.</code></td>
      <td>Divides the cycle but cannot be nested 
<strudel-editor>

 <!--
setcpm (140 / 4)
// These are akin to the [ ] notation, but these cannot be nested.
sound("bd sd . hh . hh . hh")
// The . notation can be used in conjunction with the [] notation.
// sound("[bd . sd [sd sd]] . [bd]")   
-->
</strudel-editor>
      </td>
    </tr>
  </tbody>
</table>

<p> Let's take some time to try our hand at a few rhythmic exercises. </p>

<p> <img src="/assets/images/Simple.png" alt="Exercise 1" /> </p>

<details> 
<summary> Answer </summary> 

<strudel-editor>
  <!--
setcpm(60/4) 

$1: s("~ cp ~ cp ~ ~ ~ ~") 
$2: s("hh hh hh hh hh hh hh hh")
-->
</strudel-editor>
</details>

<p> </p>


<p><img src="/assets/images/TwelveEightExercise.png" alt="Exercise 2" /> </p>

<details> 
<summary> Answer </summary> 
<strudel-editor>
  <!--
setcpm(60/4) 

$1: s(` [ [cp cp cp] [cp cp cp] [cp] [cp] ] `) 
$2: s("[hh hh hh hh hh hh hh hh hh hh hh hh]")
-->
</strudel-editor>

</details>
<p> </p>
</p>
</details>


<!-- Intermediate Rhythm-->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->

<details>
<summary> Tempo and Rhythm in Strudel - Thinking in Cycles (Intermediate) </summary>
<p>

<table>
  <thead>
    <tr>
      <th>Notation</th>
      <th>Function</th>
    </tr>
  </thead>
  <tbody>
    

  <tr>
      <td><code>!</code></td>
      <td>Replicate a pattern or part of a pattern
<strudel-editor>

<!--
setcpm (140 / 4)
sound("bd!4")
-->
</strudel-editor>
</td>
    </tr>

  <tr>
      <td><code>@</code></td>
      <td>Elongates a pattern or part of a pattern
<strudel-editor>

 <!--
setcpm (140 / 4)

sound("bd sd@2 hh")
// sound("[bd bd bd]@2 [bd]@2])
-->
</strudel-editor>

</td>
    </tr>
    <tr>
      <td><code>&lt; &gt;</code></td>
      <td>Alternates cycles

<strudel-editor>
 <!--
setcpm (140 / 4)
sound("<bd sd>")
// These can be nested. See how the nested element is addressed every other cycle:
// sound("< bd < [sd sd] [sd sd sd] > >")  
-->
</strudel-editor>
      </td>
    </tr>
    <tr>
      <td><code>{ }</code></td>
      <td>Indicates polymeter

<strudel-editor>

 <!--
setcpm (140 / 4)
// Polymeter is where two patterns with different bar lengths play at the same tempo 
// Polymeter 
sound(" { bd sd", "hh hh hh } ") 
// Polyrhythm
// sound("bd sd", "hh hh hh")
-->
</strudel-editor>
      </td>
    </tr>
  </tbody>
</table>


<p> <img src="/assets/images/TripletSimple.png" alt="Exercise 3" /> </p>

<details> 
<summary> Answer </summary> 
<strudel-editor>
  <!--
setcpm(60/4) 
$1: s(`
      [ [cp] [~ cp cp] [cp@2 cp] [cp] ]  
  `) 
$2: s("[hh!4]")
-->
</strudel-editor>

</details>
<p> </p>

<p> <img src="/assets/images/SixteenthNoteRhythmExercise2.png" alt="Exercise 4" /> </p>

<details> 
<summary> Answer </summary>
<strudel-editor>
  <!--
setcpm(60/4) 

$1: s(`<
      [ [lt lt@2 lt] [lt lt@2 lt] [~ lt] [lt] ] 
      [ [lt lt@2 lt] [~ lt@2 lt] [~ lt] [lt] ]
  >`) 

$2: s("<[hh!4] [hh!4]>")
-->
</strudel-editor>
</details>

<p> </p>
<p><img src="/assets/images/SixteenthNoteRhythmExercise.png" alt="Exercise 3" /> </p>

<details> 
<summary> Answer </summary> 
<strudel-editor>
  <!--
setcpm(60/4) 

$1: s(`<
      [ [~!3 lt] [[lt lt] lt] [~ lt] [[lt lt] lt] ]  
      [ lt lt lt lt@2 lt lt@2 lt@8 ]
  >`) 

$2: s("<[hh!4] [hh!4]>")
-->
</strudel-editor>

</details>


</p>
</details>


<!-- Advanced Rhythm-->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->

<details>
<summary> Tempo and Rhythm in Strudel - Thinking in Cycles (Advanced) </summary>
<p>

<table>
  <thead>
    <tr>
      <th>Notation</th>
      <th>Function</th>
    </tr>
  </thead>
  <tbody>
<tr>
  <td><code>*</code></td>
    <td>Speed up a pattern or part of a pattern
  <strudel-editor>

 <!--
setcpm (140 / 4)
sound("[ bd sd bd sd]*8 [bd*4 sd bd sd]")
-->
  </strudel-editor>
  </td>
</tr>

<tr>
  <td><code>/</code></td>
    <td>Slow down a pattern or part of a pattern
  <strudel-editor>
 <!--
setcpm (140 / 4)
sound("[ bd]/2 [sd]/3") // here the pattern is extended to 2X the cycle length
-->
  </strudel-editor>
  </td>
</tr>
</tbody>
</table>

<p> <strong> Euclidian Rhythms </strong> </p>
<p> This link contains not only an explanation of how it works, but also examples of common euclydian patterns  http://cgm.cs.mcgill.ca/~godfried/publications/banff.pdf </p>
<p> To put it briefly, the Euclidean rhythms take number of events to distribute across a number of pulses. Additionally, an offset parameter to say where in the pattern to begin doing this.</p>

<p> 3 events across 8 pulses with an offset of 0 would result in the following: </p>
<p> X - - X - - X - </p>

<p> With an offset of 1, the pattern would look like this: </p>
<p> - X - - X - - X </p>

  <strudel-editor>
  <!--
// "Common West African bell v240624" @by Prince Lucija
setcpm(134/4)
stack(
  s("cb:0(<4!7 <3 6>>, 12)").speed(0.5).decay(0.2)._spiral() , 
  // different steps, 12 pulses. 
  // The first 7 cycles it is 4 divs of 12
  // * - - * - - * - - * - -
  // The 8th cycle it is 3 divs of 12
  // * - - - * - - - * - - -
  // Then 7 more cycles of 4 dives of 12
  // * - - * - - * - - * - -
  // Then the 16th cycle is 6 divs of 12
  // * - * - * - * - * - * - 
    s("cb:0(<2!3 3>,12,3)").speed(1.8),
  // The first 3 cycles it is 2 divisions of 12 (offset by 3)
  // offset by 3 means starting on the 3rd of the 12 beats
  // - - * - - - - * - - - -
  // The 4th cycle it is 3 divisions of 12 (offset by 3)
  // - - * - - - * - - - * - // fourth cycle
   s("cb:3(2,3,1)*4").speed(3.0),
  // The cycles are all the same. 2 divisions of 3 offset by 1
  // The *4 means there are 4 repeats of this to form 12 beats
  //  smae as s("[- cb:3 cb:3]*4")
  // - * * - * * - * * - * *
  s("rim(1,3,2)*4"),
  // The cycles are all the same. 1 divisions of 3 offset by 2
  // The *4 means there are 4 repeats of this to form 12 beats
  // same as s("[- - rim]*4")
  // s("cb:2(7,12,3)"),  // standard african bell pattern
  // s("cb:0(3,12, 3)").speed(0.7)
)
  .bank("RolandTR707")
-->
  </strudel-editor>

<p> <strong> Nested Tuplets </strong> </p>
The following notation is taken from John Fielder's blog post on nested tuplets.
(http://klangnewmusic.weebly.com/direct-sound/lets-talk-rhythm-part-2-nested-tuplets) </p>

<img src="http://klangnewmusic.weebly.com/uploads/1/2/3/0/12308331/1727048_orig.jpg" alt="John Fielder credit" />
<p> </p>

  <strudel-editor>
  <!--
// How can we explore this exercise using Strudel's rhythmic notation?
setcpm (40/4)
let hh = sound("[hh hh] [hh hh] [hh*5]@2 [hh hh] [hh hh]")
let bd = sound("bd . bd . bd . bd . bd . bd")
// let hh = sound("[hh hh] [hh hh] [[hh*3]@2 hh hh hh]@2 [hh hh] [hh hh]")
// let hh = sound("[hh hh] [hh hh] [[hh*3]@2 [hh*5]@2 hh]@2 [hh hh] [hh hh]")
stack(hh, bd)
-->
</strudel-editor>

</details>

<!-- Patterning Notes and Chords -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->
<!-- ***************************************************** -->


<details>
<summary> Patterning notes and chords</summary>

<table>
  <thead>
    <tr>
      <th>Notation</th>
      <th>Function</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>note</code></td>
      <td> Play a note by name or MIDI note number
<strudel-editor>

  <!--
setcpm (80 / 4)
$chromatic: note("c4 df4 d4 ef4 e4 f4 gf4 g4 af4 a4 bf4 b4 c5")
  .sound("sawtooth")
  .lpf(saw.range(3000, 400))
  .lpq(14)

$chromatic2: note("c4 cs4 d4 ds4 e4 f4 fs4 g4 gs4 a4 as4 b4 c5")
  .sound("vibraphone")
  .dec(0.3)

$chromatic3: note("60 61 62 63 64 65 66 67 68 69 70 71 72").sound("piano")
// or $chromatic3: note("60 .. 72")
$chromatic4: note("72 71 70 69 68 67 66 65 64 63 62 61 60").sound("piano")
 
all(fast("<2 3 5 7>"))
-->
</strudel-editor>
</td>
</tr>


<tr>
      <td><code> , </code></td>
      <td>Stack patterns together 
<strudel-editor>

  <!--
setcpm (80 / 4)
note( "[60.5, 60, 64, 67.25, 67, 71]" )
  .adsr("0.1:0.1:0.8:0.9")
  .legato(0.1)
  .sound("gm_accordion")
  .vib(7)
  .vibmod(0.3)
-->
</strudel-editor>
</td>
</tr>
</tbody>
</table>
   

<p> Try to create a pattern that represents this measure of Chopin's Prelude Op. 28, No. 7. </p>

<img src="/assets/images/chopin.png" alt="Chopin" />
<details>
<summary> Answer </summary>
<strudel-editor>
<!--
setcpm(60/3)

$treble: note(`
  [ [cs5@3 d5] [b4, g4, d4] [b4, g4, d4] ]@3
  [ [b4, g4, d4]@2 [fs5, d5] ]@3
  `).s("square").adsr("0.1:0.2:0.4:0.3")

$bass: note(`
[ e2 [e3, e2] [e3, e2] ]@3
[ [e3, e2]@2 ~]@3
`).sound("piano")
-->
</strudel-editor>
</details>

<p> Again from John Fielder's blog, this time with melody. This is much gnarlier in Strudel due to the shifting meter. </p>

 <div class="crop">
      
<img src="http://klangnewmusic.weebly.com/uploads/1/2/3/0/12308331/1673883_orig.jpg" alt="John Fielder credit" />
</div>
<p> </p>

<strudel-repl>
  <!--
setcpm (110 / 5)

let measure1 = "[ [c5]@2 [b4]@1 [gs4 a4 fs4]@2 ]@5"
let measure2 = "[ [c5 b4 ef5]@2  [d5 c5 ef5 f5]@2 [fs5 gs5 a5 b5 c6]@2 ]@5"
let measure3 = "[ [d6 ~*5] ]@6"

let melody = note(stepcat(measure1, measure2, measure3))
  .pace(8)
  .sound("vibraphone")
  .gain(0.3)

let tick = sound("hh!5 hh!5 hh!6")
  .pace(8)

stack(melody, tick)
-->

</strudel-repl>

</details>

<details>
<summary> Working with longer samples </summary>

<table>
  <thead>
    <tr>
      <th>Notation</th>
      <th>Function</th>
    </tr>
  </thead>
  <tbody>
<tr>
  <td><code> fit </code></td>
    <td> fit a sample into a single cycle
<strudel-editor>
 <!--
samples('https://raw.githubusercontent.com/tidalcycles/Dirt-Samples/master/strudel.json')
s("breaks125").fit()
-->
</strudel-editor>
  
  </td>
</tr>

<tr>
  <td><code>/</code></td>
    <td>Slow down a pattern or part of a pattern
  <strudel-editor>
 <!--
setcpm (140 / 4)
sound("[ bd]/2 [sd]/3") // here the pattern is extended to 2X the cycle length
-->
  </strudel-editor>
  </td>
</tr>
</tbody>
</table>


<strudel-editor>
<!--
setcpm(125/5)
samples('github:tidalcycles/dirt-samples')
$1: s("breaks125")
-->
</strudel-editor>

<p> This break beat, which is indicated to be at a tempo of 125 is in 4/4.
The above cpm adds an extra beat to the cycle. We can make the break beat slow down to meet this tempo </p>

<strudel-editor>
<!--
setcpm(125/5)
samples('github:tidalcycles/dirt-samples')
s("breaks125").fit()
-->
</strudel-editor>

<p> We can make the break beat slow down to fit within x number of cycles </p>
<strudel-editor>
<!--
setcpm(125/5)
samples('github:tidalcycles/dirt-samples')
$1: s("breaks125").loopAt(2)
-->
</strudel-editor>

<p> Let's slice the break into eight parts and play them back in order. This allows us to fit the breakbeat into the cycle without pitch shifting </p>

<strudel-editor>
<!--
setcpm(125/5)
samples('github:tidalcycles/dirt-samples')
s("breaks125").chop(32)
-->
</strudel-editor>

<p> Let's change the order in which the slices are played back </p>

<strudel-editor>
<!--
setcpm(125/5)
samples('github:tidalcycles/dirt-samples')
$1: s("breaks125").slice(8, "7 .. 0")
-->
</strudel-editor>

<p> We can also use the splice function. This changes the playback speed of each slice according to its duration </p>

<strudel-editor>
<!--
setcpm(125/5)
samples('github:tidalcycles/dirt-samples')
$1: s("breaks125").splice(8, "[ [0 1 2@2 ] [ 3 4 5 6 [7 7 7] ] ]")
-->
</strudel-editor>

<p> The striate function allows us to lace together patterns. It cuts samples into x number of parts and then plays back portions in sequence. </p>

<strudel-editor>
<!--
setcpm(125/5)
samples('github:tidalcycles/dirt-samples')
s("breaks125:0 breaks125:1 breaks125:2")
  .striate(4)
  .slow(1)
  .cut(1)
  .begin("<0.0 0.01>")
  .end(0.5)
  .every(4, x=>x.lpf(saw.range(100, 3000).slow(1)))
-->
</strudel-editor>

<p> Here we use the loop function in conjunction with loopBegin and loopEnd  </p>

<strudel-editor>
<!--
setcpm(125/5)
samples('github:tidalcycles/dirt-samples')
s("breaks125").fit().loopBegin("0")
  .loopEnd("<0.5@2 0.75>")
  .loop(1)
  .cut(1)
  .struct("<x x x>")
-->
</strudel-editor>

</details>


<!-- <p> In computer music, Music-N languages gravitated toward a separate orchestra and score. The synthesis engine was separate from score-level event generation. Early analog electronic instruments make the distinction as well, providing sequenced control voltages to control parameters of audio rate modules, such as an oscillator. This paradigm was challenged by SuperCollider, a child of the Music-N lineage, by making no distinction between composition on the sample level and composition on longer time scales. </p> -->


