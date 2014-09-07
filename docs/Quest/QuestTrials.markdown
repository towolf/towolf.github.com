---
layout: mfile
title: QuestTrials
categories:
  - Quest
encoding: UTF-8
---

trial=QuestTrials(q,[binsize])

Return sorted list of intensities and response frequencies.
"binsize", if supplied, will be used to round intensities to nearest multiple of binsize.
Here's how you might use this function to display your results:
        t=QuestTrials(q,0.1);
        fprintf(' intensity     p fit         p    trials\\n');
        disp([t.intensity; QuestP(q,t.intensity-logC); (t.responses(2,:)./sum(t.responses)); sum(t.responses)]');

See Quest.