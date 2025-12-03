---
layout: post
title:  "Strudel: Web Audio to OSC Guide"
subtitle: live coding
date:   2025-10-22 16:56:52 -0400
categories: live_coding
tags: live_coding
image: /assets/images/algorave.png
---

<h2>
Transitioning to SuperCollider from Web Audio in Strudel<br> 
</h2> 

<p>
Moving from Web Audio to SuperCollider in Strudel can be a bit tricky. There are some already known steps that will get things to mostly work. This is located:
https://strudel.cc/learn/input-output/

Where in the OSC section it states:
"To get SuperDirt to work with Strudel, you need to

    install SuperCollider + sc3 plugins, see Tidal Docs (Install Tidal) for more info.
    install SuperDirt, or the StrudelDirt fork which is optimised for use with Strudel
    install node.js
    download Strudel Repo (or git clone, if you have git installed)
    run pnpm i in the strudel directory
    run pnpm run osc to start the osc server, which forwards OSC messages from Strudel REPL to SuperCollider

Now you’re all set!"

Not quite. When choosing to transition from Web Audio to SuperCollider in Strudel, there are many things that will not work out of the box. Chiefly, we are missing some samples and ways to remap those samples to pitches. 

The following github page shows this:

https://github.com/felixroos/dough-samples/tree/main

The samples of note here are:
piano
VCSL
mrid
tidal-drum-machines

Simply downloading these samples will not be enough. I hope to provide a series of steps to get this working in SuperCollider as it does in web audio. We are also missing the ability to play sound fonts, which are the things like gm_alto_sax (listed under "synths" in Strudel).

