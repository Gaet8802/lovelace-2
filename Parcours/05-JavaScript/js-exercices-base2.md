# Deuxième série d'exercices...

## Ressources
Pour vous aider, utilisez ce site. Il y a à priori la réponse à toutes les questions que vous vous poserez. Le sommaire se trouve à gauche (pas à droite comme sur Bootstrap). Fouillez, regardez, cherchez ce dont vous avez besoin. Entraidez-vous également !
- [Le guide Javascript sur le site de Mozilla](https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Introduction)
(site approuvé par [Mika](https://github.com/rivanos))


## Exercices

Créer un fichier HTML pour chaque exercice sur le pattern "ex01.html", "ex02.html",...

### **Exercice 1** - écriture d'une fonction

Créer un bouton "Calculer la surface d'un rectangle". Faites en sorte que lorsqu'on clique sur le bouton, la fonction `surfaceRectagle()` se lance. Cette fonction va demander la saisie d'une largeur, d'une longueur et afficher la surface du rectangle correspondant.

Créer ensuite un nouveau bouton "Calculer le périmètre d'un rectangle". Faites en sorte que lorsqu'on clique sur le bouton, la fonction `periRectangle()` se lance. Cette fonction va demander la saisie d'une largeur, d'une longueur et afficher le périmètre du rectangle.

Pour l'affichage des résultats, pensez à mettre du texte pour qu'on sache à quoi se réfère les réponses finales !

### **Exercice 2** - écriture d'une fonction renvoyant une valeur

Créer une fonction qui :
- demande la saisie d'un rayon;
- retourne la surface du cercle de ce rayon.
Afficher ensuite le résultat de l'appel à cette fonction en cliquant sur un bouton.

### **Exercice 3** - écriture d'une fonction avec arguments

1. Créez deux variables globales `a` et `b`, initialisées respectivement à 3 et à 2.
2. Créez une fonction `triple` prenant un argument x et renvoyant le résultat de la multiplication de x par 3
3. Créez une fonction `affiche`, appelée au clic sur un bouton, qui affiche dans des boîtes d'alerte successivement le résultat de `triple` appliquée à `a`, puis à `b`.

### **Exercice 4** - utilisation d'un tableau

1. Créez un tableau nommé `tab` dont le premier élément est -2, le deuxième 1 et le troisième 4
2. Créez une fonction `additionne` prenant un argument x et renvoyant le résultat de l'addition de x à 2
3. Créez une fonction `affiche`, appelée au clic sur un bouton, qui affiche dans des boîtes d'alerte successivement le résultat de `additionne` appliqué au premier élément, puis au dernier élément du tableau (en utilisant la propriété `length`).

### **Exercice 5** - manipulation des opérateurs

b est toujours initialisée à 2
Quel est le résultat des opérations suivantes ?

- `a=b++;`
- `a=++b;`
- `a=b--;`
- `a=--b;`
- `a+=b++;`
- `a=1; a+=++b;`
- `a=1; a-=b++;`
- `a=1; a-=++b;`
- `a=1; a+=b--;`
- `a=1; a+=--b;`

Pour chacune des opérations, afficher l'opération effectuée, la valeur de `a` après l'opération et la valeur de `b` après l'opération.

### **Exercice 6** - appel à une fonction retournant une valeur

1. Créez un tableau nommé `tab` dont le premier élément est -2, le deuxième 1 et le troisième 4
2. Créez une fonction `soustrait` prenant un argument x et renvoyant le résultat de la soustraction de x-2 si x est positif ou nul, la chaîne de caractères "Nombre négatif!" sinon.
3. Créez une fonction `affiche`, appelée au clic sur le bouton, qui affiche dans des boîtes d'alerte successivement le résultat de `soustrait` appliqué au premier élément, puis au dernier élément du tableau (en utilisant la propriété `length`).

### **Exercice 7** - utilisation de switch

Créer un bouton. Au click de ce bouton, lancer la fonction `faireChoix()`.

Cette fonction demande à l'utilisateur au moyen d'un `prompt()` de choisir entre 1, 2 ou 3.

- s'il choisit 1, on affiche avec une boîte d'alerte "1. Merci"
- s'il choisit 2, on affiche avec une boîte d'alerte "2. Bonjour"
- s'il choisit 3, on affiche avec une boîte d'alerte "3. Au revoir"
- s'il choisit autre chose, on affiche avec une boîte d'alerte "Pardon, que voulez-vous ?"

### **Exercice 8** - utilisation de switch et de l'objet date

Créer un bouton. Au click de ce bouton, lancer la fonction `jourDeLaSemaine()`. Cette fonction détermine le jour de la semaine et affiche selon le cas dimanche, lundi, mardi... etc. jusqu'à samedi.

### **Exercice 9** - utilisation de la boucle while

Créer un bouton. Au click de ce bouton, lancer la fonction `testWhile`. Cette fonction demande à l'utilisateur de saisir une chaîne de caractères contenant la lettre `p`, et le redemande tant que l'utilisateur ne l'a pas fait. Il affiche ensuite la chaîne saisie entre guillemets.

### **Exercice 10** - utilisation de la boucle for

Créer un bouton. Au click de ce bouton, lancer la fonction `somme`. Cette fonction demande trois fois à l'utilisateur de saisir un nombre et affiche ensuite la somme de ces trois nombres.

### **Exercice 11** - utilisation des boucles et tests

Créer un bouton. Au click de ce bouton, lancer la fonction `calculMoyenne`.

Cette fonction va calculer la moyenne des nombres entrés au clavier :

- demande à l'utilisateur d'entrer un nombre entier.
- si l'utilisateur entre autre chose qu'un nombre entier, un message d'alerte signale l'erreur et ensuite, la fonction redemande à l'utilisateur d'entrer un nombre entier.
- tant que le nombre entré est positif ou nul, la fonction mémorise ce nombre et l'additionne aux autres nombres précédemment entrés.
- si le nombre est négatif, alors la fonction calcule la moyenne de tous les nombres entrés en divisant la somme totale par le nombre de valeurs entrées.
- la fonction affiche le nombre de valeurs entrées
- la fonction affiche la moyenne

### **Exercice 12** - Conversion de température Celsius, Fahrenheit et Kelvin

Créer un bouton. Au click de ce bouton, on lance la fonction `conversionTemperature`.

L'utilisateur choisit d'abord dans le menu affiché quel type de conversion il souhaite, il indique son choix en indiquant le numéro correspondant dans le menu au moyen d'un prompt javascript

Ensuite, un second prompt va lui demander la température à convertir et afficher le résultat dans une boîte d'alerte.

Le menu :

0. Fin du programme
1. De Celsius vers Fahrenheit
2. De Celsius vers Kelvin
3. De Fahrenheit vers Celsius
4. De Fahrenheit vers Kelvin
5. De Kelvin vers Celsius
6. De Kelvin vers Fahrenheit

Pour calculer la conversion, utilisez les formules suivantes :

	[°F] = ([°C] x 9/5) + 32
	[K] = [°C] + 273,15
	[°C] = ([°F] - 32) / (9/5)
	[K] = (([°F] - 32) x (5/9)) + 273,15
	[°C] = [K] - 273,15
	[°F] = ([K] x 9/5) - 459,67

	où [K] représente la température en kelvin
	où [°F] représente la température en degrés Fahrenheit
	où [°C] représente la température en degrés Celsius

Exemples de valeurs à tester :
- 0 K = -273,15 °C = -459,67 °F
- 283,15 K = 10 °C = 50 °F
- 273,15 K = 0 °C = 32 °F
- 373,15 K = 100 °C = 212 °F
- 233,15 K = -40 °C = -40 °F


### **Exercice 13** - Calcul de l'IMC

L'IMC ou Indice de Masse Corporelle est utilisé pour évaluer les risques sur la santé liés au surpoids chez l'adulte.
Il se calcule en divisant le poids exprimé en kg par le carré de la taille exprimée en mètre.

    Par exemple :
    - Une personne pesant 95 kg et mesurant 1,81 m a un IMC de 95/(1.81*1.81)= environ 29,0
    - Une personne pesant 48 kg et mesurant 1,69 m a un IMC de 48/(1.69*1.69)= environ 16,8
    - Une personne pesant 61 kg et mesurant 1,57 m a un IMC de 61/(1.57*1.57)= environ 24,7

En fonction de la valeur obtenue, on peut estimer la corpulence de la manière suivante :

    - moins de 16,5 : dénutrition ou famine
    - 16,5 <= IMC < 18,5 : maigreur
    - 18,5 <= IMC < 25 : corpulence normale
    - 25 <= IMC < 30 : surpoids
    - 30 <= IMC < 35 : obésité modérée
    - 35 <= IMC < 40 : obésité sévère
    - plus de 40 : obésité morbide

Créer un bouton. Au click de ce bouton, lancer la fonction `calculIMC`.

Cette fonction va demander le poids et la taille, calculer l'IMC, ensuite l'afficher avec 2 décimales et enfin afficher un message disant dans quelle catégorie de corpulence on se situe.

## Cat tax
![Colonel Meow for the Cat Tax](Colonel-Meow.jpg)

