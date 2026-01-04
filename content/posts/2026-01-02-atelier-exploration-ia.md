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

#### Revue des différentes versions générées

**Revue opiniated par Colin, jugée en fonction des pratiques attendues sur le projet.** Le but n'est pas de juger de la pertinence des pratiques, mais de leur respect.

Un point à noter sur le code généré : comme il a été fait sur le même repository, bien que l'on soit sur des branches différentes, il est fort à parier que le code fait sur les autres branches ait eu un impact sur les générations qui sont arrivées après.

##### 1 - [Pas d'exemple + instructions TDD](https://gitlab.com/damon.colin/superextra/-/merge_requests/1)

Pour cette première génération naïve, nous n'avons pas fourni d'exemple. Un simple `/init` suivi d'un ajout d'instructions pour faire du TDD, suivi de ce prompt :

```
Add rules for ID in CLAUDE.md Ids must use UUID wrapped in specific record with parameter beeing called value

Create Skill entity. A Skill have:

- An ID
- An internationalized label
- An internationalized description

for internationalization create a Labels value object that must have a French label. Use java Locale as key. If there is no French label create a dedicated SuperextraException.
Create the endpoints to manage skills:

- Create a skill
- Get a skill
- Paginated list of skills
```

On note immédiatement que le code généré est loin de ce qui est attendu dans les normes poussées par Seed4J :
- La branche ne build pas : certaines règles checkstyle ne sont pas respectées ;
- Les tests sont trop proches des détails d'implémentation, par exemple en testant les getters ;
- Beaucoup de Javadoc, souvent inutile ;
- Pas d'utilisation systématique des outils existants dans la codebase (ex : `Collections.unmodifiableMap(new HashMap<>(values));` au lieu de `SuperextraCollections.immutable(...)`) ;
- Pas de gestion des authorizations ;
- Création compléte des objets du domain dans le controller là où le passage d'une commande à un aggregat devrait être la responsabilité du domain ;
- ...

De bonnes choses qui ont été faites :
- Utilisation du système d'exceptions internationalisées ;
- Wrapping des primitives ;
- Respect de l'architecture ;
- ...

Si cette implémentation est loin de suivre les normes attendues (mais pas clairement exprimées), elle n'en reste pas moins impressionnante sur de nombreux points.

Ce n'est qu'un ressenti, mais je pense que le temps de correction du code de cette version est supérieur au temps nécéssaire pour le faire manuellement. Ici, je ne pense pas qu'il y ait de gain de temps humain.

##### 2 - [Exemple + instructions TDD](https://gitlab.com/damon.colin/superextra/-/merge_requests/3)

Cette seconde génération a été faite en ayant un exemple de l'attendus dans la code base et des instructions pour faire du TDD ont été ajoutées dans le `CLAUDE.md` après sa génération.

Dans cette version les `Labels` ont été mis dans un shared kernel dans une seconde itération.

Le code généré est plus proche des standards attendus dans le projet :
- Pas de Javadoc inutile ;
- Des commandes et domain service pour créer les objets ;
- Utilisation des outils présents dans le repository ;
- ...

Par contre, pour les exceptions, on est revenu à une `RuntimeException`, pas d'utilisation de la gestion d'erreur internationalisée.

Bien qu'il reste du travail pour avoir quelque chose aux standards cette version à plus de chances de permettre de gagner du temps humain même si ce n'est pas encore une évidence.

##### 3 - [Exemple sans instructions TDD](https://gitlab.com/damon.colin/superextra/-/merge_requests/4)

Cette troisième génération a été faite avec un context d'exemple, mais sans donner d'instruction pour faire du TDD.

Le build ne passe pas :
- Erreur de formatage, le check ne valide pas ;
- Un test est en erreur.

Quelques problèmes :
- Du code mort, notamment avec des getters systématiques ;
- Pas d'utilisation des exceptions internationalisées.

Mais aussi de bonnes choses :
- Utilisation d'une query custom pour la pagination en triant sur un champ dans un JSONB => je ne connaissais pas, j'ai appris quelque chose ;
- Génération plus rapide (je n'ai pas pensé à noter les temps, mais 2/3 fois plus rapide de mémoire) ;
- Respect de l'architecture ;
- Des tests unitaires globalement corrects même si encore trop proches des détails d'implémentation.

À mes yeux, cette génération est un peu meilleure que la 2, mais je ne sais pas dire à quelle point elle a été facilité par les itérations précédentes.

##### 4 - [Outside-in TDD](https://gitlab.com/damon.colin/superextra/-/merge_requests/8)

Cette quatrième génération a été faite avec :
- [Des rules](https://gitlab.com/damon.colin/superextra/-/merge_requests/7) pour lesp ratiques du project ;
- Un agent pour faire de l'Outside-in TDD.

Quelques problèmes :
- Toujours pas d'exception internationalisée...
- Deserialization de `RestLabels` en utilisant les setters plutôt qu'un constructeur ;
- Pas d'utilisation de `ReponseEntity.of(...)` pour gérer une 404 quand un skill n'est pas trouvé (code généré qui fait la même chose) ;
- Tests de getters ;
- Mauvaise utilisation des assertions cucumber custom au projet. Ça fonctionne, mais c'est moins pratique que ce qui est faisable
- ...

Si cette version à encore des défauts, on est sur quelque chose qui peut être repris très rapidement, surtout que les règles peuvent être affinées pour corriger ces problèmes.

##### 5 - [Inside-out TDD](https://gitlab.com/damon.colin/superextra/-/merge_requests/9)

Cette cinquième génération a été faite avec :
- [Des rules](https://gitlab.com/damon.colin/superextra/-/merge_requests/7) pour lesp ratiques du project ;
- Un agent pour faire de l'Inside-out TDD.

Des petits défauts, mais cette version est la plus proche de ce qui aurait pu être fait à la main. Par contre, elle a été très coûteuse en temps et en tokens (je n'ai pas noté, mais, de mémoire, 1h).

##### 6 - [Test after](https://gitlab.com/damon.colin/superextra/-/merge_requests/11)

Cette cinquième génération a été faite avec :
- [Des rules](https://gitlab.com/damon.colin/superextra/-/merge_requests/7) pour lesp ratiques du project ;
- Un agent pour faire du test after.

Des défauts vraiment gênants dans cette version :
- `RestLabels` qui n'affiche que les labels FR et EN ;
- Des tests très proches des détails d'implémentation (ex `SkillsApplicationServiceTest`) ;
- ...

Même si cette version se génère un peu plus vite, elle ne fournit pas le filet de sécurité qui permettra de reprendre sereinement le code. 

##### Conclusion

Toutes les versions ont le même défaut : elles prennent beaucoup de micro-décisions auxquelles il faudra être attentif. Exemples de micro-decisions qui posent problémes dans l'exemple :
- Gestion des droits :
  - Certaines génération ont demandé ;
  - D'autres ont décidé que les `ADMIN` peuvent créer et les `USER` lire ;
  - D'autres ont décidé que tout le monde pouvait tout faire ;
  - Un a même supprimé l'authentification dans un premier temps avant qu'on demande de la remettre.
- Gestion des label. Aucune n'a voulu renvoyé le label en fonction de la langue passée en header de la requête ce qui est probablement ce qui aurait fait lors d'un développement "classique". C'ets une faiblesse du prompt, mais penser à toutes ces choses en amont est impossible.

Pour mitiger ça, faire des itérations plus petites est probablement une bonne idée. Avec le mode plan il y a plus de chances que des questions soient posées à chaque micro-décision, mais, même là, on ne peut pas être certain·e·s de ne rien louper. 

#### Resources

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
- [Prompt TDD Kent Beck](https://gist.github.com/spilist/8bbf75568c0214083e4d0fbbc1f8a09c)

### Gemini CLI

#### Tokens

Nous avons pu faire plusieurs itérations en étant bien loin de la limite d'utilisation des tokens.

#### Context windows

En plus de la limite d'utilisation des tokens, il faut tenir compte de la context windows, nombre maximal de token pour une session.

Elle est de 260k pour Claude Pro et 2M pour Gemini et Claude Max.

Il faut en théorie garder celui-ci petit (<100k) sous peine de voir sa consommation de token exploser et les résultat s'appauvrir (voir [Attention Is All You Need](https://proceedings.neurips.cc/paper_files/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf)).

Gemini CLI a un bug, qui déclenche un `429` et change de modèle quand la context windows est trop grosse, ce qui force à `/clear` souvent.

#### Concepts

- **Command** : prompt nommé réutilisable

Gemini CLI est plus basique, il n'y a pas de plan mode, ni de sub-agents (gérés par un autre outil, _jules_), ni skills, etc.

#### Commandes
Quelques commandes utiles utilisées pendant la session :

- `/init` : Fait générer un fichier `GEMINI.md` en fonction de ce qui existe dans le projet. Pas certain que l'impact soit si important quand le prompt est bon
- `/clear` : Remet à zero le context. Nécéssaire pour limiter la consommation de tokens.
- `/compact` : Pour compacter le contexte et on peut lui spécifier quoi garder. 
- `/stats` : Permet de voir où on en est dans l'usage
- `gemini --resume` : Pour relancer un Gemini en lui demandant de reprendre là où le précédent s'est arrêté.

#### Notes et impressions
Gemini 3.0 PRO (modèle) est un peu moins bon que Sonnet & Opus 4.5, ça peut être partiellement compensé par un meilleur prompting, mais le problème vient surtout de l'absence de plan mode.

À tenter avec un autre agent comme [OpenCode](https://opencode.ai/).

L'autre souci vient aussi de la méthode de comparaison qui se base sur un "one-shot prompt" avec le minimum d'info, ce qui est l'inverse de l'approche prise pour le test avec Gemini (prompt détaillé avec plusieurs itérations).

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
