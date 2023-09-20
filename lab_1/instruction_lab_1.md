# Contexte
## But du laboratoire
### Quoi
Le but de ce laboratoire est de configurer Git sur votre poste de travail et d'explorer certains des éléments que vous pouvez rencontrer en entreprise et qui nécessitent une configuration.

### Pourquoi
La configuration de Git est une étape importante avant de commencer à utiliser Git pour gérer des projets. Il est également important de comprendre les éléments que l'on peut rencontrer dans un environnement de travail et qui nécessitent une configuration pour pouvoir travailler efficacement.

# Instruction
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
### État du laboratoire 
A la fin de ce laboratoire vous devriez avoir:
- Git de configurer sur son poste local 
- Une meilleure compréhension des éléments que l'on doit configurer