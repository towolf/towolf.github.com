---
layout: mfile
title: SortCell
categories:
  - PsychOneliners
encoding: UTF-8
---

 SortCell    Sort a cell array in ascending order.  

 Description: SortCell sorts the input cell array according to the  
   dimensions (columns) specified by the user.  

 Usage: Y = SortCell(X, DIM)  

 Input:  
       X: the cell array to be sorted.  
  DIM: (optional) one or more column numbers. Simply an array of one or  
       more column numbers.  The first number is the primary column on  
       which to sort. Extra column numbers may be supplied if secondary  
       sorting is required. The defuault value is 1, if no dimension  
       array is supplied.  

 Output:  
     Y: the sorted cell array.  

 Example:    Y = SortCell(X, [3 2])  

 Note that this function has only been tested on mixed cell arrays  
 containing character strings and numeric values.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/SortCell.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/SortCell.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/SortCell.m</code>
</div>
