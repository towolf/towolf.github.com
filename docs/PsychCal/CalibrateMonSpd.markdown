---
layout: mfile
title: CalibrateMonSpd
categories:
  - PsychCal
encoding: UTF-8
---

CalibrateMonSpd

Calling script for monitor calibration.  Assumes
you have CMCheckInit/MeasSpd functions that initialize
measurement hardware and return a measured spectral
power distribution respectively.

NOTE (dhb, 8/19/12).  This code is a bit dusty, as it is not
being actively maintained.  In particular, the PTB display
control has evolved since this was last looked at carefully.
In general, you want to calibrate through the same set of
display calls you'll use in your experiment.  Below is some
prose written by Mario Kleiner that describes how the PTB
currently wants you to control and restore your clut.  In
an ideal world, this routine would be updated to match.  But
more generally, if you use this code you may want to modify
to make sure it is displaying colors the same way you will in
your experiments.  The actual work is done in CalibrateMonDrvr
and CalibrateAmbDrvr so that is where you would look.

    We have two functions for this. LoadIdentityClut() for loading an
    identity clut and configuring the GPU for identity pixel passthrough,
    and RestoreCluts, which restores to the state before
    LoadIdentityClut(). I think "[sca](/docs/sca)" calls that, as well as showing the
    cursor and other cleanup actions.

    LoadIdentityClut is also automatically called by PsychImaging etc. if
    the image processing pipeline is used for
    Bits++/Datapixx/Viewpixx,video attenuators etc.

    It is important to always use LoadIdentityClut() instead of self-made
    code. Many (most?) graphics cards on most operating systems have
    graphics driver bugs and hardware quirks which cause the self-made
    identity clut to actually not turn out to be an identity clut in the
    hardware. LoadIdentityClut() has heuristics to detect os/gpu combo
    and select an appropriately fudged lut to actually get an identity
    mapping. In case of new hardware with new quirks we should update
    that files detection logic to cope. Additionally there is
    SaveIdentityClut() to save a known good lut for automatic use with
    LoadIdentityClut, overriding its choice. And there is
    BitsPlusIdentityClutTest to test a Bits+ or Datapixx device
    thoroughly for problems and aid in fixing them. It is easy to get
    fooled into thinking you got it right, even when using a photometer,
    because some of the problems are subtle and not detectable without
    use of dynamic test patterns like in BitsPlusIdentityClutTest with
    Mono++ mode, or special debug functionality as in the
    DataPixx/ViewPixx devices.

    I use a DataPixx to test such stuff and PTB has builtin diagnostic to
    utilize that hardware to make sure that the video signal is really
    untampered.

    LoadIdentityClut also calls special functions in [Screen](/docs/Screen) that try to
    workaround or fix other hardware interference. E.g., in addition to
    cluts messing with pixel passthrough, there is also display dithering
    on any digital video output, and some new pre- and post-gamma
    corrections in latest generation hardware -- [Screen](/docs/Screen) can fix this for
    some cards on some operating systems, but only when used through
    LoadIdentityClut.

    E.g., almost all AMD cards will cause trouble on OSX when the
    PsychtoolboxKernelDriver and LoadIdentityClut etc. is not used,
    almost all NVidia cards on OSX will cause trouble unless you use some
    special NVidia kernel driver which is somewhere referenced on the
    Bits+ pages on our wiki. We have/need similar hacks on Windows, e.g.,
    PsychGPUControl() for AMD cards. On Linux either PTB's low-level
    fixes apply or they are not neccessary.

    So the CalibrateMonSpd etc. should be fixed to use
    LoadIdentityClut/RestoreCluts, everything else is just begging for
    trouble.

7/7/98  dhb  Wrote from generic.
        dhb  dacsize/driver filled in by hand, [Screen](/docs/Screen) fails to return it.
4/7/99  dhb  NINEBIT -\> NBITS.
        dhb  Wrote version for Radius 10 bit cards.
4/23/99 dhb  Change wavelength sampling to 380 4 101, PR-650 native.
9/22/99 dhb, mdr  Define boxSize.
8/11/00 dhb  Save mon in rawdata.
8/18/00 dhb  More descriptive information saved.
8/20/00 dhb  Automatic check for RADIUS and number of DAC bits.
9/10/00 pbe  Added option to blank another screen while measuring.
2/27/02 dhb  Various small fixes, including Radeon support.
        dhb  Change noMeterAvail to whichMeterType.
11/08/06 cgb, dhb  OS/X.
9/27/08 dhb  Default primary bases is 1 now.  Use RefitCalLinMod to change later if desired.
8/19/12 mk   [Ask](/docs/Ask) user for choice of display output device.