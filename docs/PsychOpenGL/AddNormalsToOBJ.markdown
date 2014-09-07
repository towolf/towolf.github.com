---
layout: mfile
title: AddNormalsToOBJ
categories:
  - PsychOpenGL
encoding: UTF-8
---

obj = AddNormalsToOBJ(obj [, flipDir=0]);
Adds surface normal vectors to the vertices of the given input 'obj' 3D
object representation, returns the new 'obj' with added vertex normal
vectors. If the input 'obj' already has normal vectors assigned, these
are overwritten!

The optional parameter 'flipDir' defines if the direction of the computed
normal vectors should be flipped by 180 degrees. Effectively, it selects
which side of the triangle is considered to be the "outside" - the direction
into which the normal vector should point.

The employed algorithm only works on triangles, not on quads. It computes
a per-triangle normal vector via normalized cross-product computation among
the edges of the triangle. Then it distributes those normals to the 3
vertices that define the triangle, accumulating contributions of all
triangles that share a vertex. At the end, the accumulated normals are
normalized and assigned as per-vertex normals.