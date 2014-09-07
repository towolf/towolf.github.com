---
layout: mfile
title: EyelinkInit
categories:
  - EyelinkOneLiners
encoding: UTF-8
---

USAGE: [result dummy]=EyelinkInit([dummy=0][enableCallbacks=1])

# Initialize Eyelink system and connection. Optional arguments:

dummy: Omit, or set to 0 to attempt real initialization,
       set to 1 to enforce to use initializedummy for dummy mode.

       If regular initialization fails, it will provide option
       for dummy initilization.

enableCallbacks: Set to 0 for operation without callbacks and
                 without display of eye camera images on the Subject PC.
                 Omit or set to 1 for callback and video display operations
                 during tracker setup, drift correction with the default callback
                 dispatcher function PsychEyelinkDispatchCallback.m.
                 Provide namestring of your own dispatcher function if
                 you want to enable callbacks and video display with a
                 non-standard, customized dispatcher.

# Optional return arguments:

Returns result=1 when succesful, 0 otherwise
Returns dummy=1 when initialized in dummy mode, 0 otherwise.
