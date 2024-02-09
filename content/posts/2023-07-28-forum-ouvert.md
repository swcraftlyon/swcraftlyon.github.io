---
title: "Forum ouvert"
date: 2023-07-28T19:00:00+01:00
tags: ["unconf", "craft"]
---

- Format: Forum Ouvert
- Sujet: Parlons des relectures de nos PR/MR
- [Meetup](https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/294927796/)
- 14 personnes présentes / 21 inscrites

## Forum ouvert


### Session 1 : 19h15 - 19h45

#### Salle 1
* [Colin] Je demande 3 PRs / MRs / jour par poste ou on fait du code, ça vous semble cohérent ou délirant ? 

_2 heures :_

- pattern (d’autres que Colin font ça)
- biais cognitifif : dur de perdre plus
- son propre score : 8 par jour en moyenne, alors que TL donc réunions
- pas de PR qui partent d’une autre PR
- mergé sans que ce soit utilisé
- relecture avec un expert métier, PO (enfin, pas le code des adapters ;-) (autre exemple : le code des adapteurs sera revue par l’experte Oracle qui verra des index manquants)
- difficultés d’adoption, ça nécessite du TDD (les séniors préfèrent payer l’apéro que d’essayer)
- ensuite la CI souffre :-D
- une grosse PR créée de la frustration (des centaines de commentaires), et du gâchis (une relecture ne devrait prendre que quelques minutes pendant un temps mort) -> ça passe par dépit
- l’enfer des grosses PR (ex: sprints de 3 semaines, la dernière est consacrée aux MRs)
- ne pas chercher la PR de 2 heures tout de suite, y aller au fur et à mesure du TDD (ex : renommage de champ). Ça serait du bruit pour rien au sein du travail principal
- Inside Out, composition plutôt qu’héritage
- débit de relecture : auto-merge accepté. Priorités :
    1. prod
    2 pause quand on en a besoin
    3 relecture de PR (très petites, claires, documentées, …)
    4. dévelopement
- attention à la friction des outils (ex : GitLab vs BitBucket)
- CI : 15 minutes max par branche, 30 sur main (plus long sur main car sécurité, e2e, …). Quand ça dépasse on investi (en urgence + de matos, puis parallélisation, cache [souvent le plus rentable], …)
- CI : maintenant on différencie l’intégration (build, tests, e2e, …) de la delivery et déploiement

#### Salle 3
* [David] Est-ce que la manière de review une PR doit être harmonisée à l'échelle de l'équipe ? C'est-à-dire que chaque dev fasse la review de la même manière.

_Contexte:_

* Une équipe de 3 ou 4
* Manière très différente de faire des PR
* Première personne : commencer par les tests, si pas bon => regarder le code plus tard, si bon => regarder le code
* Autre personne possible : télécharger le code pour la review

* Pas forcément un problème de relecture de code mais plus un problème de standard dans l'équipe

* Est-ce qu'on doit harmoniser ou non ?
* Tendance à regarder l'implémentation et vérifier par les tests ont la bonne valeur
* On a tendance à savoir assez vite si le code a été écrit en TDD ou non, avec des Types ou non

* Tenter de s'harmoniser sur le but de la relecture, comprendre pourquoi c'est codé comme ça, ce que la revue par un tiers peut apporter
* Avoir en tête le nommage, les types expressifs, fonctions expressives mais ne pas s'acharner dessus
* Si c'est automatisable, l'automatiser : exemple linter
* Utilisation d'un linter qui ajoute des commentaires parfois contraignantes
* Standard de pratique que l'équipe finit par avoir en commun, exemple:
  * Exemple : si quelqu'un ne fait pas du TDD, l'accompagner vers l'approche
* Plutôt s'interroger sur le "pourquoi" que le "comment" review une PR
* But possible de la PR : transmettre à l'équipe les changements
* Rôles tournants (par semaine) avec quelqu'un qui relit toutes les PRs ?
* Beaucoup de temps à passer sur la PR lorsqu'on ne connaît pas le sujet, peut dissuader
* Présenter la PR, le problème métier et comment on l'a résolu

* Ref : podcast <https://www.codingblocks.net/>
* <https://martinfowler.com/articles/ship-show-ask.html>

* Nous sommes plusieurs à faire de l'auto review
* Les outils de reviews (MR dans GitLab par exemple) ne sont pas toujours très pratiques pour relire

### Session 2 : 19h55 - 20h25

#### Salle 1
* [Gautier] Peer review vs pair programming : dans quelles situations sont-ils pertinents?

* Contexte :
  * Ancienne équipe sur la même timezone
  * Faire des PR : point de friction
  * Certains fusionnaient les PR sans la review
  * Effet "laisser filer" sur les PR
  * Nouvelle équipe sur des timezones différentes

* Est-ce que la PR n'est pas la "pair programming" du pauvre ?
* Sur plusieurs timezones, il est difficile de faire du pair => les PR sont sans doute plus efficaces pour ça
* Si une PR reste en review trop longtemps => nécessite une séance de pair plutôt que de laisser vivre
* Proposition de durée trop longue pour nécessiter une review en pair/mob : 3 jours
* Problème de la review obligatoire : si au moins une personne est nécessaire pour une review, ça n'inclue pas le pair/mob
* Supprimer une PR => souvent mal vu par son auteur/autrice ; plus simple lorsque la décision est collégiale
* Problème des (story) points => difficile de prendre de la hauteur pour ne pas laisser trop vivre longtemps une PR
* On a beaucoup moins de soucis avec du Pair Programming qu'avec des PR en général
* Suite à un Pair, la PR peut permettre de prendre de la hauteur
* Possible de review à chaque commit
* Utilisation d'une PR à titre d'exemple sans but d'être fusionné
* Apport du "craft" : détachement de l'humain de la PR


#### Salle 2
* [Jérémy] Propriétés d'une PR/MR : Quelle taille max ? Faut-il séparer feature et refacto ? Faut il une PR pour tout ?
* [Nolwenn] Faut-il toujours demander des relectures ?

- Plus c'est long, plus c'est compliqué à relire
- Un rename peut impacter N classes, pas intéressant
- S'efforcer de faire plusieurs commits pour faciliter la relecture plutôt qu'un énorme commit
- Organisation : par défaut on review et y'a des exceptions VS l'inverse
- Limiter la taille d'une MR :
    - Découper le problème : domaine, puis ports secondaires, puis ports primaires...
    - Si grosse refacto identifiée sur code legacy => Kent beck => MR de refacto puis MR de feature
    - Pas besoin de relecture : modifications automatiques
- Code Scene => analyse de l'utilisation du code
- Code Red: The Business Impact of Code Quality (par le créateur de codescene) ->https://www.youtube.com/watch?v=X2RdwmPqBvQ
- Feature + refacto ? Rendre le changement simple avant de faire le changement

#### Salle 3
* *[Tlaop] Checklists/standards de relecture de PR ?

- Une checklist différente par PR (en fonction du niveau de séniorité, des tâches, du parcours [ex : reconversion])
- Plutôt junior : nommage, tests, extraction de méthode, … (ça tient en un écran). On n’utilisera pas la terminologie craft, les noms de patterns, … (aider à prendre confiance)
- on peut se permettre de laisser passer des erreurs
- “injustice”
- En open-source ce sera complètement différent
- les fameuses micro-PR de renommage, … du round précédent c’est ça
- chaque personne tend à faire des erreurs qui leurs sont spécifiques (typos, visibilité, …)
- se limiter dans le nombre de retours par PR
- Conventional comments : https://conventionalcomments.org/
- Faire la review avec la personne plutôt que de mettre des commentaires (bonus: facilite le mentoring)
- les joies des PRs en open-source (barrières de langues et cultures,  temporalité des merges, …)

## ROTI :

- 3 : 3
- 3.5 : 2
- 4 : 5
- 5 : 2
