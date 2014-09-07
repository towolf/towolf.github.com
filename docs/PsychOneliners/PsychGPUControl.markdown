---
layout: mfile
title: PsychGPUControl
categories:
  - PsychOneliners
encoding: UTF-8
---

rc = PsychGPUControl(cmd, arg); -- Control low-level GPU settings.

PsychGPUControl calls into external helper tools to change certain
low-level operating settings of your systems graphics card (GPU).

Not all operating systems and GPU's support this. The function will
do nothing on unsupported OS/GPU combos.

Currently OS/X doesn't support this function at all, and on MS-Windows
and GNU/Linux, only recent ATI GPU's with recent drivers do support it.

All subfunctions return an optional 'rc' return code of zero on success,
non-zero on error or if the feature is unsupported.

# Subfunctions and their syntax & meaning:

rc = PsychGPUControl('SetDitheringEnabled', enableFlag);
\- Depending on the setting of 'enableFlag', either enable (=1) or
disable (=0) display color dithering on all connected displays.

Under normal circumstances, the GPU should decide itself if dithering
should be used or not. This function allows you to override the GPU's
automatic choice.


rc = PsychGPUControl('SetGPUPerformance', gpuPerformance);
\- Select the performance state of the GPU. 'gpuPerformance' can be set to
\0 if the GPU shall automatically adjust its performance and power-
consumption, or to one of 10 fixed levels between 1 and 10, where 1 means
the lowest performance - and power consumption, whereas 10 means the
highest performance - and maximum power consumption.

If in doubt, choose 10 for best accuracy of visual stimulus onset timing,
\0 for non-critical activities to leave the decision up to the graphics
driver and GPU.


rc = PsychGPUControl('FullScreenWindowDisablesCompositor', flag [, screenIds]);
\- Select if desktop composition should be disabled for displays where
a Psychtoolbox fullscreen onscreen window is displayed. 'flag' == 1 means
to disable composition for fullscreen windows, 0 means to enable composition
for fullscreen windows. You usually want composition to be disabled, as this
is currently the only way to get decent timing and precise visual stimulus
onset timestamping. The optional vector of 'screenIds' selects which screens
should be affected by the change. If left out or set to [], all detected
screens will be changed.




<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/PsychGPUControl.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/PsychGPUControl.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/PsychGPUControl.m</code>
</div>
