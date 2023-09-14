
# Théorie

# Contexte
## But du laboratoire
### Quoi
Dans ce laboratoire, nous allons apprendre comment travailler localement sur son poste avec Git, comment créer un dépôt Git, réaliser son premier commit, réussir son dépôt et comprendre les caractéristiques des dossiers cachés .git.
### Pourquoi
Comprendre comment travailler localement avec Git est une étape essentielle pour tout développeur. Cela permet de suivre l'historique des modifications apportées à son code, de gérer les différentes versions de son code et de travailler en équipe en facilitant le partage de code et la collaboration.

# Instruction
## Initaliser son dépot Git et y ajouter un fichier
Comment faire un dépôt Git, réaliser son premier Commit :

Ouvrir le terminal ou l'invite de commande (Command Prompt sous Windows) et accéder au répertoire souhaité en utilisant la commande suivante :

```bash
cd chemin/vers/mon-répertoire
```

Initialiser un nouveau dépôt Git en utilisant la commande suivante :
```bash
git init
```

Créer un nouveau fichier nommé "index.html" dans le répertoire "mon-répertoire". Vous pouvez le faire en utilisant votre éditeur de texte préféré ou en utilisant la commande suivante dans votre terminal :
```bash
echo "Hello World" > index.html
```
## Initaliser son dépot Git et y ajouter un fichier
Maintenant que le fichier a été ajouté dans le répertoire local, regardons au niveau de git avec la commande suivante:

```bash
git status
```

Ajouter le fichier "index.html" à l'index des modifications en utilisant la commande suivante :
```bash
git add index.html
```

Exécutons a nouveau la commande de statut:
```bash
git status
```

Comparons maintenant la différence:
```bash
On branch main
No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
nothing added to commit but untracked files present (use "git add" to track)
```

Réaliser votre premier Commit en utilisant la commande suivante :

```bash
git commit -m "Ajout du fichier index.html"
```

Avec ces étapes, vous avez créé un nouveau dépôt Git, ajouté un nouveau fichier, indexé les modifications et réalisé votre premier Commit.

## Lier son dépot a git

Maintenant que votre premier Commit est réalisé, il est temps de réussir votre dépôt Git et d'initialiser le dépôt dans le dossier actif.

- Créez un nouveau dépôt Git sur votre compte GitHub.
- Sur votre ordinateur, ajoutez l'URL du dépôt Git distant en utilisant la commande suivante : git remote add origin https://github.com/NomUtilisateur/mon-repo.git.

- Envoyez vos modifications locales vers le dépôt distant en utilisant la commande suivante : git push -u origin master.


# Conclusion
### État du laboratoire 
A la fin de ce laboratoire vous devriez avoir:

### Allez plus loin 

```bash 
git log --graph --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%an%C(reset)%C(bold yellow)%d%C(reset) %C(dim white)- %s%C(reset)' --all
```