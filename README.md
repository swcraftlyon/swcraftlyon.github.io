# sessions

Dépôt pour le code et les compte-rendus des sessions des software crafters de Lyon.

## Executer en local
- Cloner le repository : `git clone --recursive git@github.com:swcraftlyon/sessions.git`. Noter le recursive pour charger les submodules. Le thème sera manquant dans le cas inverse.
- Installer [hugo](https://gohugo.io/)
- Executer `hugo server -D` pour lancer en local et écouter les modifications

## Publier un nouveau compte-rendus
- Lancer `hugo new posts/nom-de-session.md` ou créé directement le fichier dans le répertoire posts.
- Y écrire le compte-rendu
- Pousser le code :)

## Actualiser le site
- Si cela n'a pas déjà été fait, initialisé le worktree dans dist : `git worktree add ./dist master`
- Allez dans le répertoire et mettez à jour dist: `cd dist && git fetch && git rebase && cd -`
- Lancer `hugo -d dist` pour gérer les pages
- Créer un commit avec les modifications du répertoire dist: `cd dist && git add . && git commit -m "regenerate of dev" && git push && cd -`