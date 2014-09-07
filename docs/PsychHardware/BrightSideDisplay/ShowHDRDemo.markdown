---
layout: mfile
title: ShowHDRDemo
categories:
  - BrightSideDisplay
encoding: UTF-8
---

ShowHDRDemo([imfilename][, dummymode][, sf]) -- Load and show a high dynamic range image
on the BrightSide Technologies High Dynamic Range display device.

'imfilename' - Filename of the HDR image to load. Will load our standard
low-dynamic range 'konijntjes' if 'imfilename' is omitted.

'dummymode' - If set to 1 we only run in emulation mode without use of
the HDR device or BrightSide core library.

'sf' - Scaling factor to apply.
