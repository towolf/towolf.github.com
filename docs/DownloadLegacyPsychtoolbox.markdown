---
layout: mfile
title: DownloadLegacyPsychtoolbox
categories:
  - .
encoding: UTF-8
---

DownloadLegacyPsychtoolbox([targetdirectory] [,downloadmethod=0] [,targetRevision][,flavor])

CAUTION: This script is for legacy downloads. Use DownloadPsychtoolbox
for downloads of the current Psychtoolbox 3.0.10 or later. Psychtoolbox
\3.0.9 and earlier are completely unsupported and unmaintained!

This script downloads \*old versions\* of Psychtoolbox-3, specifically
version 3.0.9 or earlier from the Subversion master server at GoogleCode
to your disk, creating your working copy, ready to use as a new toolbox
in your MATLAB/OCTAVE application. Subject to your permission, any old
installation of the Psychtoolbox is first removed. It's a careful
program, checking for all required resources and privileges before it
starts.

CAUTION: Psychtoolbox 3.0.9 and earlier \*will not work\* with 64 bit
versions of Matlab or Octave, except if you use a GNU/Linux system, e.g.,
Debian GNU/Linux or Ubuntu Linux 10.04 or later. The NeuroDebian project
(see http://neuro.debian.net) provides a very convinient installation of
Psychtoolbox for both 32 bit and 64 bit versions of Octave and Matlab via
the regular package management system of your Linux distribution.

On Mac OSX, all parameters are optional. On MS-Windows and GNU/Linux, the
first parameter "targetdirectory" with the path to the installation
target directory is required. The "targetdirectory" name may not contain
any white space, otherwise download will fail with mysterious error
messages!

On OSX, your working copy of the Psychtoolbox will be placed in either
your /Applications or your /Users/Shared folder (depending on permissions
and your preference), or you may specify a 'targetdirectory', as you
prefer.

On Microsoft Windows, you must specify the full path, including
the drive name where Psychtoolbox should be installed, e.g.,
'C:\\MyToolboxes\\'.

The desired flavor of a Psychtoolbox release can be selected via the
optional "flavor" parameter: By default, 'beta' (aka 'current') will be
installed if you don't specify otherwise, as this is almost always the
best possible choice. You can download an old versioned release via a
namestring like 'Psychtoolbox-x.y.z', e.g., 'Psychtoolbox-3.0.7' if you'd
want to download version 3.0.7. This is only useful if you run a very old
operating system or Matlab version that isn't supported by the current
"beta" anymore, so you'd need to stick with an old versioned release.
People that really love trouble can also download the 'unsupported'
flavor. "Unsupported" was formerly known as "stable" but the new name
reflects reality much better and accurately describes the level of support
you can expect from us if you use it and run into any trouble!


Normally your download should just work(TM). The installer knows three
different methods of download and tries all of them if neccessary, ie.,
if the preferred method fails, the 2nd best is tried etc. Should the
installer get stuck for an inappropriate amount of time (More than 5-10
minutes), you can try to abort it and restart it, providing the
additional 'downloadmethod' parameter with a setting of either 0 or 1,
to change the order of tried download methods to prevent the downloader
from getting stuck with a specific method in rare cases. Very
infrequently, the download servers may be overloaded or down for
maintenance, resulting in download failure. In that case, please retry a
few hours later.


The "targetRevision" argument is optional and should be normally omitted.
Normal behaviour is to download the latest revision of Psychtoolbox.
If you provide a specific targetRevision, then this script will
install a copy of Psychtoolbox according to the specified revision.

This is only useful if you experience problems and want
to revert to an earlier known-to-be-good release.

Revisions can be specified by a revision number, a specific date, or by
the special flag 'PREV' which will choose the revision before the
most current one.


INSTALLATION INSTRUCTIONS: The Wiki contains much more up to date
instructions. If in doubt, follow instructions on the Wiki!

\1. If you don't already have it, you must install the Subversion client.
For Mac OSX, download the latest Mac OSX Subversion client from:
<http://metissian.com/projects/macosx/subversion/>
(You can ignore the Subversion README file. If you do read it, you can
skip the instruction to manually add /usr/local/bin to your unix path.
That's tricky to do, and not needed for installation and updates because
we always specify the full path.) Please note that OS/X 10.5 "Leopard"
and later often come already with Subversion preinstalled, so you may
be able to skip step 1.

For Windows, download the Windows Subversion client from:
<http://subversion.tigris.org/files/documents/15/34093/svn-1.4.0-setup.exe>
Install the Subversion client on your machine by double-clicking the
installer and following the instructions. After installation of the
Subversion client, you will need to exit and restart Matlab or Octave, so it
can find the new subversion executable. In many cases it may be
neccessary to even reboot your computer after installation of subversion.
Btw. you should avoid to install the client into a path that contains
blanks/spaces/white-space as this can lead to download failures in some
cases, e.g., 'C:\\Program Files\\...' may be bad because there is a blank
between the "Program" and "Files".

Alternatively, if you don't have the neccessary permissions to install
Subversion into a system folder, you can install Subversion into an
arbitrary folder on your system (excluding ones with blanks in their
path) and then add that folder to your Matlab or Octave path. E.g. you installed
into D:\\MyOwnFolder\\Subversion\\ . Then you can do this:
addpath('D:\\MyOwnFolder\\Subversion\\'). Our installer should find the
client then.

\2. On MacOS/X, to install the Psychtoolbox in the default location
(/Applications or, failing that, /Users/Shared). Just type:

DownloadPsychtoolbox

Our standard option is in the Applications folder, but note that, as with
installation of any software, you'll need administrator privileges. Also
note that if you put the toolbox in the Applications folder, you'll need
to reinstall it when MATLAB / OCTAVE is updated on your machine. If you must
install without access to an administrator, we offer the option of
installing into the /Users/Shared/ folder instead. If you must install
the Psychtoolbox in some other folder, then specify it in the optional
first argument of your call.

On Windows or Linux, provide a pathname, e.g.:
DownloadPsychtoolbox('C:\\MyToolboxes\\');

That's it. Any pre-existing installation of the Psychtoolbox will be
removed (if you approve). The program will then download the latest
Psychtoolbox and update your MATLAB / OCTAVE path and other relevant system settings.

Enjoy! If you're new to this, you might start by typing "help
Psychtoolbox".

P.S. If you get stuck, first check the FAQ section and Download section of
our Wiki at http://www.psychtoolbox.org. If that doesn't help, post your
question to the forum by email or web:

<mailto:psychtoolbox@yahoogroups.com>
<http://groups.yahoo.com/group/psychtoolbox/messages/>
<http://groups.yahoo.com/group/psychtoolbox/post/>

Please specify your full name and the version of your operating system,
MATLAB / OCTAVE, and psychtoolbox.

# UPGRADE INSTRUCTIONS:

To upgrade your copy of Psychtoolbox, at any time, to incorporate the
latest bug fixes, enhancements, and new features, just type:
UpdatePsychtoolbox

UpdatePsychtoolbox cannot change the flavor of your
Psychtoolbox. To change the flavor, run DownloadPsychtoolbox to
completely discard your old installation and get a fresh copy with the
requested flavor.

# PERMISSIONS:

There's a thorny issue with permissions on OS/X. It may not be possible to
install into /Applications (or whatever the targetdirectory is) with the
user's existing privileges. The normal situation on Mac OSX is that a few
users have "administrator" privileges, and many don't. By default,
writing to the /Applications folder requires administrator privileges.

Thus all OSX installers routinely demand an extra authorization (if
needed), asking the user to type in the name and password of an
administrator before proceeding. We haven't yet figured out how to do
that, but we want to offer that option. This conforms to normal
installation of an application under Mac OS X.

DownloadPsychtoolbox creates the Psychtoolbox folder with permissions set
to allow writing by everyone. Our hope is that this will allow updating
(by UpdatePsychtoolbox) without need for administrator privileges.

Some labs that may want to be able to install without access to an
administrator. For them we offer the fall back of installing Psychtoolbox
in /Users/Shared/, instead of /Applications/, because, by default,
/Users/Shared/ is writeable by all users.

# SAVEPATH

Normally all users of MATLAB / OCTAVE use the same path. This path is normally
saved in MATLABROOT/toolbox/local/pathdef.m, where "MATLABROOT" stands
for the result returned by running that function in MATLAB, e.g.
'/Applications/MATLAB.app/Contents/Matlab14.1'. Since pathdef.m is inside
the MATLAB package, which is normally in the Applications folder,
ordinary users (not administrators) cannot write to pathdef.m. They'll
get an error message whenever they try to save the path, e.g. by typing
"savepath". Most users will find this an unacceptable limitation. The
solution is very simple, ask an administrator to use File Get Info to set
the pathdef.m file permissions to allow write by everyone. This needs to
be done only once, after installing MATLAB.
<http://www.mathworks.com/access/helpdesk/help/techdoc/matlab\_env/ws\_pat18.html>




<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./DownloadLegacyPsychtoolbox.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./DownloadLegacyPsychtoolbox.m">changelog</a></span>
</div>
<div class="code">
  <code>./DownloadLegacyPsychtoolbox.m</code>
</div>
