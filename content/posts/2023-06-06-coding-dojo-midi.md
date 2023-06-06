---
title: "Coding Dojo Mardi 6 Juin 2023"
date: 2022-06-06T12:15:00+01:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-06-06-2023/]
---

- Sujet : Pierre Feuille Ciseaux
- [Meetup](https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/293565557/)
- Format : Mob
- Langage : Java et TypeScript
- Nombre de participants : 8


## Rappel du sujet

Il s’agit d’implémenter les règles du jeu, qui se joue à deux, dont voici un rappel :

- les ciseaux gagnent face à la feuille et perdent contre la pierre ;
- la feuille gagne face à la pierre et perd contre les ciseaux ;
- la pierre gagne face aux ciseaux et perd contre la feuille ;
- il y a match nul quand les deux propositions sont identiques.

S’il vous reste du temps, vous pourrez gérer deux autres cas :

- le puits gagne face à la pierre ou aux ciseaux et perd face à la feuille ou la bombe ;
- la bombe gagne face au puits ou la feuille, perd face aux ciseaux ou la pierre.

## Déroulement

La session s'est déroulée par groupes de 4 : 1 mob TS et 1 mob Java.

## Rétrospective

Format nouveau ou peu pratiqué par certains.
Le mob n'est pas un format évident quand on a la main et qu'on ne sait pas où aller.
La contrainte de tourner strictement toutes les 5 minutes fonctionne bien, par rapport à d'autres formes de mobs, plus anarchiques.
Le groupe TS est parti sur une implémentation à base de [pattern Strategy](https://fr.wikipedia.org/wiki/Strat%C3%A9gie_(patron_de_conception)), proposé par le [driver](https://martinfowler.com/articles/on-pair-programming.html#DriverAndNavigator).
D'autres idées ont pu être exprimées, mais la curiosité de voir ce pattern en situation l'a emportée.
Le groupe Java en revanche, n'a pas été guidé par un intention (au sens pattern) précis, ce qui a pu donner une implémentation verbeuse et/ou fragile.

## ROTI

Pas de ROTI demandé, mais un sentiment général positif.