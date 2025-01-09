---
title: "Coding Dojo Mardi 7 Janvier 2025"
date: 2025-01-07T19:00:00+01:00
tags: ["dojo"]
---

- Sujet : [The Supermarket Receipt Refactoring Kata](https://github.com/emilybache/SupermarketReceipt-Refactoring-Kata)
- [Meetup](https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/305268780/)
- Format : Pair
- Langages : Java, TS, Python...
- Nombre de participants : 12

## Rappel du sujet

Refactoring de code legacy.
Le repository d'Emily Bache propose une base de travail dans de nombreux langages.
La présence d'une dépendance vers [Approval Tests](https://approvaltests.com/) oriente vers la mise en place d'un [Golden Master](https://en.wikipedia.org/wiki/Characterization_test).

## Déroulement

La session s'est déroulée en pair jusqu'à 20h40, suivi de 20 minutes de rétrospective, à travers Discord.
Le sujet peut se dérouler en 2 phases : construction d'un harnais de tests satisfaisant, puis [refactoring](https://en.wikipedia.org/wiki/Code_refactoring).

## Rétrospective

- Contente de faire un kata de refacto pour reprendre l'année.
- C'est bien de faire du refactoring de temps en temps.
J'ai bien aimé parce que le _métier_ est facilement compréhensible, contrairement au kata [bowling](https://codingdojo.org/kata/Bowling/), dont les règles sont peu intuitives, si on en a jamais fait.
- Content d'utiliser Approval Tests et d'aller plus loin qu'un simple [`verify`](https://github.com/approvals/ApprovalTests.Java/blob/master/approvaltests/docs/reference/Verify.md) sur un JSON (avec `verifyAllCombinations` donc).
- On a fait un peu de [mutation testing](https://en.wikipedia.org/wiki/Mutation_testing) à la main et on a vu que de temps en temps on avait des mutants qui apparaissaient.
Quand c'était rouge on rajoutait un test.
- On a fait les tests à la main : 9 tests en tout => on a pu refactorer sans ajouter d'autres tests.
Vérifier la couverture permet d'identifier les tests à rajouter.
On avait un branching coverage et un code coverage de 100 %.
- Bien aimé faire ce kata, bien que je ne l'apprécie pas plus que ça.
C'était assez tranquille : pas de problème, les directions étaient claires.
- Nous n'avons pas regardé les règles du shopping cart (ou le readme du kata) avant de commencer.
Nous serions bien incapables de dire ce qu'il fallait faire, mais avec Approval Tests, nous avons pu guider le travail par l'angle technique.
- Le polymorphisme répond bien au cas de refactoring que l'on rencontre dans ce kata.

Doit-on garder les tests liés au Golden Master ?
Probablement pas, si l'on considère que le test de caractérisation n'établit pas quel est le bon fonctionnement du système, mais bien son comportement actuel.
La priorité est d'attraper les régressions lors du refactoring.
Ces tests donnent un feedback.
Le nommage des tests n'est pas important, puisqu'a priori ils ne seront pas conservés.
On procède de façon _barbare_ pour gagner une compréhension, et affiner.
Sur un projet plus gros, ça peut être plus compliqué.
Approval Tests permet de constituer un gros jeu de données.
C'est un outil pratique quand le use case est déterministe.
Dans un vrai projet, on n'est pas obligés de tout refactorer d'un coup.
On pourrait aussi enregistrer des données en prod pour les utiliser lors des tests.

## ROTI

- 2/5 : 1
- 3/5 : 1
- 4/5 : 6
- 5/5 : 4
