# sessions

Dépôt pour le code et les comptes-rendus des sessions des software crafters de Lyon.

## Executer en local
- Cloner le repository : `git clone --recursive git@github.com:swcraftlyon/swcraftlyon.github.io.git`. Noter le recursive pour charger les submodules. Le thème sera manquant dans le cas inverse.
- Installer [hugo](https://gohugo.io/)
- Executer `hugo server -D` pour lancer en local et écouter les modifications

## Rajouter un nouveau compte-rendu
- Lancer `hugo new content/posts/nom-de-session.md` ou créé directement le fichier dans le répertoire posts.
- Y écrire le compte-rendu
- Pousser le code :)

## Actualiser le site manuellement
L'intégration continue de github est configurée pour mettre le site automatiquement à jour.  
Néanmoins, en cas de problème, voici la procédure pour le faire manuellement :
- Si cela n'a pas déjà été fait, initialisé le worktree dans dist : `git worktree add ./dist master`
- Allez dans le répertoire et mettez à jour dist: `cd dist && git fetch && git rebase && cd -`
- Lancer `hugo -d dist` pour gérer les pages
- Créer un commit avec les modifications du répertoire dist: `cd dist && git add . && git commit -m "regenerate of dev" && git push && cd -`
