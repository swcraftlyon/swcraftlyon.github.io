---
title: "Coding Dojo Mardi 16 Janvier 2025"
date: 2025-01-16T12:15:00+01:00
tags: ["dojo"]
---

- Sujet : [BugZero Trivia](https://github.com/martinsson/BugsZero-Kata)
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/305268760/)
- Format : Mob
- Langages : TS, Java
- Nombre de participants : 12 

## Rappel du sujet

Le kata propose de réfléchir puis corriger les problèmes de design posés par l'impression d'un jeu librement inspiré du [Trivial Pursuit](https://fr.wikipedia.org/wiki/Trivial_Pursuit).

## Déroulement

L'affinité au langage permet de constituer 2 mobs.
1 h 20 consacrée au refactoring, puis restitution tous ensemble dans le Hall du salon Discord.

## Rétrospective

* C'est pas mal de faire du refactoring pur, de critiquer le code, sans avoir à écrire des tests.
* On retrouve de nouveau Approval Tests pour faire les tests, comme sur la session précédente ; est-ce que ça ne fait pas doublon ?
* Approval Tests n'est pas un pattern absolu dans l'industrie, c'est un effet de niche et ce ne sont pas forcément les mêmes participants qui viennent aux katas du soir et du midi.
* Dans le groupe TS, j'ai bien aimé la liberté laissée par le kata de se fixer les règles pour aborder l'exercice.
On s'y est pris en 2 temps : déterminer nos intentions, puis rendre le code + lisible.
* Agréable à suivre.
* Dans une première étape, nous avons amené de l'outillage pour virer les code smells et y voir plus clair, en installant [P42](https://github.com/p42ai) dans VS Code et appliquant ses propositions.
Puis dans une deuxième, nous avons réfléchi et entamé le refactoring.
* On a fini avec un _record_ dont le 2ème paramètre était une fonction.
* J'ai bien aimé l'optimisation du code par le refactoring.
On découvre d'autres manières de faire, ça enrichit la caisse à outils pour le travail quotidien.
* Un peu frustré de ne pas avoir obtenu la réponse à l'issue de la mise en place de types : nous avions modélisé un type union qui renvoie une fonction ; un cas se produit où notre tableau peut retourner `undefined`.
* J'ai bien aimé comment notre compréhension progresse au fur et à mesure que nous simplifions le code.
Celle-ci fait émerger des concepts implicites dans le code d'origine qui aide encore à le clarifier (ex : `Category`, `QuestionDeck`...).
* Trop court hélas.
* On s'est battu avec la couverture de code, puis on a décidé qu'elle était suffisante et que ce n'était pas l'objet du travail du jour.
* Petit problème avec IntelliJ et la couverture du code par les tests qui ne s'affichait pas sur la classe `Game`.
* Kata difficile à animer, on s'est un peu perdu au niveau déroulé, on n'a pas trouvé d'axe de refactoring qui tiennent la route.
* Les objectifs du kata sont hyper flous, ce n'est pas simple quand il n'y a pas de guide.
* On n'est pas arrivé à la penalty box, il y a un bug (on ne peut pas en sortir, mais on ne l'a pas trouvé).

Le groupe Java soulève le fait qu'ils n'ont pas établi de structure pour la prise de parole dans le mob.
Cela présente avantages et inconvénients.

* Il faut rester concentré quand on fait des tours de 4 minutes ; une durée standard en pair.
* Professionnellement, Colin fixe des temps de parole de 7 minutes en mob quand ce n'est pas un kata pour apprendre (le mob).
* Ça laisse le temps de faire son idée, ou de l'élaborer suffisamment.
* Se donner la parole, on ne l'a pas fait, c'est dommage, je ne sais pas si certains se sont, de fait, moins exprimés.
* Dans ma situation actuelle, c'était bien de ne pas avoir à m'exprimer systématiquement.
* Je ne suis pas trop pour la division égale du temps de parole.
Parfois, on a rien à dire quand c'est notre tour, et d'autres fois on en a trop.

## ROTI

- 2/5 : 1
- 3/5 : 3
- 4/5 : 7
- 5/5 : 2
