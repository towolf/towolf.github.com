---
layout: mfile
title: PhotopigmentSpecificDensity
categories:
  - PsychColorimetricData
encoding: UTF-8
---

 densities = PhotopigmentSpecificDensity(receptorTypes,[species],[source])

 Return estimates of photopigment specific densities.

 Allowable receptor types depend on species and source, but the general
 list is:
    SCone, MCone, LCone, FovealSCone, FovealMCone, FovealLCone, Rod.

 The type argument may be a single string or a cell array of strings.  If it
 is an array, a column vector of values is returned.

 The foveal version of cone types is sensible only for primates.  Not all
 estimate sources support all receptor types.

 Note that the following three numbers are overdetermined: photopigment
 specific density (sd), photopigment axial density (ad), and outer segment
 length osl.  In particular, ad = sd\*osl.  Depending on the measurement
 method, different sources provide different pairs of these numbers.
 We have attempted to enforce this consistency in the set of routines
 PhotopigmentSpecificDensity, PhotopigmentAxialDensity, and PhotoreceptorDimensions.
 That is to say, for the same source, species, and cone type, you should get
 a consistent triplet of numbers.

 Supported species:
        Human (Default), GuineaPig.

 Supported sources:
    Rodieck (Human) (Default).
   Bowmaker (GuineaPig).
   Generic
   None (returns empty matrix as value)

 The Generic source returns a single number for all species and receptor types.
 This number is 0.015 /um.

 7/11/03  dhb  Wrote it.
 8/9/13   dhb  Comment clean up, allow 'None' to return empty as the value.