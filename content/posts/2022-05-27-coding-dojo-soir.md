---
title: "Coding dojo du soir : Calendly on steroids"
date: 2022-05-27T19:00:00+01:00 
tags: ["dojo"] 
---

- Sujet: Calendly on steroids
- Meetup: https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/285516548/
- 9 inscrits / 11 présents
- Lieu: Discord
- Format: Mob Programming
---

## Sujet
L'objectif est de fournir un système permettant la prise de rendez-vous asynchrone.  
Ainsi, fournissez un système permettant de définir les créneaux disponibles puis un moyen de prendre rendez-vous en respectant les règles suivantes :  
* Deux rendez-vous ne peuvent pas avoir lieu en même temps  
* Il y a plusieurs types de rendez-vous caractérisés par les règles suivantes :  
    * "Intro": durent 15 minutes, ne doivent pas être suivis d'un autre rendez-vous dans les 5 minutes, doivent être pris au moins 12h avant  
    * "Setup": durent 30 minutes, ne doivent pas être suivis d'un autre rendez-vous dans les 15 minutes, doivent être pris au moins 24h avant  
    * "Pair": durent 1h à 2h, ne doivent pas être suivis d'un autre rendez-vous dans les 30 minutes (1h-1h30) ou 1h, ne doivent pas être précédés d'un autre rendez-vous 1h avant, doivent être pris au moins 48h avant, il ne peut y en avoir qu'un par jour  

## Déroulement
### Groupe C#  
Approche très granulaire: uniquement des éléments, puis des heures, puis des durées (introduction du temps).  
Gestion des overlapping: logique de plages de temps.  
Certaines frustrations, des difficultés à engager un développement avant la fin d'une itération (5 minutes).  

### Groupe TypeScript  
Approche fonctionnelle, moins granulaire que celle du groupe en C#.  
Beaucoup de réflexions autour de l'overlapping, mais de grosses refactos opérées.  
Petite frustration de la part du driver, occupe régulièrement ce rôle.  
Des itérations de 5 minutes, plusieurs fois on a stoppé le chronomètre pour prendre le temps d'échanger, d'expliquer, et de s'assurer que tout le monde avait compris. __Bonne habitude à prendre et à généraliser.__  
Attention aussi à l'ordre de passage des personnes (rendre le niveau homogène sur un cycle entier).

## Références  
- Pour la gestion d'intervalles, il existe l'[algèbre des intervalles d'Allen](https://fr.wikipedia.org/wiki/Alg%C3%A8bre_des_intervalles_d%27Allen)
- [Curryfication](https://fr.wikipedia.org/wiki/Curryfication)
- [TDD, Where Did It All Go Wrong (Ian Cooper)](https://youtu.be/EZ05e7EMOLM)

## ROTI

- 5/5 : 2
- 4.5/5 : 1
- 4/5 : 8
