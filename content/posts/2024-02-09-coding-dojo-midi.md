---
title: "Coding Dojo Vendredi 9 février 2024"
date: 2024-02-09T12:15:00+01:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-09-02-2024/]
---

- Sujet : [IceCream Refactoring](https://github.com/emilybache/IceCreamForecasting-Refactoring-Kata)
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/298954212/)
- Format : Mob
- Langage : Java, Python et TypeScript
- Nombre de participants : 20


## Rappel du sujet

Ce kata de refactoring est disponible pour plusieurs langages de programmation. D'après le readme, il s'agit de couvrir par les tests et d'identifier ce qui fait que les fonctions sont difficiles à tester.

## Déroulement

Les 20 participants se sont répartis en 4 groupes.
2 groupes Java, un groupe Python et un groupe TypeScript.

## Rétrospective

Pour le premier groupe Java, le kata est beaucoup trop ambitieux pour un coding dojo du midi.
Les erreurs de design sont trop importantes pour être réglées pendant la durée de la session.
Ce kata serait adapté pour un atelier sur une journée.
Il est imprenable pour une session du midi.

Le Pythonistes ont commencé par bricoler le Scorer, i.e. faire des tests, mettre en place une petite injection pour maîtriser la météo, puis injecter cette dernière.
Lutte âpre avec la technologie et une maîtrise limitée de la météo :-).
La refonte des classes a débloqué la possibilité d'attaquer le reste.

Le groupe TS a essayé de transformer le flux de contrôle (`if`s et `switch`s) en map.
La travail s'est arrếté avec le remplacement de l'enum `IceCream` par une classe.
Un peu de temps a été perdu à chercher pourquoi la couverture du code par les tests n'était pas calculée (les tests en échec l'empêchaient).

Le deuxième groupe Java a suivi la consigne, surchargeant `Scorer#getScore()` avec une méthode `getScore(boolean sunnyDay)` et introduisant en plus du constructeur implicite un constructeur `Scorer(Random random)` permettant dans les tests de mocker Random, afin de rendre déterministes les algorithmes de `Scorer`.
De proche en proche, les classes applicatives sont devenues de plus en plus testables, mais les refactoring sont restés faibles ; le but étant de transformer juste ce qu'il fallait pour garder des tests simples sans altérer la sémantique du code fourni.
Le groupe n'est pas arrivé au terme, mais n'a pas rencontré d'obstacles significatifs pour empêcher la progression.

Le kata n'est pas si facile que ça, surtout pour des débutants.
Beaucoup d'idées différentes ont été confrontées.
Détermination difficile entre ces 2 chemins : conserver le code applicatif ce qui résulte en des tests compliqués, inversement modifier le code applicatif mais sans garantie suffisante par les tests.
Faire des mocks ou non ?

En termes d'approche, dans ce type de situation, est-il plus intéressant de prendre connaissance de toutes les classes et leurs tests ou vaut-il mieux respecter l'énoncé ?
Pour Colin, la première hypothèse est plus fastidieuse, plus longue, trop énergivore.
Explorer par les tests est toujours plus facile et donne de meilleurs résultats.
Il est par contre moins facile de répondre sur le choix du bon type de tests.


## ROTI

- 2/5 : 3
- 3/5 : 11
- 4/5 : 5
- 5/5 : 1