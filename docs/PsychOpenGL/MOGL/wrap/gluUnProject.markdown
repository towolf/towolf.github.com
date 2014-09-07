---
layout: mfile
title: gluUnProject
categories:
  - wrap
encoding: UTF-8
---

gluUnProject  Interface to OpenGL function gluUnProject

usage:  [ objX, objY, objZ, r ] = gluUnProject( winX, winY, winZ, model, proj, view )

C function:  GLint gluUnProject(GLdouble winX, GLdouble winY, GLdouble winZ, const GLdouble\* model, const GLdouble\* proj, const GLint\* view, GLdouble\* objX, GLdouble\* objY, GLdouble\* objZ)