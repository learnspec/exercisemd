---
title: Dérivées et variations — feuille d'entraînement
description: Feuille rédigée intégralement en français. Les marqueurs réservés étant des callouts, aucun intitulé de section n'a besoin d'être traduit.
author: ExerciseMD
lang: fr
kind: worksheet
grade_level: première
duration: 45
tags: [mathématiques, analyse, dérivation]
license: CC-BY-4.0
spec_version: "0.1"
---

# Dérivées et variations — feuille d'entraînement

## E1 · Calculs de dérivées

```exercise
difficulty: easy
time: 15
```

Calculer la dérivée des fonctions suivantes sur leur ensemble de
définition.

### a)

$f(x) = 3x^2 - 5x + 2$

> [!answer] $f'(x) = 6x - 5$

> [!solution]
> Dérivée terme à terme : $(3x^2)' = 6x$, $(-5x)' = -5$, et la dérivée de
> la constante est nulle. D'où $f'(x) = 6x - 5$.

> [!rubric]
> | Attendu | Points |
> |---|---|
> | Dérivée exacte | 1 |

### b)

$g(x) = \dfrac{2x - 1}{x + 3}$

> [!hint]
> Formule du quotient : $\left(\dfrac{u}{v}\right)' = \dfrac{u'v - uv'}{v^2}$.

> [!answer] $g'(x) = \dfrac{7}{(x+3)^2}$

> [!solution]
> Avec $u(x) = 2x - 1$ et $v(x) = x + 3$ :
>
> $$g'(x) = \frac{2(x+3) - (2x-1)}{(x+3)^2} = \frac{2x + 6 - 2x + 1}{(x+3)^2}
> = \frac{7}{(x+3)^2}$$
>
> valable sur $\mathbb{R} \setminus \{-3\}$.

> [!expected]
> - La formule du quotient est posée avant d'être appliquée.
> - Le numérateur est développé et simplifié sans erreur de signe.

> [!rubric]
> | Attendu | Points |
> |---|---|
> | Formule du quotient correctement posée | 1 |
> | Numérateur développé sans erreur de signe | 1 |
> | Résultat simplifié | 1 |

## E2 · Étude de variations

```exercise
difficulty: medium
time: 30
```

On considère $h(x) = x^3 - 3x^2 - 9x + 5$ sur $\mathbb{R}$.

### a)

Étudier les variations de $h$ et dresser son tableau de variations.

> [!hint]
> Commence par factoriser $h'(x)$.

> [!solution]
> $h'(x) = 3x^2 - 6x - 9 = 3(x^2 - 2x - 3) = 3(x+1)(x-3)$.
>
> Le trinôme s'annule en $-1$ et $3$, et $3 > 0$ : $h'$ est positive sur
> $]-\infty\,;-1]$, négative sur $[-1\,;3]$, positive sur $[3\,;+\infty[$.
>
> Donc $h$ est croissante, puis décroissante, puis croissante, avec un
> maximum local $h(-1) = 10$ et un minimum local $h(3) = -22$.

> [!expected]
> - Le signe de $h'$ est établi par **factorisation** ou étude du trinôme,
>   pas par des valeurs testées au hasard.
> - Le tableau fait apparaître les deux valeurs critiques et le sens de
>   variation sur les trois intervalles.

> [!rubric]
> | Attendu | Points |
> |---|---|
> | Dérivée correcte et factorisée | 1 |
> | Signe de $h'$ justifié | 1 |
> | Tableau de variations complet et cohérent | 1 |

### b)

En déduire le nombre de solutions de l'équation $h(x) = 0$.

> [!answer] Trois solutions.

> [!solution]
> $h$ est continue et strictement monotone sur chacun des trois
> intervalles. Les extremums locaux valent $h(-1) = 10 > 0$ et
> $h(3) = -22 < 0$, et $h$ tend vers $-\infty$ en $-\infty$ et vers
> $+\infty$ en $+\infty$.
>
> D'après le corollaire du théorème des valeurs intermédiaires, l'équation
> admet exactement **une** solution sur chacun des trois intervalles, soit
> **trois solutions** au total.

> [!expected]
> - Le corollaire du TVI est invoqué avec ses hypothèses : continuité **et**
>   stricte monotonie sur chaque intervalle.
> - Les signes des extremums locaux sont utilisés comme argument.

> [!rubric]
> | Attendu | Points |
> |---|---|
> | Corollaire du TVI cité avec ses hypothèses | 1 |
> | Signes des extremums exploités | 1 |
> | Conclusion : trois solutions | 1 |
