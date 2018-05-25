# Configurer GIT + GitHub



1. Lis d'abord notre [introduction made in BeCode](https://github.com/becodeorg/BeCode/wiki/Git-&-Github).
2. Inscris-toi sur Github : [https://github.com/join](https://github.com/join)


### Profil GitHub

Une fois inscrit•e, prends le temps de mettre à jour ton [profil GitHub](https://github.com/settings/profile). Prénom, Nom et obligatoirement une photo ressente de vous.

### Utiliser GitHub avec le terminal pour **Linux**

Pour te logguer à ton compte GitHub tu dois avoir **une clé SSH** (ce qui permet de ne pas devoir taper son mot de passe à chaque connexion à GitHub). 

Voici les étapes pour la créer et l'envoyer à GitHub :

1. Ouvre ton Terminal.
1. Copie/colle le texte ci-dessous, en changeant l'email par l' email de ton compte GitHub.

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Cela crée une clef ssh, avec l'email comme identifiant.

1. Generating public/private rsa key pair.
When you're prompted to "Enter a file in which to save the key," press `Enter`. This accepts the default file location.

1. Enter a file in which to save the key (/home/user/*my-key-name*): [Press enter]
1. Enter passphrase (empty for no passphrase): [Laisse vide]
1. Enter same passphrase again: [Laisse vide]
1. cat ~/*my-key-name*/*my-key-name*.pub
1. copier la clé ssh ( commence par `ssh-rsa ......`)
1. Suivre ce tuto à partir du point 2 : https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

### Utiliser Git avec le terminal pour **Mac**

Pour se logguer à votre compte GitHub vous devez avoir un clé SSH, voici les étapes qui vous permettrons de la crée et de l'envoyer à GitHub

1. Generating a new SSH key
1. Open Terminal
1. Paste the text below, substituting in your GitHub email address.

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

This creates a new ssh key, using the provided email as a label.

1. Faire le premier point [Generating a new SSH key](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
1. cat ~/.ssh/id_rsa.pub
1. copier la clé ssh ( commence par **ssh-rsa**...)
1. Suivre [ce tuto à partir du point 2](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

### Utiliser Git avec le terminal pour **Windows**

Pour se logguer à votre compte GitHub vous devez avoir un clé SSH, voici les étapes qui vous permettrons de la crée et de l'envoyer à GitHub

1. Generating a new SSH key
1. Open Terminal/cmdr.
1. Paste the text below, substituting in your GitHub email address.

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

This creates a new ssh key, using the provided email as a label.

1. Generating public/private rsa key pair.
When you're prompted to "Enter a file in which to save the key," press `Enter`. This accepts the default file location.
1. Enter a file in which to save the key (/Users/UserName/.ssh/id_rsa): [Press enter]
2. Enter passphrase (empty for no passphrase): [Type a passphrase]
1. Enter same passphrase again: [Type passphrase again]
1. cat ~/.ssh/id_rsa.pub
1. copier la clé ssh ( commence par ssh-rsa ......)
1. Suivre [ce tuto à partir du point 2](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

































