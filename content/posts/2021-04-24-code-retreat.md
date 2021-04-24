---
title: "2021 04 24 Code Retreat"
date: 2021-04-24T09:30:00+02:00
tags: ["code-retreat"]
---


- Sujet : [Langton Ant](http://codingdojo.org/kata/LangtonAnt/)
- Format : Pair programming
- Langage : Java, C#, TypeScript
- Nombre de participants : 18

## Objectif

- Améliorer nos pratiques de code

## Déroulement

- Présentation du sujet
- 5 itérations de 40 minutes avec une contrainte différente à chaque itération suivie de 10 minutes de debrief
- Golden master et pair programming à chaque itération

## Itération 1 : Golden master

- Compliqué à mettre en place avec approvaltests

## Itération 2 : Freestyle

- Reprise des tests
- Certains on commencé le refactoring
- Refactorer aide plus à apréhender le code que les tests

## Itération 3 : Babystep 2 minutes

- Compliqué au début
- Pratique de voir émerger le code au fur et à mesure
- Le code semble bien meilleur avec cette contrainte
- Permet de structurer les étapes

## Itération 4 : Ifless

- Tentatives de polymorphisme (trop lourd)
- Utilisation de map
- Extraction de chaque comportement des enums dans des fonctions
- Piste à explorer : directement intégrer les comportements dans SpecialOfferType

## Itération 5 : Random constraints

1. ajout de specs
2. primitive obsession => très bien, implique de l'immutabilité
3. ajout de feature en diminuant la complexité => attaque par le bundle, ségrégation de l'ancienne et de la nouvelle méthode de calcul
4. immutabilité => implique la primitive obsessions

## Rétro

- Envie de repartir sur la même base de code (qui est sans doûte trop gros) pour éviter les mêmes refactorings
- Les contraintes ne changeaient pas vraiment l'approche
- Beaucoup de nouvelles têtes
- Redécouverte de l'IDE pour les dev occasionnels
- On n'a pas passé assez de temps sur les tests (:with-test et approval tests nous ont éloignés)
- Proposition : faire deux mobs de 2 heures le matin, que tous le monde ai la même compréhension
- Sympa de se voir coder les uns les autres
- Malgré les différentes technos, tout s'est bien passé
- Kata proche des problématiques d'une journée de Travail
- Refactoring avec des tests permettent un grand confort
- Partage des connaissances et des pratiques
- Pas de soucis de setup
- Bien aimé les changements de partenaires

## Itération 6 : Immutabilité

- Mod sur C#
- Extraction de Items et reconstruction du Dictionnary

## ROTI

- 15 votants
- ROTI 5/5 -> 8 personnes
- ROTI 4.5/5 -> 1 personne
- ROTI 4/5 -> 6 personnes
