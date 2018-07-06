# Exercice : Narrative Domain name suggestion tool

J'entends par "domaine narratif" des noms de domaines tels que : 

- "http://viv.re"
- "http://takeme.in"
- "http://carnivo.re"

Comme tu le vois, la partie du TLD termine un mot existant, ce qui fait un peu guili dans le ventre, un petit instant d'amusement.

voici un [repository contenant tous les TLD](https://github.com/umpirsky/tld-list) dans des formats pratiques (json, xml ...) 

## Ta mission

Développe un outil, que tu voudras le plus simple à utiliser, qui permette de vérifier si la fin de ce que l'on tape dans un champs de texte pourrait être un TLD. 

Exemple : dans un champs texte, l'utilisateur a l'idée d'un produit qui s'appelerait "Do Not Forget Me!". L'interface retourne 


Bonus, vérifier ensuite si le nom de domaine suggéré est disponible (l'api de gandi.net je pense, le permet) et si oui, afficher un bouton "buy now".

Bonus, fais du TTD (Test-Driven Development). Voici une série d'inputs / outputs (ajoutes-en d'autres)

### Inputs / outputs
Ton algorithme doit retourner ces outputs lorsqu'il reçoit ces inputs:

- "do not forget me" -> "do-not-forget.me" et "donotforget.me"
- "Do not forget me!" -> "do-not-forget.me" et "donotforget.me"
- " ç!eDo not forget me!" -> "do-not-forget.me" et "donotforget.me"
- "Donuts, je t'adore." -> "donuts-je-tado.re" et "donutsjetado.re"
