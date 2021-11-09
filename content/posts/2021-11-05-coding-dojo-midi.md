---
title: "Coding Dojo Vendredi 5 Novembre 2021"
date: 2021-11-09T09:05:51+01:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-05-11-2021/]
---
- Sujet : [Battleships Kata](https://katalyst.codurance.com/battleships), un kata sur le thème de la bataille navale
- Format : Mob
- Langage : Java
- Nombre de participants : 4

## Déroulement

Vu le nombre de participants, la décision est rapidement prise de partir sur un format mob. Gautier joue le rôle de [driver](https://martinfowler.com/articles/on-pair-programming.html#DriverAndNavigator) et Nolwenn de gardien du temps.

Nous avons d'abord commencé par implémenter l'affichage de la grille, de façon naïve. Nous avons fondé la validation des tests des étapes ultérieures sur le rendu de grille. Ensuite nous avons codé l'affichage d'un gunship dans le coin supérieur gauche, puis à des coordonnées arbitraires, puis avons généralisé aux autres types de batîments.

## Rétrospective

La solution nous a permis de découvrir quelques API récentes de Java : [Text Blocks]https://docs.oracle.com/en/java/javase/16/text-blocks/index.html, très pratique pour l'affichage de la grille, [Record Classes]https://docs.oracle.com/en/java/javase/16/language/records.html (pour Gunship puis Ship) et [Switch Expressions]https://docs.oracle.com/en/java/javase/16/language/switch-expressions.html.

La démarche a plutôt fonctionné. Les refactorings ont été traités au bon moment. Le code produit est de plutôt bonne qualité. L'utilisation de l'API stream a permis d'obtenir un code concis et lisible.

## ROTI

- 5/5 : 4

