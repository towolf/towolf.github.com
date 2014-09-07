---
layout: mfile
title: PsychRTBoxDemo
categories:
  - PsychDemos
encoding: UTF-8
---

A demonstration of basic usage and functionality of the RTBox reaction time box.

Usage: PsychRTBoxDemo

This demo shows the basics of using the PsychRTBox function to control
and use the "USTC - RTBox" reaction time box, a response button box for
response collection from subjects with high timing accuracy.

You must have a compatible box attached to one of the USB ports of your
computer and the FTDI Serial-Over-USB drivers must be properly installed
and configured on your machine. Otherwise the demo will fail to start.

Only the most basic operations of the box are demonstrated with the most
basic parameter settings to get you started. Other demos will provide
more detailed introduction into more advanced features.

First the demo tests & shows basic live button queries.
Then a fake reaction time experiment is run for four trials. You have to
press a button on the box in response to a beep sound as fast as possible
and your reaction time is measured. A post-hoc method for retrieving the
timestamps of the button events is shown. This method is fast and
accurate, but only provides results after a session is finished, so
programming may appear a bit awkward to some users.

Then the same reaction time experiment is run again, this time
implementing a different method to retrieve button timestamps "live"
during the experiment session within each trial. This method is also
accurate, but involves a calibration procedure which takes about 0.5
seconds in each trial and therefore slows down the progress of each trial
a bit.

See the "help PsychRTBox" online help of the PsychRTBox driver for
detailed explanation of all commands and more commands.
