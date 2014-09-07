---
layout: mfile
title: QuestUpdate
categories:
  - Quest
encoding: UTF-8
---

q=QuestUpdate(q,intensity,response)

Update the struct q to reflect the results of this trial. The historical
records q.intensity and q.response are always updated, but q.pdf is only
updated if q.updatePdf is true. You can always call QuestRecompute to
recreate q.pdf from scratch from the historical record.

See Quest.