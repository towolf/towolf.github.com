---
layout: mfile
title: DaqFind
categories:
  - Daq
encoding: UTF-8
---

Syntax: DeviceIndex = DaqFind

Purpose: To allow various Daq functions to run without explicitly being told
         the index of the daq in PsychHID's enumeration.  Works iff there
         is one device.

History: 12/10/07   mpr   consolidated calls from other code
          1/23/08   mpr   added second attempt option if No daq found

see also DaqDeviceIndex and DaqReset