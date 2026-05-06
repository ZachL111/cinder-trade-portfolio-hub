# Review Journal

The cases below are the review handles I would use before changing the implementation.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its trading systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `spread pressure`, score 155, lane `ship`
- `stress`: `fill risk`, score 188, lane `ship`
- `edge`: `portfolio drift`, score 193, lane `ship`
- `recovery`: `quote width`, score 220, lane `ship`
- `stale`: `spread pressure`, score 150, lane `ship`

## Note

A future change should add new cases before it changes the scoring rule.
