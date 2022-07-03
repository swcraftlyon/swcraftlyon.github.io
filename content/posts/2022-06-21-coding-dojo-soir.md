---
title: "Coding Dojo Mardi 21 Juin 2022"
date: 2022-06-21T19:00:00+01:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-21-06-2022/]
---

- Sujet : Pierre Feuille Ciseaux
- Format : Mob
- Langage : TypeScript
- Nombre de participants : 7


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

La session s'est déroulée en mob.
L'utilisation conjointe de Discord et de la plateforme [CodeSandbox](https://codesandbox.io/) a permis de mettre en place une rotation facile des [drivers et navigators](https://martinfowler.com/articles/on-pair-programming.html#DriverAndNavigator).
Nous n'avons implémenté que les règles de gestion relative aux propositions pierre, feuille et ciseaux.

## Rétrospective

Premier mob pour l'un des participants.
CodeSandbox a été très appréciée.
Il nous faudra aussi tester [mob](https://mob.sh/) et [Microsft Visual Studio Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare).
Malgré sa simplicité, nous n'avons pas été au bout du kata. Pour Gautier, le dernier refactoring visant à apporter une fonction `beats` permettant à une proposition de se comparer à une autre, aurait pu attendre l'introduction du puits et de la bombe, pour avoir suffisamment de recul.

## ROTI

- 3/5 : 1
- 4/5 : 5
