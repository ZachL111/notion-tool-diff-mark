# Review Journal

The review surface for `notion-tool-diff-mark` is deliberately narrow: one fixture, one scoring rule, and one local check.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its cli tools focus without claiming live deployment or external usage.

## Cases

- `baseline`: `file span`, score 190, lane `ship`
- `stress`: `terminal width`, score 182, lane `ship`
- `edge`: `argument risk`, score 140, lane `ship`
- `recovery`: `report density`, score 178, lane `ship`
- `stale`: `file span`, score 172, lane `ship`

## Note

The useful failure mode here is a wrong decision on a named case, not a vague style disagreement.
