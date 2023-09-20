# Contexte
## But du laboratoire
### Quoi

Créer une branche, fusionner deux branches et créer une pull request.

### Pourquoi

S'initier à l'utilisation des branches, qui sont une des fonctionnalités les plus importantes de Git.

# Instruction

## Créer une branche

Pour créer une branche nous allons utiliser la commande git suivante:
```bash
git checkout -b ma-branche
```

Où ma-branche est le nom de la branche que nous voulons créer. Cette commande permet de créer une branche et de se placer dessus directement.
Nous allons maintenant faire un changement dans cette branche:
- Ajouter une ligne "Changement fait sur ma-branche" dans index.html
- Commiter les modifications en utilisant la commande suivante :
```bash
git commit -m "Changement fait sur ma-branche"
```
- créer la branche sur le dépôt distant et pousser les changements en utilisant la commande suivante :
```bash
git push --set-upstream origin ma-branche
```

Si l'on se rend sur le dépôt distant depuis notre navigateur, on peut voir la branche créée en cliquant sur le bouton drop-down "master" puis en cliquant sur le nom de la branche que nous avons créée.

## Fusionner deux branches

Plaçons nous dans le contexte suivant:
- Des nouveaux changements ont été apportés à master pendant que vous travailliez sur votre branche ma-branche
- Vous voulez donc ramenez les changements de master vers votre branche de travail, pour rester à jour

On va donc commencer par faire un changement sur master. Pour repasser sur master, nous allons utiliser la commande suivante :
```bash
git checkout master
```

Comme dans les précents labs, nous allons éditer index.html en y ajoutant une ligne, puis nous pousserons les modifications vers le dépôt distant.

Une fois que c'est fait, nous allons repasser sur la branche ma-branche:

```bash
git checkout ma-branche
```

Nous allons maintenant ramener les changements de master vers ma-branche :
```bash
git merge master
```

Il y aura probablement un conflit, selon les modifications que vous avez apportés. Comme montré dans le lab précédent, résolvez le conflit de la façon que vous voulez.
N'oubliez pas de pousser le commit de fusion vers le dépôt distant.

## Creer une pull request

Maintenant nous voulons ramener les changements de notre branche de travail vers master, pour le partager avec le reste de l'équipe.
On pourrait fusionner localement nos branches ma-branche et master, mais ce n'est pas une bonne pratique.
À la place, il faut créer ce qu'on appelle une pull request:
- Rendez vous depuis votre navigateur dans votre dépôt github
- Vous aurez sûrement un encart jaune qui vous propose directement de créer une pull request
 ![images](/images/lab5_compare_pr.png)
- vous pouvez cliquer sur le bouton "Compare & Pull Request"

Si vous n'avez pas ce bouton:
- Allez dans la section "Pull Request"
- Puis cliquez sur le bouton "New Pull Request"
- Laisser base avec master et pour compare sélectionnez ma-branche

Enfin, on peut appuyer sur le bouton "Create Pull Request".
À droite de l'écran vous avez la possibilité d'assigner plusieurs rôle:
- le reviewer sera la personne chargée de faire la revue de code de votre Pull Request
- l'assignee est en général la personne qui a fait les changements présents dans la Pull Request

Quand notre Pull Request est approuvée, on peut cliquer sur le bouton "Merge Pull Request". La fusion sera alors réalisée dans le depot distant.
Lors du prochain pull de master sur notre dépôt local, on verra les changements de notre Pull Request dans master, en local.

# Conclusion
### État du laboratoire
A la fin de ce laboratoire vous devriez savoir:
- Créer votre propre branche
- fusionner une branche dans une autre
- creer une pull request

### Allez plus loin 

```bash 
git log --graph --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%an%C(reset)%C(bold yellow)%d%C(reset) %C(dim white)- %s%C(reset)' --all
```