---
title: "Coding Dojo Vendredi 23 février 2024"
date: 2024-02-23T12:15:00+01:00
tags: ["dojo"]
aliases: [/posts/2024-02-23-petits-katas-sous-contrainte/]
---

- Sujet : Katas sous contrainte
- [Meetup](https://www.meetup.com/software-craftsmanship-lyon/events/299301424/)
- Format : Mob
- Langage : Rust
- Nombre de participants : 8 dont un nouveau


## Rappel du sujet

Session expérimentale pour laquelle on voulait tester un kata simple avec plusieurs contraintes.

## Déroulement

Session en rust sur Employee Report sans if et ni types primitifs. 

## Rétrospective
### Rust

- Le rust c’est bien quand c’est les autres qui codent car il a un bon potentiel. 
- Pas de gros point de blocage sur le langage.
- Pas grand chose de vraiment exaltant dans le langage qui explique la hype.
- Content de voir le langage pour une première fois. 

### Kata en lui-même
- L’idée du kata est de surcharger le seul test en faisant semblant que le besoin fonctionnel évolue au fur et à mesure. Comme pourrait le faire un client. Il ne faut pas chercher à créer une nouvelle méthode à chaque changement.
- Plus concentré sur le langage que l’aspect éducatif du kata.
- Les contraintes sont intéressantes pour pousser la réflexion.

## Exemples de katas sous contraintes

### Gilded Rose sans contrôle de flux

https://gitlab.ippon.fr/twitch/live-coding-fr/-/tree/master/gilded-rose-without-flow-control?ref_type=heads

### FizzBuzz sans modulo et property based testing

```haskell
module Main (main) where

import Data.Text (Text)
import qualified Data.Text as T
import Data.Char(ord)
import Control.Monad
import Test.Hspec
import Test.Hspec.QuickCheck
import Test.QuickCheck
import Data.List (isInfixOf, isSuffixOf)
import Data.Maybe (fromMaybe)

main :: IO ()
main = hspec spec

spec :: Spec
spec =
  describe "FizzBuzz" $ do
    forM_ [(1, "1"), (2,"2")] $ \(param, result) ->
      it (show param <> " should be " <> result) $
        fizzbuzz param `shouldBe` result
    it "All multiple of three start with 'Fizz'" $ 
      property $ \n ->
        n > 0 ==> isInfixOf "Fizz" $ fizzbuzz (3 * n)
    it "All multiple of five ends with 'Buzz'" $
      property $ \n ->
        n > 0 ==> isSuffixOf "Buzz" $ fizzbuzz (5 * n)

fizzbuzz :: Int -> String
fizzbuzz n = fizzbuzzStream !! (n - 1)

fizzbuzzStream :: [String]
fizzbuzzStream = zipWith fromMaybe numbers $ zipWith (<>) fizzs buzzs
  where numbers = show <$> [1..]
        fizzs = cycle [Nothing, Nothing, Just "Fizz"]
        buzzs = cycle [Nothing, Nothing, Nothing, Nothing, Just "Buzz"]
```

## ROTI

- 2/5 : 1
- 3/5 : 2
- 4/5 : 4