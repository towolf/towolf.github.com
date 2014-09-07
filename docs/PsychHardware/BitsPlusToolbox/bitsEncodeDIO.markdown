---
layout: mfile
title: bitsEncodeDIO
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

 encodedDIOdata = bitsEncodeDIO(Mask, Data, Command, windowPtr, [setGammaTable])
   Use it when you want to write DIO synchronised with screen frame.
   It will sync timer interrupt with each frame.

   'Mask' is DIO mask that must be an integer.

    'Data' is a 248 element array of integers.

    'Command' is the command code.

    'windowPtr' is the window pointer returned by [Screen](/docs/Screen)('OpenWindow').

    'setGammaTable' is an optional value that tells the function to set the
    video card gamma table to a linear function if set to 1.  If set to 0,
    the gamma table will be assumed to be linear.  By default, this is set
    to 1.