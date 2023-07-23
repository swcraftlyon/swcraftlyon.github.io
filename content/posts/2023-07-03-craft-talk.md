---
title: "Le TDD du Kata à la Production"
date: 2023-07-03T19:15:00+01:00
tags: ["talk"]
---

- Sujet : Le TDD du Kata à la Production
- Format : Talk
- [Meetup](https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/294134229/)

Présentation par [Maxime Dezette](https://fr.linkedin.com/in/maxime-dezette), développeur chez [Groupe PSIH](https://groupepsih.com/), de pistes pour pratiquer le TDD au quotidien.

Le talk était structuré en 2 parties.
La première présentait les termes et les concepts.
La seconde était un live-coding pour montrer la pratique.

## Présentation

Maxime rappelle que [TDD](https://fr.wikipedia.org/wiki/Test_driven_development) est une méthode de conception de code, dont les tests dictent l'implémentation.
Une boucle de TDD passe par trois étapes :

* Rouge : le test est rédigé mais il ne passe pas,
* Vert : l'implémentation la plus simple possible est écrite et fait passer le test,
* Remaniement/refactoring : le code est transformé pour en éliminer les [défauts](https://fr.wikipedia.org/wiki/Code_smell).

Il mentionne également l'importance des [katas de code](https://fr.wikipedia.org/wiki/Kata_(programmation)) pour pratiquer le code ou son remaniement.

Maxime examine les causes de la mauvaise qualité du code : il semble plus facile de complexifier une méthode existante quand on ne sait pas où l'on va.
À l'inverse, si l'on commence par écrire un test, s'orienter devrait devenir plus simple ?
C'est la promesse de départ.

Maxime a plus de plaisir à travailler avec TDD que sans : la succession des boucles pose les rails sur lesquels nous avançons, une micro-tâche après l'autre, le test vert confirmant que l'on va dans la bonne direction.
Cela apporte beaucoup plus de confort au travail.
Ainsi, vit-on mieux les code reviews, parce qu'on a une bonne confiance dans ce qu'on livre, et décorrèle-t-on le "ça marche" de la "maintenabilité du code".
Bien que TDD aide Maxime dans son quotidien, il concède la difficulté de faire adopter cette méthode à ses collègues.
TDD reste cantonné aux katas.
Les objections sont multiples : "les katas c'est simple, mais sur une vraie application ce n'est pas adapté", "ça marche dans le back, mais pas dans le front", "les tests prennent du temps", "les besoins exprimés changent sans arrêt, alors je ne vais pas commencer par des tests".

## Live coding

Maxime propose de développer une feature de bout-en-bout, sur une application de gestion de logiciels et de leurs dépendances dans un parc applicatif.
Cette application permet notamment de déterminer un objectif de migration des dépendances dans les logiciels.
La feature à développer est d'ajouter le taux de complétion de l'objectif fixé.
En termes d'architecture, l'application est une petite API REST avec un frontend en Vue.js, qui sont les technologies utilisées par Maxime au quotidien.

Maxime commence par rédiger un test d'ensemble avec Cucumber, dans un langage proche du métier, pour notamment participer à la documentation vivante de l'application, lisible par n'importe qui, par exemple le développeur front : "on fait notre documentation en même temps qu'on fait notre test".

Maxime conseille de designer les steps Cucumber pour avoir le feedback le plus explicite, pour savoir quand ça ne marche pas, pourquoi ça ne marche pas.
Une "Run-conf" IntelliJ permet de lancer les tests unitaires automatiquement à chaque changement.
Pour que la boucle de feedback reste courte, Les tests Cucumber sont exclus de l'exécution et doivent être lancés manuellement.
La feature Cucumber sera son test rouge le plus longtemps.
La première boucle de TDD démarre avec un test JUnit, avec le cas élémentaire d'une liste d'applications vide.

Maxime recommande de lancer les tests tout le temps, et avec la couverture, pour attraper les régressions au plus tôt.

Plus on a de tests, plus ils sont faciles à écrire, car la plomberie nécessaire à leur rédaction existe déjà.

La conception émerge au fur et à mesure des remaniements.
Au cours du live-coding, on voit apparaître que le taux de complétion typé `int` serait plus justement décrit par un type  `PercentRate`.

Les tests unitaires devraient avoir un nom parlant, et leur code organisé en [Arrange-Act-Assert](https://learn.microsoft.com/en-us/visualstudio/test/unit-test-basics?view=vs-2022#write-your-tests) ou [Given-When-Then](https://en.wikipedia.org/wiki/Given-When-Then).

Pour savoir quoi tester, on peut établir une todo list comme décrit dans [Test Driven Development: By Example](https://www.amazon.fr/Test-Driven-Development-Kent-Beck/dp/0321146530) de Kent Beck, formalisée à côté, sinon dans la tête.
Le pattern [ZOMBIES](http://blog.wingman-sw.com/tdd-guided-by-zombies) décrit par James Grenning, peut aider, tout comme ajouter un futur test avec une instruction `throw`, ou mettre en place une règle SonarQube qui force à traiter les TODOs.

Parfois, un test n'apporte rien et ne sert qu'à se rassurer.
Si la couverture du code n'évolue pas, ou que le test ne conduit pas à écrire du code, alors Maxime conseille de le supprimer.

Du domaine, on remonte à l'API, et la réutilisation des fixtures de test amène leur mutualisation dans des classes utilitaires dédiées.

On peut ensuite faire un test de composant côté front en stubbant les routes, comme décrit dans [cet article](https://blog.ippon.fr/2019/07/11/des-tests-de-composants-avec-cypress/).

TDD permet de prendre en charge sereinement les retours pour correspondre aux standards de l'entreprise.
TDD ne fait pas de nous un bon développeur.
Mais vu les gains, ça vaut le coût de l'essayer dans de vraies conditions.
Il y a cependant des prérequis : maîtriser son framework de tests, tous les niveaux de tests, savoir mocker, savoir faire des fixtures, savoir faire du code lisible, savoir remanier le code, pour que le changement soit simple (c'est ça qui est difficile selon Kent Beck).
On peut se retrouver bloqué par du code non testable, c'est une compétence à travailler (on peut s'inspirer de cette résolution du kata [Gilded Rose](https://youtu.be/sZxL4uX9ioQ)).
Il faut avoir des bases de conception, être capable de modéliser sa réponse.

Maxime conseille de pratiquer sur des cas que nous maîtrisons, des cas que nous jugeons simples, poser des questions à la communauté (notamment celle des [software crafters de Lyon](https://swcraftlyon.github.io/)), faire des katas spécialisés, aller en meetup.

> Write tests until fear is transformed into boredom. (Kent Beck)

## ROTI :

- 3/5 : 4
- 4/5 : 11
- 5/5 : 5
