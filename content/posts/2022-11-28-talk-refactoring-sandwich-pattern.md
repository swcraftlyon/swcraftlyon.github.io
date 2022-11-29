---
title: "Refactoring avec le sandwich pattern par Sepehr Namdar lundi 28 novembre 2022"
date: 2022-11-28T19:00:00+02:00
tags: ["talk", "DDD", "refactoring"]
---

- Sujet : Refactoring avec le sandwich pattern par Sepehr Namdar lundi 28 novembre 2022
- Meetup : https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/289315830/
- 36 spectateurs en moyenne
- Lieu : twitch
- Langage : Java
- Youtube : https://www.youtube.com/watch?v=1zZcXdJJzZU

## Résumé

Travailler avec un code legacy, procédural et sans tests est une tâche quotidienne de beaucoup d’entre nous, développeuses ou développeurs, et ce n’est pas très agréable.
C’est pourquoi dans cette session de live coding nous allons nous intéresser au pattern Sandwich qui pourrait nous aider à refactorer ce genres de codes.

Dans le pattern Sandwich, nous partons d'une classe (généralement un Application Service). Nous identifions où elle utilise un état partagé (généralement à partir d'une base de données). Ensuite, nous poussons ce code à ses extrêmes (haut et bas) entre lesquels nous avons un modèle du domaine immuable avec lequel nous pouvons interagir.

L'idée est de protéger notre code à l'aide d'ApprovalTest et de refactoriser ce code legacy en code centré sur le domaine. Nous utiliserons les bonnes pratiques de développement pour arriver finalement à des services qui correspondent au pattern Sandwich et à des objets du domaine riches et cohérents contenant des comportements métier.
Entre les étapes de Refactoring, nous discuterons de :

 - Comment gérer le couplage temporel
 - Domain Model Pureness Vs.Completeness
 - Quelle est la différence entre un Application Service et un Domain Service ?
 - Le pattern Sandwich nous aide-t-il à créer des Domain Services propres ?

## Déroulement

Après quelques soucis de prise de son en amont du talk, tout s’est bien déroulé. Sepehr a dédié cette présentation à Mshsa Amini. C’est une des victimes de la répression du mouvement de libération des femmes iraniennes.
 
##  Conférencier

### Sepehr Namdar

Habitué des conférences craft et autres (DDD Europe notamment), il a cofondé le meetup DDD Iran. 


## ROTI

- 1/5 : 0
- 2/5 : 0
- 3/5 : 2
  4/5 : 9
- 5/5 : 1
