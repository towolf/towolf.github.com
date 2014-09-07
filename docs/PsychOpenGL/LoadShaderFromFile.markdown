---
layout: mfile
title: LoadShaderFromFile
categories:
  - PsychOpenGL
encoding: UTF-8
---

handle = LoadShaderFromFile(filename [, shadertype] [, debug])

Loads a GLSL OpenGL shader definition from textfile 'filename' and
creates an OpenGL GLSL shader of type 'shadertype'. Returns a handle to
the new shader. If shadertype is omitted, the type of the shader is
derived from the filename extension: .vert == GL\_VERTEX\_SHADER, .frag ==
GL\_FRAGMENT\_SHADER, .geom == GL\_GEOMETRY\_SHADER, .tesscontrol =
GL\_TESS\_CONTROL\_SHADER, .tesseval = GL\_TESS\_EVALUATION\_SHADER. The
optional 'debug' flag allows to enable debugging output.

On successfull load & creation, a 'handle' to the new shader is returned.
