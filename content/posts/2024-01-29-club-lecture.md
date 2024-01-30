---
title: "Soirée lectures du Lundi 29 Janvier"
date: 2024-01-29T19:00:00+01:00
tags: ["talk", "live", "lectures"]
---

- Sujet: Club de lecture
- Format: Discussion online
- Meetup: https://www.meetup.com/software-craftsmanship-lyon/events/297930858/
- Vidéo: https://youtu.be/y8nx1RKO6CU
- 3 intervenants / 6 viewers

## (Video) "What UNIX Cost Us" - Benno Rice (LCA 2020)

- https://www.youtube.com/watch?v=9-IWMbJXoLM
- Tout ce qui a jamais été publié comme API est maintenue (aucun remboursement de dette technique)
- Divergence ouverture de device MacOS vs GNU/Linux, polling epoll (Linux) vs kqueue (FreeBSD/OpenBSD/etc.)
- Successeur à UNIX : [9Plan from Bell Labs](https://9p.io/plan9/)

## (Video) "The Early Days of id Software: Programming Principles" by John Romero (Strange Loop 2022)

- https://www.youtube.com/watch?v=IzqdZAYcwfY
- Histoire de la production rapide de jeux vidéos
- Plusieurs par par an
- Bon outillage (dev et debug)
- Toujours avoir un produit utilisable
- test en continue, sur plusieurs plateformes

## (Livre) Tidy First?: A Personal Exercise in Empirical Software Design - Kent Beck

- https://www.oreilly.com/library/view/tidy-first/9781098151232/
- Assez décevant
- Les refactoring sont basic
- Jeux sur la hype
- Le blog est meilleur : https://tidyfirst.substack.com/
- [Refactoring](https://martinfowler.com/books/refactoring.html) est mieux pour recenser les patterns

## (Dépôt) Implementation of GoF design patterns using Java 17

- https://github.com/forax/design-pattern-reloaded
- [Practical Object-Oriented Design, An Agile Primer Using Ruby](https://www.poodr.com/)
  - Passe beaucoup de temps à parler d'héritage
    - L'héritage est conçu en Ruby comme Smalltalk (un ensemble de comportements liés et de plus en plus précis) vs C++/JAVA/C# (des comportements sur une structure de données)
    - L'héritage va à l'encontre de [SOLID](https://en.wikipedia.org/wiki/SOLID)

## (Articles) Midori

- https://joeduffyblog.com/2015/11/03/blogging-about-midori/
- https://joeduffyblog.com/2016/02/07/the-error-model/
- Projet Microsoft abandonné de nouvel OS
- Basé sur un C# renfondu
- Bonne étude bibliographique
- Mini livre

## Divers
- "What I learned by solving 50 Advent of Code challenges in Rust - Luciano Mammino" https://www.youtube.com/watch?v=udHjmno-tfA
  - Les regex sont des langage de construction de machines à états complet
    - https://owasp.org/www-community/attacks/Regular_expression_Denial_of_Service_-_ReDoS
    - Deux familles en POSIX ne peut qu’avancer, alors que PERL/Ruby/… sont turing complets
    - Bon livre : https://www.amazon.fr/expressions-r%C3%A9guli%C3%A8res-par-lexemple/dp/2914010656

## (Livre) Patterns for API Design: Simplifying Integration with Loosely Coupled Message Exchanges

- https://www.oreilly.com/library/view/patterns-for-api/9780137670093/
- Assez large (RPC, Web API, Async) et pronfond (formats, policies)
- Formalise confusant et superflu

## (Livre) Lean DevOps

- https://www.leandevops.com/book/
- Bonne introduction pour décideurs et opérationnels
- Introduction à la culture
- Pour aller plus loin sur le Site Reliability Engineering : https://sre.google/books/

## Divers (la suite)

- "The Power of Value - Power Use of Value Objects in Domain Driven Design - Dan Bergh Johnsson" https://www.youtube.com/watch?v=vh-LT1mkIz4
- "The Aggregate is dead. Long live the Aggregate! - Sara Pellegrini & Milan Savić" https://www.youtube.com/watch?v=MpalYQaKKd4
- Zéro bug CTO : https://www.youtube.com/watch?v=tVAS4BLWt9Y Tech lead : https://www.youtube.com/watch?v=RuM-5sHuqb4
- "Designing Beyond the Happy Path with STÉPHANIE WALTER" https://youtu.be/u-SB1s2PTds?si=E3Qy35UeUYFFx6hV
- "ATN23 - Nicolas Adam - Mode produit mode projet arrêtons la guerre" https://www.youtube.com/watch?v=YHXBSPSc2ec
- "Define Your Audience Now, Not Later" https://www.youtube.com/watch?v=h2iKIVRLv3U
- "Data-Oriented Programming: Reduce Software Complexity" https://www.amazon.fr/Data-oriented-Programming-Unlearning-Yehonathan-Sharvit/dp/1617298573/
