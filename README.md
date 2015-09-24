# Sculpture de code avec git

Git est un outil de collaboration, donc de communication. Un bon message de 
commit doit donc exprimer `pourquoi` les modifications contenues dans le commit
ont été faites. Quelle est ton intention en ajoutant ce commit au projet ?

## Etapes

### Ecrire un message de commit utile

Un bon message de commit va éclairer les contributeur du projet sur les
raisons qui ont motivées ce commit. Par *contributeurs du projet* j'entend :

* les autres développeurs impliqués sur le projet
* toi même dans 6 mois

Tout le monde peut voir ce que tu as fait (le **quoi**) juste en lisant le code.
Mais le code ne peux jamais expliquer **pourquoi** tu as fait ce commit.

#### Ressources

* [Writing great commit messages](http://sundeepgupta.ca/writing-great-git-commit-messages/)
* [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)
  Lis cet article avec attention, et imprime les 7 règles dans ta tête et partout
  où c'est nécessaire pour que chaque commit que tu écris respecte ces règles.
* [5 Useful Tips For A Better Commit Message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
  Comme le précise cet article tu vas devoir abandonner la commande `git commit -m`
  pour `git commit`, puis écrire ton message de commit dans ton éditeur de texte.
* [Associer son éditeur de texte avec Git](https://help.github.com/articles/associating-text-editors-with-git/)
  Configure git pour qu'il ouvre ton editeur de texte préféré au moment d'écrire
  un message de commit : atom, sublime-text, vim ou même emacs 

### Sculpter sur la bonne branche

Afin de ne pas scier la branche sur laquelle tu est assis-e il faut toujours que
tu soit conscient-e de la branche sur laquelle tu te trouve. Le meilleur moyen
est de personnaliser le prompt de ton shell pour que cette information soit
toujours visible dans ton terminal.

Oh My ZSH est un framework pour gérer la configuration du shell ZSH. C'est un
ZSH est livré avec quelques plugins qui te permettrons de personnaliser ton prompt
et le comportement de ton terminal.

En installant Oh My ZSH je te conseille d'activer le plugin `git` qui va créer
des alias des commandes de git dans ton terminal. C'est à dire que tu pourra
taper les commandes:

* `gst` pour `git status`
* `ga` pour `git add`
* `gc` pour `git commit`
* `gp` pour `git push`
* ... [voir la liste complète](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugin:git)

#### Ressources

* [Installer Oh My ZSH](http://ohmyz.sh/)
* [Liste des thèmes livrés avec Oh My ZSH](https://github.com/robbyrussell/oh-my-zsh/wiki/themes)
  Choisis en un où le nom de la branche en cours est affichée, personellement
  j'utilise le thème *gallois*
* [Exemple de .zshrc](sur mon github)
  Le fichier `~/.zshrc` permet de personnaliser la configuration de ZSH (par
  exemple pour activer le plugin *git*).
  Après avoir modifié et enregistré ce fichier il faut recharger la configuration
  du shell,
  soit en ouvrant un nouveau terminal, soit avec la commande `source ~/.zshrc`
  dans un terminal déjà ouvert.

### Résummer plusieurs commit en un seul

Parfois quand on est sur la branche de travail d'une fonctionnalité, il arrive
à force de tatonnements que l'historique des commits de la branche ne veuille
plus dire grand chose. Comme nous sommes des personnes bien élevées ça nous
dérange de devoir pousser tous le bazar de notre chambre au milieu du salon ou
nos collocs se réunissent.

```
* Ajoute le logo dans la navbar
* Charge la bonne image pour le logo
* Ajoute un lien vers l'accueil sur le logo
* Change l'image avec le nouveau logo
```

Est-ce que les contributeurs du projet ont besoin de connaitre tous les tumultes
de la création d'un logo cliquable ? Peut-être qu'un résumé est suffisant :

```
* Ajoute le logo cliquable dans la navbar
  
  En cliquant sur le logo le visiteur est redirigé vers l'acceuil.
  Il s'agit de la version définitive du logo.
```

Pour garantir la paix sociale, git a anticipé ce cas de figure.  
La commande magique ? `git rebase -i`  
Swiffer n'a qu'à bien se tenir !

#### Ressources

* [Démo de Git rebase](https://www.youtube.com/watch?v=qh9KtjfjzCU)
  Regarde cette démo (~5min) pour découvrire `git rebase -i` en action

### Écrire des messages de commits au scalpel



#### Ressources

## Challenge

### Ranger sa chambre

Redonne du sens à l'historique de cette branche. Garde en tête que tes messages
de commits doivent raconter une histoire à celui ou celle qui les lis.

1. fork [ce repo]()
2. clone ton fork sur ta machine
3. Place toi sur la branche `pere-castor`
4. Remet de l'ordre dans les commits de cette branche
5. Push la branche mise à jour sur ton fork (-f)
6. Depuis github fais une pull request de la branche `

### Critères de validation

* 
