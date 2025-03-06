---
layout: post
title:  "MoxSonic Workshop"
subtitle: live coding
date:   2025-03-06 16:56:52 -0400
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

 <div id="strudel-repl"></div>
<script type="module">
  import { StrudelREPL } from "https://strudel.tidalcycles.org/repl.js";
  window.addEventListener("DOMContentLoaded", () => {
    const repl = new StrudelREPL();
    document.getElementById("strudel-repl").appendChild(repl.container);
  });
</script>




<br>