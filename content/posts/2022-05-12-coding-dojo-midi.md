---
title: "Coding Dojo Jeudi 12 Mai 2022"
date: 2022-05-12T12:15:00+01:00
tags: ["dojo"]
---

- Sujet : Etat de rapprochement
- Meetup : https://www.meetup.com/Software-Craftsmanship-Lyon/events/285516433/
- 9 inscrits / 8 présents
- Lieu : Discord
- Format : Mob programming
- Langage : Java

## Sujet

Pour un compte et une période (un mois) donnés, vous cherchez à remplacer une feuille de calcul permettant de vérifier les entrées/sorties.  
Le but étant de calculer le solde d'un compte, pour pouvoir être comparé aux relevés bancaires.  
- Itération 1 : être en mesure de tracer les mouvements effectifs sur ce compte, exemple:
    - 04/01 Cinéma -12.00€
    - 14/01 Courses -54.12€
    - 30/01 Paie +2324.00€
- Itération 2 : supporter des mouvements prévus, exemple:
    - 04/01 Cinéma -12.00€ Effectif
    - 14/01 Courses -54.12€ Effectif
    - 28/01 Facture téléphonique -19.99€ Anticipé
    - 30/01 Paie +2324.00€ Anticipé
- Itération 3 : une entrée peut être validée (à partir de n'importe quel état), exemple:
    - 04/01 Cinéma -12.00€ Validé
    - 14/01 Courses -54.12€ Effectif
    - 28/01 Facture téléphonique -19.99€ Validé
    - 30/01 Paie +2324.00€ Anticipé
- Itération 4 : lorsqu'un mouvement est effectif, puis anticipé et inversement, il devient validé
- Itération 5 : un mouvement validé peut être "dévalidé", dans ce cas, il revient à son état précédent
- Itération 6 : un mouvement anticipé peut être corrigé

## Retours

Discussions autour des [Monoids](https://en.wikipedia.org/wiki/Monoid), exemple avec notre type Amount.  
Problématique découverte sur les Monoids : une structure composée uniquement de monoids est elle même un monoid. Ce n'était pas le cas du mouvement car il contenait des propriétés comme la date.  

Quand utiliser des types dédiés ? Quand utiliser les primitives ? Réponse de Colin : primitives quand le modèle est proche d'un framework, dés qu'il travail sur du code métier, alors types dédiés.  
Code mal parti au début (en terme de qualité), puis on a exploré des solutions pour l'améliorer.  
Les types ont mis longtemps à émerger.  

Des difficultés à cadrer le périmètre fonctionnel, beaucoups de dispersion tout au long de la session.  
Pro tip: Colin comme driver, il a moins le droit de parler.  

## ROTI

- 4/5 : 1
- 3/5 : 6
- 2/5 : 1

## Pub

- Forum ouvert le 16/05 : https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/285516495/  
- Coding dojo le 27/05 : https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/285516548/