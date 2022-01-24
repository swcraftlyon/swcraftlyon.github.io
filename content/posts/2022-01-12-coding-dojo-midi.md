---
title: "Coding Dojo Mercredi 12 Janvier 2022"
date: 2022-01-12T12:15:00+01:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-12-01-2022/]
---

- Sujet : [Mastermind](https://codingdojo.org/kata/Mastermind/)
- Format : Mob
- Langage : Java
- Nombre de participants : 5

## Déroulement

De nouveau un format mob pour ce kata du midi.
Environnement Java 17, [Infinitest](https://infinitest.github.io/) et TDD ; Colin en [driver](https://martinfowler.com/articles/on-pair-programming.html#DriverAndNavigator) et Nolwenn en time-keeper.

Le but du kata est d'implémenter le rôle du codemaker dans le jeu du [Mastermind](https://fr.wikipedia.org/wiki/Mastermind), qui répond aux propositions du codebreaker par des indications sur l'écart entre la tentative et la combinaison à trouver.

Nous retenons la variante du jeu dont la combinaison repose sur 4 positions, et commençons par un cas test composé de 4 couleurs identiques (le bleu).
Nous implémentons ensuite la méthode `boolean attempt(Color, Color, Color, Color)` pour répondre à ce cas test.
Bien vite nous changeons cette signature pour retourner un `Guess` encapsulant le nombre de couleurs `wellPlaced`.
Nous introduisons `Pin` qui associe une couleur et sa position au sein d'une `Combination` qui remplace avantageusement notre séquence de `Color`.
`Guess` devient `Hint`, améliorant le vocabulaire du domaine.
L'algorithme de détermination des éléments mal placés nous donne du fil à retordre et nous occupe le restant du kata.

## Rétrospective

Le début c'est très bien passé.
Peu de palabre, on a attaqué d'emblée.
Notre travail de découpage était abouti et le design émergent vraiment propre.
En revanche nous n'avons peut-être pas eu les bons réflexes sur la calcul des mal placés, en implémentant trop vite des approches très compliquées.
Peut-être a-t-on voulu aller trop vite ?
Notre nouveau participant s'est bien retrouvé dans la démarche, mais n'étant pas javaiste a un peu décroché lorsque nous avons poussé l'utilisation des streams.
La maîtrise de l'IDE par le driver était agréable pour le mob.

## ROTI

- 5/5 : 2
- 4.5/5 : 1
- 4/5 : 2
