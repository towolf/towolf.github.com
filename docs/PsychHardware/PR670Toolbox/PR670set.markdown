---
layout: mfile
title: PR670set
categories:
  - PR670Toolbox
encoding: UTF-8
---

PR670setget - Set and get PR-670 attributes

Syntax:
configOUT = PR670setget(
configOUT = PR670config(configIN)

Description:
Sets various attributes of the PR-670.

Arguments are attribute, value pairs

Supported attributes
  'GetAperture' -- Get apperture.  Values are numeric in degrees
  'SetAperture' -- Set apperture.  Values are numeric in degrees
   Allowable values: 1 , 0.5, 0.25, 0.125