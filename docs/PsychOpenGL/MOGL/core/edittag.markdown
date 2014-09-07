---
layout: mfile
title: edittag
categories:
  - core
encoding: UTF-8
---

EDITTAG  Edit all files that contain a text tag and that match
         a filename filter

edittag( tag, filter )

e.g., edittag('---protected---','wrap/\*.m')

- 'tag' defaults to '---protected---'
- 'filter' defaults to 'WRAPDIR/\*.m', where WRAPDIR is the folder that
  holds the M-file wrappers