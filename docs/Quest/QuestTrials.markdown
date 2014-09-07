---
layout: mfile
title: QuestTrials
categories:
  - Quest
---

trial=QuestTrials\(q,\[binsize\]\)

Return sorted list of intensities and response frequencies.
"binsize", if supplied, will be used to round intensities to nearest multiple of binsize.
Here's how you might use this function to display your results:
        t=QuestTrials\(q,0.1\);
        fprintf\(' intensity     p fit         p    trials\\n'\);
        disp\(\[t.intensity; QuestP\(q,t.intensity\-logC\); \(t.responses\(2,:\)./sum\(t.responses\)\); sum\(t.responses\)\]'\);

See Quest.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./Quest/QuestTrials.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./Quest/QuestTrials.m">changelog</a></span>
</div>
<div class="code">
  <code>./Quest/QuestTrials.m</code>
</div>
