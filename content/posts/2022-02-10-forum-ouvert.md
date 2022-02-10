---
title: "Forum Ouvert"
date: 2022-02-10T19:00:00+01:00
tags: ["unconf"]
---

- Sujet: Forum Ouvert
- Meetup: https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/283463415/
- 6-7 personnes

## Sujets

- Comment aider ses experts métier à mieux comprendre le DDD ?/Comment faire que les experts métier sortent des formulaires et nous explique leur vie  ?
- Une UI, plusieurs bounded contexts et plusieurs teams
- Comment gérer le travail d'équipe lorsqu'on est désynchronisés au niveau des horaires ?
- Je manque d'inspi pour mes prochaines lectures
- Comment préparer une conférence ? (pas en tant que speaker mais en tant que participant)
- Comment inculquer une culture craft dans une équipe ? [Nolwenn]

## Session 1 19h20 - 19h45

### Comment préparer une conférence ? (pas en tant que speaker mais en tant que participant)

Porteur du sujet : **Colin**

Plusieurs stratégies pour aborder une conférence :
- cibler des sujets très spécifiques déjà un minimum connu
- aller voir des talks où l'on ne connait pas le sujet, pour découvrir
- Adapter sa "manière" de vivre la conférence à ces besoins / son niveau

Toutes les conférences ne s'abordent pas de la même manière :
- certains plutôt "généralistes" proposent des sujets accessibles à tous sans pré-requis particuliers
- d'autres sont plus spécialisées (type DDD Europe) vont proposer des talks avec des réflexions plus abouties, et nécessites plus de connaissances de base sur ces sujets

"Débuter" dans les conférences (à partir d'une journée) :
- Ne pas forcement chercher a remplir tous les slots
- Le couloir est une vraie salle intéressante (discussion adapté en terme de sujet et de niveau)
- Commencer par des conférences avec un intérêt pratique proche
- Y aller avec des personnes habituées et qui peuvent conseiller des speakers même si ça ferme le "cercle" de connaissances
- Y aller avec l'esprit ouvert VS y aller avec des questions en tête ? -> Questions = intérêt pratique

https://github.com/scraly/developers-conferences-agenda

### Comment inculquer une culture craft dans une équipe ?

Porteur du sujet : **Nolwenn**

**Contexte**: culture craft inexistante, les devs WinDev ont le choix entre changer de techno ou partir.

- (On a replacé ce qu'est la culture craft : https://manifesto.softwarecraftsmanship.org/)
- Parallèle avec l'agilité : comment savoir si on est vraiment agile ?
- Ne pas y aller avec son "bâton de pèlerin" en donnant beaucoup de termes pas compris.
- Partir de kata, aide à comprendre les notions.
- Dans son développement, utiliser des outils du DDD.
- Recentrer plus sur l'équipe (qui construit le logiciel en n'incluant pas seulement les devs).

*Sous question : comment fonctionne la résilience du craft ? Combat permanent ?*

- Nécessite de l'investissement des personnes qui découvrent/entretiennent la démarche.
- Utiliser les points de blocages de l'équipe pour proposer des outils ou méthodes venant du craft.
- Aider à faire prendre conscience que la technique est au service du métier et pas l'inverse.
- Global day of coderetreat : très bien pour apprendre des notions craft, très difficile de convaincre du monde à venir.

## Session 2 19h50 - 20h15

## Une UI, plusieurs bounded contexts et plusieurs teams

Porteur du sujet : **Romain**

Pour une page, on peut avoir plusieurs métiers, avec des données que l'on agrège (ex; une page d'un article sur Amazon).

Si l'on réfléchit sur le cycle de vie et à qui appartient les données qui sont affichées, on se rend compte qu'une organisation "un back-end en face d'un front-end" ne fonctionne pas facilement.

On peut envisager plusieurs solutions :
- un back-end fourni tout, mais doit récupérer (dupliquer) de la donnée pour la restituer, et intégrer de la complexité des autres métiers
- maintenir un service qui maintient des vues en aggrégeant des données des autres contextes
- un back-end for front-end: un seul front servi par un seul back, ce back a pour seul responsabilité de dispatcher les commandes et queries vers les services concernés

Il est intéressant de noter que seul la première solution ne remet pas en question les choix organisationnels des équipes, les autres vont au delà d'une simple décision technique et architecturale.

All our aggregates are wrong (Mauro Servienti) https://youtu.be/KkzvQSuYd5I

Micro Frontend: le casse tête des micro services étendu au FrontEnd ! (Audrey Neveu)
https://youtu.be/f6_99ExOvWs

### Comment aider ses experts métier à mieux comprendre le DDD ? / Comment faire que les experts métier sortent des formulaires et nous explique leur vie ?

Porteurs du sujet : **Adrien** et **Nolwenn**

- Comment faire en sorte que les PO parlent de leurs métier et pas d'écran ?
- Des PO qui ont un niveau acceptable c'est rare, il semble qu'il manque du bon sens.
- Parler directement avec les PO, les aider etc.. (aller en réunion avec eux etc..)
- Il faut parler avec les utilisateurs finaux, pas à un chef de chef etc...
- Les PO attendent que les utilisateurs leurs donnent directement ce qu'il faut faire.
- Il faut écouter ce que l'utilisateur veux, comprendre le besoin rée et lui proposer une solutions pas à la excel.
- Recentrer les besoins utilisateurs pour aller directement sur la valeur qu'attends les utilisateurs.
- Garder la capacité de pouvoir remettre en cause d'où va le projet.
- Le travail d'un développeur n'est pas de transformer une spec en code mais d'aller plus loin avec les experts métiers.
- Il faut prendre de la hauteur pour construire un produit, pas de clicodrome
- "creer" n'est jamais une feature ou une US, il faut prendre plus de recul.

## Session 3 20h20 - 20h45

### Je manque d'inspi pour mes prochaines lectures

Porteur du sujet : **Romain**

https://twitter.com/GeePawHill/status/1489835769334218753

### Comment gérer le travail d'équipe lorsqu'on est désynchronisés au niveau des horaires ?

Porteur du sujet : **Yhuno/Brice Leclerc**

* Livre conseillé : Team topologies https://teamtopologies.com/all-mini-books/mini-book-organization-dynamics-with-team-topologies
  * Ne pas sous estimer la loi de Conway
  * Produire une organisation qui soit à l'image des produits que l'on veut faire
  * Organisation du travail par petites itérations et parallélisées
    * Comment paralléliser ? : Team topologies
* Construire une équipe full remote https://www.youtube.com/watch?v=gSPVP0Bi7qA
* Éviter d'activer les notifications pendant le sommeil
* Deux teams distances qui travaillent ensemble :
  * Solutions
    * Code reviews par un lead dev pour synchroniser les deux équipe (rôle de messager)
    * Arrêter le projet

## Retro

Pas de format depuis longtemps, cool de l'avoir fait, à refaire.

Bon format pour apprendre.

Avant on en faisait beaucoup et on s'essouflait, maintenant on apprécie refaire le format.

Sympa de faire ce format autour du craft plutôt qu'autour du DDD.

## ROTI

- 5/5: 1 personnes
- 4.5/5: 1 personnes
- 4/5: 3 personnes
- 3/5: 1 personnes
- 1/5: 1 personne
