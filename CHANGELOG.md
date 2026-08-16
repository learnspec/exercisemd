# Changelog

All notable changes to the ExerciseMD specification are documented here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
Versioning follows [Semantic Versioning](https://semver.org/).

---

## [0.1.0] — 2026-08-16

### Context
Initial specification. ExerciseMD joins the **LearnSpec** suite as the
format for *exercises* — productions judged against a model solution,
expectations and a rubric — filling the gap left by QuizMD, which covers
match-gradable assessment. Conventions follow the
[Architecture Charter](https://github.com/learnspec/.github/blob/main/profile/README.md).

The draft was written against real, officially graded exam material and
revised as that material broke it; several rules below exist because a
paper could not be expressed, or because a grading experiment produced the
wrong result.

### Added
- File extension `.exercise.md`, with `.solution.md` as the companion
  grading kit
- Exercise / sub-question structure: `## En`, `### x)` with free-form
  labels; **flat compound labels** (`### A.1.b)`) for deep exam papers
- **Statement sections** (`###` heading not ending in `)`) and **context
  nodes** (sub-question carrying no grading callout) — structural nodes
  that carry no points
- Reserved callouts, language-neutral by design: `[!hint]`, `[!answer]`,
  `[!solution]`, `[!expected]`, `[!rubric]`, `[!anchor]`
- Document-level `[!expected]` before the first `## En`, for cross-cutting
  examination instructions
- Grading contract: `[!rubric]` normative, `[!expected]` observable
  criteria, `[!solution]` illustrative — an alternative valid path earns
  full credit
- Identified rubric rows (`E1.a-r1`) and per-row grading semantics, so a
  grade is contestable at the grain it was produced
- **Additive** rubrics (criterion + points) and **levels** rubrics
  (`[!rubric levels]`: profile descriptor + floor score) for holistic
  grading
- `strip` (profiles `solutions` and `exam`) and `merge` / `split`
  operations, with a lossless round-trip requirement
- Frontmatter: `title`, `lang`, `description`, `author`, `tags`, `kind`,
  `duration`, `total_points`, `materials`, `grade_level`, `source`,
  `created`, `updated`, `license`, `spec_version`
- Per-exercise ` ```exercise ` block: `id`, `points`, `difficulty`, `time`,
  `tags`, `bloom`, `materials`
- Validation rules in lenient and strict modes, including a warning when
  closed-answer syntax appears (it belongs in QuizMD)
- **Experimental**: `[!anchor score:N]` calibration copies for levels
  rubrics — designed after benchmarking showed that descriptors alone do
  not calibrate a grader, but not yet evaluated; may change in v0.2

### Notes
- ExerciseMD defines **no** closed-answer syntax. The boundary with QuizMD
  is deliberate: match-gradable → QuizMD, production judged against a
  rubric → ExerciseMD. Justified true/false belongs here, since the points
  are on the justification.
- Mixed exam papers (multiple-choice part + production part) compose
  through [TrackMD](https://github.com/learnspec/trackmd).
