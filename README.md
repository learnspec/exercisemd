# ExerciseMD

**ExerciseMD** is an open, Markdown-based format for writing exercises — tasks where the learner *produces* work, judged against a model solution, explicit expectations, and a rubric.

An `.exercise.md` file is valid Markdown — readable by humans, versionable in Git, printable as a worksheet. Its contribution is not the statement but the **grading contract**: a rubric whose rows are identified, so a grade can be produced, justified, and contested line by line.

## Quick example

```markdown
# Quadratic equations

## E1 · Solve

Solve in ℝ: $x^2 - 2x - 3 = 0$.

> [!hint]
> Compute the discriminant $\Delta = b^2 - 4ac$.

> [!answer] $x_1 = -1$ and $x_2 = 3$

> [!solution]
> $\Delta = 4 + 12 = 16 > 0$, so there are two real roots:
> $x = \frac{2 \pm 4}{2}$, hence $x_1 = -1$ and $x_2 = 3$.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | Discriminant computed correctly | 1 |
> | Both exact roots | 1 |
```

## Key features

- **The rubric is the contract** — one criterion per point, identified rows (`E1.a-r1`), so grading is auditable and contestable at the grain it was produced
- **Two rubric shapes** — additive (one observable criterion per point) for anything gradable on criteria; levels (profile descriptors with floors) for holistic productions
- **One canonical file** — subject and answer key are *derived* views (`strip` / `merge`), so they can never drift apart
- **Language-neutral markers** — reserved sections are callouts (`[!solution]`, `[!rubric]`…), never natural-language headings: author entirely in your own language
- **Practice and exam from the same file** — hints and worked solutions for training, the same source stripped for an exam paper
- **AI-native** — designed so a model can generate the exercise *and* grade against the rubric reproducibly

## Not a quiz

If the answer can be graded by matching — choices, blanks, pairs, ordering, a short expected answer — it belongs in [QuizMD](https://github.com/learnspec/quizmd). ExerciseMD deliberately defines **no** closed-answer syntax. A mixed exam paper composes both through [TrackMD](https://github.com/learnspec/trackmd).

## Specification

See [SPEC.md](./SPEC.md) for the full format specification.

## Implementations

No public implementation yet — v0.1 is the specification itself.

> Built an implementation? Open a PR to add it here.

## Repository structure

```
exercisemd/
├── SPEC.md              # Full format specification
├── CHANGELOG.md         # Version history
├── samples/             # Example .exercise.md files
├── schema/
│   └── exercisemd.schema.json   # JSON Schema for frontmatter validation
├── tests/
│   ├── valid/           # Files that must parse successfully
│   └── invalid/         # Files that must fail validation
└── CONTRIBUTING.md
```

## Related formats

| Format | Repo |
|---|---|
| LearnMD: instructional content | [learnspec/learnmd](https://github.com/learnspec/learnmd) |
| QuizMD: assessments | [learnspec/quizmd](https://github.com/learnspec/quizmd) |
| FlashMD: flashcards | [learnspec/flashmd](https://github.com/learnspec/flashmd) |
| NuggetMD: micro-learning | [learnspec/nuggetmd](https://github.com/learnspec/nuggetmd) |
| ExerciseMD: exercises with solutions | [learnspec/exercisemd](https://github.com/learnspec/exercisemd) |
| TrackMD: learning paths | [learnspec/trackmd](https://github.com/learnspec/trackmd) |
| CurriculumMD: reference frameworks | [learnspec/curriculummd](https://github.com/learnspec/curriculummd) |
| MediaMD: media catalogue | [learnspec/mediamd](https://github.com/learnspec/mediamd) |
| DiagramMD: diagram syntax | [learnspec/diagrammd](https://github.com/learnspec/diagrammd) |
| AnimMD: step-reveal animations | [learnspec/animmd](https://github.com/learnspec/animmd) |
| GlossaryMD: glossaries | [learnspec/glossarymd](https://github.com/learnspec/glossarymd) |
| BadgeMD: micro-credentials | [learnspec/badgemd](https://github.com/learnspec/badgemd) |
| CertMD: macro-credentials | [learnspec/certmd](https://github.com/learnspec/certmd) |
| ListenMD: speech-only episode scripts | [learnspec/listenmd](https://github.com/learnspec/listenmd) |

## Maintainers

This repository is part of the [LearnSpec](https://learnspec.org) suite, initiated and maintained by [memoneo](https://memoneo.app). Issues and pull requests are welcome.

## License

MIT — see [LICENSE](./LICENSE)
