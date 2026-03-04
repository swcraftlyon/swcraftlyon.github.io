---
title: "Open forum : IA et Craft"
date: 2026-01-27T19:00:00+02:00
tags: ["unconf"]
---

* Meetup : https://www.meetup.com/fr-fr/software-craftsmanship-lyon/events/313583278/
* Sujet : IA et Craft
* Lieu : Discord
* 32 présents / 45 inscrits

## Brainstorming

### Salle 1
- Est-ce que l'architecture hexagonal est pertinent·e dans le développement assisté par IA ?
- Est-ce que la pré-modélisation du métier avant de donnée à l'IA est pertinent·e dans le développement assisté par IA ?
- Est-ce que la réduction des commentaires inutile avec le code est pertinent·e dans le développement assisté par IA ?
- Est-ce que le mob est pertinent·e dans le développement assisté par IA ?

### Salle 3
- Est-ce que l'IA locale est pertinente dans le développement assisté par IA, par rapport au flow (lenteur) ?
- Est-ce que l'IA est pertinente en TDD ou vaut mieux travailler en mode plan ?
- Est-ce que l'IA est pertinente en review et est-ce que les dev vont "juste" devenir des reviewers. à terme ?

### Salle 4
- Est-ce que un budget limité est pertinent·e dans le développement assisté par IA ?
- Est-ce que la comprehension du code est pertinente dans le developpement assiste par IA?
- Est-ce que le pair programming est pertinent dans le developpement assiste par IA?
- Est-ce que la maitrise des competences profondes est pertinente dans le developpement assiste par IA?

### Salle 6
- Est-ce que TDD est pertinent dans le développement assisté par IA ?
- Est-ce que les tests manuels sont pertinents  dans le développement assisté par IA ?
- Est-ce que que le pair programming est pertinent dans le développement assisté  par IA ?
- Est-ce que les ADRs sont pertinents dans le développement assisté  par IA ?
- Est-ce que SCRUM est encore pertinent dans le développement assisté par IA ?

## Session 1

### Salle 1 - TDD
- Avec l'IA, je ne pratique plus le TDD
- Avec l'IA, on peut faire des steps plus grosses qu'en TDD
- J'ai l'impression que la distinction green/refactor fusionne en 1 seule étape avec l'IA
- Pour ceux qui ne font pas de bons tests, ça amplifie les problèmes
- Donner des "skills TDD" à une IA pourrait permettre d'avoir des tests de meilleure qualité que sans, surtout pour des gens voient les tests comme une contrainte. Est-ce que TDD ne vit pas sa 2nde vie ?
- Avec l'IA, les tests sont moins chers à écrire, il les fait mieux que moi
- Est-ce que l'IA écrit les tests, le code ou les 2 ?
- En itérant, on peut obtenir un contexte qui permet d'être plus minimaliste dans la demande tout en obtenant un résultat très proche de ce qu'on souhaite

### Salle 2 - Bounded Context / Subdomains / Context map


### Salle 3 - IA Local / budget limité


### Salle 4 - Archi domain centrics / architecture hexagonal

- REX de Cloudflare sur leur réécriture de Next.JS avec une semaine, un dev, 1100$
- “Most abstractions in software exist because humans need help. We couldn't hold the whole system in our heads, so we built layers to manage the complexity for us. Each layer made the next person's job easier. That's how you end up with frameworks on top of frameworks, wrapper libraries, thousands of lines of glue code.
- AI doesn't have the same limitation. It can hold the whole system in context and just write the code. It doesn't need an intermediate framework to stay organized. It just needs a spec and a foundation to build on.”
- https://blog.cloudflare.com/vinext/

- À l’inverse ManoMano est à fond pour : https://www.ifttd.io/episodes/ia-devx

- Question de finances et taille de contexte

- Question du contrôle quand ça devient complexe (REX de start-up studio qui invite à limiter le MVP à peu de features car après ça s’écroule)

- Les IA génèrent beaucoup de code

- Selon la charge des serveurs les résultats sont plus ou moins performants en termes de qualité

### Salle 5 - Réduction des commentaires inutiles avec le code


### Salle 6 - Mob/Pair/Collaboration entre devs

- Ennuyeux avec session IA
- Pair avec l'IA plus productif qu'avec des collègues?
- Gain sur la vélocité au niveau de la valeur ajouté?

### Salle 7 - Review/Place dev/Compréhension du code/Compétence du dev

- Review reste importante pour relire le code genere par l'IA. Elle semble toujours necessaire puisque l'IA est faillible. La charge cognitive reduite sur l'ecriture de code est recupere dans la relecture de morceaux de code important.
- Dans un contexte propre et deja structure, l'IA invisibilise les competences profondes qui sont deja mis en place et donnent des exemples pour les nouvelles fonctionnalites.
- Dans un contexte de base de code legacy qui n'est pas homogene, l'IA a tendance a privilegier l'approche la plus presente statistiquement plutot que d'utiliser les nouvelles structures decidees en equipe. L'IA n'a pas de parti pris contrairement aux developpeurs.
- Sur des sujets non triviaux (achitecture, decoupage des BC) on voit encore du code de mauvaise qualite.
- Plus on restrain l'ensemble dans lequel l'IA peut travailler plus elle va respecter des decisions strictes et suivre des decisions d'equipe => Travaille d'une maniere opposee a celle habituelle quand on travaille avec des juniors.

## Interlude : adoption au quotidien

* Pas au quotidien, usage perso de ChatGPT
* Depuis 10 mois, de plus en plus, cadre au maximum ses prompts/contexts, écrit peu de code, relis beaucoup
* Migration de l'usage en tant qu'intellisense, vers de l'usage multi-agent (un à la fois), 20-30% d'écriture de code
* 100% d'écriture de Claude, transcript -> ticket -> code -> deploiment, micro PRs, 100% de relecture
* Intellisence avance, stack overflow, refactoring
* Usage rare (debug)
* Pas le droit de l'utiliser sur le code, usage autant que possible à côté
* Quasiment pas d'usage, tentative de LLM local
* Usage de Claude Code depuis Janvier sur les projets perso
* Intellisence avance, stack overflow, refactoring
* Lovable (CTPO), Intellisence avance -> BMAD/agents
* Usage depuis Janvier de Codex, 100% d'écriture et de code review
* Copilot sur du Terraform (refactoring/nouveau modules), Antigravity en perso
* Coach de dev sans IA, expérimentations IA en perso, usage de l'IA pour expliquer du legacy
* 100% d'écriture de code (Claude), 5-10% de relecture, Lovable par les commerciaux
* Chat-based en entreprise, 100% d'écriture avec Claude code sur les projets perso, usage de Claude/Codex pour la relecture
* Copilot pour completion en entreprise, Claude code en perso, relecture à 100%
* Claude Code en majorité, 100% de relecture, ChatGPT uniquement au travail, perte de l'aspect sociale du craft
* Chat uniquement, paratgé sur les agents
* Début il y a 1.5 ans, accélération il y 4 mois, usage pour la veille et 100% du code généré, 80% de relecture du code
* Principalement avec Open Code, commencé il y a ~6 mois, surtout sur le boilerplate. Relus a 100%, d'abord par des agents puis personnellement. Beaucoup utiliser pour la veille et pour le débug
* (Enseignante) usage pour expérimentation, introduire l'IA à ses étudiants, utilisation comme point de départ, maquette, README, GitHub Actions workflows
* Full agents, recherche des limites des agents

## Session 2

### Salle 1  - ADRs
### Salle 2  - Scrum AKA le groupe d'irresistibles gaulois qui veulent pas fusionner dans le monogroupe (mais y'a toujours qu'un seul scribe --')
- La plupart du temps Scrum est utilisé de façon bureaucratique et n’a pas de sens
- Mais à la base c’est une démarche produit (pour itérer et incrémenter) et une façon d’animer une équipe

- Utilisation de “Kanban” pour la coordination plutôt que des itérations figées
- Quand on est ensemble ce n’est plus produire de la feature (ex : propositions UX)

- Claude enforce les règles dans le claude.md, le code est uniforme malgré des façons différentes de travailler

- La prochaine frontière c’est le produit (on livre plus de code, mais livre-t-on plus de valeur ?), ce pourquoi Scrum était inventé à la base.
- Mais Scrum date des années 80, on a mieux depuis, cf. par exemple : https://www.buildtosellbook.com/

- “Le vieux monde se meurt, le nouveau est lent à apparaître, et c'est dans ce clair-obscur que surgissent les monstres.” — Antonio Gramsci

### Salle 3 - Design up-front
### Salle 4 - Mob/Pair/Collaboration entre devs
### Salle 5 - Intérêt du métier de dev
- Au bout d'une semaine crise existancielle => Il peut challenger le metier, decouper, produire du code de qualite, s'ameliorer en continue...
- Nous libere du temps pour faire du refacto qui n'etais pas possible precedemment. Vers une casquette de PM?
- Est-ce que le code produit cree de la valeur? => Avant les objectifs etaient trop ambitieux pour l'equipe et n'arrivait pas a absorber les demandes, maintenant on arrive a etre en avance. Les features sont mesurees en terme d'usage ce qui permet de valider ou non la reussite des features.
- Le cas est tres specifique, la boite a un processus tres bien rode et le facteur limitant etait le code.
- Moins voir plus du tout de fierte apres la livraison d'une feature.
- Crise existancielle sur les competences qui sont transferes a un outils comme les ouvriers dans l'automobile => Quel metier ne va pas etre impacte?

### Salle 6 - Intérêt du métier de dev

### Salle 7 - Review/Place dev/Compréhension du code/Compétence du dev
### Salle 8 - Enseignement

## Rétrospective de l'événement
* Retours intéressants (success story)
* Beaucoup d'exemples de workflow
* Pas forcément de meilleurs résultats en copiant des skills exemples
* Retours d'expériences variés

### ROTI

* 2/5 : 2
* 3/5 : 4
* 4/5 : 6
* 4.5/5 : 1
* 5/5 : 8

