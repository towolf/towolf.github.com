---
layout: mfile
title: gluProject
categories:
  - wrap
encoding: UTF-8
---

gluProject  Interface to OpenGL function gluProject

usage:  [ winX, winY, winZ, r ] = gluProject( objX, objY, objZ, model, proj, view )

C function:  GLint gluProject(GLdouble objX, GLdouble objY, GLdouble objZ, const GLdouble\* model, const GLdouble\* proj, const GLint\* view, GLdouble\* winX, GLdouble\* winY, GLdouble\* winZ)