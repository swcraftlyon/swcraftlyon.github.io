---
title: "Coding Dojo Jeudi 10 Avril 2025"
date: 2025-04-10T19:00:00+01:00
tags: ["dojo"]
---

- Sujet : [Jeu de Nim](https://codingdojo.org/kata/Nim/)
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/306811435/)
- Format : Mob
- Langages : TS
- Nombre de participants : 8

## Rappel du sujet

Le kata propose d'implémenter un [jeu de Nim](https://fr.wikipedia.org/wiki/Jeux_de_Nim).
Une fois le jeu de base implémenté, le mob a appliqué des contraintes au design initial : immuabilité, ne plus pouvoir prendre des bâtonnets quand le jeu est terminé, ne pas pouvoir demander le gagnant si le jeu n'est pas fini.

## Déroulement

Session réalisée en mob sur Discord.
Le driver code en TypeScript.

## Rétrospective

* Session très fun.
* La dernière mise en œuvre, avec les classes `Nim10`, `Nim9`, `Nim8`, etc. chaînées ont permis de concevoir un système cohérent en compile-time : la réflexion n'est pas bête !
* Très marrant, arrivé au moment, quand on a ajouté des trucs piquants. C'était bien cool
* Pas évident de participer, étant arrivé tard.
J'avais déjà réalisé des designs similaires au dernier, notamment pour contrer par le système de types des problématiques de couplage temporel.
* J'ai bien aimé.
Je ne connaissais pas le kata.
On a galéré avec les règles.
La version _Fort Boyard_ est assez cool à implémenter.
Peut-être un peu simple pour un kata du soir, mais c'est aussi ce qui nous a permis de nous amuser.
J'ai bien aimé ce moment où on a pris conscience qu'on ne faisait pas du TDD, et il a fallu revenir aux basiques.
C'est bien de voir ça en dojo, pour prendre le temps d'analyser.

## ROTI

- 3/5 : 2
- 4/5 : 6
