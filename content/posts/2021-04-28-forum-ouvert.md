---
title: "Forum Ouvert x Ministry of testing Lyon"
date: 2021-04-28T19:00:00+01:00
tags: ["unconf"]
---

- Sujet : Forum Ouvert x Ministry of testing Lyon
- Meetup Crafters : https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/277136720
- Meetup Ministry of testing Lyon : https://www.meetup.com/fr-FR/Ministry-of-testing-lyon/events/277140735/

## Déroulé de la soirée

- 3 sessions de présentations en petits groupes
- Définition du programme de la soirée avec les sujets proprosés par les participants
- 3 sessions de discussions entrecoupées de retours rapides
- Retour sur la soirée

## Sujets


### Session 1   19h20 – 19h45
#### Salle 1 :
 -   Quand ne pas tester ? [Nolwenn]
 -   Peut-on tester son application quand on est le seul de notre équipe à vouloir tester ? [Anthony]

 -   Tester un langage descriptif (CSS par exemple) n'est pas utile
 -   Garder une logique de "toujours tester"
 -   Être le seul à tester c'est possible même si ce n'est pas aussi simple que sur les applis testées
 -   Tester au moins manuellement mais jamais "ne pas tester"
 -   Difficile de motiver des gens à faire des tests
 -   Frustrant quand on est le seul à faire du TDD
 -   On ne peut pas imposer à son équipe de faire quelque chose (exemple TDD)
 -   Motiver l'équipe en remontant les défaillances
 -   Idée pour convaincre: la notion de confiance apportée par TDD


#### Salle 3 :
 -   Qu'est-ce qui doit être testé, et à quel niveau ? [Stephan]
 -   Comment intégrer les tests dès la conception ? [Gautier]
 -   Les test de performances, bonne pratiques [Cédric]

#### Salle 4 :
 -   Documentation vivante à base de Gherkins, utile pour les pour les testeurs ? [Romain B]
 -   Comment articuler TDD et test d'acceptation (BDD + Cucumber) [Marc G]

 -   Format Gherkins : documentation exécutable.
 -   Intérêts principaux: provoquer la discussion (cf: 3 amigos), documenter les comportements du code, possibilité de créer une documentation format HTML, avec du texte et des images.
 -   Inconvénients: formalisme parfois lourd, compliqué pour les développeurs (traduction français -> code).
 -   Tips: À utiliser si vraiment des gens pour les lire, sinon rester sur des TU classiques.

#### Salle 5 :
    Quelles informations me sont utiles, de la part des devs pour tester (point de vue testeur) ? OU Quelles informations dois-je fournir aux testeurs (point de vue des devs) ? [François Le Nôtre]

Impliquer les tester en amount facilite la communication et augmente la valeur apporté par les testeurs.
Si ils interviennent en bout de chaine, alors ils sont vu comme un frein et ils ont pas les infos pour bien faire leur travail.

Salle 6 :



### Session 2   19h50 – 20h15
#### Salle 1 :
 -   Les snapshot/approval tests sont-ils compatibles avec TDD ? [Anthony]

 -   Snapshot testing peut aider à trouver des cas lorsqu'on en trouve pas
 -   Peut être utile pour du refacto
 -   Utile pour stabiliser une base de code
 -   Non utile pour le design mais utile pour consolider
 -   Moyen de valider un système, assez incompatible avec TDD au final mais un outil intéressant en compensation.

#### Salle 2 :
 -   Comment prenez-vous en compte la réalité/ les contraintes de l'environnement de Production dans vos développements et  dans vos tests ? [François L]

 -   Environnement de recette quasi iso (matériel un poil moins véloce) pour les machines physiques
 -   Mise en prod avec des scripts testés (démarche de rapprochements des pratiques entre les devs et les ops)


#### Salle 3 :
 -   Quel marche a suivre pour passer de "pas de test" à des tests pertinents et pragmatiques ? [Colin]
 -   Identifier une ou plusieurs personnes dans l'équipe qui ont de l'influence sur la base de code et les convaincre  de passer le pas pour distiller de la connaissance dans l'équipe

 -   Dans certains cas il sera compliqué de convaincre, par exemple lorsque l'ego entre en jeu

 -   Deux démarches envisagées :
   - Mesurer, identifier et corriger de manière incrémentale
   - Montrer un exemple et "embarquer" les personnes qui sont les plus intéressées
#### Salle 4 :
 -   Qui doit écrire les test d'interface (ui) ? Sont-ils vraiment utiles ? [Stephan]

 -   Historiquement les outils étaient compliqués et l'utilisation & la maintenance des tests étaient compliqués, l'expérience utilisateur c'est amélioré au cours des années (à minima pour le web).
 -   Tester pour vérifier un comportement UI ou un test de bout en bout ? -> les deux.
 -   On ne veut pas tout tester de cette manière, uniquement des scénarios clés pour le business.
 -   Tests UI -> développeur
 -   Tests de bout en bout -> développeur & testeur, important que de testeur ait confiance dans le test (pas besoin de le redérouler manuellement)

 -   Présentation sur test-container https://www.youtube.com/watch?v=0TvWv4L_IJM

### Session 3   20h20 – 20h45
#### Salle 1 :
 -   Peut on tester manuellement ? [Colin]

 -   Intéressant pour le test exploratoire
 -   Intérêt du crowd testing (Applause/utest, weAreTesters, ...)
 -   Restrictions technologiques

#### Salle 2 :
 -   Caractériser des bugs et identifier des points chauds sur l'application : des méthodes ? [Romain B]

 -   RUM : real-user-monitoring -> voir les habitudes des utilisateurs, où passent-t-ils ?
 -   APM : application-performance-managment -> trace une action à des transactions, requêtes en BDD

#### Salle 3 :
 -   C'est quoi la Q/qualité ? [Anthony]
 -   https://www.youtube.com/watch?v=9kk_yOATc70

 -   Lié à la maintenabilité (concept plus sonvent compris/concret)

#### Salle 5 :
 -   Comment tester l'asynchrone ? |Gautier]
 -   Comment test les API externes ? [Gautier]

 -   Le fait d'être en asynchrone est une bonne pratique dans le cas où une API externe peut ne pas répondre
 -   Basé sur Kinesis, le but est de testé que les parties du système (producteur/consommateur) peuvent se parler
 -   Le problème est de garantir la cohérence des intéractions entre deux systèmes
 -   Il faut versionner les contrats et assurer que les contrats soit rétrocompatibles
 -   Article sur le pattern Saga : https://www.infoq.com/articles/saga-orchestration-outbox/
 -   Lors de la dépendance sur une API, utiliser des sous-ensemble de l'API et des parsers tolérants


## Retro:
 - Bien passé dans l'ensemble.
 - Trop court ? Pause pas assez marqué ?
 - Bien aimé l'outil Discord pour l'organisation du forum ouvert, bonne fluidité.
 - Pause plus longue pour échanger sur les sessions précédentes ?
 - Les sessions allaient vite
 - Beaucoup d'échanges et des valeurs communes dev/testeurs
 - Retours mitigés (sessions trop courtes, pas assez de temps entre les sessions)
 - Proposition : 35 minutes de sessions / 10 de retours

## ROTI

 - 3/5 : 2
 - 4/5 : 11
 - 5/5 : 2
