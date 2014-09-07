---
layout: mfile
title: DaqAInScanBegin
categories:
  - Daq
encoding: UTF-8
---

params=DaqAInScanBegin(DeviceIndex,options)
Calls DaqAInScan with the options set to only begin, and not continue or
end. You should subsequently call DaqAInScanContinue (as many times as
you like) and, finally, DaqAInScanEnd to get the data. For example:
    options.FirstChannel=FirstChannel;
    options.LastChannel=LastChannel;
    options.count=count;
    options.f=f;
    params=DaqAInScanBegin(DeviceIndex,options);
    for i=1:frames
        % add code here doing something useful
        params=DaqAInScanContinue(DeviceIndex,options);
    end
    params=DaqAInScanContinue(DeviceIndex,options);
    [data,params]=DaqAInScanEnd(DeviceIndex,options);
See also DaqAInScan, DaqAInScanContinue, DaqAInScanEnd,
Daq, DaqPins, DaqTest, PsychHIDTest.