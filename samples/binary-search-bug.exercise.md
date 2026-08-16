---
title: Debugging a binary search
description: A programming exercise where the graded production is a diagnosis, a fix and a test — expectations carry most of the contract.
author: ExerciseMD
lang: en
kind: practice
grade_level: undergraduate
duration: 30
tags: [computer-science, algorithms, debugging]
materials: [computer]
license: CC-BY-4.0
spec_version: "0.1"
---

# Debugging a binary search

## E1 · Find, explain and fix the defect

```exercise
points: 6
time: 30
```

The function below is meant to return the index of `target` in a sorted
list, or `-1` if it is absent. It returns `-1` for some inputs where the
target *is* present.

```python
def search(xs, target):
    lo, hi = 0, len(xs) - 1
    while lo < hi:
        mid = (lo + hi) // 2
        if xs[mid] == target:
            return mid
        if xs[mid] < target:
            lo = mid + 1
        else:
            hi = mid - 1
    return -1
```

### a)

Give a concrete input on which the function is wrong, and state what it
returns versus what it should return.

> [!answer] `search([1, 2], 2)` returns `-1`; it should return `1`.

> [!solution]
> Any input where the target is the last element examined works. With
> `xs = [1, 2]` and `target = 2`: `lo = 0`, `hi = 1`, the loop condition
> `lo < hi` holds, `mid = 0`, `xs[0] = 1 < 2` so `lo = 1`. Now `lo == hi`,
> the loop exits, and the function returns `-1` — but `xs[1] == 2`.
>
> The single-element case `search([5], 5)` fails for the same reason.

> [!expected]
> - The input is **concrete** (actual values), not a description of a
>   family of inputs.
> - Both the observed and the expected return value are stated.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | A concrete failing input | 1 |
> | Observed and expected results both stated | 1 |

### b)

Explain the root cause in one or two sentences.

> [!solution]
> The loop condition `lo < hi` excludes the case where the search interval
> has been narrowed to a single element: when `lo == hi`, that element is
> never compared to the target, so a target sitting at that position is
> reported absent.

> [!expected]
> - The explanation names the **invariant that is violated**: the search
>   interval `[lo, hi]` is inclusive, so the loop must run while
>   `lo <= hi`.
> - "The condition is wrong" or "off-by-one error" without saying *which*
>   case is skipped does not earn the point.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | Root cause identified as the excluded single-element interval | 2 |

### c)

Fix the function, and write one test that fails before your fix and passes
after it.

> [!answer] Change the loop condition to `while lo <= hi:`.

> [!solution]
> ```python
> def search(xs, target):
>     lo, hi = 0, len(xs) - 1
>     while lo <= hi:            # was: lo < hi
>         mid = (lo + hi) // 2
>         if xs[mid] == target:
>             return mid
>         if xs[mid] < target:
>             lo = mid + 1
>         else:
>             hi = mid - 1
>     return -1
>
>
> def test_finds_last_element():
>     assert search([1, 2], 2) == 1
> ```

> [!expected]
> - The fix is **minimal** — rewriting the function in another style is
>   accepted only if it is correct, but the point rewards repairing the
>   identified defect.
> - The test must genuinely fail on the original code: a test on
>   `search([1, 2], 1)` passes before the fix and earns nothing.

> [!rubric]
> | Criterion | Points |
> |---|---|
> | Correct fix | 1 |
> | A test that actually discriminates between the two versions | 1 |
