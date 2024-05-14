---
title: "Reprendre la main sur mon backend Node (Testing & refactoring)"
date: 2024-05-14T12:20:15+02:00
tags: ["atelier"]
---

- Sujet : Reprendre la main sur mon backend Node (Testing & refactoring)
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/300920814/)
- Format : Deux mobs de 5 et 6
- Nombre de participants : 12
- Des premières participations

## Contexte

Il s’agissait de tester un atelier de deux heures qui se tiendra à la conférence Tech & Wine le 18 juin (https://technwine.fr/).

La base de code est disponible sur [github](https://github.com/jsorant/talks).

## Retrospective

### Propositions d'amélioration

- Démarrage difficile avec Supertest pour le groupe dans lequel l'animateur n'était pas là. Proposition : écrire le squelette du premier test pour ne pas avoir à chercher la doc de Supertest
- Retirer TestContainers et le présenter en conclusion
- Consignes plus directives (par exemple : le test doit couvrir la ligne N).
- Ecrire qu'il faut pas tester la route "/"
- Faire évoluer le README à chaque step
- Ajouter des hints de plus en plus précis
- Créer une page html pour consommer l’API et s’éviter un postman ou une extension dans l’IDE.
- Mettre des exemples de retours API (histoire d’avoir un id mongo valide).

## ROTI

- 3/5 : 1
- 4/5 : 5
- 4.5/5 : 1
- 5/5 : 2
