---
title: "Forum ouvert des communautés francophone Jeudi 29 février 2024"
date: 2024-02-29T19:00:00+01:00
tags: ["forum-ouvert"]
aliases: [/posts/2024-02-29-forum-ouvert-communaute-francophone/]
---

- Sujet : Forum ouvert des communautés craft francophone
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/298508836/)
- Format : Forum ouvert
- Nombre de participants : 22

## Les sujets
### Vos REX sur du Trunk Base Development vs Git flow [Ando - Lyon]

Git Flow : dev -> branche -> dev -> main https://nvie.com/posts/a-successful-git-branching-model/
Trunk Based : main -> branche -> main https://trunkbaseddevelopment.com/

scaled trunk ou smaller team
pré requis:
  * Attention au côté blocage CI: test auto pertinent (-> TDD)
  * pas de hotfix,

question besoin : doit on livrer tôt?

question de process actuel: est-ce qu'on met la sécurité devant le besoin de livrer tôt ou inversement?

Manqué de temps

### OOP vs FP, quel choix pour quoi ? [Jérémy - Lyon]

#### REXs
* défi de faire une api sans classe, bilan => pas de retour en arrière
* utilisation au quotidien (mic FP OOP)
* utilisation au quotidien (mix FP OOP)

#### Pros
* Currying
* principes fonctionnels
* Monades / Either
* pattern matching
* écriture plus simple

#### Cons
* peu devenir très verbeux
* difficile quand on vient de l'oop

#### Avantage POO
 * visibilité / abstraction / encapsulation
 * modélisation du métier
 * Code custom plus évolué que Either pour les cas métiers
 * composition over inheritance

FP plus proche de la donnée
POO plus proche du comportement

Beaucoup d'avantages côté FP pour un code plus clair, moins buggé

### Quelles habitudes avez-vous mises en place pour faire de la veille techno? [Alvaro - Lausanne]

Apprendre à apprendre, un MOOC mettant en valeur les habitudes (et autres !): https://www.coursera.org/learn/learning-how-to-learn

#### problématiques

* Dédier du temps à l'apprentissage
* Mettre en place des habitudes
* Profiter de temps libres / s'en créer : trajets (vélos, train, voiture, ...)
* Trouver les bons outils pour rendre ce temps efficace (ex: Momento pour les podcasts)
* Trouver des sources de qualité
* Le SEO mène à pousser toujours + de contenu de basse qualité, difficile de trouver les pépites
* Plutôt que de chercher sur google, se baser sur des recommandations de qualité (communautés, meetups, ...)

L'importance de la mise en place d'habitudes : https://jamesclear.com/atomic-habits

Template de mon collègue Thomas permettant de mettre en place des routines plus facilement : https://www.notion.so/Template-Atomic-Habits-de-James-Clear-b4c4cfe3527a4a56b6ec296df9735c8a

Xtrem Tech Watch : https://yoan-thirion.gitbook.io/knowledge-base/agile-coaching/xtrem-watch-decouvrez-la-puissance-de-la-veille-collective

App de podcast Transcript auto aux instants choisis: https://apps.apple.com/fr/app/momento-podcasts/id1530089886

Chacun a des habitudes liées à son quotidien (ex : trajets)

Pour trouver des bonnes sources : recommandations, discussions

### Vous avez écrit un livre / voulez le faire, vous vous y prenez comment ? [Colin - Lyon]

#### REX Nicolas : EBook

Avoir une version imprimée
Comment s'organiser dans l'écriture

* Commencé par un blog
* Écrivait régulièrement sur le sujet de code legacy
* Explorer, creuser le sujet
* Objectif initial : mettre à un seul endroit les idées, ce que j'utilise le plus

2 activités :
* Écrire
* Arranger réorganiser

Auto édition (ebook)

    Utilisation d'un projet OpenSource qui fait les différents EBooks depuis du markdown : https://github.com/SaraVieira/starter-book

S'appuyer sur ce livre comme base quand il intervient quelque part

    Un artefact clair que les gens identifient (un produit d'appel)
    Un endroit pour envoyer les gens quand ils posent toujours les même questions

En cas de coquille

    Il y a un process à suivre
    Refaire toutes les étapes jusqu'à la génération

Ecrire un bouquin c'est toujours plus long et plus compliqué mais c'est une bonne ressource pour capitaliser

#### REX Colin : Livre Blanc distribué gratuitement + Livre en cours de relecture

Écrit un livre blanc chez Ippon

    Soucis d'échanges avec l'illustration (charte graphique notamment)
    Partager l'état de sa refléxion
    A aidé à se positionner en interne

Envoyé en relecture un livre 240 pages -> auto-editer
Pour expérimenter la démarche.

    Comprendre les contraintes de l'édition papier

Auto-éditeurs

    bookelis : https://www.bookelis.com/

Écrire

    Tout dans un google doc
    Maitrise
    Facile à partager pour relecture

Tu peux déléguer la partie technique
ISBN quand imprimé
Lulu : https://www.lulu.com/
Leanpub : https://leanpub.com/


### REX - Vive la mutabilité, comment faire du python m'as ouvert le cerveau [Romain - Lyon]
#### Contexte
Calculs sur GPU, doit aller vite (à la micro seconde). On prend tous les raccourcis possibles.
Principe immutable appliqué => x10 sur le temps

Bilan : immutable c'est très peu performant (quand on a des besoins forts en vitesse de calcul)

Partial class pour splitter une classe dans plusieurs fichiers

Talk: DDD sous pression ?  => https://www.youtube.com/watch?v=_qOYkgB3H48

Tradeoff pour répondre à une contrainte précise

### Qu'est-ce qui manque dans l'Advent Of Craft pour que ça soit profondément utile au plus grand nombre ? [Yoan - Genève]
https://github.com/advent-of-craft/advent-of-craft
https://sammancoaching.org/society/contributors/emilybache.html

* Advent of Craft se rapproche du côté compétition de Advent of Code alors que ce n'est pas le but
* Pousser l'entraide
* En mob programming
* Format learning hour
* Solution a-t-il besoin d'être publié le lendemain? Pourquoi pas le même jour?
exemple de tuple, via des e-mails https://tuple.app/code-quality-challenge (ça se ressemble dans le format)

Il peut être intéressante de proposer des sessions "d'entrainement" au cours de l'année. Pour celles et ceux qui sont un peu timide.

### Demandes de feedbacks sur des slides à propos de baby steps / outils de TCRDD [pin - paris]

Référence au jeu vidéo : accroche (l'audience geek) quick save et reload

Il y a un terme (beaucoup utilisé dans baldurs gate 3) => save scumming

Escalade :

* matelas surélevé
* La partie sécurité du matelas a été bien perçue

git-gamble : un outil pour déveloper des choses en faisant des petites étapes https://pinage404.gitlab.io/git-gamble/

TCR | TDD | TCRDD

Diagrams : https://rachelcarmena.github.io/2018/11/13/test-driven-programming-workflows.html

Les slides en hébergé vont plus vite

### Egoless c’est bien mais comment faire avec les non-devs ? [Nolwenn – Lyon]
La critique du code ne semble pas si répandue que ça en dehors de nos communautés craft. Le rush semble un obstacle à la critique.
Le travail en tunnel des fonctionnels ne permet un travail collaboratif et ils s’exposent à des critiques ou des questions qui auraient pu être réglées plus tôt. Critiques qui peuvent source de tensions. Est-ce que des blocs graphiques communs qui permettrait de centrer les critiques sur la valeur à ajouter ?

Egoless Crafting : https://egolesscrafting.org/

### Comment donner du feedback ? [Yoan]
Stop the compliment sandwich : https://adamgrant.substack.com/p/stop-serving-the-compliment-sandwich

Outils :
FEBA / DESC / OSCAR

Ressources :
* Infographie Bloculus : https://bloculus.com/sauvez-des-vies-faites-des-feedbacks/
* Les 5 dysfonctions d'une équipe : https://xxl-strategie.fr/index.php/2017/11/08/les-5-dysfonctionnements-dune-equipe-la-pyramide-de-lencioni/
* Méthode DESC : https://blog.hubspot.fr/marketing/methode-desc
* La Communication Non Violente (liste des sentiments / besoins) : https://www.cnvsuisse.ch/wp-content/uploads/2016/06/Codex-2.pdf

### Prioriser la dette technique avec le "behavioral analysis" [Nicolas - Montréal]

Article qui récapitule les liens présentés: https://understandlegacycode.com/behavioral-analysis

L'idée cœur: utiliser les informations présentes dans "git log" pour visualiser des informations sur une base de code donnée, et aider à prendre des décisions.

Livres:
* Your Code as a Crime Scene - https://pragprog.com/titles/atcrime2/your-code-as-a-crime-scene-second-edition/
* Software Design X-Rays - https://pragprog.com/titles/atevol/software-design-x-rays/
* Notes sur le bouquin: https://understandlegacycode.com/blog/key-points-of-software-design-x-rays/


Hotspot Analysis pour identifier la dette technique à traiter en priorité:
* https://understandlegacycode.com/blog/focus-refactoring-with-hotspots-analysis/
* https://github.com/adamtornhill/code-maat outil open-source pour générer ce genre de graphes
* https://codescene.io/ outil SaaS payant qui fait tout ça pour vous (par l'auteur des livres)

Knowledge map: https://understandlegacycode.com/blog/identify-who-to-ask-with-knowledge-maps/
Pas mal pour identifier "qui maîtrise quoi" dans la base de code.

Idées:
* Aide le offboarding - "qu'est-ce-que Nicolas maîtrise et doit absolument partager?"
* Aide à identifier si les équipes sont alignées avec l'architecture - "tiens, on à l'équipe
* Payments et Core qui travaillent chacun sur ce module, c'est étonnant…"

Super intéressant pour avoir des graphes concrets pour discuter avec les différentes parties prenantes (y compris non-dév). Stratégie: relever des infos avec les outils open-source, présenter > si ça accroche, discuter budget pour outil payant pour aller plus loin et se simplifier la vie.

### On fait un Gilded Rose sans contrôle de flow parce que pourquoi pas ! [Colin - Lyon]

Railwayswitch : https://github.com/forax/design-pattern-reloaded/tree/master/src/main/java/railwayswitch

🚊

Un kata prochainement là dessus ? 0=)

### Encore un peu du Trunk Base ? [Ando - Lyon]
Prérequis pour mettre en place, notamment les pair, mob programming, test auto ceinture bretelle
Des gens ont pris des (mauvais) décisions architectural, ce qui engendre des process en plus pour se protéger
Attention:
    - au onboarding, bien gérer car ça peut faire peur
    - l'ego de certains développeurs qui pensent pouvoir faire mieux sans les contrôles qualité
    - l'habitude des gens de pas forcément faire des petits commits...
tester du TDB que sur develop sur un périmètre plus petit

### [suite session 2 salle 4] s'il y a plus de feedbacks sur les présentations, je prends [pin]
https://pinage404.gitlab.io/git-gamble/

L'installation peut prendre du temps
Sur windows l'installation semble compliquée

Marc :
- je n'ai pas eu trop de difficultés à utiliser la commande
- La documentation : beaucoup de niveaux d'indentation (un peu déroutant pour moi)
- Super agréable suprise : les hooks

## Retours

  * Première participation par hasard, instructif, court et efficace.
  * Difficulté à prendre des notes et écouter, il faudrait de la bonne volonté pour saisir des commentaires en cours de discussion.
  * Participation en tant que pur spectateur sans porter de sujet.
  * Très enrichissant, participation plutôt passive mais instructive.
  * Agrégation des notes est top
  * Début difficile de faire l’exercice de l’échange en ligne via discord mais passer le premier cap tout va pour le mieux.
  * Comment en organiser plus souvent ?
  * Le renouvellement des têtes et le nombre important sont une des clés de la réussite de la soirée


## ROTI

- 3/5 : 3
- 4/5 : 10
- 5/5 : 9