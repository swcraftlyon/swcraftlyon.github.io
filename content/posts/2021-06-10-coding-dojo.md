---
title: "Coding Dojo Jeudi 10 Juin 2021"
date: 2021-06-21T09:33:44+02:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-10-06-2021/]
---
- Sujet : [Elections kata](https://github.com/SoftwareCraftsmanshipGrenoble/elections)
- Format : Pair
- Langage : Java, Kotlin, TypeScript
- Nombre de participants : 12

## Déroulement

En modifiant son pseudo Discord, chacun a indiqué le langage de programmation qu'il voulait utiliser. Les groupes se sont ensuite construits naturellement.

## Rétrospective

Le kata était assez gros, probablement trop pour une session de ce type.
Il y a vraiment de quoi faire et nous pourrions aisément animer un code retreat avec.
Le kata semble plus conséquent que [Trivia](https://github.com/jbrains/trivia).
Il pourrait décourager les développeurs qui aiment faire aboutir leur travail.

Pour transformer ce code, qui implémente ce qui ressemble à un [scrutin indirect](https://fr.wikipedia.org/wiki/Scrutin_indirect), diverses approches ont été prises.
Certains ont cherché à faire émerger des types pour lutter contre la [Primitive Obsession](https://refactoring.guru/smells/primitive-obsession), d'autres ont focalisé leur attention sur la ségrégation des responsabilités, et comprendre le métier en passant.
Le kata renferme des bugs (s'il y a moins de 3 candidats, si personne ne vote...), que le refactoring permet de faire émerger.
Le groupe TypeScript a questionné l'utilisation de [TSDX](https://tsdx.io/) dans le sujet, car les boucles de feedback sont longues comparées à [Jest](https://jestjs.io/), et conseille de ne surtout pas modifier le jeu de données.
