# Cinder Trade Portfolio Hub Walkthrough

I use this file as a small checklist before changing the Zig implementation.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | spread pressure | 155 | ship |
| stress | fill risk | 188 | ship |
| edge | portfolio drift | 193 | ship |
| recovery | quote width | 220 | ship |
| stale | spread pressure | 150 | ship |

Start with `recovery` and `stale`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The useful comparison is `quote width` against `spread pressure`, not the raw score alone.
