---
title: Invalid — declared points do not match the rubric
lang: en
total_points: 10
spec_version: "0.1"
---

# Invalid — declared points do not match the rubric

## E1 · Solve

```exercise
points: 5
```

<!-- INVALID: the exercise declares points: 5 and the frontmatter declares
     total_points: 10, but the rubric rows below sum to 3. An explicit
     `points:` must match the sum of the rubric rows, and `total_points`
     must match the computed total. -->

Solve in $\mathbb{R}$: $x^2 - 4 = 0$.

> [!solution]
> $x^2 = 4$, hence $x = -2$ or $x = 2$.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | Method stated | 1 |
> | Both roots | 2 |
