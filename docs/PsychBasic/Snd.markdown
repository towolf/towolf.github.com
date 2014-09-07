---
layout: mfile
title: Snd
categories:
  - PsychBasic
encoding: UTF-8
---

err = [Snd](/docs/Snd)\(command,\[signal\],\[rate\],\[sampleSize\]\)

Old Sound driver for Psychtoolbox. USE OF THIS DRIVER IS DEPRECATED FOR
ALL BUT THE MOST TRIVIAL PURPOSES\!

Have a look at the help for PsychPortAudio \("help PsychPortAudio" and
"help InitializePsychSound"\) for an introduction into the new sound
driver, which is recommended for most purposes.

[Snd](/docs/Snd)\(\) is a rather dumb and primitive wrapper around the PsychPortAudio\(\)
driver. It uses PsychPortAudio's most basic functionality to achieve
"sort of ok" sound playback. The driver is used in high-latency,
low-timing precision mode, so [Snd](/docs/Snd)\(\)'s audio playback timing will likely
be very unreliable.

Alternatively you can create an empty file named '[Snd](/docs/Snd)\_use\_oldstyle.txt' in
the PsychtoolboxConfigDir\(\) folder, ie., \[PsychtoolboxConfigDir '[Snd](/docs/Snd)\_use\_oldstyle.txt'\]
This will enable the old-style implementation of [Snd](/docs/Snd)\(\), which is equally
shoddy and works as follows:

While [Snd](/docs/Snd) used to use a special purpose low level driver on MacOS-9 which
was well suited for cognitive science, [Snd](/docs/Snd) for all other operating
systems \(Windows, MacOS-X, Linux\) just calls into Matlab's Sound\(\)
function which is of varying - but usually pretty poor - quality in most
implementations of Matlab. There are many bugs, latency- and timing
problems associated with the use of [Snd](/docs/Snd).

GNU/OCTAVE: If you don't use the PsychPortAudio based [Snd](/docs/Snd)\(\) functin, then
you must install the optional octave "audio" package from Octave-Forge,
as of Octave 3.0.5, otherwise the required sound\(\) function won't be
available and this function will fail\!


Supported functions:
--------------------

[Snd](/docs/Snd)\('Play', signal \[, rate\]\[, sampleSize\]\) plays a sound.

rate=[Snd](/docs/Snd)\('DefaultRate'\) returns the default sampling rate in Hz, which
currently is 22254.5454545454 Hz on all platforms for the old style sound
implementation, and the default device sampling rate if PsychPortAudio is
used. This default may change in the future, so please either specify a
rate, or use this function to get the default rate. \(This default is
suboptimal on any system except MacOS-9, but kept for backwards
compatibility\!\)

The optional 'sampleSize' argument used with [Snd](/docs/Snd)\('Play'\) is only retained
for backwards compatibility and has no meaning, unless you opt in to use
the old-style implementation on Matlab with some operating systems. - It
is checked for correctness, but other than that it is ignored. Allowable
values are either 8 or 16.

[Snd](/docs/Snd)\('Open'\) opens the channel, which stays open until you call
[Snd](/docs/Snd)\('[Close](/docs/Close)'\). [Snd](/docs/Snd)\('Play',...\) automatically opens the channel if it isn't
already open. In reality 'Open' does nothing in the current
implementation and is silently ignored .

[Snd](/docs/Snd)\('[Close](/docs/Close)'\) immediately stops all sound and closes the channel.

[Snd](/docs/Snd)\('Wait'\) waits until the sound is done playing.

isPlaying=[Snd](/docs/Snd)\('IsPlaying'\) returns true if any sound is playing, and
false \(0\) otherwise.

[Snd](/docs/Snd)\('Quiet'\) stops the sound currently playing and flushes the queue, but
leaves the channel open.

"signal" must be a numeric array of samples.

Your "signal" data should lie between -1 and 1 \(smaller to play more
softly\). If the "signal" array has one row then it's played monaurally,
through both speakers. If it has two rows then it's played in stereo.
\([Snd](/docs/Snd) has no provision for changing which speaker\(s\), or the volume, used
by a named snd resource, so use READSND to get the snd into an array,
and supply the appropriately modified array to [Snd](/docs/Snd).\)

"rate" is the rate \(in Hz\) at which the samples in "signal" should be
played. We suggest you always specify the "rate" parameter. If not
specified, the sample "rate", on all platforms, defaults to OS9's
standard hardware sample rate of 22254.5454545454 Hz. That value is
returned by [Snd](/docs/Snd)\('DefaultRate'\). Other values can be specified.

OSX & WIN: "samplesize". [Snd](/docs/Snd) accepts the sampleSize argument and passes
it to the Matlab SOUND command.  SOUND \(and therefore [Snd](/docs/Snd) also\) obeys the
specified sampleSize value, either 8 or 16, only if it is supported by
your computer hardware.

[Snd](/docs/Snd)\('Play',sin\(0:10000\)\); % play 22 KHz/\(2\*pi\)=3.5 kHz tone
[Snd](/docs/Snd)\('Play',\[sin\(1:20000\) zeros\(1,10000\);zeros\(1,10000\) sin\(1:20000\)\]\); % stereo
[Snd](/docs/Snd)\('Wait'\);                % wait until end of all sounds currently in channel
[Snd](/docs/Snd)\('Quiet'\);               % stop the sound and flush the queue

For most of the commands, the returned value is zero when successful, and
a nonzero error number when [Snd](/docs/Snd) fails.

[Snd](/docs/Snd)\('Play', signal\) takes some time to open the channel, if it isn't
already open, and allocate a snd structure for your sound. This overhead
of the call to [Snd](/docs/Snd), if you call it in the middle of a movie, may be
perceptible as a pause in the movie, which would be bad. However, the
actual playing of the sound, asynchronously, is a background process that
usually has very little overhead. So, even if you want a sound to begin
after the movie starts, you should create a soundtrack for your entire
movie duration \(possibly including long silences\), and call [Snd](/docs/Snd) to set
the sound going before you start your movie. \(Thanks to Liz Ching for
raising the issue.\)

NOTE: We suggest you always specify the "rate" parameter. If not
specified, the sample rate, on all platforms, defaults to OS9's
standard hardware sample rate of 22254.5454545454 Hz. That value is returned
by [Snd](/docs/Snd)\('DefaultRate'\).

See also PsychPortAudio, [Beeper](/docs/Beeper), AUDIOPLAYER, PLAY, MakeBeep, READSND, and WRITESND.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychBasic/Snd.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychBasic/Snd.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychBasic/Snd.m</code>
</div>
