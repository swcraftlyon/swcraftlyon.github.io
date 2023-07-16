---
title: "Forum ouvert avec les crafters de Paris et Strasbourg"
date: 2023-06-15T19:00:00+01:00
tags: ["unconf", "ddd"]
---

- Sujet: Forum Ouvert
- [Meetup](https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/293586607/)
- 10-14 personnes

## Forum ouvert avec les crafters de Paris et Strasbourg

Après [NewCrafts](https://ncrafts.io/), les communautés craft de [Strasbourg](https://swcraftstras.github.io/), [Paris](https://www.meetup.com/fr-FR/paris-software-craftsmanship/) et Lyon ont décidé de se rencontrer pour un forum ouvert, structuré en 3 sessions de 25 minutes suivies d'une rétrospective.

## Session 1 19h25 – 19h50

### Salle 1 : Comment coder un processus métier (quand passer à l’étape suivante, annuler, mettre en attente) ? (Nolwenn)

- Recoder une machine à état ?
https://github.com/arthur-noseda/gamebook/tree/main/backend/src/main/java/com/ingeniouscontraptions/games/gamebook/domain/encounter
- Qui a la charge de savoir les prochains états possibles
- Comment gérer les droits dans le processus métier
- Est-ce que ça ne devient pas compliqué si on crée une classe par état ?

### Salle 2 : En fait organiser une conférence c'est facile ! et Qu'est-ce que vous voudriez voir aborder comme sujets dans une conf "avancée" sur le craft ? (Colin)

Sujets à aborder dans une conférence :

- Exemple d'une "vraie" application suivant les bonnes pratiques
- Value / Velocity-Driven Development

Choisir la version facile : 

- Pas de CFP
- Moins de 150 personnes (plus simple pour les salles / nourriture / boissons)
- Acheter des services (même pour les trucs simple).

- Attention à HT/TTC quand on échange avec les pros
- Prix d'un billet, quel est le bon montant pour certifier l'engagement sans être excessif
- Pour gagner du temps être directif sur le choix des sujets est efficace

### Salle 3 : Quelqu'un peut m'expliquer “Parse, don't validate” ? (Marc)

- https://lexi-lambda.github.io/blog/2019/11/05/parse-don-t-validate/
- https://xtrem-tdd.netlify.app/Flavours/parse-dont-validate
- https://khorikov.org/posts/2021-11-08-converting-result-to-maybe/
- https://github.com/les-tontons-crafters/nir-kata
- [Domain Modeling Made Functional](https://pragprog.com/titles/swdddf/domain-modeling-made-functional/) de [Scott Wlaschin](https://fsharpforfunandprofit.com/)
- https://www.youtube.com/watch?v=T4SvCLLxTDg&ab_channel=SoftwareCraftsmanshipLuxembourg
- https://www.youtube.com/@nickchapsas
- https://youtu.be/a1ye9eGTB98 (Don't Throw Exceptions)

Un exemple réel : https://github.com/taxi-gestion/api 
=> défintions des codecs avec io-ts : https://github.com/taxi-gestion/api/blob/main/src/commands/schedule-fare/schedule-fare.definitions.ts
=> la gateway : https://github.com/taxi-gestion/api/blob/main/src/commands/schedule-fare/schedule-fare.validation.ts

### Salle 4 : JPP des katas que je vois en dojo. C'est pas mieux de coder des vrais trucs en dojo ? Vous attendez quoi d'un dojo ? (Othman)

https://sammancoaching.org/
Choisir le kata en fonction de ce qu'on veut exercer comme skill / domaine / techno.
Essayer d'aller à des dojos avec une audience constante pour ne pas se retrouver à chaque fois dans des dojos "débutants" ou "tdd"
20 minutes de setup, 30 minutes de comment nommer une variable, et après il faut clôturer.
=> Pas la même expérience aux Software Crafters Lyon.
Utiliser Cyberdojo pour réduire le temps de setup.

### Salle 5 : Aidez-moi à animer des sessions Ensemble Programming en full remote (Ando)

- Mettre un timer (par exemple [mob timer](http://mobtimer.zoeetrope.com/))
- [Technique Pomodoro](https://fr.wikipedia.org/wiki/Technique_Pomodoro)
- Commencer avec peu de participants (3-4 personnes)
- Travailler sur les tickets car pas de culture kata
- Pas de TDD car pas de culture TDD
- un seul objectif pédagogique à la fois
- utiliser un framapad pour noter les tâches à faire
- bien poser / expliquer le sujet en début de session

## Session 2 19h55 – 20h20

### Salle 1 : L'algo FVP (final version perfected) pour prioriser ses tâches (Jonathan L.)

http://markforster.squarespace.com/blog/2021/11/16/the-final-version-perfected-fvp-instructions-reposted.html

1. Je mets un point devant la tâche que je dois faire actuellement (en commençant par la première tâche).
2. Je compare avec les autres tâches par l'importance que je leur accorde à l'instant t (par exemple la tâche 2 gagne sur la tâche 1). Toutes les tâches importantes sont donc marquées par e caractère point en préfixe. Les interblocages sont résolus par la comparaison une à une de la tâche avec les autres (par exemple, Mettre un pantalon est plus important qu'acheter du lait, car j'ai besoin d'un pantalon pour acheter du lait).
3. Je commence la dernière tâche qui a un . et je la marque avec un X, puis je remonte
4. Quand toutes les tâches pointées ont été exécutées, je passe aux tâches non pointées.
5. Si une tâche devient caduque dans la todo list, je la vire.
6. Les tâches sont ajoutées à la suite les unes des autres.

- . Acheter du lait
- . Envoyer un mail à mon patron
-  Poser ma démission
- X Faire un cadeau à Colin
- X Réparer cette porte qui claque
- . Mettre un pantalon

### Salle 3 : Tester l'intégration à un système externe, est-ce vraiment automatisable ? (Cédric H.)

Couts vs Efforts d'un test.

### Salle 4 : Feedback cartes Xtrem Smells (Yoan) ET/OU Clean code du point de vue la cognition (Yoan)

- [Code Reading in Practice](https://www.oreilly.com/library/view/code-reading-in/9781098133818/)
- Env 60% du temps on lit du code
- Utile d'optimiser notre lecture de code
- Pour apprendre efficacement
- Flash cards
- Pratique régulière : répétition espacée
- JetBrains semble utiliser en partie cette approche : [Hyperskill](https://hyperskill.org/)
- Elaborer autour du concept pour faciliter l'ancrage (ex. se rappeler de comment sont faites les monades dans différents langages)
- Indexes for learning :  https://techleadjournal.dev/episodes/63/
- De Groot Chess experiment : Expert vs Newbies
- ["How to teach programming (and other things)?" by Felienne Hermans](https://youtu.be/g1ib43q3uXQ)
- [Set de cartes](https://miro.com/app/board/uXjVMD2Gxsw=/?share_link_id=367068083359)
- [Infographie du livre "Programmer's Brain" (et plus)](https://yoan-thirion.gitbook.io/knowledge-base/xtrem-reading/my-book-infographics)

# Salle 5 : Comment j’ai appris Rust (Nolwenn)

- [The Book](https://doc.rust-lang.org/book/)
- [Exercism](https://exercism.org/tracks/rust)
- [rustlings](https://rustlings.cool/)
- et des katas

## Session 3 20h25 – 20h45

### Salle 1 : Qui veut m'aider à préparer mon tout premier atelier d'example mapping? (Marc)

### Salle 2 : "Railway programming" pour intégrer les erreurs dans votre flux (Romain)

Typecheck / Rulecheck ... le pattern Gateway aux stéroïdes pour une API type-safe, worth it ? [Romain]

- [Railway Programming: la voie vers un code plus honnête (Romain Berthon et Sylvain Coudert)](https://youtu.be/xQ7Fstshckk)
- Domain Modeling Made Functional de Scott Wlaschin

### Salle 3 : Je code une TodoList avec de l'event sourcing (Jonathan L.)

### Salle 4 : Introduction a JHipster Lite (Colin)

### Salle 5 : On me demande de faire des mega formulaires, ou est le domaine métier ? (Cédric H.)

- Des validations côté front pour retour rapide
- Event sourcing 

## Rétrospective

- Sympa de faire des petits talks de 20-30 minutes. Le cadre fait qu'on a pas de solution toute faite, mais c'est cool.
- C'est passé super vite. Plein de nouveaux gens, c'est trop bien.
- Assez content, participation à des trucs intéressants, pas trop de regrets de n'avoir pu participer à tout.
- Je n'ai pas vu le temps passer. Temps raisonnable par rapport au nombre de sujets.
- Très bonne idée de mettre tous les liens dans le framapad. Les liens rajoutés sur le framapad attirent du public.
- Les interstices auraient mérité une rétro de 30 s / 1 minute pour donner les "take away" de la session. Compliqué avec le timing. - Chacun a vécu "sa" soirée.
- L'événement au global s'est bien déroulé, c'est à refaire. Peut-être en mêlant les communautés.
- Le framapad est un très bon outil.
- Est-ce qu'on n'irait pas vers une fédération des communautés craft, pour organiser ce type d'événements à l'avenir ?

## ROTI :

- 3 : 1
- 3.5 : 1
- 4 : 6
- 5 (la meilleure soirée de la journée selon Nolwenn) : 6
