---
layout: mfile
title: AlphaBlendSettingTest
categories:
  - PsychTests
encoding: UTF-8
---

failFlag=AlphaBlendSettingTest([screenNumber])

Test that [Screen](/docs/Screen)('BlendFunction') recalls the same alpha blending values
as previoulsy set.

If no return argument is provided, then TestAlphaBlendSetting issues an error
when a test fails.  If a return argument is supplied then it signals a
failed test only by returning true, without issuing an error.

See also: AlphaBlendingTest, PsychAlphaBlending