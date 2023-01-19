---
title: "Coding Dojo Jeudi 19 Janvier 2023"
date: 2023-01-19T19:00:00+01:00
tags: ["dojo"]
aliases: [/posts/coding-dojo-07-12-2022/]
---

- Sujet : [Ohce](https://kata-log.rocks/ohce-kata)
- Meetup : https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/290874741/
- Format : Mob
- Langage : F#
- Nombre de participants : 5

## Rappel du sujet

- Afficher des 'greetings' en espagnol en fonction de l'heure.
- Le but était de pratiquer les mocks/Outside-in..

## Déroulement

- Nous avons commencé avec une fonction prenant heure + nom
- Nous avons introduit un type `Hour` avec les trois moments de la journée (Dia/Tarde/Noche)
  - La question d'avoir un type limité aux 24 heures (soit par enumeration, soit par types dépendants [https://arrow-kt.io/docs/meta/](https://arrow-kt.io/docs/meta/))
  - Nous l'avons écarté car les trois cas répondaient aux requêtes
- Nous avons fait un factory dans le domain qui renvoyait un `Result` (`Either`)
- Ce qui violait la *separation of concerns*
- Nous avons testé spécifiquement la validation

## Rétrospective

- Deux premières participations
- Difficultés d'avoir des instructions clair en tant que driver
- Le driver a trouvé qu'il ne fallait pas expérimenter en mob
  - Les navigateurs ont trouvés intéressant de voir les erreurs qu'ils auraient fait lors de l'aprentissage
- La conception a été fait par composition inside-out, à l'inverse du sujet
- "Le bias du navigateur du départ, est-ce qu'on appel ça le Christophe Collo(mb|n) ?"
- Pas mal de difficultés sur des problèmes techniques qui ont cassées le rythme
- Envis de plus s'axer sur le design (architecture hexagonale)

## ROTI
- 2/5 : 1
- 3/5 : 2
- 4/5 : 2
