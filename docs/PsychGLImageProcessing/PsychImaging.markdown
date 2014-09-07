---
layout: mfile
title: PsychImaging
categories:
  - PsychGLImageProcessing
encoding: UTF-8
---

rc = PsychImaging(subcommand [,arg1][,arg2][....,argn]) - Control common
functions of the Psychtoolbox GPU image processing pipeline.

This function allows you to setup and control various aspects and common
functions of the Psychtoolbox image processing pipeline in a simple way.
Various standard scenarious can be conveniently set up with this routine,
e.g., geometric transformations of your stimulus image, various types of
display correction, ...

If you want to perform less common, unusual or simply not yet supported tasks
with the pipeline, use the low-level [Screen](/docs/Screen)('HookFunction', ...)
interface instead and have a peek in the M-File code for the
PsychImaging.m file to learn about the low-level interface.
See "help PsychGLImageprocessing" for more info.


# Subcommands and their meaning:

PsychImaging('PrepareConfiguration');
- Prepare setup of imaging pipeline for onscreen window.
This is the first step in the sequence of configuration steps.


PsychImaging('AddTask', whichChannel, whichTask [,param1]...);
- Add a specific task or processing requirement to the list of actions
to be performed by the pipeline for the currently selected onscreen
window. 'whichChannel' is a string with the name of the channel to
configure:

'LeftView' applies the action to the processing channel
for the left-eye view of a stereo configuration. 'RightView' applies the
action to the right-eye view of a stereo configuration. 'AllViews' applies
the action to both, left- and right eye view channels of a stereo
configuration or to the single monoscopic channel of a mono display
configuration. Other options are 'Compositor', 'FinalFormatting' and
'Finalizer' for special purpose channels. Set this to 'General' if the
command doesn't apply to a specific view, but is a general requirement.

'whichTask' contains the name string of one of the supported
actions:

\* 'UseGPGPUCompute' Enable use of GeneralPurposeGPU computing support.
  This prepares use of Psychtoolbox functions which are meant to
  interface with, or take advantage of, the general purpose computation
  capabilities of modern graphics processing units and other massively
  parallel compute acceleration hardware, e.g., DSP's, or multi-core
  processors. Interfacing with such hardware is done via common standard
  compute API's like NVidia's CUDA or the cross-platform OpenCL API.

  Use of this function often requires specific modern GPU hardware and
  the installation of additional driver software, e.g., NVidia's freely
  available CUDA SDK and runtime, or the free and open-source GPUmat
  toolbox. Read 'help PsychGPGPU' for further info.

  This function just detects and selects supported GPU compute API's for
  use with Psychtoolbox and initializes them and some Psychtoolbox
  function to take advantage if appropriate. While you could use those
  API's by themselves without calling this init function, Psychtoolbox
  builtin processing functions would not be able to take advantage of the
  API's or perform efficient and fast data exchange with them.

  Usage: PsychImaging('AddTask', 'General', 'UseGPGPUCompute', apitype [, flags]);

  'apitype' Allows selection of the compute API to use. The value 'Auto'
  leaves the choice to Psychtoolbox. The value 'GPUmat' selects the
  high-level, free and open-source GPUmat compute toolkit for Matlab.
  Currently no other choices are supported, but this is expected to
  change in the future.

  'flags' An optional string of keyword flags to determine behaviour.
  There aren't any flags defined yet.


\* 'SideBySideCompressedStereo' [Ask](/docs/Ask) for stereo display in a horizontally
  compressed side-by-side format. Left and Right eye images are drawn at
  full framebuffer resolution by usercode. [Screen](/docs/Screen)('[Flip](/docs/Flip)', ...) draws them
  horizontally compressed side-by-side to each other. They are scanned
  out to the display device this way and then the display device itself
  uncompresses them back to full resolution and displays them
  stereoscopically, typically via built-in alternating frame-sequential
  stereo with stereo goggles, but other methods are conceivable. This is
  one popular stereo frame packing format for stereo on HDMI display
  devices. Once you've set up a stereo display mode via PsychImaging, you
  can tweak its specific parameters by calling the function
  SetCompressedStereoSideBySideParameters().

  Usage: PsychImaging('AddTask', 'General', 'SideBySideCompressedStereo');


\* 'InterleavedColumnStereo' [Ask](/docs/Ask) for stereo display in interleaved mode.
  The output image is composed from the lefteye and righteye stereo
  buffers by interleaving their content: Even columns are filled with
  content from the left buffer, odd columns are filled with content from
  the right buffer, i.e., Col 0 = Left col 0, Col 1 = Right Col 0, Col 2
  \= Left col 1, Col 3 = Right col 1, ....

  This mode is useful for driving some auto-stereoscopic displays. These
  use either some vertical parallax barriers or vertical lenticular
  lense sheets. These direct light from even columns to one eye, light
  from odd columns to the other eye.

  Usage: PsychImaging('AddTask', 'General', 'InterleavedColumnStereo', startright);

  If 'startright' is zero, then even columns are taken from left buffer. If
  'startright' is one, then even columns are taken from the right buffer.

  You can use the RemapMouse() function to correct GetMouse() positions
  for potential geometric distortions introduced by this function.


\* 'InterleavedLineStereo' [Ask](/docs/Ask) for stereo display in interleaved mode.
  The output image is composed from the lefteye and righteye stereo
  buffers by interleaving their content: Even lines are filled with
  content from the left buffer, odd lines are filled with content from
  the right buffer, i.e., Row 0 = Left row 0, Row 1 = Right row 0, Row 2
  \= Left row 1, Row 3 = Right row 1, ....

  This mode is useful for driving some types of stereo devices and
  goggles, e.g., the iGlasses 3D Video goggles in interleaved stereo
  mode.

  Usage: PsychImaging('AddTask', 'General', 'InterleavedLineStereo', startright);

  If 'startright' is zero, then even lines are taken from left buffer. If
  'startright' is one, then even lines are taken from the right buffer.

  You can use the RemapMouse() function to correct GetMouse() positions
  for potential geometric distortions introduced by this function.%


\* 'DualWindowStereo' [Ask](/docs/Ask) for stereo display in dual-window mode (stereomode 10)

  Only use this function under MacOSX. If possible on your setup and OS,
  rather use a single window, spanning both stereo display outputs, and use
  stereomode 4 or 5 to display dual-display stereo. That is much more
  efficient in terms of speed, computational load and memory consumption,
  also potentially more robust with respect to visual stimulation timing.

  Usage: PsychImaging('AddTask', 'General', 'DualWindowStereo', rightEyeScreen [, rightEyeWindowRect]);

  The left-eye image will be displayed on the screen and at a location
  specified as usual via PsychImaging('Openwindow', screenid, ..., rect);
  The right eye image will be displayed on screen 'rightEyeScreen'. If
  the optional 'rightEyeWindowRect' is specified, then the right eye image
  is not displayed in a fullscreen window, but in a window with the bounding
  rectangle 'rightEyeWindowRect'.


\* 'UseVirtualFramebuffer' [Ask](/docs/Ask) for support of virtual framebuffer, even if
  it isn't strictly needed, given the remaining set of requirements. Most
  of the tasks require such a framebuffer - it gets enabled anyway. In a
  few cases, e.g., to simplify your code (no need for special cases), it
  may be useful to activate such a framebuffer even if it isn't strictly
  needed. This option activates a minimal buffer with 8 bits per color
  cmponent fixed point precision.

  Usage: PsychImaging('AddTask', 'General', 'UseVirtualFramebuffer');


\* 'UseDisplayRotation' [Ask](/docs/Ask) to use builtin panel fitter exclusively for
  rotating the framebuffer. This is useful if you want to turn your
  display device from landscape (= normal upright) orientation into
  portrait orientation (= rotated by 90 degrees clockwise or
  counterclockwise). In such a case you will want to rotate the
  framebuffer by 90 degrees as well, but you should \*not\* use the "rotate
  monitor" function of your operating system for this purpose, as this
  will very likely interfere with visual stimulus presentation timing and
  timestamping! Use this task instead. It will perform rotation in a
  similar way, but without severe interference to timing. However, there
  is one limitation to this method: Multisample anti-aliasing currently
  does not work if you use our framebuffer rotation.

  Usage: PsychImaging('AddTask', 'General', 'UseDisplayRotation', angle);

  'angle' is the desired rotation angle. The only values which will give
  well defined and useful results are multiples of 90 degrees, useful
  values are essentially 0, +90, -90 and 180 degrees for no rotation,
  clockwise rotation, counterclockwise rotation and upside down rotation.

  This function is mutually exclusive with 'UsePanelFitter', but if you
  need to use both, you can omit 'UseDisplayRotation' and pass the
  'angle' parameter to 'UsePanelFitter' instead, which also accepts an
  'angle' parameter with the same meaning.

  This function is not very mature yet: If you want to use the
  panelfitter for anything beyond simple framebuffer rotation by 90
  degree increments, you will likely hit bugs or limitations which will
  require significant tinkering by you.


\* 'UsePanelFitter' [Ask](/docs/Ask) to use builtin panel fitter. This allows you to
  define a virtual size for your onscreen window. The window will behave
  as if it had that virtual size wrt. all size queries and drawing
  operations. However, at [Screen](/docs/Screen)('[Flip](/docs/Flip)') time, the visual content of the
  window will be resized by a fast scaling operation to the real size of
  the windows framebuffer, ie., its real onscreen size. Scaling uses
  bilinear interpolation or better for high quality results. After
  rescaling to the real size, post-processing and display of your
  stimulus image will proceed at full resolution. This function is useful
  if you want to display a stimulus designed for a specific display
  resolution on a display device of different higher or lower resolution.
  Given that size and shape of the virtual framebuffer and real display
  window may not match, the function provides you with multiple possible
  choices on how to rescale your stimulus image, e.g., to maximize
  display area, or to preserve the aspect ratio of the original image,
  trading off displayed area etc.

  Usage: PsychImaging('AddTask', 'General', 'UsePanelFitter', size, strategy [, srcRect, dstRect][, angle]);

  'size' is a [width, height] vector defining the width x height of the
  virtual window in pixels.

#   'strategy' a text string selecting the scaling method. Following settings are possible:

  'Full' - [Scale](/docs/Scale) to full window size. Aspect ratio is not preserved,
           unless the virtual window and the real onscreen windows 'rect'
           already have the same aspect ratio, in which case this will be
           a simple scaling operation.

  'Aspect' - [Scale](/docs/Scale) to maximum size possible while preserving aspect
             ratio. This will center the stimulus and add black
             horizontal or vertical borders as neccessary.

  'AspectWidth' - [Scale](/docs/Scale) aspect ratio preserving to cover full display
                  width. Cut off top and bottom content if neccessary.

  'AspectHeight' - [Scale](/docs/Scale) aspect ratio preserving to cover full display
                   height. Cut off left and right content if neccessary.

  'Centered' - Center stimulus without any scaling, add black borders
               around stimulus or cut away border regions to get a
               one-to-one mapping.

  'Custom' - This works like the 'srcRect' and 'dstRect' parameters of
             [Screen](/docs/Screen)('DrawTexture'): Cut out a 'srcRect' region from the
             virtual framebuffer and display it in the 'dstRect' region.
             'srcRect' and 'dstRect' are given in typical [left, top, right, bottom]
             format.

  'angle' is an optional rotation angle. If provided and non-zero, the
  panelfitter will also rotate the output framebuffer by the given
  rotation angle. Note: This doesn't work very well yet with most
  framebuffer sizes and scaling strategies. What does work is if the
  specified 'size' is identical to the onscreen windows size, or is its
  transposed size (ie., if window is width x height pixels, then height x
  width pixels will work as 'size' parameter) and the rotation angle is a
  multiple of 90 degrees. This is mostly useful for display rotation from
  landscape orientation into portrait orientation. Your mileage with
  other configurations or rotation angles will vary.

  Example: Suppose your real window covers a 1920 x 1080 display.

  PsychImaging('AddTask', 'General', 'UsePanelFitter', [800 600], 'Aspect');
  -> This would give you a virtual window of 800 x 600 pixels to draw
  into and would rescale the 800 x 600 stimulus image to 1440 x 1080
  pixels and display it centered on the 1920 x 1080 pixels display.
  Aspect ratio would be correct and the image would cover the full height
  1080 pixels of the display, but only 1440 out of 1920 pixels of its
  width, thereby leaving black borders on the left and right side of your
  stimulus.

  PsychImaging('AddTask', 'General', 'UsePanelFitter', [800 600], 'AspectHeight');
  -> Would do the same as above.

  PsychImaging('AddTask', 'General', 'UsePanelFitter', [800 600], 'AspectWidth');
  -> Would create a final image of 1920 pixels width, as you asked to
  cover the full display width, aspect ratio would be correct, but the
  top and bottom 75 pixels of your original stimulus would get cut away,
  because they wouldn't fit after scaling without distorting the image.


\* 'UseFastOffscreenWindows' [Ask](/docs/Ask) for support of fast Offscreen windows.
  These use a more efficient storage, backed by OpenGL framebuffer
  objects (FBO's). Drawing into them isn't faster, but \*switching\*
  between drawing into onscreen- and offscreen windows, or switching
  between drawing into different offscreen windows is faster. They also
  support a couple of other advanced features and performance
  improvements in conjunction with the imaging pipeline.
  If you only specify this task, then you'll get the benefit of fast
  windows, without the cost of other features of the pipeline you might
  not need.

  Usage: PsychImaging('AddTask', 'General', 'UseFastOffscreenWindows');


\* 'EnableCLUTMapping' Enable support for old-fashioned clut animation /
  clut mapping. The drawn framebuffer image is transformed by applying a
  color lookup table (clut). This is not done via the hardware gamma
  tables as in the good ol' days, but by application of the clut via
  image processing. Hardware gamma tables don't provide well defined
  timing on modern hardware, therefore they aren't suitable anymore.

  You can update the clut to be applied at the next [Screen](/docs/Screen)('[Flip](/docs/Flip)');
  via the command [Screen](/docs/Screen)('LoadNormalizedGammatable', windowPtr, clut, 2);

  'clut' needs to be a clutSize-by-3 matrix, with 'clutSize' slots and
  one column for each of the red, green and blue color channels.

#   Setup command:

  By default, a clut of 256 slots with (R,G,B) values is used, but you
  can provide the optional 'clutSize' parameter to use clut's with more
  slots. The maximum number depends on your GPU, but 2048 are typically
  supported even on very low-end cards.

  If you set 'highprecision' to 1, the clut will resolve values at more
  than 8 bit per color channel on modern hardware. This usually only
  makes sense if you also use a more than 8 bpc framebuffer with more
  than 256 slots as clutSize.

  Usage: PsychImaging('AddTask', whichView, 'EnableCLUTMapping' [, clutSize=256][, highprecision=0]);
  Example: PsychImaging('AddTask', 'AllViews', 'EnableCLUTMapping');


\* 'FloatingPoint16Bit' [Ask](/docs/Ask) for a 16 bit floating point precision
  framebuffer. This allows more than 8 bit precision for complex drawing,
  compositing and image processing operations. It also allows
  alpha-blending with signed color values and intermediate results that
  are outside the displayable range, e.g., negative. Precision is about 3
  digits behind the decimal point or 1024 discriminable displayable
  levels. If you need higher precision, choose 'FloatingPoint32Bit'.

  Usage: PsychImaging('AddTask', 'General', 'FloatingPoint16Bit');


\* 'FixedPoint16Bit' [Ask](/docs/Ask) for a 16 bit integer precision framebuffer.
  On graphics hardware that supports this, a 16 bit signed integer
  framebuffer will be created. Such a framebuffer can store intermediate
  color values in the normalized range [-1.0 ; +1.0] with a precision of
  15 bits per component. Only positive values between 0.0 and 1.0 are
  displayable in the end though. If the graphics hardware does not support this,
  a 16 bit unsigned integer framebuffer is tried instead. Such a framebuffer
  allows for 16 bits of precision per color component. However, many graphics
  cards do not support alpha-blending on such a framebuffer, and
  intermediate out-of-range values (smaller than zero or bigger than one) aren't
  supported either. Such values will be clamped to the representable [0.0 ; 1.0]
  range instead. Additionally this mode is only supported on some graphics
  hardware. It is a special purpose intermediate solution - more accurate
  than 16 bit floating point, but less capable and less accurate than 32
  bit floating point. If you need higher precision, choose 'FloatingPoint32Bit'.

  The main sad reason this switch exists is because some graphics hardware or
  graphics drivers do not support floating point precision textures and
  framebuffers due to some ridiculous patent restrictions, but they do
  support a 16 bit signed or unsigned integer precision format. The switch
  is basically a workaround for the broken patent systems of many countries.

  Usage: PsychImaging('AddTask', 'General', 'FixedPoint16Bit');


\* 'FloatingPoint32Bit' [Ask](/docs/Ask) for a 32 bit floating point precision
  framebuffer. This allows more than 8 bit precision for complex drawing,
  compositing and image processing operations. It also allows
  alpha-blending with signed color values and intermediate results that
  are outside the displayable range, e.g., negative. Precision is about
  6\.5 digits behind the dezimal point or 8 million discriminable displayable
  levels. Be aware that only the most recent hardware (NVidia Geforce
  8000 series, ATI Radeon HD 2000 series) is able to perform
  alpha-blending at full speed in this mode. Enabling alpha-blending on
  older hardware may cause a significant decrease in drawing performance,
  or alpha blending may not work at all at this precision! If you'd like
  to have both, the highest precision and support for alpha-blending,
  specify 'FloatingPoint32BitIfPossible' instead. PTB will then try to
  use 32 bit precision if this is possible in combination with alpha
  blending. Otherwise, it will choose 16 bit precision for drawing &
  blending, but 32 bit precision at least for the post-processing.

  Usage: PsychImaging('AddTask', 'General', 'FloatingPoint32Bit');


\* 'FloatingPoint32BitIfPossible' [Ask](/docs/Ask) PTB to choose the highest precision
  that is possible on your hardware without sacrificing functionality like,
  e.g., alpha-blending. PTB will choose the best compromise possible for
  your hardware setup.

  Usage: PsychImaging('AddTask', 'General', 'FloatingPoint32BitIfPossible');


\* 'NormalizedHighresColorRange' [Ask](/docs/Ask) PTB to use a normalized range of
  color and luminance intensity levels in the interval [0; 1], ie. values
  between zero and one for minimum and maximum intensity. Also ask for
  unclamped colors -- intermediate results are allowed to take on
  arbitrary values, e.g., also negative values. All [Screen](/docs/Screen)() 2D drawing
  commands should operate at maximum color/luminance precision.

  Usage: PsychImaging('AddTask', 'General', 'NormalizedHighresColorRange' [, applyAlsoToMakeTexture]);

  The command PsychImaging('AddTask', 'General', 'NormalizedHighresColorRange', 1);
  is automatically executed if you used PsychDefaultSetup(featureLevel)
  with a featureLevel of >= 2 at the top of your experiment script,
  \*except\* that clamping is \*not\* disabled by default in this case! To
  disable clamping you'd still need to add this task explicitely, as
  unclamping may have unintended side effects on old graphics hardware.

  The optional flag 'applyAlsoToMakeTexture' defaults to zero. If set to 1,
  then a unit color range of expected input values in the [0; 1] range is
  also applied to standard 8-Bit precision textures in [Screen](/docs/Screen)('MakeTexture')
  if the provided Matlab imageMatrix is of double precision type instead of
  uint8 type. This allows to specify standard textures in the same consistent
  value range 0-1 as other drawing colors, for cleaner code. Such textures
  will still be limited to 0-1 range and only resolved into 256 intensity
  levels, unless you also set the optional 'floatprecision' flag in [Screen](/docs/Screen)('MakeTexture')
  to a value of 1 or 2. We still apply this limitation, as high precision textures consume
  more memory and other resources and are incompatible with very old graphics
  hardware.

  This is just a convenience shortcut for [Screen](/docs/Screen)('ColorRange', win, 1, 0, applyAlsoToMakeTexture);
  with the added benefit of allowing to specify the background clear
  color in normalized 0-1 range as well. This command is implied by use
  of any of the high precision display device drivers (for attenuators,
  Bits+ box etc.). It is only needed if you want to create the same
  visual results on a 8 bit standard framebuffer without needing to
  change your code, or if you want to set the 'applyAlsoToMakeTexture' flag to a
  setting of non-zero, so unit colorrange also applies to [Screen](/docs/Screen)('MakeTexture').


\* 'DisplayColorCorrection' Select a method for color correction to apply to
  stimuli before output conversion and display. You have to specify a
  color correction method 'methodname' to apply as parameter, see "help
  PsychColorCorrection" for an overview of supported color correction
  methods and their adjustable parameters. The imaging pipeline will be
  set up to support the chosen color correction method. After you've
  opened the onscreen window, you can use the different subcommands of
  PsychColorCorrection() to change parameters of the color correction
  algorithm at runtime.

  Usage: PsychImaging('AddTask', whichView, 'DisplayColorCorrection', methodname);

  Example: PsychImaging('AddTask', 'FinalFormatting', 'DisplayColorCorrection', 'SimpleGamma');
  This would apply a simple power-law gamma correction to all view
  channels of a stereo setup, or the single view of a monoscopic setup.
  Later on you could use the methods of PsychColorCorrection() to
  actually set the wanted gamma correction factors.

  Please note that we use the channel 'FinalFormatting' instead of
  'AllViews' as we'd usually do. Both specs will work, but a selection
  of 'FinalFormatting' will lead to faster processing in many cases, so
  this is preferred here if you want to apply the same setting to all
  view channels - or to a single monoscopic display. Should you find
  that things don't work as expected, you might try 'AllViews' instead
  of 'FinalFormatting' - There are subtle differences in how they
  process your instructions, which may matter in some corner cases.


\* 'EnablePseudoGrayOutput' Enable the high-performance driver for the
  rendering of up to 1786 different levels of gray on a standard - but
  well calibrated - color monitor and 8 bit graphics card. This is done
  by applying an algorithn known as "Pseudo-Gray" or "Bit stealing".
  Selecting this mode implies use of 32 bit floating point
  framebuffers, unless you specify use of a 16 bit floating point
  framebuffer via 'FloatingPoint16Bit' explicitely. If you do that, you
  will not quite be able to use the full 10.8 bit output precision, but
  only approximately 10 bits. The expected range of luminance values is
  between 0 and 1. See "help CreatePseudoGrayLUT" for further
  explanation.

  Usage: PsychImaging('AddTask', 'General', 'EnablePseudoGrayOutput');


\* 'EnableGenericHighPrecisionLuminanceOutput'
  Setup Psychtoolbox for conversion of high precision luminance images
  into a format suitable for special high precision luminance display
  devices. This is a generic support routine that uses LUT based
  conversion.

  Usage: PsychImaging('AddTask', 'General', 'EnableGenericHighPrecisionLuminanceOutput', lut);


\* 'EnableVideoSwitcherSimpleLuminanceOutput'
  Setup Psychtoolbox for conversion of high precision luminance images
  into a format suitable for driving the "VideoSwitcher" high precision
  luminance display device which was developed by Xiangrui Li et al.

  This implements the simple converter, which only needs the
  Blue-To-Red-Ratio of the device as input parameter and performs
  conversion via a closed-form formula without any need for lookup
  tables. This is supposed to be fast.

  See "help VideoSwitcher" for more info about the device and its
  options.

  Usage: PsychImaging('AddTask', 'General', 'EnableVideoSwitcherSimpleLuminanceOutput' [, btrr] [, trigger]);

  - The optional 'btrr' parameter is the Blue-To-Red-Ratio to use. If the
  parameter is left out, the btrr value will be read from a global
  configuration file.

  - The optional 'trigger' parameter can be zero for "No trigger", or 1
  for "Use trigger as configured". By default, trigger is off (==0).
  Enabled, one can use the VideoSwitcher('SetTrigger', ...); function to
  configure when and how a trigger signal should be emitted. Trigger
  signals are simply specific pixel patterns in the green output channel.
  That channel is recognized by the VideoSwitcher as a trigger signal
  control channel.


\* 'EnableVideoSwitcherCalibratedLuminanceOutput'
  Setup Psychtoolbox for conversion of high precision luminance images
  into a format suitable for driving the "VideoSwitcher" high precision
  luminance display device which was developed by Xiangrui Li et al.

  This implements the simple converter, which only needs the
  Blue-To-Red-Ratio of the device as input parameter and performs
  conversion via a closed-form formula without any need for lookup
  tables. This is supposed to be fast.

  See "help VideoSwitcher" for more info about the device and its
  options.

  Usage: PsychImaging('AddTask', 'General', 'EnableVideoSwitcherCalibratedLuminanceOutput' [, btrr] [, lut] [, trigger]);

  - The optional 'btrr' parameter is the Blue-To-Red-Ratio to use. If the
  parameter is left out, the btrr value will be read from a global
  configuration file.

  - The optional 'lut' paramter is a 257 elements vector of luminance
  values, which maps blue channel drive indices to luminance values. This
  lut needs to be acquired via a calibration procedure by use of a
  photometer. If 'lut' is left out, the table will be read from a global
  configuration file.

  - The optional 'trigger' parameter can be zero for "No trigger", or 1
  for "Use trigger as configured". By default, trigger is off (==0).
  Enabled, one can use the VideoSwitcher('SetTrigger', ...); function to
  configure when and how a trigger signal should be emitted. Trigger
  signals are simply specific pixel patterns in the green output channel.
  That channel is recognized by the VideoSwitcher as a trigger signal
  control channel.


\* 'EnableNative10BitFramebuffer' Enable support for output of stimuli
  with 10 bit precision per color channel (10 bpc / 30 bpp / "Deep color")
  on graphics hardware that supports native 10 bpc framebuffers.

  Many graphics cards of the professional class AMD/ATI Fire series
  (2008 models and later) and all current models of the professional class
  NVidia Quadro series (2008 models and later), as well as all current models
  of the consumer class NVidia GeForce series under Linux, do support 10 bpc
  framebuffers under some circumstances. 10 bpc display on classic CRT monitors
  which are connected via analog VGA outputs is supported. Support for digital
  display devices like LCD/OLED panels or video projectors depends on the specific
  type of display output connector used, the specific panels, and their video
  settings. Consult manufacturer documentation for details. In general, 10 bpc
  output may be supported on some graphics cards and displays via DisplayPort
  or HDMI video outputs, but to our knowledge not via DVI-D outputs.

  If such a combination of graphics card and display is present on your system
  on Linux or Microsoft Windows, then Psychtoolbox will request native support
  from the standard graphics drivers, ie., it won't need to use our own
  homegrown, experimental box of tricks to enable this.

  Apple OSX, as of version 10.9 "Mavericks", does not support 10 bpc framebuffers,
  so 10 bpc output will only work with our own box of tricks - if at all.

#   Psychtoolbox experimental 10 bpc framebuffer support:

  Additionally we support ATI/AMD Radeon hardware of the X1000, HD2000 - HD8000,
  series and later models under Linux and OSX via our own low-level setup mechanisms.
  These models support a native ARGB2101010 framebuffer, ie., a system
  framebuffer with 2 bits for the alpha channel, and 10 bits per color channel.

  As this is supported by the hardware, but not by the standard ATI
  graphics drivers, we follow a hybrid approach: We use a special kernel
  level driver to reconfigure the hardware for 10 bpc framebuffer support.
  Then we use a special imaging pipeline formatting plugin to convert
  16 bpc or 32 bpc stimuli into the special data format required by this
  framebuffer configuration.

  You'll need to install and load the special Psychtoolbox kernel driver
  on OSX. On Linux you must have run PsychLinuxConfiguration at least once
  on your system at some point. You'll need to have one of the supported AMD
  Radeon gfx-cards (see above) for this to work. Read 'help PsychtoolboxKernelDriver'
  for info about the driver and installation instructions on OSX.

  CAUTION: Support for 10 bpc framebuffers on AMD Radeon graphics cards
  under OSX is highly experimental and not guaranteed to work reliably on
  any system configuration. While it has been successfully tested on multiple
  versions of OSX (10.4, 10.5, 10.6 and 10.8) with some X1000 cards,
  some HD2000/3000 cards and HD 4870 cards, this feature could fail on other
  systems or even after any operating system upgrade! Use at your own risk and
  verify proper operation carefully before production use. The same experimental
  status is true for use on Linux with the proprietary AMD Catalyst graphics drivers.
  If you use Linux with the free and open-source AMD graphics drivers, 10 bpc
  framebuffer support should work reliably, so use of the open-source drivers on
  Linux is recommended for reliable results.

  Getting a 10 bpc framebuffer working is only the first half of what you need for
  high color precision output. Your graphics card must also be able to transmit the
  video signal at high precision to the display device and the display must be able
  to faithfully reproduce the high precision image. 10 bpc output has been verified
  to work for analog VGA connected CRT monitors and displays on both AMD and
  NVidia graphics cards which do support 10 bpc framebuffers, so with a analog VGA
  CRT you should be safe. The status of 10 bpc output to digital display devices differs
  a lot across devices and OS'es. Output of 10 bpc framebuffers to standard 8 bpc digital panels
  via digital dithering is known to work, but that is not the real thing, only a simulation
  of 10 bpc via dithering to 8 bpc. This may or may not be good enough for your specific
  visual stimulation paradigm. On a DVI-D connected digital display, this dithered output
  is the best you will ever get. DisplayPort: Recent NVidia and AMD graphics cards can
  output to some suitable DisplayPort displays with 10 bpc or higher precision on Linux,
  and maybe also on MS-Windows, but you have to verify this carefully for your specific display.
  HDMI: Recent Intel graphics cards can output up to 12 bpc precision to HDMI deep color
  capable displays on Linux, and maybe also on MS-Windows. All AMD graphics cards of model
  Radeon HD-5000 or later (and equivalent Fire-Series models) can output to HDMI deep color
  capable displays with 10 bpc real precision at least if you use a Linux kernel of version 3.16
  or later with the open-source AMD graphics drivers. At least on Linux 3.16 you will need to add
  the kernel command line option "radeon.deep\_color=1" to the kernel boot loader options, e.g.,
  by editing /etc/default/grub and running "sudo update-grub2" afterwards. This because deep
  color output is disabled by default, to work around various broken hdmi display devices.

  The status with the proprietary AMD drivers on Linux or on MS-Windows is unknown.
  Apple OSX 10.9 and earlier do not support any high precision video output over any digital
  output, neither DVI-D, nor DisplayPort or HDMI. All you'll get at best on OSX is simulated > 8
  bpc via dithering.

  Usage: PsychImaging('AddTask', 'General', 'EnableNative10BitFramebuffer' [, disableDithering=0]);

  This function will setup a 32 bpc floating point resolution framebuffer by
  default for Psychtoolbox drawing and stimulus processing. Output will happen
  into a 10 bpc framebuffer. The function will also disable the graphics cards
  gamma tables, so you'll need to use PsychImaging(...'DisplayColorCorrection'...)
  for gamma and color correction if you need this.

  The function will \*not\* disable dithering on digital displays by default,
  but leave that decision to the operating system and graphics drivers of
  your machine. A well working OS would disable dithering on a 10 bpc or
  higher color depth display, if the display reports its capability to the
  OS via its EDID info. It would enable dithering on < 10 bpc displays, so
  you'd get a "pseudo 10 bpc" display where 10 bpc color depths is
  simulated on a 6 bpc or 8 bpc display via the dithering.

  You can disable dithering manually on some graphics cards by providing the
  optional 'disableDithering' flag as 1. Currently mostly AMD cards allow this
  control. NVidia or Intel cards require manual setup to force dithering off.


\* 'EnableNative11BitFramebuffer' Enable support for output of stimuli
  with almost 11 bit precision per color channel (11 bpc / 32 bpp / "Deep color")
  on graphics hardware that supports native 11 bpc framebuffers. This will
  request an ~ 11 bpc framebuffer from the operating system. If it can't
  get such a framebuffer on Linux or OSX with AMD graphics hardware,
  it will use our own homegrown setup code to provide such a framebuffer
  anyway on Radeon X1000, HD-2000 and later graphics cards and equivalent
  Fire-Series graphics cards.

  Read all the explanations in the section above for 'EnableNative10BitFramebuffer'
  for capabilities, limitations and possible caveats on different systems.

  Please note that this "11 Bit framebuffer" is not quite 11 bpc precision, but
  only about ~ 10.6666 bpc precision. Specifically, the framebuffer can only
  store at most 32 bits of color information per pixel, so it will store 11 bit
  precision for the red channel (2048 distinct red intensity levels), 11 bit
  (2048 levels) for the green channel, but only 10 bit (1024 levels) for the blue
  channel, for a total number of 11 + 11 + 10 bits = 32 bits of color information
  per pixel, or 4 billion different possible colors. A true 11 bpc framebuffer would
  need 33 bits per pixel, and current graphics hardware can't handle that.

  How many bits of precision of these ~ 11 bpc actually reach your display device?
  - Analog VGA only provides for maximum 10 bpc output precision on all shipping
    NVidia and AMD graphics cards. Intel graphics cards only allow for 8 bpc.
  - DisplayPort or HDMI might allow for transfer of 11 bpc precision, in general they
    support up to 12 bpc. However additional hardware restrictions for your graphics
    card may limit precision to as low as 10 bpc. To our knowledge, only AMD graphics
    cards support ~ 11 bpc framebuffers at all. Radeon HD-7000 and earlier can only
    truly process up to 10 bpc, so 'EnableNative11BitFramebuffer' may not gain you any
    precision over 'EnableNative10BitFramebuffer' in practice on these cards. AMD cards
    of the "Sea Islands" family or later, mostly models from the year 2014, should be able
    to process and output up to 12 bpc over HDMI or DisplayPort, so they'd be able to output
    true ~11 bpc images. However, this hasn't been verified by us so far due to lack of
    suitable hardware.

  So obviously: Measure very carefully on your setup what kind of precision you really
  get and make sure not to be fooled by dithering.

  Usage: PsychImaging('AddTask', 'General', 'EnableNative11BitFramebuffer' [, disableDithering=0]);


\* 'EnableBrightSideHDROutput' Enable the high-performance driver for
  BrightSide Technologies High dynamic range display device for 16 bit
  per color channel output precision. See "help BrightSideHDR" for
  detailed explanation. Please note that you'll need to install the 3rd
  party driver libraries for that display as described in the help file.
  PTB doesn't come bundled with that libraries for copyright reasons.

  Usage: PsychImaging('AddTask', 'General', 'EnableBrightSideHDROutput');


\* 'UseDataPixx' Tell Psychtoolbox that additional functionality for
  displaying the onscreen window on a VPixx Technologies DataPixx device
  should be enabled.

  This command is implied by enabling a DataPixx video mode by one of the
  commands for the DataPixx in the following sections.

  'UseDataPixx' mostly prepares use of a variety of subfunctions in the
  DataPixxToolbox ("help DataPixxToolbox") and in the PsychDataPixx()
  high-level driver ("help PsychDataPixx").


\* 'EnableDataPixxL48Output' Setup Psychtoolbox for L48 mode of the VPixx
  Technologies DataPixx device. This loads the graphics hardwares gamma
  table with an identity mapping so it can't interfere with DPixx video
  processing. It also sets up automatic generation of control signals to
  support the features of DPixx that are available via the functions in
  PsychDataPixx(). You will be able to upload new CLUT's into the DPixx
  by use of the [Screen](/docs/Screen)('LoadNormalizedGammaTable', window, clut, 2);
  command. CLUT updates will be synchronized with [Screen](/docs/Screen)('[Flip](/docs/Flip)') commands.
  Please note that while L48 CLUT mode works even with very old
  graphics hardware, this is a pretty cumbersome way of driving the
  DPixx. On recent hardware, you will want to use M16 or C48 mode
  (see below). That allows to draw arbitrarily complex stimuli with as
  many colors as you want and PTB will take care of conversion into the
  M16 or C48 format for DataPixx.

  Usage: PsychImaging('AddTask', 'General', 'EnableDataPixxL48Output');


\* 'EnableDataPixxM16Output' Enable the high-performance driver for M16
  mode of the VPixx Technologies DataPixx device. This is the fastest and
  most elegant way of driving the DPixx box with 16 bit luminance output
  precision. See "help DataPixx" for more information. Selecting this
  mode implies use of 32 bit floating point framebuffers, unless you
  specify use of a 16 bit floating point framebuffer via
  'FloatingPoint16Bit' explicitely. If you do that, you will not be able
  to use the full 16 bit output precision, but only approximately 10 bits.

  Usage: PsychImaging('AddTask', 'General', 'EnableDataPixxM16Output');

  If you want to make use of the color overlay plane in M16 mode, then
  call the function like this:

  Usage: PsychImaging('AddTask', 'General', 'EnableDataPixxM16OutputWithOverlay');
  See the explanation of color overlays in the section
  'EnableBits++Mono++OutputWithOverlay' - behaviour of color overlays is
  identical for the CRS Bits++ and the VPixx DataPixx.


\* 'EnableDataPixxC48Output' Enable the high-performance driver for the
  C48 mode of VPixx technologies DataPixx box. This is the fastest and
  most elegant way of driving the DataPixx box with 16 bit per color
  channel output precision. See "help DataPixx" for more information.
  Selecting this mode implies use of 32 bit floating point framebuffers,
  unless you specify use of a 16 bit floating point framebuffer via
  'FloatingPoint16Bit' explicitely. If you do that, you will not be able
  to use the full 16 bit output precision, but only approximately 10 bits.

  Usage: PsychImaging('AddTask', 'General', 'EnableDataPixxC48Output', mode);

  See the section below about 'EnableBits++Color++Output' for the meaning
  of the mandatory "mode" parameter.

  You can use the RemapMouse() function to correct GetMouse() positions
  for potential geometric distortions introduced by this function for
  "mode" zero.


\* 'UseBits#' Tell Psychtoolbox that additional functionality for
  displaying the onscreen window on a Cambridge Research Systems Bits#
  device should be enabled.

  This command is implied by enabling a Bits+ or Bits# video mode by one
  of the commands for the Bits+/Bits# in the following sections, if the
  driver can auto-detect a connected Bits# device. If it cannot auto-detect
  a connected Bits# device and this command is omitted, Psychtoolbox will
  instead assume that an older Bits+ is in use and only allow functionality
  common to Bits# and Bits+, without automatic video mode switching.

  If you provide this command, you can optionally specify the name of the
  serial port to which your Bits# is connected, instead of leaving it to
  the system to find this out (either via configuration file or via a
  guess-o-matic).

  Usage: PsychImaging('AddTask', 'General', 'UseBits#' [, BitsSharpSerialPort]);

  'BitsSharpSerialPort' is optional and can be set to the name of a serial
  port for your specific operating system and computer, to which the Bits#
  is connected. If omitted, Psychtoolbox will look for the name in the first
  line of text of a text file stored under the filesystem path and filename
  [PsychtoolboxConfigDir 'BitsSharpConfig.txt']. If that file is empty, the
  serial port is auto-detected (Good luck!).

  'UseBits#' mostly prepares use of a variety of new Bits# subfunctions
  in the BitsPlusPlus() high-level driver ("help BitsPlusPlus").


\* 'EnableBits++Bits++Output' Setup Psychtoolbox for Bits++ mode of the
  Cambridge Research Systems Bits++ box. This loads the graphics
  hardwares gamma table with an identity mapping so it can't interfere
  with Bits++ T-Lock system. It also sets up automatic generation of
  Bits++ T-Lock codes: You will be able to upload new CLUT's into the
  Bits++ by use of the [Screen](/docs/Screen)('LoadNormalizedGammaTable', window, clut, 2);
  command. CLUT updates will be synchronized with [Screen](/docs/Screen)('[Flip](/docs/Flip)')
  commands, because PTB will generate and draw the proper T-Lock code
  into the top line of your onscreen window. Please note that while
  Bits++ CLUT mode works even with very old graphics hardware, this is a
  pretty cumbersome way of driving the Bits++. On recent hardware, you
  will want to use Mono++ or Color++ mode (see below). That allows to
  draw arbitrarily complex stimuli with as many colors as you want and
  PTB will take care of conversion into the Color++ or Mono++ format for
  Bits++.

  Usage: PsychImaging('AddTask', 'General', 'EnableBits++Bits++Output');


\* 'EnableBits++Mono++Output' Enable the high-performance driver for the
  Mono++ mode of Cambridge Research Systems Bits++ box. This is the
  fastest and most elegant way of driving the Bits++ box with 14 bit
  luminance output precision. See "help BitsPlusPlus" for more
  information. Selecting this mode implies use of 32 bit floating point
  framebuffers, unless you specify use of a 16 bit floating point
  framebuffer via 'FloatingPoint16Bit' explicitely. If you do that, you
  will not be able to use the full 14 bit output precision of Bits++, but
  only approximately 10 bits.

  Usage: PsychImaging('AddTask', 'General', 'EnableBits++Mono++Output');

  If you want to make use of the color overlay plane in Mono++ mode, then
  call the function like this:

  Usage: PsychImaging('AddTask', 'General', 'EnableBits++Mono++OutputWithOverlay');

#   Then you can query the window handle of the overlay window via:

  overlayWin = PsychImaging('GetOverlayWindow', window);

  'overlayWin' is the handle to the overlay window associated with the
  overlay of onscreen window 'window'. The overlay window is a standard
  offscreen window, so you can do anything with it that you would want to
  do with offscreen windows. The only difference is that the window is a
  pure index window: It only has one "color channel", which can be written
  with color values between 0 and 255. Values 1 to 255 get mapped to the
  corresponding color indices of the Bits++ overlay plane: A zero value is
  transparent -- Content of the onscreen window is visible. Positive
  non-zero color values map to the 255 indices available in overlay mode,
  these get mapped by the Bits++ CLUT to colors. You can define the
  mapping of indices to CLUT colors via the
  [Screen](/docs/Screen)('LoadNormalizedGammaTable', window, clut, 2); command.

  Updates of the overlay image are synchronized to [Screen](/docs/Screen)('[Flip](/docs/Flip)')
  updates. If you draw into the overlay window, the changed overlay image
  will become visible at [Screen](/docs/Screen)('[Flip](/docs/Flip)') time -- in sync with the changed
  onscreen window content. The overlay plane is not automatically cleared
  to background (or transparent) color after a flip, but its content
  persists across flips. You need to clear it out manually via a
  [Screen](/docs/Screen)('FillRect') command.


\* 'EnableBits++Color++Output' Enable the high-performance driver for the
  Color++ mode of Cambridge Research Systems Bits++ box. This is the
  fastest and most elegant way of driving the Bits++ box with 14 bit
  per color channel output precision. See "help BitsPlusPlus" for more
  information. Selecting this mode implies use of 32 bit floating point
  framebuffers, unless you specify use of a 16 bit floating point
  framebuffer via 'FloatingPoint16Bit' explicitely. If you do that, you
  will not be able to use the full 14 bit output precision of Bits++, but
  only approximately 10 bits.

  Usage: PsychImaging('AddTask', 'General', 'EnableBits++Color++Output', mode);

  "mode" is a mandatory numeric parameter which must be 0, 1 or 2. In
  Color++ mode, the effective horizontal display resolution is only half
  the normal horizontal resolution. To cope with this, multiple different
  methods are implemented to squeeze your stimulus image horizontally by
  a factor of two. The following options exist:

  0 = This is the "classic" mode which was used in all Psychtoolbox
  versions prior to 22nd September 2010. If you want to keep old code
  working as is, select 0. In this mode, your script will only see a
  framebuffer that is half the true horizontal resolution of your
  connected display screen. Each drawn pixel will be stretched to cover
  two pixels on the output display device horizontally. While this
  preserves the content of your stimulus image exactly, it means that the
  aspect ratio of all displayed text and stimuli will be 2:1. Text will
  be twice as wide as its height. Circles or squares will turn into
  horizontal ellipses or rectangles etc. You'll need to do extra work in
  your code if you want to preserve aspect ratio properly.

  You can use the RemapMouse() function to correct GetMouse() positions
  for potential geometric distortions introduced by this function for
  "mode" zero.

  Example: A fine vertical grid with alternating vertical white and black
  lines would display as expected, but each white or black stripe would be
  two pixels wide on the display instead of one pixel wide.

  1 = Subsample: Your framebuffer will appear at the same resolution as
  your display device. Aspect ratio of drawn stimuli/text etc. will be
  correct and as expected. However, every 2nd column of pixels in your
  stimulus (ie., all odd-numbered x-coordinates 1,3,5,7,...) will be
  completely ignored, only even columns are used!

  Example: A fine vertical grid with alternating vertical white and black
  lines would display as a purely white image, as only the white pixels
  in the even columns would be used, whereas the black pixels in the odd
  columns would be ignored.

  2 = Average: Your framebuffer will appear at the same resolution as
  your display device. Aspect ratio of drawn stimuli/text etc. will be
  correct and as expected. However, each pair of adjacent even/odd pixel
  columns will be averaged before output. Stimulus pixels 0 and 1 will
  contribute the mean color for display pixel 0. Pixels 2 and 3 will be
  averaged into display pixel 1 and so on. Visually this gives the most
  pleasing and smooth results, but if adjacent even/odd pixels don't have
  the same color value, you'll obviously get an output color that is
  neither the color of the even pixel nor the odd pixel, but the average
  of both.

  Example: A fine vertical grid with alternating vertical white and black
  lines would display as a 50% gray image, as the alternating white and
  black columns would be averaged into the average of white and black,
  which is 50% gray.


\* 'EnableDualPipeHDROutput' Enable EXPERIMENTAL high-performance driver
  for HDR display devices which are composites of two separate displays.

  EXPERIMENTAL proof-of-concept code with no real function yet!

  This is meant for high-precision luminance or color output. It implies
  use of 32 bpc floating point framebuffers unless otherwise specified by
  other calls to PsychImaging().

  The pair of specially encoded output images that are derived from
  content of the onscreen window shall be output to both, the display
  associated with the screen given to PsychImaging('OpenWindow',...); and
  on the screen with the index 'pipe1Screen', using appropriate encoding
  to drive the HDR device or similar composite device.

  Usage: PsychImaging('AddTask', 'General', 'EnableDualPipeHDROutput', pipe1Screen [, pipe1Rectangle]);

  Optionally you can pass a 'pipe1Rectangle' if the window with the
  pipe1 image shall not fill the whole 'pipe1Screen', but only a
  subregion 'pipe1Rectangle'.


\* 'AddOffsetToImage' Add a constant color- or intensity offset to the
  drawn image, prior to all following image processing and post
  processing operations:
  Outimage(x,y) = Inimage(x,y) + Offset. If the framebuffer is in a color
  display mode, the same offset will be added to all three color
  channels.

  Usage: PsychImaging('AddTask', whichView, 'AddOffsetToImage', Offset);
  Example: PsychImaging('AddTask', 'AllViews', 'AddOffsetToImage', 0.5);


\* 'MirrorDisplayTo2ndOutputHead' Mirror the content of the onscreen
  window to given 2nd screen, ie., to a 2nd output connector (head)
  of a dualhead graphics card. This should give the same result as if one
  switches the graphics card into "Mirror mode" or "Clone mode" via the
  display settings panel of your operating system. Use of the "Mirror
  Mode" or "Clone Mode" of your operating system and graphics card is
  preferable to use of this command, if that works for you. The OS
  builtin facilities are usually faster, more efficient and thereby
  more reliable wrt. timing and synchronization!

  This function only works for monoscopic displays, ie., it can not be
  used simultaneously with any stereo display mode. The reason is that it
  internally uses stereomode 10 with a few modifications to get its job
  done, so obviously neither mode 10 nor any other mode can be used
  without interference.

  Only use this function for mirroring onto the 2nd head of a dual-head
  graphics card under MacOS/X, or if you need to mirror onto a 2nd head
  on MS-Windows and can't use "desktop spanning" mode on Windows to
  achieve dual display output. If possible on your setup and OS, rather use
  'MirrorDisplayToSingleSplitWindow' (see below). That mode should work
  well on dual-head graphics cards on MS-Windows or GNU/Linux, as well as
  in conjunction with a hardware display splitter attached to a single
  head on any operating system. It has the advantage of consuming less
  memory and compute ressources, so it is potentially faster or provides
  a more reliable overall timing.

  Usage: PsychImaging('AddTask', 'General', 'MirrorDisplayTo2ndOutputHead', mirrorScreen [, mirrorRectangle]);

  The content of the onscreen window shall be shown not only on the
  display associated with the screen given to PsychImaging('OpenWindow',
  ...); but also (as a copy) on the screen with the index 'mirrorScreen'.

  Optionally you can pass a 'mirrorRectangle' if the window with the
  mirror image shall not fill the whole 'mirrorScreen', but only a
  subregion 'mirrorRectangle'.


\* 'MirrorDisplayToSingleSplitWindow' Mirror the content of the onscreen
  window to the right half of the desktop (if desktop spanning on a
  dual-display setup is enabled) or the right-half of the virtual screen
  if a display splitter (e.g., Matrox Dualhead2Go (TM)) is attached to a
  single head of a graphics card. This should give the same result as if one
  switches the graphics card into "Mirror mode" or "Clone mode" via the
  display settings panel of your operating system. Use of the "Mirror
  Mode" or "Clone Mode" of your operating system and graphics card is
  preferable to use of this command, if that works for you. The OS
  builtin facilities are usually faster, more efficient and thereby
  more reliable wrt. timing and synchronization!

  Usage: PsychImaging('AddTask', 'General', 'MirrorDisplayToSingleSplitWindow');

  Optionally, you can add the command...
  PsychImaging('AddTask', 'General', 'DontUsePipelineIfPossible');
  ... if you don't intend to use the imaging pipeline for anything else
  than display mirroring. This will allow further optimizations.


\* 'RestrictProcessing' Restrict stimulus processing to a specific subarea
  of the screen. If your visual stimulus only covers a subarea of the
  display screen you can restrict PTB's output processing to that
  subarea. This may save some computation time to allow for higher
  display redraw rates.

  Usage: PsychImaging('AddTask', whichChannel, 'RestrictProcessing', ROI);

  ROI is a rectangle defining the area to process ROI = [left top right bottom];
  E.g., ROI = [400 400 800 800] would only create output pixels in the
  screen area with top-left corner (400,400) and bottom-right corner
  (800, 800).


\* 'FlipHorizontal' and 'FlipVertical' flip your output images
  horizontally (left- and right interchanged) or vertically (upside down).

  Usage: PsychImaging('AddTask', whichChannel, 'FlipHorizontal');
  Usage: PsychImaging('AddTask', whichChannel, 'FlipVertical');

  You can use the RemapMouse() function to correct GetMouse() positions
  for potential geometric distortions introduced by this function.


\* 'GeometryCorrection' Apply some geometric warping operation during
  rendering of the final stimulus image to correct for geometric
  distortion of your physical display device. You need to measure the
  geometric distortion of your display with a suitable calibration
  procedure, then compute an inverse warp transformation to undo this
  distortion, then provide that transformation to this function.

  Usage: PsychImaging('AddTask', whichChannel, 'GeometryCorrection', calibfilename [, debugoutput] [, arg1], [arg2], ...);

  'calibfilename' is the filename of a calibration file which specified
  the type of undistortion to apply. Calibration files can be created by
  interactive calibration procedures. See 'help CreateDisplayWarp' for a
  list of calibration methods. One of the supported procedures is, e.g.,
  "DisplayUndistortionBezier", read "help DisplayUndistortionBezier". The
  recommended method for most cases is 'DisplayUndistortionBVL', read
  "help DisplayUndistortionBVL" for help.

  The optional flag 'debugoutput' if set to non-zero value will trigger
  some debug output about the calibration with some calibration methods.

  The optional 'arg1', 'arg2', ..., are optional parameters whose
  meaning depends on the calibration method in use.

  Use of geometry correction will break the 1:1 correspondence between
  framebuffer pixel locations (x,y) and the mouse cursor position, ie. a
  mouse cursor positioned at display position (x,y) will be no longer
  pointing to framebuffer pixel (x,y). If you want to know which
  pixel in your original stimulus image corresponds to a specific
  physical display pixel (or mouse cursor position), use the function
  RemapMouse() to perform the neccessary coordinate transformation.


\* More actions will be supported in the future. If you can think of an
  action of common interest not yet supported by this framework, please
  file a feature request on our Wiki (Mainpage -> Feature Requests).


After adding all wanted task specifications and other requirements,
call...

[windowPtr, windowRect] = PsychImaging('OpenWindow', screenid, [backgroundcolor], ....);

- Finishes the setup phase for imaging pipeline, creates a suitable onscreen
window and performs all remaining configuration steps. After this
command, your onscreen window will be ready for drawing and display of
stimuli. All specified imaging operations will get automatically applied
to your stimulus before stimulus onset.


After the window has been opened you can call the following commands any
time at runtime:

PsychImaging('RestrictProcessingToROI', window, whichChannel, ROI);
- Restrict the processing area of viewChannel 'whichChannel' of onscreen
window 'window' to the rectangular subarea defined by 'ROI'. See the
explanation above for subtask 'RestrictProcessing'. This does exactly the
same but allows a dynamic change of the restricted area at any point
during your experiment script.


PsychImaging('UnrestrictProcessing', window, whichChannel);
- Remove a restriction of the processing area of viewChannel
'whichChannel' of onscreen window 'window' to a previously defined
subarea. Can be called anytime during your scripts execution.


[overlaywin, overlaywinRect] = PsychImaging('GetOverlayWindow', win);
- Will return the handle to the 'overlaywin'dow associated with the
given 'win'dow, if any. Will abort with an error message if the 'win'dow
doesn't have an associated overylay window.
Currently, only the CRS Bits+ box in Mono++ mode and the VPixx DataPixx
box in M16 mode does support overlays. Other output drivers don't support
such a feature. See "help BitsPlusPlus" for subfunction
'GetOverlayWindow' for more explanations of the purpose and properties of
overlay windows. The explanations apply to the DPixx device as well if it
is opened in videomode 'M16WithOverlay'.



# The following commands are only for specialists:

[imagingMode, needStereomode] = PsychImaging('FinalizeConfiguration');
- Finish the configuration phase for this window. This will compute an
optimal configuration for all stages of the pipeline, but won't apply it
yet. You'll have to call [Screen](/docs/Screen)('OpenWindow', windowPtr, ......,
imagingMode, ...); with the returned 'imagingMode' + any other options
you'd like to have for your window. After that, you'll have to call
PsychImaging('PostConfiguration') to really apply and setup all your
configuration settings. If you don't have unusual needs, you can simplify
these steps by simply calling PsychImaging('OpenWindow', ....);
with the same parameters that you'd pass to [Screen](/docs/Screen)('OpenWindow', ....);
PsychImaging will perform all necessary steps to upon return, you'll have
your window properly configured.


PsychImaging('PostConfiguration', windowPtr [, clearcolor]);
- To be called after opening the onscreen window 'windowPtr'.
Performs all the setup work to be done after the window was created.




<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychGLImageProcessing/PsychImaging.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychGLImageProcessing/PsychImaging.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychGLImageProcessing/PsychImaging.m</code>
</div>
