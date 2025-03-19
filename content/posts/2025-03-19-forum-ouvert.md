---
title: "Forum Ouvert du Mercredi 19 Mars 2025"
date: 2025-03-19T19:00:00+01:00
tags: ["forum-ouvert"]
---
- Sujet : Forum ouvert
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/306666704/)
- Format : Forum ouvert
- Nombre de participants : 9

## Sujets
### Les techs et les UX/UI, comment collaborer efficacement ?
Animé par **Nolwenn**
Comment arriver à travailler sans valider des maquettes en amont ?
Comment réduire le bruit ?
Pas sec niveau métier
Problème de maturité du projet
Ne pas aller trop dans la complexité dans la maquette
Idée : agir sur les autres sujets : commencer à livrer des trucs petits
L'outil actuel est un fichier excel modulaire

### Qu'est-ce qu'on lit? 
Animé par **Léo**
Mes lectures:
    1. clean code
    2. The Software Craftsman
    3, Clean architecture
    4. Extrem Programming Explained
    5. Extreme Programming (petit livre avec une chevre)
    6. Refactoring (vielle version en Java)
    7. DDD (blue, red et green)
    8. Building LLMs for Production. (Bouchard)
Les prochaines lectures:
    - Pragmatic programmer
    - Clean Coder
    - Release It!: Design and Deploy Production-Ready Software
    - les livres dans https://discord.com/channels/689540719861563395/1308394133051801600
Deceptions:
    - Clean Craftsmanship (beaucoup de redite par rapport)
    - Tiddy First;
En vrai on peut en relire

### Comment je documente facilement et de manière effficace mon API Back End Java Spring
Animé par **Réda**
Présentation de l'architecture hexa

### Comment je change mon framework frontend (Stencil) sans tout casser ? Comment j'ammene de l'hexa dans le front et comment je gere mon injection de dependances dans des frameworks autre que Angular ?
Animé par **Léo**
Dans les autres frameworks:
    - Angular, utilisation de providers dans les modules avec des tokens types fonction Inject qui prend un token et renvoie une implem
    - Vue, dans script setup il y a possibilite d'utiliser une fonction inject native de Vue. Pour les tests de composants Vue il est possible de changer les injectins avec mounted. Il est possible de faire des tests de compsants en utilisant Cypress et intercepter les appels APIs. UT pour les mapping (retour api vers le front), utilisation de Zod pour faire des tests de contrats
    - React, inject ou provide n'existe pas, on utilise les contexts. Comme un composant React qui sera dans le DOM (1 context par injection) et va generer.
    - Svelte 
Une lib d'injection existe (piqure) developee par Antho himself.

### Quelqu'un a déjà eu une organisation efficace pour traiter des sujets cross-squads ?
Animé par **Maxime**
Questions posées : Comment trouver un moyen de se coordonner ? comment s'organiser ?
Plusieurs solutions évoquées => 
- Feature team , si c'est l'équipe qui gère le service, il  y a moins de synchro
- Créer des équipes provisoires pour la feature
Autres Problématiques : Les POs n'ont pas les mêmes priorités
- Certaines équipes tournent tout le temps , pour mieux répartir les charges
- organisation qui permette de disposer d’une force de travail qui suit la charge de feature et une force de travail constante (type opensource avec des mainteneurs officiels)
- organisation d’un hackaton pour plier une feature transverse et limiter les points de synchronisation

### Quels sont les meilleurs moyens de faire de la veille sans se retrouver submergé d'informations
Animé par **Réda**
Twitter
En entreprise pendant certaines heures pour partager
Lire JEP
Lire les nouveautés d'ES
Podcasts
- Artisan Dévelopeurs
- Les Castcodeurs https://lescastcodeurs.com/
- PunkinDev
- Aller dans les salons/meetups/conférences

### Agent AI et autres copilotes, quels sont vos usages et vos retours ?
Animé par **Nolwenn**
- Utile pour du mapping depuis du JSON ou pour générer un contrat openAPI
- Etude faite sur une baisse de fiabilité au niveau du code avec l'utilisation de l'IA
- Parfois utile en faisant du TDD
- Exemple de cas d'utilisation d'outils : Copilot avec Inside Out, suggestion des IA dans le front est pratique, par exemple l'outil arrive à déduire le token, ou retravailler du code css dans le refactoring
- pas de prompt que de l’autocompletion
- Problématiques liées à la confidentialité et aux données de l'entreprise
IA utilisée sur des scénarios Gherkin pour voir les "trous dans la raquette"

### Quelles conferences vallent le coup avant cet ete ?
Animé par **Léo**
Mixit
Lyon Craft
Alpes Craft - 2e journée = forum ouvert
Volcamp
Sunny Tech
Dev Fest Nantes
Socrates
Breizh Camp
Voxxed
Snowcamp
Tarif abuse (il faut y aller avec sa boite):
    DDD Europe
    FlowCon
    New Craft

### Si jamais des gens veulent avoir un retour d'un passage d'un écosystème Java vers .Net (dernières versions), j'ai fait le switch il y a un an.
Animé par **Maxime**
Pas de notes

## Rétrospective
Retours sur la session :
- 2e participation à ce type de format, j'ai donné 3 sujets, les 3 ont eu beaucoup de participants, merci pour les échanges
- Découverte de ce format, c'est une première, je vais revenir
- Première fois, super expérience
- Plusieurs participations déjà, ça semble plus fluide avec moins de participants, échanges plus dynamiques
- Pour un participant très junior comme moi, c'est très technique, et hors de mon niveau

## ROTI
- 3/5 : 2
- 4/5 : 7
