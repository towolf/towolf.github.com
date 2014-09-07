---
layout: mfile
title: PR670write
categories:
  - PR670Toolbox
encoding: UTF-8
---

PR670write - Write a string of characters to the PR-670.

Syntax:
PR670write(cmdStr)
PR670write(cmdStr, appendCR)

Description:
Writes a string of characters to the PR-670.  By default, it appends a
carriage return (CR) to the end of the string.  Note that if the CR is
already there, it won't be appended. The CR can be disabled as
some commands do not need it.  See the PR-670 documentation for which
command need the CR.

Input:
cmdStr (1xN char) - String of characters to send.
appendCR (scalar) - 1 to append a CR, 0 to not append.  Default: 1