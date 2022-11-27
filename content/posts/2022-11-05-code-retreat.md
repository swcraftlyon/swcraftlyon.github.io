---
title: "Code Retreat 05 Novembre 2022"
date: 2022-11-05T09:00:00+01:00
tags: ["code-retreat"]
---

- Sujet : Falcon CO2
- Meetup : https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/288442752/
- 44 inscrit·e·s

## Sujet

Le sujet de cette année n'était pas le jeu de la vie.  
Le but était de récupérer le cout de CO2 (et ses équivalents) des lancements des Falcon 9 sur une période donnée.  
La construction et le lancement ont un cout. Et il faut donner l'équivalence par rapport à 1kg de Boeuf et un trajet Paris-New York.  
Suivant la période, il faut y avoir plusieurs lancements, avec le réemploi ou non de la fusée.  
Les données sont récupérables via l'api https://api.spacexdata.com/v5/launches  

## Session 1 (Discovery)

Timming un peu court pour tout faire  
Un peu compliqué de rentrer dans le sujet pour certaines personnes. Un rappel imprimé aurait été une bonne idée  

## Session 2 (Immuable &| Blind Navigator)

Qu'est-ce qui est de la responsabilité du domaine ?  
Le blind navigator c'est compliqué : il faut communiquer.  
Le blind navigator quand tu dis ce que tu veux et pas comment le faire ça marche bien.  
Passage java / TS pas simple.  
Pas été plus loin que la première session.  
Contrainte d'immutabilité pas vraiment une contrainte pour les personnes habituées.  

## Session 3 (TCR &| Object Calisthenics)

Perte de codes (11 personnes)  
Oubli de la contrainte au début puis tout recommencer (Langage RUST)  
TCR + calisthenics compliqué : astuce oublier calisthenics au début puis faire apparaitre dans la phase refactoring  
TCR, discussion avant de coder permet de faire moins de revert  

## Session 4 (Mute &| Ping Pong)

Un peu moins efficace que les autres session et surprise lors de la découverte des tests. Déroutant mais a tester en paiur "classique"  
"On a fait n'importe quoi, on est parti dans le mur tout de suite"  
Les claviers aie aie aie (max, bepo, azerty, ...)  
Problèmes quand le test laissé est faux...  

## Session 5 (Contraintes aléatoires)

C'était très bien, on commence a bien connaitre le kata, on avance bien !  
Les contraintes ont permit la construction d'un kata de refacto...  
La contrainte "no if" n'a pas vraiment eue d'impacts  

## Session 6 (Primitive Obsessions &| Evil TDD)

Chill pour certains (mob java).  
Primitive obsession nous a empêché d'être si méchant que ça sur le Evil TDD.  
Evil pas possible avec les tests de propriétés qu'on a fait dès le départ.  
Le contre mob ils sont partis sur la récupération des données via l'API ce qui était bien au bout de la 6ième itération.  

## Session globale

Double pouce
Le mob pour apprendre le TDD c'est top.  
Pas eu de sessions Ovni cette année (juste un peu de Haskell)  
Nombreux donc pas de difficultés à trouver des gens qui pratiquent le même langage.  
Bonne taille pour ce type d'event.  
Sujet vraiment bien, première itération compliqué mais après assez libre de partir sur du calcul ou vers l'intégration de l'API. Plus concret que du FizzBuzz par exemple.  

## ROTI

- 0/5 : 0
- 1/5 : 1 (sujet pas accroché, rien appris)
- 2/5 : 0
- 3/5 : 2 (débutant donc rame, connaissais déjà le kata et pas de révolutions)
- 4/5 : 14
- 5/5 : 17

L'ensemble des retours des facilitateurs sont également très positifs.

Pistes d'améliorations:
- Proposer des bootstraps pour éviter que certains groupes perdent une itération.

## Comptes-rendus externes

- https://gautier.difolco.dev/2022-11/gdcr-summary/
