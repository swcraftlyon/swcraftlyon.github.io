---
title: "Living documentation - tu ne sais pas encore mais tu l'as déjà documenté"
date: 2022-12-23T19:00:00+01:00
tags: ["talk"]
---

- Sujet : Living documentation - tu ne sais pas encore mais tu l'as déjà documenté
- Format : Talk  
- Meetup : https://www.meetup.com/fr-FR/software-craftsmanship-lyon/events/289884378/
- Replay : https://youtu.be/SC_anhY2Sag
- Slides : https://baldir-fr.github.io/slides-living-documentation/#/
- Repo des slides : https://github.com/baldir-fr/slides-living-documentation/

## Living Documentation

Présentation par [Marc Bouvier](https://u.baldir.fr/me/) coach technique et co-organisateur du meetup [Software Crafters Strasbourg](https://swcraftstras.github.io/).

### Qu'est-ce que la documentation ?

Marc définit la documentation d'un produit informatique comme la connaissance partagée.
Prenant l'exemple d'un consultant abordant un nouveau projet, il décrit les difficultés rencontrées pour accéder à une documentation utile.
Les obstacles dans l'obtention des droits d'accès au repo, l'organisation du projet, la flakiness des tests, la dépendance à des outils tiers (suite Office) sont autant de facteurs agravants.

### Que documenter ?

Pour Marc, l'effort de documentation doit se faire sur les connaissances spécifiques, requises sur le long terme, ou par de nombreuses personnes.
Il recommande de capitaliser sur la connaissance interne au produit : le code, les tests, les générateurs de documentation ([JavaDoc](https://docs.oracle.com/javase/8/docs/technotes/tools/windows/javadoc.html#CHDFCBAD), [JSDoc](https://jsdoc.app/), [Doxygen](https://www.doxygen.nl/)...), les commentaires exécutables (pour [Python](https://docs.python.org/3/library/doctest.html), [Elixir](https://elixir-lang.org/getting-started/mix-otp/docs-tests-and-with.html), [Rust](https://doc.rust-lang.org/rustdoc/write-documentation/documentation-tests.html), ou [Go](https://github.com/apitoolkit/doctests)), les manifestes, l'IaC, les pipelines, les logs et traces, l'outillage... pour aboutir à une documentation vivante, fiable, collaborative et pertinente.

### Des idées pour augmenter la documentation

Marc nous livre une quantité d'idées pour améliorer notre documentation :

* Réduire le bruit (enlever les redondances, travailler le nommage)
* Partager un langage commun (ubiquitous language)
* Penser BDD en utilisant ou non [Cucumber](https://cucumber.io/) ou [SpecFlow](https://specflow.org/)
* Utiliser les [code snippets](https://openjdk.org/jeps/413) dans la JavaDoc, en Java 18
* Développer des tests d'architecture avec [ArchUnit](https://www.archunit.org/)
* Alimenter un Word Cloud depuis le code (par exemple avec [ce plugin Maven](https://livingdocumentation.github.io/livingdoc-maven-plugin/wordcloud.html))
* Annoter le code pour s'y référer plus tard (par ex : `@GoodExample`) ou générer un glossaire
* Utiliser des générateurs de diagrammes ([PlantUML](http://www.plantuml.com/), [Mermaid](https://mermaid.js.org/), [ditaa](https://ditaa.sourceforge.net/), [Graphviz](https://graphviz.org/))
* Utiliser des outils d'analyse statique de code ([SonarLint](https://www.sonarsource.com/products/sonarlint/), [SonarQube](https://www.sonarqube.org/), [SonarCloud](https://sonarcloud.io/), [ESLint](https://eslint.org/), [GitLab SAST analyzers](https://docs.gitlab.com/ee/user/application_security/sast/)...)
* Implémenter une visite guidée du code ([CodeTour](https://marketplace.visualstudio.com/items?itemName=vsls-contrib.codetour) ou [Asciidoctor](https://asciidoctor.org/))
* Développer des API REST avec des contrôles hypermédias
* Mélanger le code et la documentation sous forme de notebooks ([Jupyter](https://jupyter.org/), [Livebook](https://livebook.dev/))
* Concevoir un Design System
* Ecrire ses présentations avec [Asciidoctor reveal.js](https://docs.asciidoctor.org/reveal.js-converter/latest/)
* Rédiger des messages de commit pour construire l'historique des intentions derrière les modifications (par ex. avec [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)) et [traiter votre code comme une scène de crime](https://www.youtube.com/watch?v=7FApEq8wum4)
* Écrire les README en Markdown (ou en AsciiDoc)
* Mettre en place un parcours d'accueil comme décrit par [Dan North](https://www.youtube.com/watch?v=lvs7VEsQzKY)
* Rédiger des [Architecture Decisions Records](https://adr.github.io/)
* Générer des rapports d'audit d'accessibilité avec [FRAGO](https://github.com/DISIC/frago)
* Produire son propre [technology radar](https://radar.thoughtworks.com/)
* Convertir les fichiers Compose en représentation graphique (par ex. avec Graphviz)
* Utiliser l'IDE pour générer les documentations techniques, diagrammes ad-hoc et graphes de dépendance
* Commencer l'automatisation par la documentation des étapes nécessaires, puis en convertissant ces étapes en scripts appelés par un outil d'exécution de pipelines

### L'importance des conversations entre humains

Au delà des outils, les conversations entre humains sont primordiales :

* Avec le métier
* Les revues de code
* Le pair programming, le mob programming
* Le 3 amigos

## ROTI :

- 3/5 : 1
- 4/5 : 5
