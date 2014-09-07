---
layout: mfile
title: gluUnProject4
categories:
  - wrap
encoding: UTF-8
---

gluUnProject4  Interface to OpenGL function gluUnProject4

usage:  [ objX, objY, objZ, objW, r ] = gluUnProject4( winX, winY, winZ, clipW, model, proj, view, near, far )

C function:  GLint gluUnProject4(GLdouble winX, GLdouble winY, GLdouble winZ, GLdouble clipW, const GLdouble\* model, const GLdouble\* proj, const GLint\* view, GLdouble near, GLdouble far, GLdouble\* objX, GLdouble\* objY, GLdouble\* objZ, GLdouble\* objW)