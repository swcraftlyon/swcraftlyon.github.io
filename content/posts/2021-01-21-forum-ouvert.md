---
title: "Forum ouvert avec le JUG Lyon"
date: 2021-01-21T13:45:00+01:00
tags: ["unconf"]
---

- Sujet : Forum ouvert cross communautés
- Meetup Crafters : https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/275193027/
- Meetup JUG : https://www.meetup.com/fr-FR/lyonjug/events/275565153/

## Déroulé de la soirée

- 3 sessions de présentations en petits groupes ; 
- Définition du programme de la soirée avec les sujets proprosés par les participants ;
- 3 sessions de discussions entrecoupées de retours rapides ;
- Retour sur la soirée.

# Session1: 19h30 - 19h50

## Salle 1 : Matthieu - Le DDD, comment l'aborder ? Comment l'appliquer ?

Faire du DDD: Orientation métier, mettre au centre le métier. Distinguer le métier pour faire en sorte que l'application reste maintenable.  
Context technique: pertinent de faire du DDD? une question de besoin performance ? Le critère est plus de voir si la complexité du métier. Les patterns stratégiques peut permettre de bien délimité les parties techniques ou simple et les parties complexes.  
Impossible si pas de contact avec les experts métiers ? Beaucoup plus difficile mais pas impossible ?  
Faire du DDD pour de l'orchestration d'API ? Non pas forcément pertinent dans ce genre de situation  
Attention à ne pas lier la coucher de persistence et le domaine métier, ce n'est pas compatible  


## Salle 2 : Adrien - L'architecture, c'est quoi ?
Pas de CR

## Salle 3 : Colin - C'est quoi le software Craftsmanship ?    

Des définitions très différentes de ce qu'est le Software Crafstmanship.  
Un ensemble d'outils pour se simplifier la vie via du TDD, DDD...  
Le DDD est le boss de fin, complexe à appréhender.  
TDD est plus simple à appréhender mais attention Test first != TDD.  

# Salle 4 :Maxime - comment refactorer un code pas totalement couvert par des tests mais qui possède beaucoup de dépendances ?

Golden master

The Mikado method. Reprend la philosophie TCR ([Test, Commit or Revert](https://blog.engineering.publicissapient.fr/2020/03/20/domptez-vos-refactoring-avec-la-mikado-method/ ))
[mikadomethod](http://mikadomethod.info/)

Attention : éviter de prendre trop de temps à réfactorer (définir le scope, on peut se retrouver à découvrir des impacts cachés)

## Salle 5 : Nolwenn – Lombok, oui ? non ?

C'est non ! ;) (Charles) C’est ça ! Ou oui mais pour poser un logger avec une annotation.
    
## Salle 6 : Comment choisir entre les paradigmes de programmation Objet/fonctionnel/procédural-jean charles?

On commence souvent par l'objet puis on découvre le fonctionnel mais c'est difficile car le paradigme est très différent
Lombok : ça incite a casser l'encapsulation
C'est pas un soucis de mélanger


# Session 2: 19h55 - 20h15


## Salle 1 : Quel workshop vous interesserait en ligne ? (florent)

EventStorming
Global code retreat
CQRS: comprendre l'architecture, comment on construit un CQRS. Regarder une vidéo et en discuter ? Avoir une petite présentation puis rentrer dans le code
Lié le monde AI et java, comment on récupère model, comment on le transite. Atelier F# avec mathias
Workshop architecture hexagonal

## Salle 2 : Quelle est la bonne manière d'initialiser le jeu de données de tests unitaires? (Mossroy)

Idées :

- avoir une base unique dans laquelle sont les données : pourri. Le test n'est pas répétable. Problèmes quand la structure change
- utiliser les APIs de l'applicatif pour insérer les données (ou une API créée pour ça, sans règles de gestion). Inconvénient : nécessite de repartir à zéro à chaque fois
- framework type DBUnit ou DBSetup
- Flyway

Pour la base de test, plusieurs approches : H2 (in-memory), ou TestContainers  
Pour initialiser la structure : parfois l'ORM peut s'en occuper, parfois Flyway/Liquibase  

## Salle 3 : Colin - Comment savoir si l'herbe est plus verte ailleurs ?

Questions envisageables :
- Est-ce que le degré d'inconfort est supportable ? 
- Qu'apporte l'inconfort dans la position ?
- Quelles sont tes valeurs fortes ? A quel moment sont-elles heurtées ?
- Ton environnement de travail est-il supportable ?
- Question du salaire - Valeur du salarié corrélée au montant du salaire ? 

## Salle 4 : Maxime - les design pattern c'est has been ?

Les framework ne doivent pas être des contraintes  
On peut continuer à faire de l'OOP (en java)  
en gros : ça dépend xD  
Utilisé mais pas forcément nommé. Pratique surtout pour se comprendre entre pair  

## Salle 5 : Matthieu - Quel est la différence entre  un bon et un mauvais projet?

Plusieurs aspects : techniques, humains, managériaux.  
Projet qui se passe bien : pas de micro-management, maturité de l'équipe, respect, confiance, responsabilité.  
Séparation build & run, frictions systémiques entre les groupes.  
Technos vieilles / pas maintenues -> difficile  
Dette techniques / legacy -> pourquoi le code est comme ça / quelles sont les décisions sous-jacentes  
http://pages.cs.wisc.edu/~remzi/Naur.pdf -> du code sans les sachants sera quasiment toujours perçu comme du "code de merde"  
Technos adaptées aux problématiques et cas d'usages, concepts sous-jacents maitrisés  
Temps dédiés pour monter en compétence et se former  

## Salle 6 : Maxime - les streams envers et contre tout ? 

Pas de CR

# Session 3: 20h20 - 20h40

## Salle 1 : Colin - Ya t'il une vie autre que @RestController into @Service into @Repository ?

[C'est possible :D](https://docs.google.com/document/d/1AnMeSI7RNA3zGQ2sKa0aKBThBeV6-CdDzn9fN1NGolQ/edit)

## Salle 2 : Pourquoi rester sur java8 ? && Matthieu - Les modules Java 11, quels cas d'usage ?

Pas de CR

## Salle 3 : Gautier - Comment onboarder un dev freelance ?

Pas de CR

## Salle 4: Romain - Faut-il être passionné ? && Charles - (R)allumer le feu ! : faire naitre la passion (du dev) & combatre la fatigue

Non :)  On peut être très bon et professionnel sans être passionné  
Passion: Est-ce que l'on ferait le même travail si on était pas payé? Est-ce que c'est un loisir comme les autres ?  
Pas toujours simple de garder la motivation constamment.  
Faire deux choses pour varier ? Casser la monotonie, découvrir de nouvelles choses.  
Pomodoro pour rythme la journée  
Ne pas hésiter à relativiser sur ses compétences et ses ambitions  

## Salle 5 : Maxime - comment écrire un bon test unitaire ?

Pas de CR
    
## Salle 6 : Christophe - Télétravail à l'heure du covid, et après?

Pas de CR
