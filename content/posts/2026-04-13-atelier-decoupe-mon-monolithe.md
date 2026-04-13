---
title: "[Distanciel] Atelier Découpe mon monolithe"
date: 2026-04-13T19:00:00+02:00
tags: ["atelier", "ddd"]
---

- Sujet : Découpe mon monolithe
- [Meetup](https://www.meetup.com/fr-fr/software-craftsmanship-lyon/events/314002481/)
- Miro : https://miro.com/app/board/uXjVGjrpCrQ=/
- Format : Atelier
- Animateurs : Florent Pellet
- Lieu : en ligne (distanciel)
- Nombre de participants : entre 16 et 20

## Description

Vous vous dites qu'il faut arrêter de faire du logiciel couplé, arrêter de faire grossir le monolithe. Peut-être même commencer à faire des micro-services indépendants ! sauf que… ces services ne seront peut-être pas si indépendants que ça :(. Ce workshop est conçu pour ceux qui se posent ces questions.

Votre mission lors de cet atelier est de découper un morceau d'un monolithe existant. Embarquez pour un voyage architectural vers les synchronising services et un monde de possibilités s'ouvrira. Vous visiterez le Bubble Context, Sagas, Process manager, Bounded Context, Open Host Service, Compensating Events et Domain Events…

## Déroulement

L'atelier a commencé par une présentation du sujet autour du monde ferroviaire. Le point de départ passait par un schéma de base de données d'un monolithe. L'idée du découpage commençait par savoir quel contexte peut être responsable de quelle donnée.

Première étape : remplir une matrice pour savoir ce qui est en lecture et écriture.

Suite à la première étape, il y a eu une remarque au sujet de CQRS pour voir s'il y avait un rapport avec la matrice.

Une présentation de la notion de Bubble Context a été faite pour expliquer comment aborder un découpage des données en fonction de modules. Plusieurs mécaniques ont étés présentés :

- Bubble Context
- Autonomous Bubble - synchronous
- Autonomous Bubble - events
- Autonomous Bubble - state stream
- Autonomous Bubble - notification stream
- Exposing legacy assets as services

Références :
- Getting Started with DDD When Surrounded by Legacy Systems - Eric Evans https://www.domainlanguage.com/wp-content/uploads/2016/04/GettingStartedWithDDDWhenSurroundedByLegacySystemsV1.pdf
- Should we create a shared kernel ? - Nick Tune https://www.domainlanguage.com/wp-content/uploads/2016/04/GettingStartedWithDDDWhenSurroundedByLegacySystemsV1.pdf

Un cas d'exemple a été donné pour illustrer une façon de découper.

Deuxième étape : choisir un pattern qui fonctionnerait sur la durée.

Une solution possible a ensuite été proposée avant une présentation d'une approche sur la base de donnée.

Dernière étape : faire un exemple de découpage avec deux offres, une ancienne et une nouvelle.

Une solution possible a été proposée avant la rétrospective.

## Rétrospective

- Très intéressant, mais le temps passe vite
- Problème d'accès au Miro
- Peut-être que de partir de la BD dans le dernier exercice n'était pas la bonne solution
- Cool de faire le découpage et d'augmenter la complexité
- Difficile de se lancer sur les étapes

## ROTI

- 2/5 : 1
- 3/5 : 3
- 4/5 : 11
