---
title: "[Lyon Craft] Kebab Kata animé par Romeu Moura"
date: 2026-05-12T14:00:00+02:00
tags: ["dojo"]
---

- Sujet : [Kebab Kata](https://lyon-craft.fr/sessions/kebab-kata.html) ([Guide facilitateur](https://github.com/malk/the-kebab-kata))
- Facilitateur : [Romeu Moura](https://www.linkedin.com/in/romeu/)
- Nombre de participants : 21
- Format : groupes de 2 ou 3
- Langages : Java, C#, Typescript

## Déroulement

### Setup initial

Un environnement de développement au choix avec un test au rouge.  
Pour ce kata, il vaut mieux privilégier un environnement avec lequel on est à l'aise. Découvrir un langage ici est une mauvaise idée.  

### Déroulé

Durant ce kata, Romeu (le facilitateur) va jouer plusieurs personnages pour diriger un projet sur 4 sprints de 25 minutes.  

Un sprint se déroule de la façon suivante:  

- Le client exprime ses demandes.
- Les équipes codent (et les personnages interfèrent, influencent les équipes).
- Chaque équipe doit faire une démonstration de 45 secondes au client qui **ne sait pas** coder. Mentir au client est autorisé.  
- Des membres de chaque équipe vont faire des revues de code de 2 minutes sur le code d'autres équipes. Ces revues sont honnêtes et constructives, il n'y a pas de compétition entre les équipes.

### Sprint 1

Le *client* présente son business à ses équipes backend. Celui-ci a une demande : il veut pouvoir dire à ses clients si un kebab est végétarien ou non.  
Etonnament, pour un client qui ne sait pas coder, il est déjà très directif en relayant la demande de l'équipe front-end : il décrit un objet `kebab` avec une méthode `isVegetarian()` sans paramètres. Le `kebab` est construit avec une liste d'ingrédients.  

Budget initial : 10 minutes, mais en vrai, 7 minutes ça suffit non ?

Au moment de la démo, certaines équipes jouent le jeu, demande des précisions, une liste de potentiels ingrédients, et un délai pour les éventuelles corrections à apporter suite aux retours du client.

### Sprint 2

Le client semble être réceptif à la sensibilité craft de ses équipes et leur laisse un peu plus de temps pour finir le sprint précédent. Il demande également une seconde fonction `isPesetarian()`.  

Budget total alloué : 7 minutes.  

### Sprint 3

Le client à deux nouvelles features:

- La fonction `doubleCheese()` double le fromage au même endroit : un kebab "pain, fromage, viande, pain" devient "pain, fromage, fromage, viande, pain".  
- La fonction `removeOgnon()` qui retire tous les oignons.

Il oriente encore le design du code en relayant les demandes de l'équipe front-end. Ces nouvelles fonctions doivent retourner un nouveau `kebab`, l'équipe front n'utilisera plus l'ancien kebab. Si aucun changement n'est nécessaire, alors ces fonctions peuvent retourner le même kebab.  

Vu la demande conséquente, un budget de 15 minutes est alloué.

### Interlude

Bravo pour cette mise en production, high-five, fiesta... Et vous êtes tous virés !

Maintenant, les participants jouent le rôle de nouveaux développeurs qui remplacent les anciens.  
Le client se plaint d'un legacy et demande un audit du code **sans aucune modification**.  

Budget de l'audit : 3 minutes.

Le facilitateur sort de son rôle client pour s'assurer que chaque équipe a identifié des choses qui pourraient être modifiées et demande de conserver une version de se code.

### Sprint 4

Le client n'a pas de nouvelle demande fonctionnelle à exprimer, il demande uniquement aux équipes de résorber la dette technique. Pour aider les équipes, il a fait appel à un architecte.  

L'architecte dirige les équipes vers le [pattern composite](https://refactoring.guru/fr/design-patterns/composite). Il prend le temps d'expliquer le pattern dans le contexte du kebab.  
Cela ressemble à : `new Tomato(new Cheese(new Ognon(new Bread())))`.  

L'architecte tient à son statut, pour contester ses propositions, il faut lui soumettre des arguments forts.

Le facilitateur donne une information aux participants : l'architecte a tort. Il suggère d'explorer plusieurs solutions pour trouver des contre-propositions.

Budget alloué : 20 minutes.

## Rétrospective

### Debrief du dernier sprint sur la décision d'architecture

- Problématique : la logique est difficile à suivre puisqu'éclatée dans plein de classes, coût d'onboarding plus élevé.
  - Contre-argument : logique simple pour chaque ingrédient.
  - Contre-argument : si le pattern est le bon, alors le coût de l'onboarding reste acceptable.
- Problématique : Si on oublie le pain à la fin de la chaine, alors ça ne marche pas.
  - Contre-argument : si tu oublies le pain, alors sur certains langages ne compileront pas.
- Problématique : la récursion rend difficile la visualisation de la chaine. En debug, on voit juste l'enfant et on ne voit pas l'ensemble des ingrédients.
  - Contre-argument : c'est une question de familiarité, si l'on est habitué alors ce n'est pas un problème.
- Problématique : un composite peut être un noeud ou une feuille.
  - Contre-argument : dans notre contexte, n'importe quel ingrédient est un kebab.
- Problématique : pas de Tail Call Optimisation sur certains langages utilisés.
  - Contre-argument : dans ce contexte métier, peu de chance que ça soit un problème pour la performance.
- Problématique : avec composite, ajouter un nouvel ingrédient est très peu coûteux, ajouter un nouveau comportement l'est énormément.
  - Trade-off inverse : [pattern visitor](https://refactoring.guru/fr/design-patterns/visitor) qui rend coûteux l'ajout d'un ingrédient et peu coûteux l'ajout d'une règle. Pour ce kata c'est une bonne solution.

### Debrief sur les comportements adoptés

La qualité du code est le reflet d'un ensemble de comportements des différents acteurs. Tous sont de bonne volonté, mais ils ne font pas preuve de rigueur et sont dépassés/incompétents. Des exemples :  

- Pression par les timings/deadlines. Seul le client définit la durée des sprints et leur contenu de façon unilatérale sans concertation avec les équipes. Pour amplifier cela, les timings réels étaient toujours plus courts que ceux réellement annoncés.
- Séparation des équipes : "vous n'iriez pas plus vite sur deux ordinateurs ?".
- Les orientations techniques : le client a énormément drivé l'implémentation.
- La séparation back/front. Romeu confesse qu'il a un personnage "équipe front-end", il n'a jamais eu l'occasion de le jouer, car personne n'a demandé à lui parler.
- Architecte "vertical" : il décrit un pattern, mais n'explique pas pourquoi il l'a choisi. S'en fout de l'audit, il ne demande pas ce qui a été dit.
- Les personnages ne s'impliquent pas toujours : le client n'est pas intéressé par ce qu'il se passe aux démos et ne s'implique pas pendant le développement.
- Aucun feedback du client sur les raisons pour lesquelles l'équipe est virée.
- Les besoins étaient exprimés sous la forme de la solution plutôt que de la problématique, on voit ce que le client demande, mais pas pourquoi.
- Permettre de continuer à coder pendant que les autres font la démo maintient les équipes à flux tendu, ce qui les empêche de prendre du recul sur ce qu'ils sont entrain de faire.

Points positifs:  

- La revue du code des autres a diffusé de nouvelles idées.

## ROTI

- 4/5 : 50%
- 5/5 : 50%
