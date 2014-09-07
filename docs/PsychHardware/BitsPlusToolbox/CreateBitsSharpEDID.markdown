---
layout: mfile
title: CreateBitsSharpEDID
categories:
  - BitsPlusToolbox
encoding: UTF-8
---

CreateBitsSharpEDID - Create proper EDID file for connected display for CRS Bits#

Usage: CreateBitsSharpEDID(outputEDID [, inputEDID='MON\_EDID.edid']);

'inputEDID' filename of raw EDID input file.
'outputEDID' filename of to be written processed EDID output file.

The function reads a raw EDID file, marks the EDID as DVI-D display
device, so the computer sends DVI-D data to the Bits#, regardless if the
Bits# is connected to a analog VGA CRT monitor or some DVI-D display.
Then it adds a proper checksum and writes the new EDID file, ready for
use with the Bits#.

The Bits# provides the DDC detected EDID of a connected display in the
Firmware folder under MON\_EDID.edid. It expects a valid EDID file for use
in the EDID folder.
