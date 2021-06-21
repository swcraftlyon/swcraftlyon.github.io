---
title: "Soirée lectures du Mardi 15 Juin 2021"
date: 2021-06-21T10:38:12+02:00
tags: ["talk", "live", "lectures"]
---

- Sujet: Les Crafters parlent de bouquins
- Format: Discussion online
- Meetup: https://www.meetup.com/Software-Craftsmanship-Lyon/events/278407271/
- Vidéo: https://youtu.be/DRbah8pLwtU

**[Explore It!](https://pragprog.com/titles/ehxta/explore-it/) de Elisabeth Hendrickson** présenté par Adrien

Cette lecture de 150 pages environ, aborde les projets informatiques sous l'angle du test d'exploration.
On découvre ce qu'est le test d'exploration, comment faire les sessions d'exploration à plusieurs, comment rentrer dans les spécifications et les challenger, divers outils, en particulier sur la sécurité...
Cette lecture recommandée par Adrien l'a aidé à assumer son rôle grandissant de lead.
Il a trouvé des similarités avec l'example mapping et plein de tips utiles.
Le livre s'adresse en particulier aux personnes en charge du testing.

**[Domain Modeling Made Functional](https://pragprog.com/titles/swdddf/domain-modeling-made-functional/) de Scott Wlaschin** par Romain

Ecrit en 2018, par Scott Wlaschin ([son blog](https://fsharpforfunandprofit.com/)), ce livre de 300 pages propose d'explorer un cas métier concret et d'aller jusqu'à son implémentation.

La première partie présente le cas fictif de la prise de commande, et introduit la démarche DDD.
De fausses interviews permettent de creuser le besoin et de montrer l'aspect itératif de la démarche.
Wlaschin fait émerger les concepts puis les regroupe en bounded contexts.

Au cours de la deuxième partie, Wlaschin modélise les briques constitutives de l'application sous forme de types algébriques avec F# et aborde le concept de composition.

La troisième partie s'intéresse à l'implémentation.
Romain a beaucoup aimé la métaphore du railway programming, pour implémenter la gestion des erreurs.
Le livre détaille l'exposition des données et leur persistance.
Un dernier chapitre, original, imagine des évolutions potentielles, pour voir si le design tient ou si, au contraire, des points de tension apparaissent.

La lecture de ce seul livre ne transforme pas en expert du Domain-Driven Design, du langage F# ou de Functional Programming, mais la mise en commun de ces concepts est bien expliquée.
Bien qu'elle ne soit pas recommandée aux débutants purs, auxquels des pré-requis pourraient manquer, la lecture de ce livre est conseillée, y compris pour les aficionados de OOP.
L'auteur utilise peu de jargon et prend soin de bien le définir.

**[Specifying State Machines with Temporal Logic](https://wickstrom.tech/programming/2021/05/03/specifying-state-machines-with-temporal-logic.html) d'Oskar Wickström** présenté par Gautier

L'article présente un moyen pour représenter un système comme une machine à états évoluant au cours du temps et des opérateurs temporels (next, always, eventually, until).
Pas nécessairement pratique à utiliser dès demain (quid de la scalabilité sur nos problèmes quotidiens), mais un travail intéressant sur la visualisation des systèmes, qui peut donner des idées pour raisonner.
La représentation retenue s'éloigne du traditionnel diagramme états/transitions pour se concentrer sur l'aspect temporel.
Gautier nous recommande aussi d'aller lire les posts de [Bret Victor](http://worrydream.com/).

**[!!Con 2019- Tail Call Optimization: The Musical!!](https://www.youtube.com/watch?v=-PX0BV9hGZY) de Anjana Vakil & Natalia Margolis** présenté par Colin

Une masterclass de talk, i.e. le mieux mené, le plus dynamique des talks selon Colin : l'explication du Tail Call Optimization en karaoké sur des chansons de Disney.
Présentation en 3 actes et en duo, 11 minutes 27 de bonheur, le texte et le support sont extras.

**[Combatting the Near Enemies of DDD](https://www.youtube.com/watch?v=4yr130f-1FE) de Andrew Harmel-Law and Gayathri Thiyagarajan** présenté par Colin

Talk très conseillé qui parle des situations où l'on on croit avoir la bonne cible, mais on se trompe.

**[Experiments in Reasoning](https://www.youtube.com/watch?v=uvOZisJWqg0) de Aslam Khan** présenté par Colin

Mention honorable pour ce talk dans lequel on s'interroge sur notre métier.

**[Continued Learning: The Beauty of Maintenance](https://www.youtube.com/watch?v=3gib0hKYjB0) de Kent Beck** présenté par Colin

4 talks en 1. D'abord, Kent Beck parle du stress et fait l'analogie entre le stress avant de parler en conférence et l'excitation, enfant, quand on attend ses cadeaux de Noël.
Cette analogie permet à Beck de se persuader, avant de monter sur scène, qu'il est excité et pas stressé.
Ensuite une partie sur le couplage et la cohésion, puis une sur faire le changement facile et enfin une alerte sur le retour du Waterfall, que Beck nous appelle à combattre avec le feu.

**[The Future of Programming](https://www.youtube.com/watch?v=8pTEmbeENF4) de Bret Victor** présenté par Florent

Avec un storytelling rétro, Bret Victor nous montre que nous avons la mémoire courte dans notre métier et qu'il y a eu des innovations incroyables que nous avons pour partie oubliées.
Les projections sur le futur de notre métier sont amusantes.

**[Attacking end-to-end email encryption](https://media.ccc.de/v/35c3-9463-attacking_end-to-end_email_encryption) de Sebastian Schinzel** présenté par Florent

Cette vidéo explique très bien une faille sur l'échange de mails avec chiffrement.
Schinzel explique les problèmes que l'on peut avoir avec des formats très ouverts comme le PDF, dans lequel on peut embarquer du JavaScript et crypter pour partie seulement.
Pas besoin d'être expert pour regarder cette vidéo.

**[Hacking the Nintendo Game & Watch](https://media.ccc.de/v/rc3-11527-hacking_the_nintendo_game_watch) de Thomas Roth** présenté par Florent

Explication du mécanisme de sécurité de la console de Nintendo.
Revoir the [Old Man Glitch](https://www.youtube.com/watch?v=NU-lcw8-G-c) sur le même thème. Dans la même, sur [sa chaîne Youtube](https://www.youtube.com/c/HusseinNasser-software-engineering), Hussein Nasser explique des exploits.

**[Les Cantos d'Hyperion](https://fr.wikipedia.org/wiki/Les_Cantos_d%27Hyp%C3%A9rion) de Dan Simons** par Florent

Grand classique, cycle découpé en 4 tomes (2500 pages), écrit dans les années 90.
En le lisant de nos jours, beaucoup de réflexions intéressantes sur notre dépendance à l'informatique ainsi qu'une trame philosophique sur la vie et la mort.

**[Retour sur le Blend 2021](https://www.blendwebmix.com/)** présenté par Arthur

Le Blend, conférence lyonnaise qui existe depuis 2013 et qui traite du  Web sous ses aspects tech, design et business.
C'est bien, allez-y.
Les vidéos ne sont pas encore disponibles mais devraient l'être prochainement.

## ROTI

- 1 5/5
- 8 4/5
