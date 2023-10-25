# Contexte
## But du laboratoire
### Quoi
Installer les éléments préalables nécessaire a la journée de formation

### Pourquoi
Focuser sur l'apprentissage dans la journée de formation et non sur l'installation

# Instruction
## Télécharger Git pour Windows
1. Allez sur le site Web de Git : https://git-scm.com/downloads et télécharger la dernière version.

2. Lors de l'installation assurez vous de cocher ces options:
- ![images](/images/lab0_default_option_git_installation.png)

3. Vous pouvez prendre l'éditeur par défaut de votre choix, mais pour ce cours j'utiliserais visual studio code:
- ![images](/images/lab0_default_editor.png)

4. Prenez la deuxième option et nous allons utiliser le nom main dans le contexte de la formation. Cette configuration peut être changé par la suite.
- ![images](/images/lab0_default_editor.png)

5. Pour le reste des étapes suivantes vous pouvez prendre l'option par défaut.


## Créer son compte GitHub

1) Allez sur le site Web de GitHub : https://github.com/
2) Cliquez sur "S'inscrire" en haut à droite de la page
3) Entrez votre adresse e-mail, un mot de passe et un nom d'utilisateur
4) Cliquez sur "Créer un compte"


Après avoir valider le compte avec le code d'activation reçu par email, il suffit de descendre complè
tement en bas de la page et de cliquer sur *skip personnalisation*. La formation ne nécessite pas d'activer des fonctionnalités en particulier offerte par la plateforme GitHub.

Nous y revidendrons par contre en fin de journée!

## Configurer Git avec les informations de base
1. Ouvrez une invite de commande (ou un terminal) sur votre poste de travail.
2. Entrez les commandes suivantes pour configurer votre nom d'utilisateur et votre adresse e-mail associée à Git :

```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre@adresse-email.com"
```

## Mettre en place **git credentials manager**

Dans certains environnements, il est nécessaire d'utiliser un gestionnaire de mot de passe pour stocker les informations d'identification de Git, telles que les noms d'utilisateur et les mots de passe. Le gestionnaire de mot de passe Git est appelé Git Credentials Manager.

Si vous avez suivi les instructions du laboratoire 0, le manager devrait être installé et devrait vous demander vos informations lors de la première connexion avec github.

```bash
git config --show-origin --get-all credential.helper
```

Un résultat similaire a ceci devrait sortir:

```bash
file:C:/Program Files/Git/etc/gitconfig manager
file:C:/Users/sebas/.gitconfig  C:/Users/MY_USER/AppData/Local/Programs/Git\ Credential\ Manager/git-credential-manager
file:C:/Users/sebas/.gitconfig  manager
```

1. Ouvrez une invite de commande (ou un terminal) et exécutez la commande suivante pour activer Git Credentials Manager :

```bash 
git config --global credential.helper manager
```

## Identifier les éléments que l'on croise souvent en entreprise
### Proxy 
Dans de nombreux environnements d'entreprise, l'accès à Internet est configuré via un proxy. Pour configurer Git pour travailler via un proxy, vous devez configurer les paramètres de proxy Git en entrant les commandes suivantes :

```bash
git config --global http.proxy http://user:password@proxy_address:proxy_port
git config --global https.proxy https://user:password@proxy_address:proxy_port
```

Remplacez user et password par vos informations d'identification de proxy, proxy_address par l'adresse IP ou le nom de domaine de votre proxy et proxy_port par le port de votre proxy.


# Conclusion
## État du laboratoire
A la fin de ce laboratoire vous devriez avoir: 
- Github for windows installé avec succès sur votre poste
- Un compte GitHub 
- Git de configurer sur son poste local 