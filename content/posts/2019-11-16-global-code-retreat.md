---
title: "Global Code Retreat Samedi 16 November 2019"
date: 2019-11-16T09:43:18+02:00
tags: ["gdcr"]
aliases: [/posts/global-code-retreat-16-11-19/]
---

- Sujet : [Langton Ant](http://codingdojo.org/kata/LangtonAnt/)
- Format : Pair programming
- Langage : Java, Python, C++, Scala, TypeScript, F#, Kotlin
- Nombre de participants : 25

## Objectif

- Améliorer nos pratiques de code

## Déroulement

- Présentation du sujet
- 6 itérations de 45 minutes avec une contrainte différente à chaque itération suivie de 15 minutes de debrief
- TDD et pair/mob programming à chaque itération

## Itération 1 : Mise en place

Compliqué à lancer, approche TDD difficile quand pas l'habitude.  
Deux grandes étapes : switch color & switch direction.  
Nécessite de connaitre uniquement ses voisins.  
Par quoi commencer ? La grille ? La fourmi ?  
Composition de comportements simples : changement de direction, de couleur.  

## Itération 2 : Reset-hard toutes les 2 minutes

2 minutes un peu short, mais force à discuter en amont.  
Limite de temps pousse à simplifier, s'en tenir à l'essentiel.  
Plusieurs fois itération beaucoup trop grosse -> bien redécouper après.  
Appris beaucoup -> Eclipse (raccourcis clavier).  
Logique fonctionnelle en peu de temps.  
2 minutes tests et code puis 2 minutes refactoring.  
Toutes les 2 minutes clavier change de main.  
Partir du bas, car baby steps.  
Pas de structure de contrôle.  
Impose de partir beaucoup plus petit -> parti de la grille, mais très simple.  
On ne peut pas pousser un refactoring en 2 minutes.  
Pousse à faire des refactoring pas cassants.  
Comment amener de la fonctionnalité en 2 minutes.  
Donne lieu à plein de stratégies.  
Pas facile de voir avantages dans le stress.  
Manque un outil comme un sablier.  
Des mini-rétros pas comptées dans le temps (parfois entre chaque itération).  
Tant que l'on ne touche pas au clavier, pas de chrono.  
Pas grave de jeter le code.  

## Itération 3 : Code immutable

Pas d'attributs, uniquement des constantes.  
Découverte de F# & Scala : immutabilité naturelle, bonne introduction au fonctionnel.  
Découvre encore des choses sur Kotlin, même en s'en servant tous les jours.  
Pas vécu comme une réelle contrainte (pour certains), juste une autre façon de faire.  
Frustration de ne pas arriver plus loin dans le kata après trois itérations -> est-ce que l'approche de l'exercice a changé après trois itérations ?  
C++ peut définir des méthodes constantes, elle ne peut pas changer un état.  

## Itération 4 : Blind navigator

Il faut partir petit => vraiment en aveugle.  
Mieux vaut un truc qui marche, mais mal refactoré plutôt qu'un truc à moitié fait.  
Itération stable.  
En tant que navigateur (celui qui donne les instructions), on a beaucoup de pouvoir.  
Oblige une communication permanente : celui qui a le clavier doit parler.  
Capacité d'écoute de partout.  
Partie très lourde côté navigateur : détails.  
Pas besoin de penser à la syntaxe (en tant que navigateur).  
Corresponds au quotidien.  
Capable d'échanger sans subordination.  
Trouver granularité du test.  
Manque une boucle de feedbacks avec l'aspect "aveugle", feedback nettement plus long.  
Permets d'aller au bout de l'idée sans la tuer dans l'oeuf : le navigateur va au bout de son raisonnement.  
Quand on se voit, impression d'être au casque.  
Expression corporelle importante, compensation par des précisions.  
Suggestion d'évolution : mauvais son.  

## Itération 5 : Porter un maximum d'informations sur l'état dans le type

Beaucoup d'objets à créer et maintenir.  
Simple tant qu'on ne gère pas la grille.  
Tous les cas doivent être représentés.  
Pour ne pas stocker la grille, on peut appeler une fonction qui retournera la fonction pour le prochain tour (usage de la récursivité).  
Questionne beaucoup plus sur la responsabilité de chaque type.  

Cardinalité d'une cellule (hypothèse : la cellule ne connaît pas ses coordonnées) :  

```
  Couleur * Direction option
    = 2 couleurs * (Pas de fourmi + une fourmi avec 4 directions)
    = 2 * (1 + 4)
    = 10 états (types) possibles pour une cellule
```

Proposition de variante : pas de primitive et pas de cas interdit.

## Itération 6 : Test && commit || revert

Test + code + refactor puis exécute les tests : créé beaucoup d'enjeux.  
Réutilise plus du code sur lequel on connaît le comportement.  
S'assurer d'avoir un test qui marche et d'aller au plus simple, puis commit avant de refactorer.  
Les enjeux et le stress générés reviennent souvent, on va au plus petit possible (test, micro-refactoring).  
Presque tout le monde a dû revert au moins une fois.  
Bon exercice pour savoir si nos tests sont trop gros.  
Idée : sprint & démo || revert  

## ROTI

- 24 votants
- ROTI 5/5 -> 8 personnes
- ROTI 4/5 -> 16 personnes
