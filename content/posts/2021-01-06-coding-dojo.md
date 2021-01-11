---
title: "Coding Dojo du Mercredi 6 janvier 2021"
date: 2021-01-06T19:00:00+01:00
tags: ["dojo"]
---

- Sujet : Movie Rental
- Format : mob programming
- Meetup : https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/275192996/
- Nombre de participants : 8 participants

## Déroulé du kata

 - Quelques refactorings mineurs
 - Extraction de la classe Rental
 - Extraction de l'interface Render et de la classe CliRender
 - Déplacement des switch du priceCode dans Movie (qui devient abstraite et récupère le calcul du prix et des points)
   - L'abstraction est mal placé car *Movie a besoin des Rental
   - "Ça peut avoir un intérêt dans le bounded context de la facturation, mais pas dans celui d'un top des films"
   - Alternativement on aurait pu avoir MovieType

## Les retours en fin de session

 - Le driver a été très navigator
 - Le kata s'est bien passé (on est allé au bout)
 - Le mob s'est bien passé (beaucoup de discussions)
 - Manque d'un protocole de communication
   - Alternativement on aurait pu faire proposition / contre-proposition
   - L'harmonie est venu du driver (qui n'a pas pu être pré-empté à cause de la distance)
 - Tout le monde à joué le jeu

## Roti :
- 4 : 2 personnes
- 4.5 : 1 personne
- 5 : 5 personnes
