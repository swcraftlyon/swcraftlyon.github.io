---
title: "Coding Dojo mercredi 13 octobre 2021"
date: 2021-10-13T19:00:00+02:00
tags: ["dojo", "kata"]
aliases: [/posts/coding-dojo-13-10-2021/]
---

- Sujet : [Salary slip](https://github.com/sandromancuso/salaryslipkata) ([Version avec update des dépendances par Nolwenn](https://github.com/NolwennD/salaryslipkata))
- Format : Mob programmings
- Meetup: https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/281010233/
- Langage : Java, C#, Python
- Nombre de participants : 14

## Déroulement

Groupes Python & Java:  
Un driver, un seul navigateur qui change toutes les 5 minutes, les autres peuvent poser des questions.  

Groupe C#:
Un driver, tout le monde navigateur en même temps.

## Rétrospective

Travail de compréhension des calculs: nécessite de comprendre les paliers à appliquer pour appliquer les pourcentages.  
Quelques difficultés avec les arrondis.  
Plusieurs approches pour les assertions: tester des strings (rendering) ou uniquement la valeur.  

Groupe Python:  
Grosse problématique au fil des itérations: chaque itération ajoute des propriétés à tester dans les anciens tests.  
Pas de bonne solution trouvée pour ce problème.  
Pour une nouvelle règle, on ajoutait la valeur par défaut dans les anciens tests et faisait compiler, puis on ajoutait le nouveau test avec le comportement.  

Le kata a peut-être un défaut: trop de bruit sur le métier (effort de compréhension important) pour pouvoir pleinement se concentrer sur la technique.  

Gestion des plages:  
Quand on passe à la plage suivante, le montant de la précédente peut être représenté par une valeur constante.  
On peut être tenté de juste calculer la dernière plage et sommer aux constantes des plages précédentes.  
Les calculs sont plus simples mais il peut être plus difficile de d'avoir une vision "big picture" des calculs que l'on réalise.  

## Roti

- 3/5: 1
- 4/5: 10
- 5/5: 3