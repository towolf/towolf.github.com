---
layout: mfile
title: UpdatePsychtoolbox
categories:
  - .
encoding: UTF-8
---

UpdatePsychtoolbox(targetdirectory, targetRevision)

Update your working copy of the Psychtoolbox with the latest bug fixes,
enhancements, and features from the master server.

If you are using a Psychtoolbox provided by NeuroDebian, this is not
needed. You will be automatically notified of updates to Psychtoolbox by
your operating systems update manager as soon as they become available.

The "targetdirectory" argument is optional. If present, it gives the path
of the Psychtoolbox folder to update. If omitted, UpdatePsychtoolbox will
update the Psychtoolbox folder found by Matlab's or Octave's "which"
command. For example:

UpdatePsychtoolbox
UpdatePsychtoolbox('~/Applications/Psychtoobox')

The "targetRevision" argument is optional and should be normally omitted.
Normal behaviour is to upgrade your working copy to the latest revision.
If you provide a specific targetRevision, then this script will
\*downgrade\* your copy of Psychtoolbox to the specified revision. This is
only useful if you experience problems after an update and want to revert
to an earlier known-to-be-good release. Revisions can be specified by a
revision number, a specific date, or by the special flag 'PREV' which
will downgrade to the revision before the most current one. By executing
this script multiple times with the 'PREV' specifier, you can
incrementally downgrade until stuff works for you.

UpdatePsychtoolbox cannot change the beta-vs-stable flavor of your
Psychtoolbox. To change the flavor, run DownloadPsychtoolbox again.
