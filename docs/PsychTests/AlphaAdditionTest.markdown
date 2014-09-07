---
layout: mfile
title: AlphaAdditionTest
categories:
  - PsychTests
encoding: UTF-8
---

failFlag=AlphaAdditionTest([screenNumber])

Combine two alpha layers by addition and verify the result.

If no return argument is provided, then TestAlphaAddition issues an error
when a test fails.  If a return argument is supplied then it signals a
failed test only by returning true, without issuing an error.

See also: AlphaBlendingTest, PsychAlphaBlending