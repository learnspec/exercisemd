---
for: ./sequences-midterm.exercise.md
lang: en
license: CC-BY-4.0
spec_version: "0.1"
---

# Midterm — recursive sequences (grading kit)

Companion to `sequences-midterm.exercise.md`. Headings mirror the subject;
statements are not repeated. `merge` recombines the two files into the
canonical form, `split` produces them again — losslessly.

## E1

### a)

> [!solution]
> **Base case.** $u_0 = 10 \leq 15$: the property holds at $n = 0$.
>
> **Inductive step.** Assume $u_n \leq 15$ for some $n$. Then
>
> $$u_{n+1} = 0.8\,u_n + 3 \leq 0.8 \times 15 + 3 = 15$$
>
> **Conclusion.** By induction, $u_n \leq 15$ for every natural number $n$.

> [!expected]
> - All three steps are present and identifiable (base case, inductive
>   step, conclusion).
> - The inductive step starts from the hypothesis and uses the fact that
>   $x \mapsto 0.8x + 3$ is increasing (or bounds directly) — checking a
>   few values numerically does not establish the result.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | Base case | 0.5 |
> | Inductive step carried out from the hypothesis | 1 |
> | Conclusion and structure of the induction | 0.5 |

### b)

> [!answer] $(v_n)$ is geometric with ratio $0.8$ and first term $v_0 = -5$.

> [!solution]
> For every natural number $n$:
>
> $$v_{n+1} = u_{n+1} - 15 = 0.8\,u_n + 3 - 15 = 0.8\,(u_n - 15) = 0.8\,v_n$$
>
> So $(v_n)$ is geometric with ratio $q = 0.8$ and first term
> $v_0 = u_0 - 15 = -5$.

> [!expected]
> - The computation starts from $v_{n+1}$ and reaches $0.8\,v_n$ by
>   explicit factorisation — stating the ratio without computing earns
>   nothing.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | $v_{n+1}$ computed through to $0.8\,v_n$ | 1 |
> | Ratio and first term stated | 0.5 |

### c)

> [!answer] $u_n = 15 - 5 \times 0.8^n$, and $\lim u_n = 15$.

> [!solution]
> Since $(v_n)$ is geometric, $v_n = v_0\,q^n = -5 \times 0.8^n$, hence
>
> $$u_n = v_n + 15 = 15 - 5 \times 0.8^n$$
>
> As $0 < 0.8 < 1$, $\lim_{n\to\infty} 0.8^n = 0$, so
> $\lim_{n\to\infty} u_n = 15$.
>
> **Interpretation.** The sequence approaches 15 without reaching it: 15 is
> the equilibrium value of the modelled process (the fixed point of
> $x \mapsto 0.8x + 3$).

> [!expected]
> - The limit is justified by $|q| < 1$, not merely asserted.
> - The interpretation connects the limit to long-run behaviour.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | Correct explicit expression for $u_n$ | 0.5 |
> | Limit justified by $0 < 0.8 < 1$ | 0.5 |
> | Relevant interpretation | 0.5 |
