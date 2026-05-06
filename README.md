# cinder-trade-portfolio-hub

`cinder-trade-portfolio-hub` is a compact Zig repository for trading systems, centered on this goal: Design a Zig verification harness for portfolio systems, covering simulation kernel, seeded input scenarios, and failure-oriented tests.

## Problem It Tries To Make Smaller

This is intentionally local and self-contained so it can be inspected without credentials, services, or seeded history.

## Cinder Trade Portfolio Hub Review Notes

The first comparison I would make is `quote width` against `spread pressure` because it shows where the rule is most opinionated.

## Working Pieces

- `fixtures/domain_review.csv` adds cases for spread pressure and fill risk.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/cinder-trade-portfolio-walkthrough.md` walks through the case spread.
- The Zig code includes a review path for `quote width` and `spread pressure`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Design Notes

The core code exposes a scoring path and the added review layer uses `signal`, `slack`, `drag`, and `confidence`. The domain terms are `spread pressure`, `fill risk`, `portfolio drift`, and `quote width`.

The Zig addition stays small enough to inspect in one sitting.

## Example Run

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Tests

The check exercises the source code and the review fixture. `recovery` is the high score at 220; `stale` is the low score at 150.

## Known Limits

The repository is intentionally scoped to local checks. I would expand it by adding adversarial fixtures before adding features.
