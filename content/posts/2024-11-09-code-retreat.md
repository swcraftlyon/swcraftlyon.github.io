---
title: "Code Retreat 9 Novembre 2024"
date: 2024-11-09T09:00:00+01:00
tags: ["code-retreat", "GDCR"]
---

- Sujet : Jeu de la vie
- [Meetup](https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/303123696/?eventorigin=group_past_events)
- 33 inscrit·e·s / 27 présent·e·s

## Introduction
- contraintes permanentes :
  - [TDD](https://tidyfirst.substack.com/p/canon-tdd)
  - pair programming

## Session 1 : Decouverte
- Première fois pour le jeu de la vie, il est pas simple a appréhender
- Illustration des règles pas claires => sont aller voir ailleurs (Wikipedia notamment)
- Commencer par une grille c'est complique (6 groupes) => Il faut trouver les bonnes positions pour faire un cas a la fois moitie
- Commencer par une cellule ça biaise ton design (i.e. design centre sur une cellule alors que l’énoncé le centre sur la grille)
- Design avec des non cellules => plutôt qu'un état on a une position
- Java est très verbeux pour démarrer du TDD rapidement => seulement 1.5-2 tests => 
  - discussion sur les règles 
  - discussion de la TODO 
  - discussion sur comment représenter le voisinage.
- Découverte des tests paramétrés pour gérer le nombre de voisins
- Représentation d'un etat:
  - Boolean
  - Enum
  - Union Type
- Pas d'utilisation de la TODO list
- cell based peut biaiser l’implémentation (bool / enum)
- 1 groupe qui n’a modélisé que les cellules vivantes

## Session 2 : Small method + Indentation once (+ Ping Pong)
- 3 groupes satisfait de son iteration
- chaud de faire de l'outside in
- trop de question philosophique sur la notion de grille cellule etc
- une baby step mega longue mais on s'en sort. C'etait un papy step. Idem pour un autre groupe papy step.
- Hardcoder le resultat attendu permet d'iterer sur cette ligne la et avancer.
- un groupe: un qui etait un peu perdu et a laisser le binome avancer: difficulte du choix de scenario, quoi tester, voir ce qu'il avait en tete
- ping pong: Colin adore torturer Batipste mais il le vit bien
- ping pong: parfois un peu challengeant de le recevoir
- contraintes pas trop dur a respecter, a l'aise

## Session 3 : Primitive Obsession + Blind navigator (+ Fluent API)
- Qaund on tarvaille avec les gens avec lesquels on pair c'est plus simple.
- Quelques cas de triche ou on regarde l'ecran
- On communique avec des dessins/schema
- Dialogue sur une orientation et pas sur l'implementation
- Le navigateur demande souvent l'etat du projet compile tests passent
- Fluent API => peu de changement vu que le sope est reste simple et le nommage precedent etait deja bon
- La contrainte vecu en tant que navigateur est tres agreable on a le temps de se poser des questions
- Peut etre rappeller le cycle TDD pour les non inities

## Session 4 : TCR (+ no if statement)
- La vitesse de frappe n'est pas la clef
- Certains groupes ont plus jeter du code que d'en ecrire
- Baby baby step: preparer le code pour qu'il puisse accueillir le prochain test -> boucle de 1 min
- Inside out plutot que Outside in, impression que c'est plus facile en inside out en tcr
- Pause d'une iteration pour permet d'implementer la prochaine iteration. Reflechir dans quelle direction on va aller
- Discuter ensemble pour se mettre d,accord avant de lancer le chrono. 
- Beaucoup plus utilise la phase de refacto en TCR que dans les autres sessions
- contrainte  no if statement: pattern matching et etonnament trop facile en peu de temps
- pseudo pattern matching en TS, c'etait rigolo
- Impression que pour commit en 2 minutes, il faut discuter 7 minutes? Depend des groupes, pas forcement 7 minutes
- Discuter va plus vite que de coder.
- Bien modeliser le probleme avant de coder.
- Sur un probleme complexe, parfois faut d'abord essayer d'implementer des trucs et voir ce qui se passe car difficile a anticiper.
- Simple de discuter sur les deux prochaines iterations de 5 minutes que dans la vraie vie sur 6 mois
- Commencer par la grid: on est aller droit dans le mur meme avec 5 minutes, vaut mieux reflechir avant ou changer de strategie
- découpage des phases :
  - tests avec implementation hard coded implementation 
  - vrai implementation 
  - refactoring / nommage
- pousse à l’action -> besoin de discussion 

## Session 5 : Evil TDD (+ max 1 parameters)
- Definir une API malefique c'est drole mais quand il faut implementer les regles c'est extremement difficile
- Liste de tous les cas un par un dans l'implementation => Possible de le contrer avec de la randomisation => Test de propriete propose par les framework de tests.
- Difficile de devenir malefique, quelques pistes donnees par les organisateurs.
- Ca permet aussi de decouvrir cerraines capacites de languages (support des emojis)
- Curryfication pour contrer le max 1 parametre, max 1 parametre c'est une contrainte qui reduit evil
- On se rend compte qu'il faut etre pragmatique a base de copier coller.
- chaque pair a tenté de pousser un design => difficile à réconcilier 
- introduire un random dans les tests (PBT)

## Retro globale
- Varier les languages et les approches pour resoudre le kata
- Rester sur le meme exercice permet de tester differentes approches sans revoir les regles et de se focus sur l'implementation
- Differentes approches certaines sont plus facile a aborder => Inside out plus simple a apprehender
- Varier les binomes permet de decouvrir et redecouvrir les pratiqes TDD.
- Outside in peut etre simple a apprehender si on abstrait l'aspect matrice pour se concentrer sur une liste.
- Le navigateur doit bien connaitre les regles metiers => utilisation de simulateur pour verifier nos cas de tests
- Malgre l'habitude du kata on arrive a s'amuser toute la journee
- Combinaisons sont pas toutes pertinantes
- Un event IRL c'est quand meme la convivialite

- Contraintes preferees:
  - blind navigator => force a visualiser, a mettre avec ping pong

- Contraintes moins plebisites:
  - Evil parce que difficile a se mettre en mode malefique => faire en mob avec un evil cache
  - TCR => Empeche de creuser en profondeur un sujet
  - 4 lignes / méthodes

- Deroulement de la journee:
  - Accueil en bas c'etait top
  - Changement d'horaire
  - Rappel de cannon TDD bien apprecie

### ROTI
- 2/5 : 1 => pas de nouvelles approches car fait souvent
- 3/5 : 2 => pas de nouvelles approches car fait souvent
- 4/5 : 14
- 5/5 : 8

## Session 6 : mob + calisthenics (+ immutable)
- Inside out on a fait une methode qui ne sert a rien. Ex: methode isAlive sans avoir le vrai besoin de le faire
- Outside in c'est plutot pour des archi plus grosse, cas reel.
- En mob on passe pour du evil aux yeux des autres sans le faire volontairement.
- Mob a 8 qui ne se connaissent pas c'est trop. On dirait du pair qui regarde, prend pas assez la parole et trop passif.
- Navigator qui lead peut ecraser les personnes plus timides.
- Contraintes pas forcement regarder attentivement.
- Session trop courte
