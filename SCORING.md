# Scoring Log

With this repo and [flare-timing](https://github.com/BlockScope/flare-timing)
cloned as siblings the following commands show how to score all tasks at once
for the **Forbes Flatlands Hang Gliding Championships 2015** competition.

```
> ../../bin/extract-input --file=forbes2015.fsdb
Extracted 6 tasks from "Forbes Flatlands Hang Gliding Championships 2015"
Extracting tasks completed in 943.72 ms

> ../../bin/task-length --file=forbes2015.comp-input.yaml
forbes2015.comp-input.yaml
Measuring task lengths completed in 4.10 m

> ../../bin/cross-zone --file=forbes2015.comp-input.yaml
Reading competition from 'forbes2015.comp-input.yaml'
Tracks crossing zones completed in 36.33 s

> ../../bin/tag-zone --file=forbes2015.cross-zone.yaml
Reading zone crossings from 'forbes2015.cross-zone.yaml'
Tagging zones completed in 606.68 ms

> ../../bin/align-time --file=forbes2015.comp-input.yaml
Reading competition from 'forbes2015.comp-input.yaml'
Reading flying time range from 'forbes2015.cross-zone.yaml'
Reading zone tags from 'forbes2015.tag-zone.yaml'
Aligning times completed in 30.54 m

> ../../bin/discard-further --file=forbes2015.comp-input.yaml
Reading competition from 'forbes2015.comp-input.yaml'
Reading task length from 'forbes2015.task-length.yaml'
Reading zone tags from 'forbes2015.tag-zone.yaml'
Filtering times completed in 33.56 s

> ../../bin/mask-track --file=forbes2015.comp-input.yaml
Reading competition from 'forbes2015.comp-input.yaml'
Reading task length from 'forbes2015.task-length.yaml'
Reading flying time range from 'forbes2015.cross-zone.yaml'
Reading zone tags from 'forbes2015.tag-zone.yaml'
Masking tracks completed in 30.51 s

> ../../bin/land-out --file=forbes2015.comp-input.yaml
Reading land outs from 'forbes2015.mask-track.yaml'
Land outs counted for distance difficulty completed in 65.53 ms

> ../../bin/gap-point --file=forbes2015.comp-input.yaml
Reading pilots absent from task from 'forbes2015.comp-input.yaml'
Reading pilots that did not fly from 'forbes2015.cross-zone.yaml'
Reading start and end zone tagging from 'forbes2015.tag-zone.yaml'
Reading masked tracks from 'forbes2015.mask-track.yaml'
Reading distance difficulty from 'forbes2015.land-out.yaml'
Tallying points completed in 721.25 ms
```
