---
layout: mfile
title: PsychTweak
categories:
  - PsychBasic
encoding: UTF-8
---

PsychTweak() - Apply tweaks to various Psychtoolbox parameters.

This function allows to tweak some low-level operating parameters of
Psychtoolbox. Such tweaks often affect all mex files, not only specific
files. You must execute this function before any other Psychtoolbox mex
file is used, otherwise mex files will not pick up consistent settings
and weird things may happen! If in doubt, execute "clear mex" before
executing this function.

Currently the function mostly implements tweaks for MS-Windows to allow
to cope with the brokeness of the system, especially in the domain of
timing and timestamping.


Available subfunctions:
\=======================


PsychTweak('Reset');

-- Reset some, but not all, tweaks to defaults.


PsychTweak('PrepareForVirtualMachine');

-- Tweak some settings so Psychtoolbox can sort of run inside a Virtual
Machine - or at least limp along in a way that is unsuitable for
production use, but good enough for some basic testing & development of
the toolbox itself, or maybe for some simple demos.


PsychTweak('ScreenVerbosity', verbosity);

-- Set initial level of verbosity for [Screen](/docs/Screen)(). This can be overriden via
[Screen](/docs/Screen)('[Preference](/docs/Preference)','Verbosity'). The default verbosity is 3 = Errors,
Warnings and some Info output.


PsychTweak('UseGPUIndex', gpuidx);
-- Use GPU with index 'gpuidx' for low-level access on Linux and OSX,
instead of the automatically chosen GPU. This only works on multi-gpu
systems. Hybrid-Graphics MacBookPro laptops are automatically handled,
so there shouldn't be any need for this manual selection. The manual
selection is needed in classic multi-gpu systems, e.g., MacPros or
PC workstations with multiple powerful GPUs installed. On such systems,
normally the first GPU (index 0) would always be used. This command
allows to override that choice.


Debugging of [GStreamer](/docs/GStreamer) based functions:
---------------------------------------


PsychTweak('GStreamerDebug', debugconfig);

-- Select level of verbosity for [GStreamer](/docs/GStreamer) low-level debug output.
See \<http://docs.gstreamer.com/display/GstSDK/Basic+tutorial+11%3A+Debugging+tools\>
for explanation of debug options.


PsychTweak('GStreamerDumpFilterGraph', targetDirectory);

-- [Ask](/docs/Ask) [GStreamer](/docs/GStreamer) to dump a snapshot of its current media processing
pipeline into a .dot file at each important pipeline state change. These
.dot files can be read by open-source tools like GraphViz and turned into
visualizations of the complete structure and state of the media
processing pipeline. `targetDirectory` must be the full path to an
existing directory where the .dot files should be written to.


PsychTweak('GStreamerPlaybackThreadingMethod', methodId);
-- [Ask](/docs/Ask) [GStreamer](/docs/GStreamer) to use multi-threaded video decoding method 'methodId'
for video playback if multi-threaded video decoding is requested by
user-code. Only some codecs support this. Currently available values are:
1 = Frame-Threading, 2 = Slice-Threading, 3 = 2+1 = Frame and Slice
threading. By default, Frame+Slice threading will be used.


Debugging of USB based functions:
---------------------------------


PsychTweak('LibUSBDebug', verbosity);

-- Select level of verbosity for low-level debug output of USB functions.
This currently sets the debug level of libusb-1.0 based functions, e.g,
PsychHID, PsychKinectCore, some videocapture functions and others.
Possible values: 0 = Silence (default), 1 = Errors, 2 = Errors +
Warnings, 3 = Errors + Warnings + Info messages.


MS-Windows only tweaks:
-----------------------

PsychTweak('BackwardTimejumpTolerance', secs);

-- Allow system clock to report a time that is up to `secs` in the past,
ie., for time to jump backwards, without triggering any clock error
handling. Some broken or deficient computer hardware shows this
misbehaviour and MS-Windows can't cope with it. Normally PTB would
trigger workarounds and error handling, but a small amount of this error
apparently must be tolerated even on the latest generation of processor
hardware to make some systems workable at all under MS-Windows.

By default, PTB tolerates up to 100 nanoseconds aka 1e-7 secs of error.

Some Intel Core i5 / i7 cpu's have been reported to exhibit errors of
multiple microseconds, sometimes up to even over 10 microseconds!


PsychTweak('ForwardTimejumpTolerance', secs);

-- Allow system clock to report a time that is up to `secs` in the future,
ie., for time to jump forward, without triggering any clock error
handling. Some broken or deficient computer hardware shows this
misbehaviour and MS-Windows can't cope with it. Normally PTB would
trigger workarounds and error handling, but a small amount of this error
apparently must be tolerated even on the latest generation of processor
hardware to make some systems workable at all under MS-Windows.

By default, PTB tolerates up to 250 msecs aka 0.25 secs of error, not
because we expect such large errors on a well working system, but because
the detection logic needs to allow some room for fuzzyness to avoid false
alerts on heavily loaded systems.


PsychTweak('ExecuteOnCPUCores', corelist);

-- Restrict execution of timing sensitive Psychtoolbox processing threads
to a subset of logical processor cores on a multi-core / multi-processor
computer. This allows to workaround some bugs in timing hardware, but can
seriously degrade performance and general timing behaviour of
Psychtoolbox under more demanding workloads, so this may either help or
hurt, depending on the system setup and application.
`corelist` must be a vector with the numbers of cores that PTB threads
are allowed to execute on, numbering starts with zero, ie., the 1st
processor core has the number zero.

By default, PTB does not restrict threads on Windows Vista and later, or
on other operating systems than Windows, but restricts all threads to
core zero on Windows XP. The most meaningful use of this parameter is to
either restrict processing to core zero for Windows Vista and later if
you know that this helps, or to allow threads on WindowsXP to execute on
all available cores if you know that your system configuration is not
susceptible to timing bugs in multi-core mode. PTB will normally
automatically switch to single-core operation on any OS if timing bugs
are detected -- it tries to fix itself.


PsychTweak('ClockWorkarounds' [, warning = 1][, lockCores = 1][, lowres = 0][, abort = 0][, defaultlowres = 0]);

-- Define how PTB should behave if it detects clock problems due to
broken or misconfigured hardware. All flags are boolean with 1 = enable,
0 = disable, and all flags are optional with reasonable default settings.

`warning`: 1 = Print critical warning messages to the command window to
warn user about potentially broken timing in its scripts.
This setting is on by default.

`lockCores`: 1 = On first signs of trouble, switch to single processor
operation, locking all processing threads to cpu core zero, then
continue. Many multi-processor related clock bugs can be "fixed" this
way, but performance and execution timing may be seriously impaired if
all threads have to compete for computation time on one single processor
core, while all other cores on a multi-core machine are essentially
unused and idle. See help for `ExecuteOnCPUCores` for more explanation.
This setting is on by default.

`lowres`: 1 = Switch to a low-resolution backup timer if the `lockCores`
workaround is disabled or proven ineffective to solve the problem. The
lowres timer has only +/- 1 msec resolution and this workaround may only
allow you to continue with very simple experiment scripts. Experiment
scripts involving sound via PsychPortAudio + ASIO sound hardware,
Videocapture or Videorecording, and other types of hardware input/output
may fail in weird ways. Even for simple scripts, this may create new
weird timing related problems.
This setting is off by default due to the trouble it can cause.

`abort`: 1 = Abort userscript / session if clock problems can't be fixed
/ worked around sufficiently well via the `lockCores` workaround, ie., if
after enabling the workaround a successive clock error gets detected.
This setting is off by default.

`defaultlowres`: 1 = Use low-res backup timer by default, ignore the
high-precision clock. This may help a script on a broken system to limp
along, but is not recommended for production use, because it has the same
problems as the `lowres` workaround.
This setting is off by default.


History:
 9\.07.2012  mk  Wrote it.
31\.08.2014  mk  Remove 'DisableCVDisplayLink' option, CVDisplayLinks
                are off by default as of PTB 3.0.12 and must be enabled
                by selecting a VBLTimestampingmode \> 0 via [Screen](/docs/Screen)('[Preference](/docs/Preference)'),
                as they are way too unreliable and crash prone.
