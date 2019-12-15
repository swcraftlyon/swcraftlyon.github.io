# sessions

Dépôt pour le code et les compte-rendus des sessions des software crafters de Lyon.

## Executer en local
- Cloner le repository : `git clone --recursive git@github.com:swcraftlyon/sessions.git`. Noter le recursive pour charger les submodules. Le thème sera manquant dans le cas inverse.
- Installer [hugo](https://gohugo.io/)
- Executer `hugo server -D` pour lancer en local et écouter les modifications

## Publier un nouveau compte-rendus
- Lancer `hugo new posts/nom-de-session.md` ou créé directement le fichier dans le répertoire posts.
- Y écrire le compte-rendu
- Lancer `hugo` pour gérer les pages
- Créer un commit avec les modifications du répertoire `docs`
- Pousser le code :)

