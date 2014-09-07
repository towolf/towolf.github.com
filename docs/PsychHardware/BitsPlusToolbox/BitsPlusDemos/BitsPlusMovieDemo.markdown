---
layout: mfile
title: BitsPlusMovieDemo
categories:
  - BitsPlusDemos
encoding: UTF-8
---

BitsPlusMovieDemo

BitsPlusMovieDemo displays a counterphase flickering grating, by lookup
table animation, using the Bits++ box.

Note that you need to precompute the cluts and write them into
offscreen memory in advance, so that the blits happen fast.  In
this example, each clut goes into its own offscreen window.  In
real applications, we have found that the precomputation is considerably
faster if we allocate one large offscreen window and put each clut
into a different rect inside of it.