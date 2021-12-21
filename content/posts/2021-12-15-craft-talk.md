---
title: "DDD, CQRS, and Event Sourcing, beyond the hype"
date: 2021-12-15T19:00:00+01:00
tags: ["talk"]
---

- Sujet : DDD, CQRS, and Event Sourcing, beyond the hype
- Format : Talk  
- Meetup : https://www.meetup.com/fr-FR/Software-Craftsmanship-Lyon/events/282137789/
- Replay : https://www.youtube.com/watch?v=SxkfkOBzacE

## Déroulement de la soirée

Présentation par [Allard Buijze](https://twitter.com/allardbz) (AxonIQ), suivie d'une démo.

Dans ce talk, Allard revient sur l'utilisation de CQRS ([Command & Query Responsibility Segregation](https://en.wikipedia.org/wiki/Command%E2%80%93query_separation#Command_query_responsibility_segregation)) et ES (Event Sourcing) dans le contexte des microservices.
L'émergence des microservices, dont la modularité devait permettre de répondre aux problèmes posés par le "big ball of mud" a bien souvent conduit à une collection de petites "balls of mud".
Les événements permettent de réduire un peu l'effort de modification du système tout entier, en réduisant le couplage entre services, mais leur mise en place complique l'infrastructure.
Il n'est pas facile de délimiter les responsabilités des composants dès la genèse du système.
Allard recommande plutôt de construire un monolithe de façon structurée, puis au fur et mesure que le produit évolue, extraire des modules pour les déployer et les mettre à l'échelle indépendamment.

DDD ([Domain-Driven Design](https://fr.wikipedia.org/wiki/Conception_pilot%C3%A9e_par_le_domaine)) peut aider, mais il est facile de se perdre en chemin.
Un domaine est une chose complexe, dont on ne s'intéresse véritablement qu'à un aspect.
Pour cela, on construit [un modèle](https://en.wikipedia.org/wiki/All_models_are_wrong) qui sert notre besoin.
Avec ses patterns stratégiques, qui sont plus abstraits (bounded contexts, etc.), DDD ajoute de la structure à notre modèle.
Allard propose ensuite de faire un détour par le [Reactive Manifesto](https://www.reactivemanifesto.org/) et les [Reactive Principles](https://principles.reactive.foundation/), un ensemble de principes qui peuvent aider pour construire des systèmes distribués.
Par définition du manifeste, un système réactif est [Message-Driven](https://www.reactivemanifesto.org/glossary#Message-Driven).
Les messages ne se limitent toutefois pas aux seuls événements, il y a aussi les commandes (Commands) et les requêtes (Queries), dont l'intention est différente.
Ces différents types de messages ont des besoins de routage différents.
On peut utiliser [publish-subscribe](https://fr.wikipedia.org/wiki/Publish-subscribe) pour les événements.
Les effets de bord produits par une commande ne doivent généralement être déclenchés que depuis un seul composant, une commande n'est donc routée que vers un seul composant qui retourne un acquittement.
Pour les requêtes, plusieurs solutions existent selon le cas d'utilisation : point-à-point, scatter-gather, souscription (par exemple avec des [Server-sent events](https://fr.wikipedia.org/wiki/Server-sent_events)).
L'utilisation des patterns adaptés en fonction du type de messages permet la [Location Transparency](https://www.reactivemanifesto.org/glossary#Location-Transparency).
Par la suite, Allard clarifie la différence entre Event Streaming et Event Sourcing (enregistrer les événements et les évaluer pour déterminer l'état courant).
Il y a des raisons métier à concevoir un système event sourcé et des raisons techniques, notamment pour gérer la complexité dans les modèles, mais nous manquons de familiarité avec ES.

CQRS et ES se complètent bien, et [Axon](https://axoniq.io/), le produit sur lequel travaille Allard peut aider à implémenter des systèmes Message-Driven.
D'un point de vue infrastructure, le choix se fait classiquement entre un [Message Broker](https://fr.wikipedia.org/wiki/Agent_de_messages), qui permet d'envoyer des messages de façon fiable, ou un ESB ([Enterprise Service Bus](https://fr.wikipedia.org/wiki/Enterprise_service_bus)) qui peut prendre des décisions fondées sur le contenu des messages. Axon se situe entre les 2 et comprend les patterns de routage et les différents types de messages.
Allard revient sur la nécessité de se familiariser avec [EventStorming](https://www.eventstorming.com/), DDD et [Event Modeling](https://eventmodeling.org/).

## Roti :

- 5/5 : 4
- 4/5 : 3
- 3/5 : 1
- 2/5 : 1
