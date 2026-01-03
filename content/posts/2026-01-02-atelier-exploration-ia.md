---
title: "Exploration augmented coding"
date: 2026-01-02T14:00:00+02:00
tags: ["ia"]
---

## Sujet 
Exploration de différentes IA de développement.  
Le but est d'ajouter une feature dans [ce projet](https://gitlab.com/damon.colin/superextra) qui a été généré avec [Seed4J](https://github.com/seed4j/seed4j).  

L'objectif métier du projet est de faciliter la mise en relation de freelances dans les métiers du service (service en salle, cuisine, plonge, ...) et des personnes qui ont besoin d'extra. Pour ça, les freelances doivent s'inscrire sur la plateforme et renseigner leurs informations. Dans ces informations elles seront amenées à sélectionner leurs `Skills` qui seront essentiels pour la suite.

Pour l'exercice nous nous sommes concentré sur la gestion d'un catalogue de `Skills`. Un `Skill` c'est :
- Un identifiant (sous forme d'UUID) ;
- Un label internationalisé ;
- Une description internationalisée.

Pour les textes internationalisés, on utilise les `Locale` de Java et il faut forcément renseigner le Français. Lors de la récupération du texte, on obtient soit lel texte dans la locale si elle existe soit du Français.

En amont de l'atelier quelques expérimentations ont été faites :
- [Génération du contexte sans donner d'exemple de code](https://gitlab.com/damon.colin/superextra/-/merge_requests/1) ;
- [Génération du contexte avec un exemple de code d'un autre contexte](https://gitlab.com/damon.colin/superextra/-/merge_requests/3) ;
- [Génération avec exemple de code et instructions pour faire du TDD](https://gitlab.com/damon.colin/superextra/-/merge_requests/4).

## Déroulé
Pour les différentes phases d'expérimentations, nous nous sommes repartis en 3 groupes :
- 2 avec Claude Code ;
- 1 avec Gemini.

Pour la première itération les 3 groupes sont partis de la [branche avec un exemple](https://gitlab.com/damon.colin/superextra/-/merge_requests/5) et ont essayé de créer des skills permettant la génération de contexte.  

Nous avons ensuite fait une première mise en commun de nos trouvailles et enchainer sur une seconde itération, avec pour objectif de créer un agent.

## Apprentissages

Cette section rassemble nos apprentissages après quelques heures. **Nous ne sommes pas expert·e·s, les informations présentées ici peuvent être fausses !!!**

Un questionnement en commun sur les deux IA testées : comment gérer ce nouveau flux de travail ? Même si ces IA génèrent du code rapidement, il y a quand même plusieurs minutes (voir dizaines de minutes) entre deux actions. Il faut donc trouver comment gérer ce rythme. Nous avons envisagé / explorer :
- L'utilisation de plusieurs générations en parallèle
  - Nous avons fait des tests avec lew worktree git (`git worktree add ../project-feature-a feature-a`, `git worktree remove ../project-feature-a`) qui fonctionnent bien
  - Nous avons discuté de la possibilité d'utiliser des agents directement pilotés par la CI
- Travailler à des tâches d'analyses / de préparation du prompt suivent en attendant le résultat du premier
- De faire des actions toute autres, mais probablement pas une bonne idée pour le context switching.

Ces discussions sur l'organisation du travail en ont créé d'autres sur les impacts sur la santé mentale :
- La relecture de milliers de lignes de code générées n'est probablement pas passionnant à moyen terme, surtout qu'il faut essayer de rester attentif·ve·s à toutes les micro-décisions prises dans le processus ;
- Le context switching permanent pose aussi question.

### Claude

#### Tokens

Nous avons très vite compris que les tokens seraient le nerf de la guerre et nous avons rapidement épuisé nos quotas. 
Nous avons fait un essai en changeant de modèle, mais les résultats n'étaient pas satisfaisants sur le modèle le moins couteux en tokens (Haiku).  

Un groupe a changé de souscription pour passer sur un forfait à ~100 € mensuel (c'était prévu et ça n'a pas posé de problème particulier). L'abonnement à 20 € / mois ne permet clairement pas de travailler toute la journée avec l'outil.

Sur la suite de la journée, optimiser l'utilisation des tokens a été un fil rouge.

#### Concepts

- **Command** : description de commandes qui seront utilisées telles qu'elles par Claude.
- **Rule** : Règles qui s'appliquent à un ensemble de fichiers, on donne le pattern de fichiers et Claude les appliquent automatiquement.
- **Skill** : Instructions pour faire une action donnée. Claude s'appuie dessus s'il découvre qu'il doit faire opération.
- **Agent** : Instructions pour prompter un agent qui va orchestrer différentes opérations.

Pour générer ces différents éléments, nous avons demandé à Claude de le faire en se basant soit sur le contexte d'exemple soit sur la documentation générée par Seed4J. Nous avons ensuite repris les fichiers générés.

- [Un premier set de rules, commandes et agents](https://gitlab.com/damon.colin/superextra/-/merge_requests/7)
- [L'agent qui fait du test after](https://gitlab.com/damon.colin/superextra/-/merge_requests/10)
- [Set de rules manquantes](https://gitlab.com/damon.colin/superextra/-/merge_requests/12) (fait en demandant simplement à Claude de générer les règles manquantes en se basant sur le code existant)

Nous nous sommes rendu compte que Claude est vraiment bon pour trouver des patterns dans du code existant et en faire des règles. Une approche dans laquelle on fait un exemple et on s'appuie dessus pour faire la configuration de Claude est probablement une bonne idée.

En générant ces fichiers, non seulement on obtient du code plus proche des pratiques que l'on souhaite, mais on économise aussi beaucoup de tokens qui sont clairement le nerf de la guerre !

#### Commandes
Quelques commandes utiles utilisées pendant la session :

- `/init` : Fait générer un fichier `CLAUDE.md` en fonction de ce qui existe dans le projet. Ce fichier est essentiel pour avoir des résultats probants !!!
- `shift + tab` : Permet de changer de mode pour passer en `plan mode` qui permet de répondre à des questions et d'ajuster le plan avant de lancer la génération. Avec cette approche, nous avons observé de bien meilleures générations !
- `/skills` : Liste les skills disponibles. Très utile pour savoir si notre skill fraichement crée est bien pris en compte :D.
- `/context` : Pour voir le remplissage du context.
- `/clear` : Remet à zero le context. Nécéssaire pour limiter la consommation de tokens.
- `/compact` : Pour compacter le contexte et on peut lui spécifier quoi garder. 
- `/agents` : Permet de voir les agents existants, mais surtout d'en créer de nouveaux en étant guidés.
- `/status` : Permet de voir où on en est dans l'utilisation de Claude, on peut changer d'onglet avec tab et shift + tab.
- `/model` : Permet de consulter le modèle utilisé et de changer au besoin.
- `/ide` : Pour lier le terminal system à l'IDE et avoir les demandes de validation dans l'IDE tout en gardant le terminal système.
- `ctrl + t` : Pour voir toutes les taches.
- `ctrl + o` : Pour voir la sortie de tous les agents. Très utile quand un agent nous pose une question et qu'on ne la voit pas, mais qu'on doit y répondre :D.
- `claude -c` : Pour relancer un Claude en lui demandant de reprendre là où le précédent s'est arrêté.

#### Consoles
Pendant une partie de la session, nous avons utilisé l'intégration de Claude Code dans IntelliJ mais ce n'est clairement pas au point :
- Glitch graphiques ;
- Mauvaise lisibilité ;
- Grosse impression de lenteur.

L'utilisation d'un terminal en dehors de l'IDE semble, pour le moment, plus adapté.

### Resources

- [Best practices Claude Code](https://www.anthropic.com/engineering/claude-code-best-practices) vraiment un très bon article !
- Collections de skills & agents Claude Code :
  - https://github.com/giuseppe-trisciuoglio/developer-kit
  - https://github.com/anthropics/skills
  - https://github.com/meetrais/claude-agent-skills
  - https://github.com/lodetomasi/agents-claude-code
  - https://github.com/wshobson/agents
  - https://github.com/VoltAgent/awesome-claude-code-subagents
- [Documentation des skills](https://code.claude.com/docs/en/skills)
- [Pricing des modèles](https://platform.claude.com/docs/en/about-claude/pricing)
- [Suivi consommation](https://claude.ai/settings/usage)
- [Astuces pour économiser des tokens](https://gist.github.com/artemgetmann/74f28d2958b53baf50597b669d4bce43)

## Retrospective

Super session : permet de voir ce que l'on entendait sur l'utilisation des agents pour du code. La comparaison Claude Code VS Gemini était aussi intéressante

Super intéressant. J'expérimente depuis quelques mois et comparer avec les explorations des autres personnes est intéressant. Plein de choses à apprendre, à comprendre sur le prompt, l'usage etc.

Très cool. Ça permet de prendre le temps de creuser le sujet. Voir le comportement, la consommation de tokens, ...

Pas vu le début, mais la fin était intéressante avec le côté "one shot" d'une feature et la discussion sur les impacts sur la santé mentale.

Je suis venu en tant que "réfractaire", notamment à cause de la hype et, au final, je suis assé perplexe du résultat mais, en même temps, il y a des risques sur toutes les micro-décisions. Ça a probablement un impact sur le rythme et l'organisation du travail. Un autre point me dérange, c'est le fait que ça ne soit pas prédictif ce qui est un problème. +1 sur tout ça

Pas très convaincu par l'outil :
- Impact sur les micro-décisions ;
- Comment gérer le context switching ;
- L'impact environnemental et le fait que les sociétés n'aient, pour le moment, pas d'intérêt à optimiser ce point dans un contexte de forte concurrence économique.

À voir si on a une amélioration sur la consommation énergétique pas la suite, si ça devient une priorité. Une chance que ça arrive par les impacts économiques, mais est-ce que ça mitigera l'augmentation de l'usage... Probablement pas

Au niveau économique : toute la croissance US est basée sur cette bulle, que vas-t-il se passer quand elle va exploser ?

## ROTI (après beaucoup de départs...)

Nous étions environ 30 au début de cet atelier de 4 heures, mais beaucoup de personnes sont parties avant la fin. En 
partant, elles ont donné de bons feedbacks sur la session que nous n'avons pas formalisé sous forme de note.

- 2/5 : 1
- 3/5 : 2
- 3.816844 : 1
- 4/5 : 4
- 4.5/5 : 2
- 5/5 : 3
