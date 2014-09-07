---
layout: mfile
title: Ask
categories:
  - PsychOneliners
encoding: UTF-8
---

reply = [Ask](/docs/Ask)(window,message,[textColor],[bgColor],[replyFun],[rectAlign1],[rectAlign2],[fontSize=30])

Draw the message, using textColor, right-justified in the upper right of
the window, call reply=eval(replyFun), then erase (by drawing text again
using bgColor) and return. The default "replyFun" is 'GetClicks'. You may
want to use 'GetChar' or 'GetString'.

"rectAlign1" and "rectAlign2", if present, are applied after the above
alignment. The values should be selected from: RectLeft, RectRight,
RectTop, RectBottom. Alternatively you can pass in one of the strings
'left','top','right','bottom','center'.

If you want to align the text to a different rectangular box than the
window, then pass the rectangle defining that box as argument
'rectAlign1', and the wanted alignment as argument 'rectAlign2', e.g.,
if rectAlign1 = [400 300 600 400] and rectAlign2 = 'center', then the
text 'message' would get centered in the box with left-top corner
(400,300) and right-bottom corner (600,400).

"fontSize" is the font size you want text typed in; will restore old
fontsize before returning.

Typical uses:
reply=[Ask](/docs/Ask)(window,'Click when ready.'); % Wait for (multiple) mouse clicks, return number of clicks.
reply=[Ask](/docs/Ask)(window,'What''s your name?',[],[],'GetString'); % Accept keyboard input, but don't show it.
reply=[Ask](/docs/Ask)(window,'Who are you?',[],[],'GetChar',RectLeft,RectTop); % Accept keyboard input, echo it to screen.

See also GetString.