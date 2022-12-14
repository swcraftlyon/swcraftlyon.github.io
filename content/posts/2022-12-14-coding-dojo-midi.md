---
title: "Coding Dojo Mercredi 14 Décembre 2022"
date: 2022-12-14T12:15:00+01:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-14-12-2022/]
---

- Sujet : [Nearest Color](https://codingdojo.org/kata/NearestColor/) ; [lien sur Meetup](https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/289884566/)
- Format : Mob
- Langage : TypeScript
- Nombre de participants : 5

## Rappel du sujet

On cherche la couleur la plus proche, exprimée en hexadécimal dans un ensemble contenant les couleurs `rouge`, `vert` et `bleu`.

## Déroulement

La session s'est déroulée en mob.
Anthony était driver.
Nous avons commencé par exprimer les types `Component` et `Color`, puis en faisant du [Test-Driven Development](https://en.wikipedia.org/wiki/Test-driven_development), nous avons commencé à implémenter la fonction `findNearest(Color): Color`.

Au fur et à mesure que les cas tests ont été ajoutés, nous avons eu besoin d'introduire la notion de distance entre ``Component``s.

Nous l'avons d'abord implémentée naïvement en soustrayant le charCode de la lettre représentant le nombre hexadécimal, mais la rupture entre `9` et `A` nous a fait préférer un mapping explicite.

Une fois la distance exprimée pour un `Component` il restait à sommer la distance pour les 3 ``Component``s composant une couleur, puis à exploiter cette distance entre 2 couleurs pour déterminer meilleure proximité.

## Rétrospective

- Un kata pas si simple, qui offre des approches différentes.
Le kata ne guide pas assez pour découvrir la notion de distance (mais l'auteur va y remédier).
Le kata force à découper.
- Un des participants a éprouvé des difficultés à suivre.
- Un kata très agréable, chouette de guider dans une langage (TS) différent de celui utilisé au quotidien (Python ou Java).
- Il manquait la dernière méthode et des refactorings.
C'est très agréable de voir d'autres gens travailler, ça permet de voir comment ils raisonnent, prenant des directions différentes des nôtres.
Un peu déçu de ne pas aller au bout.
Permet de voir un TDD avec plus rigueur.
- Comme souvent, on n'a pas pu aller au bout du kata, et la tentation de finir se fait au détriment du refactoring, étape clé du cycle Red-Green-Refactor de TDD, c'est dommage que cette étape cruciale soit régulièrement sacrifiée.


## ROTI

On a oublié de demander le ROTI 🙃.
