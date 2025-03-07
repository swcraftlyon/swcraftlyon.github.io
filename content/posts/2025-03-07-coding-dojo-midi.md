---
title: "Coding Dojo du Vendredi 07 Mars 2025"
date: 2025-03-07T12:15:00+01:00
tags: ["dojo"]
---

- Sujet : [Bowling](https://codingdojo.org/kata/Bowling/)
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/306455410/)
- Format : Mob
- Langages : TS, Java
- Nombre de participants :  11

## Rappel du sujet
Le kata propose de calculer le score final d'une partie de bowling, à partir d'une séquence de lancers donnée.
Chaque partie comprend 10 tours et à chaque tour le joueur a droit à 2 lancers maximum.

Calcul du score d'un tour :
- si en 2 lancers, les quilles ne sont pas toutes tombées, le score est égal au nombre de quilles tombées.
- si en 2 lancers, les quilles sont toutes tombées, c'est un spare. Le score est égal à 10 + le nombre de quilles qui tomberont au prochain lancer.
- si en 1 lancer, les quilles sont toutes tombées, c'est un strike. Le tour est fini, il n'y a pas de deuxième lancer. Le score est égal à 10 + le nombre de quilles qui tomberont au prochain tour (total des 2 lancers)
- si le joueur fait un spare au dernier tour il fait un lancer bonus pour pouvoir calculer le score du tour.
- si le joueur fait un strike au dernier tour, il fait deux lancers bonus pour pouvoir calculer le score du tour.
- si le joueur fait un spare ou un strike lors d'un lancer bonus on n'en tient pas compte et on ne comptabilise que le nombre de quilles tombées pour le calcul du tour en cours.
- Le score final correspond au total des scores de chaque tour.

Exemples deséquences de lancers : 
(x = strike, / = spare, - = échec, 1 à 10 = nombre de quilles tombées)
X X X X X X X X X X X X -> 10 lancers - 10 strikes + 2 lancers bonus - 2 strikes = 10 tours x 30 points = 300 points
9- 9- 9- 9- 9- 9- 9- 9- 9- 9- -> 20 lancers de 9 points + échec = 10 tours x 9 points = 90 points
5/ 5/ 5/ 5/ 5/ 5/ 5/ 5/ 5/ 5/5 -> 21 lancers - 10 paires de 5 + spare + 1 lancer bonus de 5 points = 10 tours x 15 points = 150

## Déroulement
Les participants ce sont répartis en 2 mobs:  1 en Java et 1 en TS.

## Rétrospective
Retours sur la session :
- C'était top merci
- J'aurais pu mieux me préparer en regardant les règles avant. J'étais un peu perdu, mais ca va, j'ai appris des choses, je serais tenté de refaire la kata.
- Le besoin n'était pas compris de mon côté. Quand je comprends pas le besoin c'est compliqué.
- J'ai trouvé très frustrant le fait de ne pas interagir ensemble, frustrant de voir quelqu'un galérer seul, ou quelqu'un foncer sans comprendre. Je pense que comme on est en remote, les gens décrochent très vite.
- Précision apportée sur le fait qu'on peut poser des questions et interagir même si un seul est officiellement navigateur. 
- Certains ont joué avec des monoïdes :D
- C'est pas la première fois que je faisais le kata bowling, mais là les règles étaient bien connues par les autres participants, car le résumé de virginie était plutôt bon, on a pu aller plus loin que d'habitude dans le kata, c'est hyper interessant.
- C'était cool, on est allés jusqu'à une reduction, après une version mutable, on a typé beaucoup plus, c'était chouette.
- La juste compréhension des consignes en amont d'un kata, semble être un frein pour plusieurs participants.
- Même des tests qui passent au vert directement peuvent être utiles par la suite pour encadrer un refacto.
- J'ai bien aimé, j'avais pas fait ce kata depuis longtemps, je le trouve très didactique.


## ROTI
- 4/5 : 9
- 5/5 : 1
- 1 personne est partie avant le ROTI
