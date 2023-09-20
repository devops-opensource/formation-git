# Contexte
## But du laboratoire
### Quoi

Créer un dépot Git distant et le synchroniser avec le dépot local.

### Pourquoi

Assurer la persistance du dépôt Git et permettre de travailler en équipe.

# Instruction

## Créer son dépôt distant

Nous allons commencer par créer un dépot sur Github.
Pour cela:
- rendez vous sur https://github.com et connectez vous
- en haut à gauche, cliquez sur le bouton "new" en vert
- Choisissez lui un nom, "mon-premier-repo" par exemple
- Cliquez sur le bouton "create repository"

![images](/images/lab3_create_repo.png)

## Lier son dépôt local au dépôt distant

Maintenant que votre dépôt distant a été créé, il est temps de le lier au dépôt local.
- Depuis votre navigateur, copier l'URL du dépôt Github distant

- Sur votre ordinateur, ajoutez l'URL du dépôt Git distant en utilisant la commande suivante : 
  ```bash
  git remote add origin https://github.com/NomUtilisateur/mon-premier-repo.git.
  ```

- Envoyez vos modifications locales vers le dépôt distant en utilisant la commande suivante : 
  ```bash
  git push -u origin master.
  ```

## Synchroniser son dépôt local avec le dépôt distant

Pour voir comment récupérer des changements faits par une autre personne, nous allons simuler des changements sur le dépot distant en éditant notre index.html depuis notre navigateur :
- dans votre dépôt distant, cliquez sur index.html, puis cliquez sur le crayon à droite "edit this file", cela ouvrira un éditeur
- Procédez à quelques changements dans le texte, en ajoutant des points d'exclamation par exemple
- Enregistrez et commitez les modifications en cliquant sur le bouton "commit changes"
- Laissez le message de commit par défaut et appuyer une seconde fois sur le bouton "commit changes"

Pour ramener ces changements dans notre dépôt local, nous allons utiliser la commande suivante : 
```bash
git pull origin master.
```

Si vous ouvrez index.html en local, vous verrez que les changements que vous avez fait sur le dépôt distant ont bien été ramenés dans votre dépôt local.

# Conclusion
### État du laboratoire 
A la fin de ce laboratoire vous devriez savoir:
- Créer un dépôt sur Github
- Pousser des changements sur un dépôt distant
- Récupérer des changements depuis un dépôt distant

### Allez plus loin 

