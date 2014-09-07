---
layout: mfile
title: RetIrradianceToIsoRecSec
categories:
  - PsychColorimetric
encoding: UTF-8
---

 [isoPerConeSec,absPerConeSec,photoreceptors] = ...
        RetIrradianceToIsoRecSec(irradianceWatts,irradianceS,[photoreceptors])

 Convert retinal irradiance, measured in watts/um^2-wlinterval to
 isomerizations per cone per second.

 The passed photoreceptors structure defines the transmissive media through
 which the light must pass and the properties of the photoreceptors.  It
 is not modified by this routine, but the routine can return default
 values.

 Default values return estimates for human L, M, and S foveal cones.

 In many cases, data can either be specified by numerical value or by
 source string.  When both are passed, values override strings.

 The routine also returns the absorption rate and a filled in version
 of the photoreceptors structure.

 See also: DefaultPhotoreceptors, FillInPhotoreceptors, IsomerizationsInEyeDemo
   IsomerizationsInDishDemo.

 7/25/03  dhb  Wrote it by pulling in code from elsewhere.