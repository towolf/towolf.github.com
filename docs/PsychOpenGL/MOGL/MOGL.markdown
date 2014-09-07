---
layout: mfile
title: MOGL
categories:
  - MOGL
encoding: UTF-8
---

CONTENTS.M  Contents of mogl toolbox

mogl is a collection of M-File wrappers and a MEX file that allow to call
all OpenGL commands from Matlab as one is used to from the C programming
language.


The initial OS/X PowerPC version of the 'OpenGL for Matlab' low level
interface wrapper mogl was developed, implemented and generously
contributed to Psychtoolbox under the GPL license by Prof. Richard F.
Murray, University of York, Canada. Porting to other operating systems
and architectures, OpenGL 2.x support, and further extensions and
maintenance has been done by Mario Kleiner.

The code has been relicensed by Richard Murray and Mario Kleiner to the
more permissive MIT license since 2011.

# Directory structure is as follows:

    core/

        \(first group:  main toolbox functions\)

        moglcore.mexmac -- main MEX interface to OpenGL functions
        oglconst.mat    -- constants used by OpenGL routines
        setupdate.sh    -- shell script to start or stop 'update' process
                           \(normally called via wrap/glmSetUpdate.m\)

        \(second group:  miscellaneous helper files\)

        edittag.m       -- edit all M-files that contain a given string
        finish.m        -- automatically run when quitting MATLAB
        mor.m           -- bitwise OR of multiple input arguments

    source/

        \(first group:  files that generate interface code\)

        autocode.m      -- MATLAB script that generates gl\_auto.c and M-file
                           interfaces to moglcore.mexmac
        autono.txt      -- list of OpenGL functions that autocode.m should not
                           generate interfaces for;  most of these appear
                           in gl\_manual.c
        gl\_auto\_init.c  -- file used in generating gl\_auto.c;  contains
                           top portion of file, i.e., \#includes, etc.
        oglconst.m      -- MATLAB script that searches through OpenGL header
                           files for \#defined constants, and writes them
                           to oglconst.mat as variables
        headers/\*.h     -- OpenGL headers to parse in addition to system
                           header files.
        private/\*.m     -- miscellaneous helper files for autocode.m

        \(second group:  files that compile to produce moglcore.mexmac\)

        gl\_auto.c       -- automatically generated interfaces to OpenGL functions
        gl\_manual.c     -- manually generated interfaces to OpenGL functions
        glm.c           -- GLM library of GLUT-like functions - not build
                           by default -- deprecated.
        moglcore.c      -- main MEX interface function
        mogltypes.h     -- useful data types
        makefile        -- makefile to compile C files into moglcore.mexmac

    wrap/\*          -- wrapper M-files that check arguments, etc., and
                       then call to moglcore.mexmac to run OpenGL functions


The following three commands will completely regenerate mogl.

\>\> autocode     % generate gl\_auto.c and wrapper M-files
\>\> \! make       % compile C code to produce MEX files
\>\> oglconst     % save constants from header files in a .mat file


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOpenGL/MOGL/Contents.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOpenGL/MOGL/Contents.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOpenGL/MOGL/Contents.m</code>
</div>
