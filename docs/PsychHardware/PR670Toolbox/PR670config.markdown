---
layout: mfile
title: PR670config
categories:
  - PR670Toolbox
encoding: UTF-8
---

PR670config - Update the PR-670 configuration.

Syntax:
configOUT = PR670config
configOUT = PR670config(configIN)

Description:
Updates the PR-670 configuration according to 'configIN'. If no input is
provided, returns the current configuration string. 'configIN' can be in
the form of the string returned from PR670config, or a cell containing values
ordered { Units, Exposure, N Samples, CIE Observer, Sync Mode, Frequency }.