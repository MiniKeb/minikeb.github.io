---
layout: post
title: Et si je vous faisais un retour sur NCrafts... (troisième partie)
---

## Jour 1 - Functional Programming in C# - [*Tomasz Jaskula*][TomaszJaskula]

Dans cette [session][Slides], Tomasz nous montre qu'il est possible de faire du [fonctionnel en C#][Code].

Il commence en expliquant que la composition est bien souvent le moyen utilisé pour résoudre la complexité dans nos programmes et nous trouvons souvent une aide dans les frameworks d'injection de dépendances.  
Ces derniers semblent nous faciliter la vie pour résoudre les dépendances, pourtant ils nous font oublier à quel point il peut être douloureux d'écrire du code non couplé en POO[^1].  
Avec ces frameworks, on finit par avoir énormément de code de <s>plomberie</s> configuration par rapport au code qui importe vraiment. Par exemple, lorsqu'une nouvelle personne arrive dans une équipe utilisant un de ces frameworks, il y a tout un tas de magie qu'il ne peut comprendre juste en lisant le code.

En programmation fonctionnelle, on résoud la complexité en composant les fonctions. Les dépendances sont donc directement fournies en paramètre aux fonctions qui les utilisent: L'application partielle entre en jeu.

Tomasz continue sa session avec une [démonstration][Code] de parsing d'un texte en C#. Il y a un peu de code nécessaire pour wrapper/dé-wrapper le résultat, mais l'ensemble reste simple et lisible.

Il termine sa session en expliquant que cela aurait effectivement encore été plus simple en F#, mais le but était de montrer que le faire en C# n'était pas si compliqué et retirait la part de *magie* des frameworks d'injection.

Pour finir, faites simple et recentrez vous sur le code nécessaire à votre business.

---

[^1]: Programmation Orientée Objet

[TomaszJaskula]: https://twitter.com/tjaskula
[Code]: https://github.com/tjaskula/Talks/tree/master/FunctionalCSharp
[Slides]: http://fr.slideshare.net/tjaskula/functional-dependency-injection-in-f