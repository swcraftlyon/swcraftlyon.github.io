---
title: "Modular monolith with DDD"
date: 2022-03-15T19:00:00+01:00 
tags: ["dojo"] 
---

- Sujet: Modular monolith with DDD
- Meetup: https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/284219560/
- 30 inscrits / 20ène présents
- Lieu: discord

## Déroulement

Présentation rapide du Kata.  
Colin a proposé 3 pistes:
- Gérer des MeetingLocation online qui n'auront pas les mêmes règles ni les mêmes informations que les offlines;
- Revoir la structure d'un meeting pour représenter les différents états de manière plus explicite;
- Faire un code clinique sur ce repo et peut-être contribuer des évolutions;

6 groupes sont proposés:
- Salle 1 - online meetings: gérer meeting avec remote
- Salle 2 - modélisation état meeting: meeting passé/future même chose => être plus explicite
- Salle 3 - Code cleaning
- Salle 4 - Autre repo "DDD"
- Salle 5 - Autre kata
- Salle 6 - Living doc

3 groupes ont été formés:
- Salle 2 - modélisation état meeting: meeting passé/future même chose => être plus explicite
- Salle 3 - Code cleaning
- Salle 6 - Living doc

## Salles 
### Modélisation état meeting: meeting passé/future même chose => être plus explicite
Le groupe a essayé de modéliser sous forme de machine à état l'aggregate pour représenter chaque étape du cycle de vie de l'aggregate.  
Cela a permet de mettre en évidence qu'un nombre de commandes n'était utile et vraiment disponible uniquement pour certaine étape.  
Le groupe a également exploré la gestion des participants.

### Code cleaning
Exploration du code pour trouver des smells.  
Les aggregates étaient mieux délimités que la soirée précédente avec le framework.  
Les smells semblaient plus au niveau métier, sur la modélisation. Pour cette séance, c'était un peu trop vaste pour explorer cela (README imposant).

### Living documentation
Arthur:
- Expliquer les intentions de l'architecte (niveau de maturité REST, choix des technos, ...)
- Vu d'ensemble de "qu'est-ce que ça fait ?"

Adrien:
- Se retrouver facilement dans le code 
- Architecture
- Grands principes
- Suivre le plus simplement possibles les changements

Colin: 
- Avoir un "rappel" facilement accessible pour les différents "concepts" manipulés, MAIS ne pas avoir une lecture exhaustive lors de l'arrivée sur la code base pour éviter une surcharge mentale inutile

Tools & ideas:
- https://structurizr.com/  
- Annotations de "marquage"  (ex https://gitlab.com/cdamon/vdd/-/blob/main/src/main/java/com/craft/vdd/BusinessContext.java)  
- Build a C4 model using annotations to build a plantuml diagram  
- https://apimundo.com/  
- maat : https://github.com/adamtornhill/code-maat  
- https://promyze.com/fr/  

Convictions: 
- JIRA ça ne peut pas être la doc

## ROTI

- 3/5 : 2
- 4/5 : 4
- 5/5 : 2
