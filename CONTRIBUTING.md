# Contributing to ExerciseMD

Thank you for your interest in improving the ExerciseMD specification.

## Ways to contribute

### Report an ambiguity or bug in the spec
Open a [GitHub Issue](https://github.com/learnspec/exercisemd/issues) describing:
- The section of the spec that is unclear or incorrect
- Your interpretation and the alternative interpretation
- A concrete `.exercise.md` example that demonstrates the ambiguity

### Propose a new feature
Open an issue with the label `proposal` and describe:
- **Problem** — what use case is not covered by the current spec?
- **Proposed syntax** — a concrete `.exercise.md` example of the new feature
- **Impact on existing files** — is it backward-compatible?
- **Impact on implementations** — what does a parser need to do?
- **Impact on grading** — does it change how a conforming grader awards points?

Proposals are discussed openly. A feature is added to the spec once:
1. There is clear consensus on the syntax
2. At least one implementation has validated it in practice
3. Sample files and tests are provided

### Propose a change to the grading contract
Changes to `[!rubric]`, `[!expected]` or the grading semantics deserve more
than a syntax discussion: they change what a grade *means*. A proposal in
this area should show **evidence** — ideally scored productions graded
against the current rule and the proposed one, so the effect on real
grading is visible rather than argued.

### Add a sample file
Add an `.exercise.md` file to `samples/` that demonstrates a feature or use
case not yet covered. Open a PR with a brief description.

Samples must be **original work** or unambiguously free to redistribute.
Do not contribute exam papers, scoring guidelines, or student scripts that
belong to an examination board or a publisher.

### Add a test case
- `tests/valid/` — files that any conforming parser **must** accept
- `tests/invalid/` — files that any conforming parser **must** reject, with a comment explaining why

Each test file should have a companion `.md` or comment explaining the expected behaviour.

### Add your implementation
Edit `README.md` to add your parser, grader, or tooling to the implementations table.

## Versioning

The spec follows [Semantic Versioning](https://semver.org/):
- **Patch** (0.1.x) — clarifications, typo fixes, no behaviour change
- **Minor** (0.x.0) — new backward-compatible features
- **Major** (x.0.0) — breaking changes (rare, requires strong justification)

Features marked **experimental** in the spec are exempt: they may change or
be removed in a minor release. `[!anchor]` is experimental in v0.1.

## Code of conduct

Be respectful and constructive. This is a technical specification — discussions should focus on the format, not personalities.
