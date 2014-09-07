---
layout: mfile
title: SetupPsychtoolbox
categories:
  - .
encoding: UTF-8
---

SetupPsychtoolbox - In-place setup of PTB without network access.

This script prepares an already downloaded working copy of Psychtoolbox
for use with Matlab or Octave. It sets proper paths, performs online
registration if connected to a network and takes care of special setup
operations for the Java based GetChar implementation.

This setup routine is meant for people who want to install Psychtoolbox
but don't have direct access to the internet. Installation in that case
is a three step procedure:

1\. Download and unpack a full working copy of PTB into your target
folder. Obviously you need to somehow get a copy, either via conventional
download from a computer with network connection (See 'help
DownloadPsychtoolbox' or 'help UpdatePsychtoolbox') or from a helpful
colleague.

2\. Change your Matlab/Octave working directory to the Psychtoolbox installation
folder, e.g., 'cd /Applications/Psychtoolbox'.

3\. Type 'SetupPsychtoolbox' to run this script.

Please be aware that the recommended method of installation is via the
online Subversion system, i.e., DownloadPsychtoolbox and
UpdatePsychtoolbox. Some functionality may not work with a copy that is
set up via this script, e.g., PsychtoolboxVersion may provide incomplete
version information. Convenient upgrades via UpdatePsychtoolbox may be
impossible. Download size with this method is much higher as well.

If you get stuck, post your question to the forum by email or web:
<mailto:psychtoolbox@yahoogroups.com>
<http://groups.yahoo.com/group/psychtoolbox/messages/>
<http://groups.yahoo.com/group/psychtoolbox/post/>
Please specify your full name and the version of your operating system,
MATLAB or Octave and Psychtoolbox.



<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./SetupPsychtoolbox.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./SetupPsychtoolbox.m">changelog</a></span>
</div>
<div class="code">
  <code>./SetupPsychtoolbox.m</code>
</div>
