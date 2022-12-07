---
title: "Coding Dojo Mercredi 7 Décembre 2022"
date: 2022-12-07T19:00:00+01:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-07-12-2022/]
---

- Sujet : No Space Left On Device
- Format : Mob
- Langage : Java
- Nombre de participants : 5

## Rappel du sujet

Il s’agit d’implémenter un système de fichiers constitué de dossiers et de fichiers.
La taille d'un dossier est définie comme la somme de taille des fichiers et des dossiers qu'il contient.
Le but est trouver tous les dossiers de taille au plus 100000.

## Déroulement

La session s'est déroulée en mob.
Nolwenn était driver.
Nous avons utilisé le [pattern composite](https://en.wikipedia.org/wiki/Composite_pattern) pour décrire les fichiers et les dossiers.
Nous avons traité le problème de récursivité proposé par le kata, en utilisant des [Record Classes](https://docs.oracle.com/en/java/javase/16/language/records.html), des [Sealed Classes](https://docs.oracle.com/en/java/javase/16/language/sealed-classes-and-interfaces.html) et des streams.
Le [Gist](https://gist.github.com/NolwennD/de3178fb60ad187da503d1ab0759ff47) de notre production.

## Rétrospective

Bonne durée, pas trop simple.
Nous étions le bon nombre pour faire un mob programming.
Certains edge cases et refactoring ont été laissés de côté, mais l'essentiel a été traité.
Nous aurions pu nommer les dossiers et les fichiers pour réduire gagner plus de certitudes sur les dossiers retournés par nos tests.

## ROTI

- 4/5 : 5
