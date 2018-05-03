## Objectifs

- Amélioration des compétences en Markdown
- Amélioration des compétences en Git
- Apprentissage d'un workflow avec des contributeurs sur GitHub

## Instructions

Durée : 1 Jour

A plusieurs, jouer à réaliser un [Cadavre exquis](https://fr.wikipedia.org/wiki/Cadavre_exquis_(jeu)) en utilisant Git pour échanger vos contributions. 
**Principe** : arriver à travailler sur les mêmes fichiers en même temps, en gérant les conflits (ou en les évitant).  

### Etape 1 : Initialisation
1. Créer un dépôt sur GitHub nommé `Exercice-Cadavre-Exquis-MonPrenom`
1. Créer un fichier *README.md*
1. En markdown, donner un titre à votre histoire
1. `clone` de votre dépôt sur votre ordinateur
1. Créer une branche __"developpement"__
1. Aller dans cette nouvelle branche
1. Rédiger *3* lignes de textes pour débuter une histoire dans le *README.md* __(en utilisant un maximum le markdown)__
1. Faire un `add`
1. Faire un `commit`
1. Faire un `push` de la branche __"developpement"__
1. Inviter vos collègues en tant que __contributeurs__

### Etape 2 : Contributions
1. Aller sur un dépôt où vous avez été invité
1. Faire un `clone`
1. Faire `git branch -a` pour afficher la liste des branches sur le serveur
1. Faire un `pull` de la branche __"developpement"__
1. Faire un `checkout` sur la branche __"developpement"__
1. Créer une branche nommée __"ajouts-votre-prenom"__ à partir de __"developpement"__
1. Ajouter vos *3* lignes de texte dans le *README.md* à la suite du précédent utilisateur 
1. Faire un `add`
1. Faire un `commit` 
1. Faire un `push`de la branche  __"ajouts-votre-prenom"__
1. Faire un `merge` de votre branche __"ajouts-votre-prenom"__ avec __"developpement"__
1. Faire un `push`de la branche  __"developpement"__
1. Faire ceci pour tous vos autres collègues

### Etape 3 : Versioning
1. Quand tous vos collègues sont passés chez vous, retourner sur votre dépôt
1. Faire un `merge` de "developpement" sur "master"
1. Faire un `tag` de "master" nommé __"version-1"__

### Etape 4 : Correction
1. Créer une branche "corrections" à partir de __"master"__
1. Faire les corrections d'orthographe. S'il n'y en a pas, ajouter la mention ("Sans faute")
1. Faire un `add`
1. Faire un `commit` 
1. Faire un `push`
1. Faire un `merge` avec __"master"__
1. Aller sur la branche __"developpement"__
1. Mettre à jour __"developpement"__ en faisant un merge avec la branche __"corrections"__

### Etape 5 : Fixer les acquis
Rédigez en MarkDown un memo personnel sur le fonctionnement de Git, le `workflow`, les commandes utiles. Gardez-le disponible à tout moment. Complétez-le durant la formation, au fur et à mesure que vous comprenez mieux et que vous rencontrez de nouvelles situations.

## Ressources

- [Git Basics](https://rogerdudler.github.io/git-guide/index.fr.html)
- [Git Cheat Sheet](https://rogerdudler.github.io/git-guide/files/git_cheat_sheet.pdf)

![Git workflow](http://blog.launchdarkly.com/wp-content/uploads/2016/07/Slide2.jpg)

