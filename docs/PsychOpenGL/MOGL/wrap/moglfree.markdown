---
layout: mfile
title: moglfree
categories:
  - wrap
encoding: UTF-8
---

moglfree(ptr) -- Free a memory buffer inside mogl which was previously
created via a call to ptr = moglmalloc(...) or ptr = moglcalloc(...).
ptr = A pointer to the buffer to free. This is the handle returned by
moglmalloc() or moglcalloc().

After successfull release, ptr will be invalid, \*do not use it anymore\*
or Matlab/Octave will possibly crash or do other nasty things!

moglcalloc()'ed or moglmalloc()'ed memory buffers can be released as well
all at once via moglfreeall, and they are automatically released when
moglcore is clear'ed via clear moglcore, clear mex or clear all.
