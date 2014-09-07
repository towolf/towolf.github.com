---
layout: mfile
title: PsychHIDDAQS
categories:
  - Daq
encoding: UTF-8
---

daqdevs = PsychHIDDAQS -- Enumerate and preprocess HID-DAQ device list.

Used as helper by Daq toolbox functions. Retrieves the USB-HID devices
list from PsychHID, prefilters all DAQ device entries, so they have a
well defined productID, product name string and a somewhat unique
serialNumber -- as far as this is possible. Leaves unsupported (non-DAQ)
device entries alone.

It then caches the preprocessed list to save processing time on
successive calls to the function.
