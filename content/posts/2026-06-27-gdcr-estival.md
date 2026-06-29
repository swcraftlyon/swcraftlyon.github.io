---
title: "Code retreat estival"
date: 2026-06-27T09:00:00+02:00
tags: ["kata", "code-retreat"]
---

- [Meetup](https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/315022846/)
- Sujet : [Trivia](https://github.com/jbrains/trivia)
- Langages : Java, TypeScript, Python
- Nombre de participants : 12

## Session 1 : Golden Master

- Quelques galères de setup de Python, de blagues de NodeJS.
- Choix de fixer le random ou de tester méthode par méthode.

## Session 2 : Primitive obsession

- Frustant de ne pas aller au bout -> faut coder plus vite !
- Quelques galères de fin de ligne avec Windows
- Création de classes Player avec un état en Python, découverte que la sortie de prison n’est jamais appelé.
- Création de Players qui gère de joueur courant sans index

## Session 3 : Choix du public
### Propositions
- pas de return
- pas de contrôle de flux (vainqueur)
- immutabilité
- TCR 30 secondes
- supprimer les effets de bord
- monade
- limiter les mots clés du langage
- blind navigator
- ne rien modifier à la main
- pas plus de 3 lignes par fonction

### Retours
- Quel est le bon point d’entrée pour attaquer un refacto (30 secondes pour être vert), comment : dupliquer le code, méthode mikado
- chercher à avoir du polymorphisme
- utilisation de map ou d’optional

## Session 4 : Tell don’t Ask
- fallait inliner comme des crados mais bien compris l’intérêt de la contrainte
- pas de retour (auteur : Antho)

## Session 5 : Immutabilité
- très poussif, il ya beaucoup à faire
- repousser la mutation au plus loin mais en commençant au niveau des méthodes en conservant un état mutable global

## Rétro globale
- Merci pour le petit déj \o/
- toujours pas la joie comme kata mais ça se fait !
- Sympa de voir des gens, refaire du Java dans un IDE
- Première fois passionnante, permet de voir des problèmes différents du quotidien, de voir les manques de connaissances à combler
- Agréable d’être en petit comité, permet de passer plus de temps avec les gens, moins de frictions
- limite sur le setup, Golden master compliqué entre les sorties console et le random

## ROTI

- 3/5 : 3
- 4/5 : 6
- 5/5 : 4
