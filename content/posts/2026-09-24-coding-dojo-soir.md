---
title: "Coding Dojo Jeudi 24 Septembre 2026"
date: 2026-09-24T20:00:00+01:00
tags: ["dojo"]
---

- Sujet : [Mathematical AST](https://codingdojo.org/kata/mathematical-ast/)
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/316501782/) / [Guild](https://guild.host/events/en-ligne-coding-dojo-gy0p4h)
- Format : 2 mobs
- Langages : Java et TypeScript
- Nombre de participants : 12

## Rappel du sujet

Le but du kata est de parser des expressions arithmétiques comme `"3 6 -6 * +"` (cf. [notation polonaise inverse](https://fr.wikipedia.org/wiki/Notation_polonaise_inverse)), en construisant un [arbre de la syntaxe abstraite](https://fr.wikipedia.org/wiki/Arbre_de_la_syntaxe_abstraite) (ou AST en anglais).

## Déroulement

Session réalisée en mobs par affinité de langage sur [Discord](https://discord.gg/T6wJUWW).

## Rétrospective

* Un de mes premiers katas, super contente.
* Merci, il faut que je prenne confiance.
* Très content de notre petite solution.
Le refactoring à la fin était fou, c'était très sympa.
* Nous n'avons pas fait la représentation graphique proposée.
Solution faite un peu à l'arrache, puis on a typé un peu à droite et à gauche.
On a parsé le texte, ressorti l'algo qui est dans le [bouquin de C](https://fr.wikipedia.org/wiki/The_C_Programming_Language) (utilisation d'une pile).
On n'a pas traité la représentation en objets.
L'implémentation a pris 40 à 45 minutes puis beaucoup de refeactor.
* Ça aurait été pas mal de créer les abstractions, mais en outside-in on parse l'expression.
Le but c'était d'utiliser [Visitor](https://fr.wikipedia.org/wiki/Visiteur_(patron_de_conception)).
* On a abordé pas mal de notions, c'était un peu intimidant, mais fun aussi.

## ROTI

- 1.5/5 : 1
- 3/5 : 3
- 4/5 : 2
- 4.9 : 1
- 5/5 : 3
