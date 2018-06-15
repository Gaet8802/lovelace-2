# Le SSH

## Introduction
Puisque on développe pour le web, on doit pouvoir, tu l'auras compris, mettre les fichiers qu'on développe avec nos gentils petits ordinateurs plein de stickers, sur des ordinateurs  qui eux **servent** les fichiers à l'humanité connectée. Ce sont les ordinateurs que te fournissent moyennant monnaie sonnante et trébuchante (ou carte de crédit) les hébergeurs tels que [Gandi](https://gandi.net), [OVH](https://www.ovh.com/fr/), [siteground](https://www.siteground.com/), [AWS](https://aws.amazon.com/fr/), [DigitalOcean](https://www.digitalocean.com/)...

Mais comment faire, concrètement ? Il y a beaucoup d'options possibles, mais pour faire court, la meilleure, c'est le SSH. Parce qu'elle offre plus de sécurité que le FTP ou le http.

Et là, je t'entends t'exclamer :  

## Qu'est-ce que c'est que le èsèshache ?

Le SSH ou *Secure Shell* est un protocole de communication permettant à un "client" (un utilisateur ou même une machine distante) d'ouvrir une session interactive sur une machine distante (serveur) afin d'envoyer des commandes ou des fichiers de manière sécurisée :

 - Contrairement au FTP, les données circulant entre le client et le serveur sont **cryptées**, ce qui garantit leur confidentialité (personne d'autre que le serveur ou le client ne peut lire les informations transitant sur le réseau). Il n'est donc pas possible [d'écouter le réseau](https://www.commentcamarche.com/contents/68-analyseurs-reseau-sniffers) à l'aide d'un [analyseur de trames](https://www.commentcamarche.com/contents/68-analyseurs-reseau-sniffers).
 - Le client et le serveur **s'authentifient mutuellement** afin d'assurer que les deux machines qui communiquent sont bien celles que chacune des parties croit être. Il n'est donc plus possible pour un pirate d'usurper l'identité du client ou du serveur ([spoofing](https://www.commentcamarche.com/contents/71-usurpation-d-adresse-ip-mystification-spoofing)).
 
## Pourquoi en a-t-on besoin (en tant que web dev) ?

En un mot : pour le **déployement**.  
Dans le métier de développeur web on est amené à developper des sites en local (serveur sur notre machine physique)  et puis les transférer sur une *machine de production* (un ordinateur en ligne, quelque part dans le monde, jouant le rôle de serveur). 

## Comment ça marche

Pour l’exemple nous allons utiliser une Raspberry. Celle-ci déjà pré-configurée par votre formateur avec un [serveur Apache](https://fr.wikipedia.org/wiki/Apache_HTTP_Server) et connexion SSH activée.

Pour se connecter en SSH à une autre machine on aura besoin de 3 choses :  

- La commande `ssh`
- des paramètres, tels que `-p`pour le port (par défaut: `22`)
- Le nom d’utilisateur avec lequel on veut se connecter
- Le nom de la machine en réseau ou son ip

La syntaxe donne ceci : 
`ssh user@machineIP` ou `ssh user@machineName`

**Exercice**  
Un serveur de test est disponible sur le wifi `BC_HUB` sous le nom : `becode-server` à l'adresse `10.20.0.238` (elle a peut-être changé, demande à ton coach. Rappelle-lui que la commande est `hostname -I`sur Linux, pour obtenir son adresse iP locale ;-) ). Le port est `1992`.

Connecte-toi en utilisant l'adresse IP, le port, en tant qu'utilisateur `junior`, dont le mot de passe est `yolo`.


Une autre manière de trouver l’adresse IP de la machine est d’utiliser dans ton terminal la commande: `arp -a`

Celle-ci retourne les adresses IP des différentes machines connectées au même réseau que toi.  
Il existe aussi une application nomée “Fing” qui te permet plus facilement de trouver les ip sur ton smartphone.

## Maintenant que je suis connecté, que puis-je faire?

Une fois connecté à l'ordinateur distant, tu peux tout faire... Ou du moins tout ce que l’utilisateur avec lequel tu t'es connecté à le droit de faire !

Voici quelques commandes que tu peux effectuer

- Dans quel directory suis-je ?  ( `pwd`)
- créer un fichier `touch fichier.txt`
- surveiller l'état de la machine (`top` et [plus](https://www.howtogeek.com/107217/how-to-manage-processes-from-the-linux-terminal-10-commands-you-need-to-know/))
- voir l'état des disques durs ([doc](https://askubuntu.com/questions/432836/how-can-i-check-disk-space-used-in-a-partition-using-the-terminal-in-ubuntu-12-0/432842))

## Transférer un fichier de ta machine à la machine distante

Scénario classique : tu as un hébergement web sur un VPS (Virtual Private Server). Typiquement, tu n'auras qu'un accès via SSH,et donc la console.

Tu veux déployer un fichier html. Voici comment faire : 

1. Va dans le dossier servi par le serveur Apache: `/var/www/html`
1. Crée un repertoire portant ton prenom et nom, sans espace ni caractère spéciaux : `ton-prenom-nom`. 
1. ferme ta session  via `exit`
1. Crée un fichier **index.html** sur ton bureau.
1. Modifie ce fichier html et ajoute "Hello I'm ton_nom ". Sauvegarde et ferme-le.
1. Ouvre un nouveau terminal et accède au dossier de ton bureau :  
	- (via la commande `cd ~` ( `~` est un raccourci vers le dossier de l'utilisateur courant).
	- Introduis la commande `ls -lh` pour lister le contenu du dossier dans lequel tu te trouves. Tu devrais voir votre dossier bureau (Desktop).
	- rentre dans le dossier de ton bureau (`Desktop`en anglais). 
	- une fois dedans, affiche le contenu. Tu devrais voir le fichier html que tu viens de créer parmi les autres fichier/dossier sur votre bureau.
1. Maintenant que nous sommes dans le terminal et situé dans le dossier bureau on va pouvoir **transférer notre fichier html sur le serveur**. Souviens-toi, tu as créé un dossier portant ton nom. On va transférer dans ce dossier, via la commande `scp` (Secure CoPy).  
2. Tape la commande: `scp ./index.html junior@adresseIP:/var/www/html/ton-prenom-nom/`

**Syntaxe de la commande scp**  

```bash
scp : secure copy 
./index.html : c’est la "source", le chemin menant au fichier que je souhaite tranférer
junior : mon login de connexion au serveur 
10.20.0.238 : ip de mon serveur distant
:/var/www/html/ton-prenom-nom/ : la "Destination", le répertoire dans lequel je veux copier la source sur mon serveur distant
```
**SI TOUT VA BIEN VOTRE FICHIER HTML SERA VISIBLE À l’ADRESSE**

[http://10.20.0.238/ton-prenom-nom/index.html](http://10.20.0.238/ton-prenom-nom/index.html)

Bravo vous avez utilisez le SHH pour copier un fichier !

## Aller plus loin

Maintenant, tu dois te dire : ce n'est pas très pratique. Et non, c'est vrai... En réalité, ce que l'on fait, c'est des choses comme ceci: aller dans le dossier de destination (le dossier publié), utiliser git pour `pull` la branche `master`! 

Avec ton binôme, peux-tu imaginer la procédure ? Et si tu essayais, dans ton dossier ?


![](./redpill.gif)
