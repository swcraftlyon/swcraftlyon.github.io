---
title: "Forum Ouvert du Samedi 28 Mars 2026"
date: 2026-03-28T10:00:00+01:00
tags: ["forum-ouvert"]
---
- Sujet : Les limites de nos pratiques
- [Meetup](https://www.meetup.com/fr-fr/software-craftsmanship-lyon/events/313895555/)
- Format : Forum ouvert
- Nombre de participants : 14

## Sessions

### Session 1 : 10h20 - 10h40 
#### Salle 1 :  DDD
- Qu'es ce que ça veux dire faire du DDD ? 
- le DDD est proche d'une philosophie donc pas de vrai ou de faux. 
- Es-ce que c'est un probléme de pratique ou de pratiquant ?
- les framework DDD ? 
- Trop focaliser sur une partie, en oubliant le reste.
- Qu'es ce qu'on met derriére derriére le mot métier / domain ?
- DDD et hors application de gestion ?

#### Salle 2 :  Architecture hexagonale
- Pas adapte aux petits projets (mais c'est des on dit et comment on défini petit projet)
- Ne pas oublier que le CRUD existe pour des cas spécifiques sans (ou avec peu de) logique métier 
- Ralenti le développement sur des domaines avec peu ou pas de règles métiers
- Test fiables pour les implémentation des ports et adaptateurs

#### Salle 3 :  Pair programing / Ensemble programing
- Plus lent que le développement en solo pendant la phase d’homéostasie de l'état de l'art
- Travail en synchrone, problématique pour les workflow décomposés
- Pas compatible avec les horaires différents dans l'équipe
- Pas compatible avec les différences de fonctionnement
- Difficile à faire fonctionner avec le développement assisté par IA
- Peu créer des réactions de frustrations à cause des différences de rythme pendant trop longtemps
- Parfois difficile de formaliser une explication à chaud (idée : formaliser un TODO et on verra après)
- Problèmes d'efficacité quand les différences de niveau sont trop importantes
- Parfois difficile de "bien prendre" les retours en direct
- Sensation d'être jugé  (infantilisant / punitif)

### Session 2 - 10h50 - 11h10

#### Salle 1 :  EventSourcing
* Long à mettre en oeuvre (démarrage)
* Force à structurer les processus, ce qui peut mettre en défaut dans la phase exploratoire
* Peut provoquer un rejet assez massif (e.g. quand on a pas l'habitude)
* Deux philosophies opposées : conserver l'historique à tout prix vs ne garder que les events utiles (réécriture)
* Gestion des événements legacy
* Difficulté à appréhender pour les personnes habituées au développement centrés sur la BDD
* Semble lourd/overengineered si on ne cherche qu'à écrire en base
* Anonymisation/RGPD

#### Salle 2 :  merge request / pull request /code reviews

- Difficulté de relecture sur les MR/PR trop longues : 
      - Difficile de se concentrer sur ce qui doit être relu
      - Création de frustration par le délai
- Les objectifs à prendre en compte ne sont pas partagés par tout le monde, ce qui crée des frustration
- Peut être mal pris quand le code est vu comme une extension de soi-même
- Parfois difficile de détacher la personne du code
- Création de sous ensemble d'états de l'art dans l'équipe
- Peut être difficile de faire une critique (au sens neutre)
- https://blog.codinghorror.com/the-ten-commandments-of-egoless-programming/
- Peut créer un bottleneck et un stock de valeur
- Difficile de revenir sur un sujet démarré il y a potentiellement longtemps

#### Salle 3 :  microservices

* Server less vs micro service vs nano service
* Complexification des interactions entre modules/contextes
* Risque de sécurité dans les interactions entre micro services (multiplie les points d’entrées)
* Ralenti l’exécution fonction vs http call
* Demande plus de compétences (infrastructure) pour les devs
* Monitoring et observabilité plus complexe
* Incohérence des données liées aux transactions entre services
* Tester dans l'infrastructure un nouveau micro service
* Retro compatibilité dans les versions deployees 
* Divergence des standards entre équipes => changement d’équipe plus difficile, interactions entre micro service non triviale
* Architecture plus coûteuse si tous les services ont un trafic similaire
* Obligation de synchronisation de l'ensemble des services lors de modifications avec un impact global sur l'application
* En cas de différentes technos entre micro services, sur des petites équipes, on va demander des profils polyvalents et moins spécialisés.
* Nécessite eco-système Linux uniquement

### Session 3 - 11h20 - 11h40

#### Salle 1 :  Daily meetings

- Fuseaux horaires incompatibles
- Pas de vraie écoute, tout le monde regarde son téléphone
- La durée qui déborde régulièrement
- Souvent pris pour un point de synchro / projet -> peu de valeur
- Début en retard
- Coupure dans la journée
- On attend le daily pour commencer à travailler
- Pratique parfois imposée / subie sans comprendre l'objectif
- Parfois difficile d'expliquer ce qui a été fait
- Exhausteur d'insécurités
- Moment attendu pour demander de l'aide, ce qui arrive souvent trop tard
- "On en parle après le daily"

#### Salle 2 :  TypeDD

* En fonction du langage, plus ou moins de difficultés à exprimer les contraintes
* Trade-off entre limite du langage, compréhension du code et exhaustivité
* Est-ce qu'on essaye pas d'avoir raison du premier coup et donc on se retrouve pas dans des cas de coûts irrécupérables => Design Up-front? => Ça dépend de la démarche mais oui on peut se retrouver en difficulté si on tente de définir l'ensemble des éléments avant de se concentrer sur les fonctions/méthodes
* Avec des personnes qui ont plus l'habitude de se baser sur des tests ou d'autres éléments concrets, l'approche est difficile a justifier.
* Coût supplémentaire pour début en voyant les conversions à faire pour passer d'un type à l'autre
* Vient en opposition avec des structures qui comportent des fonctions avec beaucoup de responsabilités peu être complique de faire le changement de mindset.
* Rajoute de la complexité avec des fonctions de conversion et de guard pour s'assurer qu'une structure respecte le type souhaite.
* Difficulté à mettre en pratique sur des bases de code existantes, mais des données mal formatées/corrompues.
* Gestion des cas d'erreur spécifiques aux règles des types.

#### Salle 3 :  CQRS
Snif j'étais tout seul
    
#### Salle 4 : vertical slices
* Personne

## Rétrospective
* Bien aimé le samedi matin
* Empêche certaines activités +++
* Échanges intéressants
* Exercice intéressant "penser contre soit-même"
* Envis de participer à toutes les sessions en parallèle
* Difficile de faciliter quand on n'aime pas une approche => venir quand on n'aime une approche plus que de venir à faire des reproches

## ROTI

* 3/5 : 1
* 4/5 : 6
* 5/5 : 3
