---
title: "Coding dojo Mercredi 15 Juillet 2020"
date: 2020-07-15T14:00:00+02:00
tags: ["dojo"]
---
- Sujet: Kata Panini sur les monoïds de Cyrille Martraire 
- Format: Mob programming
- Meetup: https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/271371158/
- Nombre de participants : 7 participants

## Définition d'un Monoïd :

Un monoïd a trois propriétés :  
 - Composition: a + b = c  
 - Associativié: (a + b) + c = a + (b + c)  
 - Identité (élément neutre): a + identity = a = identity + a 

Exemples :  
- addition   
- multiplication  
- concaténation de chaines, de listes, tableaux  
- pile de goblets, de post-it  
- etc...

Une structure composée uniquement de monoids est elle même un monoïd.

## Retours des participants :

Distinguer l'ingrédient de la portion pour clarifier le fonctionnel.  

On peut avoir un monoïd local (abstractions utile localement), mais on est pas obligé de l'exposer au monde extérieur : Monoïd utile pour obtenir les valeurs nutritionnelles, les compabilités diététiques du panini, mais pas forcément  idéal si on veut poser des règles sur les ingrédients qui doivent le composer (ex: un a toujours un seul pain). 

Elements clairs, faciles à manipuler, facile également d'ajouter de nouveaux éléments.

## ROTI :

- 5/5 -> 1
- 4/5 -> 6
