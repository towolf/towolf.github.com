---
layout: mfile
title: Gamepad
categories:
  - PsychGamepad
encoding: UTF-8
---

result = Gamepad(command [,arg1] [,arg2])

Gamepad reads the state of any USB game controller. Gamepad was
previously named "JoyStick", the name has been changed to agree with the
USB Human Interface Device (HID) terminology.

Gamepad provides built-in help.  For usage, enter "Gamepad" alone on the
command line.

# Performance tips:

As initialization of Gamepad takes significant time, you should call it
once at the beginning of your script before entering the trial loop.
After plugging/unplugging or replugging of any USB devices you \*must\*
call Gamepad('Unplug') or clear all, so Gamepad can recognize the changed
hardware configuration at next invocation. Actually, a clear all is
recommended, as Gamepad('Unplug') doesn't work reliably on non-OSX systems.

The subfunctions for state queries of axis, button and hat state are
optimized for low execution time -- suitable for time critical parts of
your trial loop. All other functions, e.g., for query of the number of
buttons etc. are not optimized, so they shouldn't be called in time
critical parts of your loop.

If you need ultra-fast queries, check the help for 'GetButtonRawMapping',
'GetAxisRawMapping' and 'GetHatRawMapping' for a slightly inconvenient,
but superfast way to query device state.


# LINUX

Gamepad uses the [Screen](/docs/Screen)() mex file and its mouse query functions.
On Linux, gamepads and joysticks are treated as a special type of
mouse/pointing device with multiple extra axes and buttons. If your
GamePad is not recognized, you may need to install the joystick driver,
e.g., via "sudo apt-get install xf86-input-joystick" on a Debian/Ubuntu
system. You may also wish to install a custom joystick configuration file
to customize the mapping and behaviour of buttons and axis, and if the
Joystick also operates as a mouse or not. An example configuration file
with installation instructions is available in the
Psychtoolbox/PsychContributed folder under the name "52-MyLinuxJoystick.conf".

# OSX

GamePad uses the PsychHID function, which provides a universal
interface to USB HID devices, including keyboards.

On OS X Gamepad is an .m file but provides built-in help to match the
behavior of Gamepad on other platforms where it is a mex file.

# WIN

Gamepad is not yet supported on Windows. WinJoystickMex() in the
Psychtoolbox/PsychContributed subfolder may serve as a temporary
replacement.
----

See also: PsychGamepad, PsychHID