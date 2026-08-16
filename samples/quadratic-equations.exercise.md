---
title: Quadratic equations — practice sheet
description: Three graded tasks on solving and modelling with quadratics. Hints, worked solutions and an additive rubric.
author: ExerciseMD
lang: en
kind: worksheet
grade_level: grade 10
duration: 40
tags: [mathematics, algebra, quadratics]
license: CC-BY-4.0
spec_version: "0.1"
---

# Quadratic equations — practice sheet

## E1 · Solving directly

```exercise
difficulty: easy
time: 10
```

Solve the following equations in $\mathbb{R}$.

### a)

$x^2 - 5x + 6 = 0$

> [!hint]
> Compute the discriminant $\Delta = b^2 - 4ac$.

> [!answer] $x_1 = 2$ and $x_2 = 3$

> [!solution]
> $\Delta = (-5)^2 - 4 \times 1 \times 6 = 1 > 0$, so there are two real
> roots:
>
> $$x = \frac{5 \pm 1}{2} \quad\Rightarrow\quad x_1 = 2,\ x_2 = 3$$

> [!rubric]
> | Criterion | Points |
> |---|---|
> | Discriminant computed correctly | 1 |
> | Both exact roots | 1 |

### b)

$2x^2 + 4x + 5 = 0$

> [!hint]
> What does the sign of $\Delta$ tell you?

> [!answer] No real solution.

> [!solution]
> $\Delta = 16 - 40 = -24 < 0$, so the equation has **no real solution**.
> Concluding from the sign of $\Delta$ is enough — no further work is
> required.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | Discriminant computed correctly | 1 |
> | Conclusion justified by the sign of $\Delta$ | 1 |

## E2 · Modelling

```exercise
difficulty: medium
time: 25
```

A gardener has 20 m of fencing to enclose a rectangular vegetable patch
against a wall. The wall forms one of the four sides, so that side needs no
fencing.

### a)

Writing $x$ for the width of the patch (the sides perpendicular to the
wall), express the area $A(x)$ as a function of $x$ and state its domain.

> [!hint]
> How many sides consume fencing? Express the length in terms of $x$ first.

> [!answer] $A(x) = x(20 - 2x)$ for $x \in\, ]0\,;10[$

> [!solution]
> The fencing covers two widths and one length: $2x + L = 20$, so
> $L = 20 - 2x$ and
>
> $$A(x) = x(20 - 2x) = 20x - 2x^2$$
>
> Constraints: $x > 0$ and $L > 0 \Leftrightarrow x < 10$, hence
> $x \in\, ]0\,;10[$.

> [!expected]
> - The set-up starts from an explicit fencing budget (two widths, one
>   length); a labelled sketch counts as justification.
> - The domain is *justified* by both positivity constraints, not merely
>   asserted.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | Fencing budget stated and length expressed in terms of $x$ | 1 |
> | Correct expression for $A(x)$ | 1 |
> | Domain justified | 1 |

### b)

Determine the dimensions that maximise the area, and the value of that
maximum area.

> [!hint]
> $A$ is a quadratic: its extremum is at $x = -\dfrac{b}{2a}$.

> [!answer] Width 5 m, length 10 m, maximum area 50 m²

> [!solution]
> $A(x) = -2x^2 + 20x$ is a downward parabola ($a = -2 < 0$), so its
> maximum is at
>
> $$x = -\frac{20}{2 \times (-2)} = 5$$
>
> giving a width of 5 m, a length $L = 20 - 10 = 10$ m and an area
> $A(5) = 50$ m².
>
> *Alternative valid paths*: vertex form $A(x) = -2(x-5)^2 + 50$, or the
> sign of $A'(x) = -4x + 20$.

> [!expected]
> - Any valid optimisation route is accepted (vertex, vertex form,
>   derivative) provided the **maximality** is justified (sign of $a$, or a
>   variation table).
> - All three final values are stated explicitly, with units.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | A valid optimisation method, carried through | 2 |
> | Maximality justified | 1 |
> | Dimensions and area correct, with units | 1 |
