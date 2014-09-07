---
layout: mfile
title: AlphaMultiplicationTest
categories:
  - PsychTests
encoding: UTF-8
---

passedFlag=AlphaMultipicationTest([screenNumber])

# TestAlphaMultiplication:

    Test for perfect alpha multiplication precision for alpha values 0 and
    1\. OpenGL guarantees precise alpha muliplicaion for only those alpha
    values. TestTestAlphaMultipicationAlphaTimes tests that guarantee.

    Test all alpha modes in all combinations.  This verifies that [Screen](/docs/Screen) sets
    modes properly

Note that [Screen](/docs/Screen) alpha values fall in the range 0-255 while OpenGL alpha
values are normalized between 0-1; OpenGL alpha value 1 is equivalent to
[Screen](/docs/Screen) alpha value 255.

If no return argument is provided, then TestAlphaMultipication issues an error
when a test fails.  If a return argument is supplied then it signals a
failed test only by returning true, without issuing an error.

See also: AlphaBlendingTest, PsychAlphaBlending