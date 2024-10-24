---
title: "Forum ouvert des communautés francophone Mercredi 23 octobre 2024"
date: 2024-10-23T18:00:00+02:00
tags: ["forum-ouvert"]
---

- Sujet : Forum ouvert des communautés craft francophone
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/303232450/)
- Format : Forum ouvert
- Nombre de participants : 20

## Sujets

### AMA : écrire et publier un livre

Animé par **Colin**.

Le ROI direct n'est pas terrible, mais il peut être plus intéressant de manière indirecte.

Écrire parce que ça le détend.

Parce que c'est le média qu'il consomme.

Résumé : Écrivez un bouquin ! C'est cool !

### Mentorer quand on est junior

Animé par **Adeline**.

Le mentoring concerne une étudiante de ADA tech school : une femme qui fait du Java, s'intéresse à DDD et peut-être au _Craft_.

En tant que mentor que faut-il :

- faire ?
- pas faire ?
- répondre aux attentes ?

Se baser sur le livre [Agile Technical Practices Distilled principles](https://www.amazon.fr/Agile-Technical-Practices-Distilled-principles/dp/1838980849) pour avoir des étapes progressives. [Quelques revues sur ce livre aussi par ici](https://www.goodreads.com/book/show/41758433-agile-technical-practices-distilled?from_search=true&from_srp=true&qid=P0nYk3ba71&rank=1). 

Attention à ne pas passer en mode descendant voir directif.

TDD = But ou Moyen ?

Utiliser la méthode des 5 "pourquoi" pour voir s'il y a une demande cachée ?

Idée de contribution à du logiciel libre avec [Beta.gouv](https://beta.gouv.fr/) / [JHipster Lite](https://github.com/jhipster/jhipster-lite) pour travailler sur une base de code existante avec des bonnes pratiques.

Participation à l'[Advent of Craft](https://github.com/advent-of-craft/2024).

Définir des objectifs progressifs comme une TODO list pour aider à la progression. Il ne faut pas que les objectifs restent figes, ils peuvent changer voir être supprimés pour garder un cap attrayant.

Attention à l'overwhelming !

Roadmap ? Cartographie des concepts : https://roadmap.sh/ (ex. https://roadmap.sh/java).


### Animer et faire perdurer une communauté craft

Animé par **Jérôme**, **Julien** et **Isabelle**.

- De la régularité pour que les participants puissent anticiper sur leurs agendas ;
- Préparer et informer sur les sujets à l'avance afin de motiver ;
- Varier les formats ;
- Alimentation à partir des écoles pour les étudiants ;
- Faire tourner les rôles afin que l'organisation ne repose pas toujours sur la même personne mais plus sur un groupe ;
- Passer d'une communauté gérée par une personne à une communauté qui s'auto-organise. (selon Colin 3 phases dans la vie d'une communauté : d'abord 1 personne, ensuite plusieurs, ensuite, à la fin, des évents qui sont fait sans les orgas (c'est le cas de Lyon Craft)) -> demander aux personnes qui viennent souvent pour ;
- Notion de Démocratie Dictatoriale Distribuée apportée par Colin. On lance une idée, et on la fait si personne ne nous convainc de pas la faire, mais on l'assume seul.

Rôles tournants :

- Date : définit les dates pour le mois suivant ;
- Sujet : Trouve le sujet ;
- Accueil : Trouve et gère la salle et l'accueil ;
- Compte rendu : Rédige le compte rendu ;
- Coordinateur : doit s'assurer que les 4 autres postes sont gérés (ne le fait pas forcément, mais doit s'assurer que c'est fait).

Initiative : tant que personne ne me convainc pas que c'est une connerie je peux le faire et je suis responsable.

Idée de format : club de lecture… mais on ne parle pas tous de la même chose. On présente un livre, article que l'on ait aimé ou pas. Ça permet de confronter les idées et de partager.

Autres idées : gouter tech, soirée DDD, soirée retour de conf, test d'atelier, fish bowl.

Comptes rendus : https://swcraftlyon.github.io/

### C'est la dèche – trouver une mission pour finir l'année à l'équilibre :) 

Animé par **Marc**.

Accepter d'être porté ?

Trouver un Lead.

Une stratégie.

Communiquer à des non-tech.

Passer par un tech et lui demander le nom d'un non-tech (Tech en phase).

Si tu veux qu'on travaille ensemble.

Tu me trouves quelqu'un qui a telle enveloppe budgétaire et tu me cales un call de 30 minutes.

Les petites structures ne négocient pas le TJ, elles prennent ou ne prennent pas.

Ils réfléchissent au nombre de jours. Et que je peux apporter de la valeur sur ce nombre de jours.

Le problème ce n'est jamais le prix.

Pas expliquer ce que je sais faire. Comprendre le problème de la personne, explique que tu peux apporter plus que ce que ça lui coute ;

La clarté de l'offre de service.

Quand on est sur scene.

Un livre ça aide aussi :)

BBL : donner la présentation sans avoir l'état d'esprit de vendre.

Transformer lead en entretien.

En entretien : convaincre d'acheter.

Linkedin : être contacté, apport d'affaire.

Plusieurs niveaux de réseau (intéressant d'attaquer plusieurs niveaux) :

- 1 proche ;
- 2 para-social ;
- 3 full prospection (quanti) (peut être délégué).

Une deuxième personne qui te présente

> Hey ! ya Marc qui va te contacter sur ça.

---

Mission très courte

Ex. event storming et ça peut pivoter.

### Tests unitaires, intégration, E2E... est-ce que le nom est important ?

Animé par **Xavier**.

- Pas parler de test unitaire : on veut un test rapide. Définir rapide (eg 3s c'est lent si on run souvent) ;
- Un test lent va monter tout ton UI par exemple et appeler la DB ;
- Si codé en TDD (eg : dans un fichier) puis refactoré dans plusieurs fichiers, c'est difficile de bien voir que tout est testé dans la PR. Dans ce cas-là, peut-être montrer le coverage ;
- Définir une stratégie de tests : unitaire, composants, intégration ;
- Comment passer de l'unité = fonction à unité = comportement ?
- Pas de consensus sur ce qu'est une unité dans un TU : eg (recherche rapide) https://www.blinkingcaret.com/2016/04/27/what-exactly-is-a-unit-in-unit-testing/ ;
- Si les tests sont trop couplés au code, ça change dès que l'on change l'implem ou alors on mock tout et on ne teste rien (malgré le coverage) => Réussir à le prouver pour challenger la vision des collègues et de l'entreprise ;
- Se faire aider par un externe (intervenant, conference ou autre) qui seront peut-être plus facilement à l'écoute sans se sentir attaque (comme ça pourrait être le cas avec une personne en interne).

[A complete workshop for your team to see what’s a good test strategy](https://philippe.bourgau.net/a-complete-workshop-for-your-team-to-see-what-s-a-good-test-strategy/) (Philippe Bourgau)

### Comment amener / inspirer progressivement le DDD dans une équipe

Animé par **Julien**, **Jérôme** et **Isabelle**.

Les techs s'intéressent souvent au framework et moins souvent à leur manière d'architecturer leur code.

Le métier, les commerciaux changent régulièrement leurs terminologies.

Cas pratique dans une équipe où le dir tech essaye d'inculquer l'approche dans des équipes essentiellement constituées de junior :

On utilise des katas (soit existants, soit en les créant de toute pièce).

En priorité bosser avec ceux qui sont chauds (et tant pis pour les autres). Récupérer du feedback pour les identifier et pour se rassurer (parfois l'enthousiasme n'est pas forcément celui qu'on perçoit).

Pour les katas, utiliser des vrais sujets et debriefer sur la valeur apportée par l'approche DDD.

Ne pas chercher à faire toute l'approche DDD :

- zoom sur Value Object
- ACL entre 2 services

Les dev s'oriente plutôt naturellement sur des formations tech/framework.

Peut-être orienter les choix pour amener sur des formations DDD.

Mettre des objectifs derrière les choix de formation.

Demander des argumentaires pour les demandes de formation (Quels intérêts pour moi, pour l'entreprise, pour les produits/projets, pour les clients ?). Préparer le même argumentaire pour les formations DDD.

### C'est quoi l'archéologie du code ? Métaphore de la dette technique avec un donjon et des monstres (code smells)

Animé par **Marc**.

Parallèle entre le code legacy et l'investigation pour comprendre le sens et l'interêt de celui-ci avec l'étude archéologique.

Trouver une image plus ludique avec des donjons et des monstres.

Illustration du couplage avec le jeu [Labyrinthe](https://www.espritjeu.com/jeu-de-societe/labyrinthe.html). 

Le blob et slime qui grossi et devient légèrement envahissant.

Récuperer les trésors => extraire la logique metier.

Aventuriers :

- Prêtre : coach ?

Among us :

- Traitre ? Team aqua et team magma => persuade que leur idée est la bonne alors qu'en fait pas tant.

Qui vont dans la mauvaise direction ?

Méthode mikado, cartographier ton chemin.

- Orcs must die (tower defense et fps) ;
- Mobs feature qui vont en prod ;
- PO pression pour aller vite ;
- Bien agencer ses pièges ;
- Sinon être submergé.

Tower defense => placer ses defenses pour se protéger des creatures (si elles passent le bug arrive en prod) On peut se dire que la pression d'une deadline nous fait mal placer/choisir nos defenses. => On peut rearranger nos defenses pour mieux se protéger === refacto.

Code mort : le labyrinthe évolue et des salles sont entourées de murs.

Métro : stations fantômes.

Expert métier = vieux sage ? qui a la connaissance, Gandalf, te guide.

La personne qui est là depuis 15 ans.

Panneaux = documentation ?

Tests auto : c'est quoi ?

Métaphore de Tod : code mausolée.


### Codons un exemple de mauvais TU

Ca code avec **Colin**.

### Comment sortir du syndrome de l'imposteur en informatique

Animé par **Martin**.

- bien s'entourer ❤ ;
- Ne pas hésiter à être dans l'authenticité ;
- Faire de la formation continue ;
- Trouver la petite chose qui me permet de me dire que je suis légitime ;
- Se focaliser sur ce que j'ai et pas sur ce que je n'ai pas ;
- Construction plutôt d'immédiateté. Petit pas par petit ;
- Merci au syndrome : Il me permet d'avancer, comment je peux changer ce frein en moteur ?

[Tips pour combattre le syndrome de l'imposteur (Aurélie Vache)](https://www.youtube.com/watch?v=MGt-DpYf30g).

## Retours

- Bien aimé le format en ligne ;
- Le pad est une bonne idée ;
- Avec Discord ça marche bien ;
- Pas trouvé de système pour lever la main ;
- Content de la session, arrivé les mains dans les poches, reparti les poches pleines ;
- Pas de prise de tête ;
- Pas d'idée de sujet => quand même trouvé un au dernier moment ;
- Perte de motivation avant l'événement => très agréablement surpris de l'événement => permis de faire un sujet ;
- Paradoxalement l'horaire est une bonne horaire pour certains mais pas pour d'autres ;
- Session enrichissante ;
- Bien aimé le regroupement des communautés craft.

## ROTI

- 1 personne a noté 3.81278
- 10 personnes ont noté 4
- 4 personnes ont noté 5

## Promo

On peut ajouter notre meetup sur la carte mondiale : https://www.softwarecrafters.org/
https://guild.host/software-crafters/network

### Strasbourg

https://swcraftstras.github.io/

http://stras.dev

### Grenoble

Journal du dev par Sandre Banna.

https://www.meetup.com/fr-FR/software-craftsmanship-grenoble/

### Limoges

Book club : compte rendu très cool pour les book club.

### Quebec

https://guild.host/software-crafters-quebec/events

### Montréal

https://www.meetup.com/software-crafters-montreal/

Forum ouvert 1 fois par mois.

### Lille

https://www.linkedin.com/company/software-craft-lille/ -> peut-être qu'il y a d'autres sites, mais pas mal d'infos ici.

https://www.meetup.com/fr-FR/software-craftsmanship-lille/

https://discord.gg/6ANhzc8WCS


### Lyon

Recherche de diversité dans l'organisation

### Luxembourg

https://guild.host/software-craft-luxembourg/events
