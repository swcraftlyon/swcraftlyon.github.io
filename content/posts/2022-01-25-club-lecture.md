---
title: "Soirée lectures du Mardi 25 janvier 2022"
date: 2022-01-25T19:00:00+01:00
tags: ["talk", "live", "lectures"]
---

- Sujet: Les Crafters parlent de bouquins
- Format: Discussion online
- [Meetup](https://www.meetup.com/Software-Craftsmanship-Lyon/events/282937143/)
- [Replay](https://youtu.be/ZVKQcveesTE)

## Sujets

**Livre : [Les BDD Books](https://www.bddbooks.com/) de Gáspár Nagy & Seb Rose** présenté par Romain

Deux courts livres, Discovery et Formulation, initialement prévus dans une série de 3 ouvrages autour de BDD.
Discovery met en scène une équipe métier qui découvre son besoin au travers d'[Exemple Mapping](https://en.wikipedia.org/wiki/Specification_by_example).
Formulation reprend cette même équipe et apprend commment passer du résultat de l'Exemple Mapping à une formulation en [Gherkin](https://en.wikipedia.org/wiki/Cucumber_(software)#Gherkin_language).
Initialement, le troisième livre devait s'appeler Automation, n'est pas encore paru, mais devrait être remplacé par des tips & tricks autour de la living documentation, un peu dans l'esprit de [97 Things Every Programmer Should Know](https://www.oreilly.com/library/view/97-things-every/9780596809515/)
[L'appel à contribution pour le troisième livre](https://docs.google.com/document/d/1nn33AC_PMH0EgU9OE5H6nCjUihmA10Cb5CoMVl_fcJU/edit).
Plein de bons conseils, la lecture vaut le coup, que l'on connaisse ou pas BDD, et ne prend pas beaucoup de temps.

**Article : [Functional Event Sourcing Decider](https://thinkbeforecoding.com/post/2021/12/17/functional-event-sourcing-decider) de Jeremie Chassaing** présenté par Romain

Jérémie Chassaing, référence française du langage F# et des systèmes [CQRS](https://en.wikipedia.org/wiki/Command%E2%80%93query_separation#Command_Query_Responsibility_Separation)-ES, décortique toute l'anatomie d'une application event-sourcée et la décompose en blocs de construction, comment les composer, comment construire une architecture event-sourcée, modulaire, dont les éléments sont facilement substituables par d'autres implémentations.
Pour aller plus loin, Tlaop propose [Distributed DDD, CQRS et EventSourcing](https://www.youtube.com/watch?v=m9tXT_q5odA) de Jérémie Chassaing à Devoxx (2013).

**Livre : [Ravage](https://www.babelio.com/livres/Barjavel-Ravage/6590) de René Barjavel** présenté par Florent

Florent n'a pas aimé ce livre, publié en 1943, à cause de la critique du progrès et les aspects misogynes du texte.
Il conseille néanmoins la lecture des 20 premières pages pour la description de la vie dans le futur imaginée par l'auteur.

**Talk : [Cloud Souverain](https://www.youtube.com/watch?v=FkACIjjCTQE) par Quentin Adam** présenté par Florent

Une vidéo très intéressante sur le Cloud souverain, malgré les GIF animés qui perturbent l'attention.
[L'intervention de Question Adam sur le podcast des cast codeurs](https://lescastcodeurs.com/2021/09/02/lcc-262-interview-cloud-de-confiance-avec-quentin-adam/).

**Documentaire : [Disparaître - Sous les radars des algorithmes](https://www.arte.tv/fr/videos/100750-000-A/disparaitre-sous-les-radars-des-algorithmes/) sur Arte.tv**, proposé par Florent

Un documentaire qui parle entre autres du projet de Framasoft concurrent à Facebook.

**Talk : [La lévitation quantique](https://www.youtube.com/watch?v=6kg2yV_3B1Q) Julien Bobroff** proposé par Florent

Une super présentation.

**Jeux vidéo : [Why 4:54 is the perfect speedrun - Super Mario Bros. World Record Speedrun Explained](https://www.youtube.com/watch?v=U7RzoIEoSMY)**, proposé par Florent

Une explication du speedrun du premier Super Mario Bros, réalisé sans outils.

**Article : [Are We Really Engineers?](https://www.hillelwayne.com/post/are-we-really-engineers/)** et **[We Are Not Special](https://www.hillelwayne.com/post/we-are-not-special/)** proposé par Florent

Hillel Wayne s'intéresse aux nombreux parallèles entre notre métier de développeur et le métier d'ingénieur (hormis nos boucles de feedback qui sont courtes).

**Article : [Cognitive Load Theory and its Applications for Learning](https://www.scotthyoung.com/blog/2022/01/04/cognitive-load-theory/) par Scott H. Young** présenté par Romain

Cet article fait une très bonne introduction à [The Programmer's Brain](https://www.manning.com/books/the-programmers-brain), que Romain recommande également.
L'article parle de nos capacités cognitives limitées et les difficultés auxquelles nous sommes confrontées pour apprendre de nouvelles choses.
Par exemple, pour rentrer efficacement dans une nouvelle code base, trouver le bout de code qui effectue une tâche particulière nous surcharge moins que de commencer par corriger un bug.

**Série TV : [Un village français](https://fr.wikipedia.org/wiki/Un_village_fran%C3%A7ais)** présenté par Romain

Cette série, très documentée et fidèle à la réalité historique, dépeint le village fictif de Villeneuve dans le Jura pendant la seconde guerre mondiale.
La série présente la création des maquis, comment asseoir la nouvelle république après la guerre, comment juger les actes commis en temps de guerre.

**Livre : [Domain Storytelling](https://domainstorytelling.org/)** présenté par Tlaop

Cet ouvrage de 227 pages est une bonne surprise.
Il repart des use cases, mais 15 ans plus tard, avec beaucoup de pratique, avec une notation très graphique, et des conseils et astuces pour animer les ateliers.

Au travers d'un use case assez simple, la première partie du livre présente la notation, qui fait vaguement penser à UML pour son côté graphique, la modélisation, comment gérer le scope (le processus métier est-il numérisé ou non), les outils, l'animation des ateliers, et le rapport avec les autres techniques de modélisation : DDD, [EventStorming](https://www.eventstorming.com/), [User Story Mapping](https://www.jpattonassociates.com/story-mapping/), Example Mapping, [Storystorming](https://storystorming.com/), use case, UML, BPMN, en quoi c'est différent, comment on peut faire pour passer de l'un à l'autre ou les combiner.

La deuxième partie du livre décrit à quoi le Design Storytelling peut servir, à l'aide d'un Use Case plus profond. Comment trouver les boundaries, comment passer des sub-domains aux Bounded Contexts, comment passer des Bounded Contexts au Team Contexts, comment transiter vers le code, comment s'en servir au niveau organisationnel, détecter le shadow IT...
Les nombreuses références témoignent de l'honnêteté de la démarche de l'auteur.

L'outil [Egon.io](https://egon.io/) est en ligne pour mettre en pratique la méthode du livre.
