---
layout: mfile
title: GPUFFTDemo1
categories:
  - GPGPUDemos
encoding: UTF-8
---

GPUFFTDemo1([fwidth=11]) - Demonstrate use of GPGPU computing for 2D-FFT.

This demo makes use of the FOSS GPUmat toolbox to perform a GPU
accelerated 2D FFT + filtering in frequency space + 2D inverse FFT on our
favourite bunnies. GPUmat allows to use NVidia's CUDA gpu computing
framework on supported NVidia gpu's (GeForce-8000 series and later, aka
Direct3D-10 or OpenGL-3 capable).

It shows how a Psychtoolbox floating point texture (with our bunnies
inside) can be efficiently passed to GPUmat as a matrix of GPUsingle data
type, which is stored and processed on the GPU. Then it uses GPUmat's fft
routines for forward/inverse fft's and matrix manipulation. Then it
returns the final image to Psychtoolbox as a new floating point texture
for display. The same steps are carried out with Matlab/Octave's regular
fft routines on the cpu for reference.

Requires the freely downloadable NVidia CUDA-5.0 SDK/Runtime and the free
and open-source GPUmat toolbox as well as a compute capable NVidia
graphics card.

# Parameters:

'fwidth' = Width of low-pass filter kernel in frequency space units.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychDemos/GPGPUDemos/GPUFFTDemo1.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychDemos/GPGPUDemos/GPUFFTDemo1.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychDemos/GPGPUDemos/GPUFFTDemo1.m</code>
</div>
