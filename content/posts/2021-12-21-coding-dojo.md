---
title: "Coding Dojo Mardi 21 Décembre 2021"
date: 2021-12-21T19:00:00+01:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-21-12-2021/]
---

- Sujet : [Belote](https://fr.wikipedia.org/wiki/Belote#R%C3%A8gles_du_jeu)
- Format : Mob
- Langage : Java
- Nombre de participants : 6

## Déroulement

Nous décidons de partir sur un format mob. Colin assure le rôle de [driver](https://martinfowler.com/articles/on-pair-programming.html#DriverAndNavigator) et crée un espace de travail Java 17 sous Eclipse avec le plugin [Infinitest](https://infinitest.github.io/).

En TDD, nous commençons par implémenter une méthode `valueOf` qui retourne la valeur d'une carte passée en paramètre.
Progressivement, nous enrichissons l'énumération `Card` avec de nouvelles valeurs, introduisons l'énumération `Suit` et ajoutons un paramètre `trump` à `valueOf` pour représenter la couleur d'atout.
Nous avons ensuite créé `Trick` pour représenter un pli de 4 cartes et en calculer la valeur en points.
Le prochain concept nous a fait beaucoup hésiter.
D'abord appelé `Score`, il sera finalement renommé `Team` et endosse la responsabilité de calculer les points de l'équipe au cours de la partie.

## Rétrospective

Le kata nous a permis de continuer la découverte des récents ajouts à Java, notamment les [Switch Expressions](https://docs.oracle.com/en/java/javase/16/language/switch-expressions.html) et les [Sealed Classes](https://docs.oracle.com/en/java/javase/15/language/sealed-classes-and-interfaces.html).

## ROTI

La session, de même que la belote en tant que kata, a recueilli ce ROTI :

- 5/5 : 1
- 4/5 : 4
- 3/5 : 1
