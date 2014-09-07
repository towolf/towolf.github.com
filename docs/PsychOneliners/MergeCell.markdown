---
layout: mfile
title: MergeCell
categories:
  - PsychOneliners
encoding: UTF-8
---

Merges contents of multiple cell arrays into one big cell array

c = MergeCell(varargin)

MergeCell takes any number of cell vectors (contain the same datatype)
and concatenates their contents into one big cellvector
Any signleton inputs are expanded as needed, these inputs can be 1x1
cells or the contained datatype itself

Example: To add some information about fit to plot legend, we'd wan't to
append information about the fit to the line labels:

linelbls = {'line a','line b','line c'};
chi2\_r   = [.9 1 4.2];
chi2\_rtxt= arrayfun(@(x) sprintf('slope: %.3f',x),chi2\_r,'UniformOutput',false);

leglbls  = MergeCell(linelbls,', chi^2\_r: ',chi2\_rtxt);
% leglbls  = MergeCell(linelbls,{', chi^2\_r: '},chi2\_rtxt); would be equivalent
