---
title: "Lyon Craft 4 avril 2023"
date: 2023-04-04T09:00:00+01:00
tags: ["lyon-craft", ]
aliases: [/posts/lyon-craft-04-04-2023/]
---

# Keynote d’ouverture

# From Legacy to Hexagonal: A Live Coding Journey

# EventStorming

L'[EventStorming](https://www.eventstorming.com/) est un atelier formalisé par Alberto Brandolini, il a pour but d'aider les participants à rapidement construire une compréhension partagée des processus et problématiques du métier exploré.  
Il s'agit donc d'un atelier exploratoire où l'on va se concentrer sur l'espace du problème, et non sur la définition d'une solution.  

## Rétrospective

Retour participant: De la frustration exprimée par certaines personnes qui auraient voulu aller encore plus loin (c'est le problème quand le métier exploré est sympa :smiley: ).  
Remarque des facilitateurs : nous étions beaucoup pour une session (environ 15 par groupes), cela peut apporter une certaine lenteur/lourdeur sur le déroulé de la session.  
Remarque des facilitateurs : Le format employé lors de cette session était plutôt "classique", il existe des façons de l'animer [plus dynamiques](https://blog.ippon.fr/2020/02/19/un-event-storming-avec-alberto-brandolini/), mais elles nous semblaient moins adaptées pour une première approche de l'exercice.  
Tips : une technique pour cadrer le périmètre de la session consiste à poser le premier et le dernier du processus à explorer.  
À la fin de la session : on jette __tout__ ! L'important reste les échanges et la connaissance partagée lors de la session. La compréhension, le besoin et le métier vont évoluer par la suite, si l'on ressent le besoin d'un event storming, il est préférable d'en faire un nouveau.  
Quand faire un EventStorming ? : L'usage de l'event storming est une bonne introduction pour une équipe, idéal aussi pour explorer un sous-ensemble/une problématique spécifique.  
Question : Les entités sont-elles représentées dans un EventStorming ? Non. Attention, à ne pas confondre l'agrégat de l'EventStorming (un ensemble cohérent de commandes, events, policies et readmodels) avec le pattern tactique défini dans le Domain-Driven Design.
Question : Comment définir le contenu d'un readmodel ? Tout dépend de la granularité recherchée, il s'agit des données nécessaires pour qu'un acteur prenne une décision.  

## ROTI 
Moyenne à 4/5

# Codons un jeu du pendu

## Rétrospective intermédiaire

Découverte du TDD, début difficile et du mal à voir la phase de refacto. 
Choisir le niveau de scope des tests qui à tester des méthodes privées. Si trop haut niveau, trop long pour faire une implémentation rapide.
Utilisation des tests paramétriques pour avoir des aspects plus comportementaux. Bémol sur les tests paramétriques qui tend à nommer la méthode de test `it_works`.

## Rétrospective intermédiaire 2

Stratégie de sprint sur le TCR avec du pseudo-code à implémenter en deux minutes. Viser le comportement qui doit apparaître avant les aspects techniques. Le but du TCR est de pousser au refactoring
au plus tôt.

Au global les participants étaient surpris de la richesse du kata car il n’autorise pas de faire un tout droit et c’est fini. Il permet de faire de nombreux choix design.

## ROTI
 
- 4/5 : 16
- 5/5 : 2

# Un démarrage TDD accéléré !

## Présentation

TDD c'est hyper difficile. Ah non en fait c'est facile. Ah, j'avais pas tout compris. Oh c'est ça ?"… Je vous propose de (re)démarrer ensemble la découverte de TDD, en live-coding. Objectif : booster votre apprentissage, reconnaître des erreurs de compréhension de TDD, et les bannir au plus vite.

## Orateur

Je suis développeur, lead dev, coach craft et practice manager chez Ippon. Mes passions tournent autour du Craftsmanship et de l'Ecologie, pour les deux termes dans mon environnement professionnel, et à la maison :)

## Support

https://github.com/onepunchmagne/garden

# Du DDD chez Enedis, pourquoi ?

# Initier une pattern library

## Rétrospective



## ROTI

- 1/5 : 
- 2/5 : 
- 3/5 : 
- 4/5 : 
- 5/5 :

# Capturer le comportement de mon legacy pour le faire évoluer

## Rétrospective



## ROTI

- 1/5 : 
- 2/5 : 
- 3/5 : 
- 4/5 : 
- 5/5 :

# Comment on n’a (toujours) pas codé de back-end après un an en production

# Un développeur sous couverture parmi les utilisateurs

# Un kebab aux spaghettis, ça vous tente ?

## Rétrospective



## ROTI

- 1/5 : 
- 2/5 : 
- 3/5 : 
- 4/5 : 
- 5/5 :

# C’est l’histoire de la vie, le cycle (presque) éternel.

## Notes

- Sujet : Game Of Life en commençant par la cellule
- 9 pairs + 1 solo
- 3 en C#, 2 en TypeScript, 4 en Java, 1 en Vue/TypeScript
- Le participant en Vue à été jusqu'à sortir un visuel de la grille

## Rétrospective

- Bonne introduction
- Sujet simple à apréhendé
- Bien guidé
- Pas de gros problèmes

## ROTI

- 1/5 : 
- 2/5 : 2
- 3/5 : 7
- 4/5 : 5
- 5/5 :
