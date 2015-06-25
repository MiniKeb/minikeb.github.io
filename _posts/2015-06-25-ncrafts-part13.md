---
layout: post
title: Et si je vous faisais un retour sur NCrafts... (dernière partie)
---

## Jour 2 - Keynote: The T in TDD : tests, types, tales - [*Mathias Brandewinder*][MathiasBrandewinder]

Pour cette dernière session, Mathias nous offre du codage en direct[^1] avec brio, malgré quelques soucis techniques[^2].  
Il reprend donc l'exemple de multi-devises du [livre de Kent Beck][TDDByExample], et va comparer l'implémentation en C# avec TDD à celle en F# et son retour immédiat grâce à la [REPL][REPL].

Le différence entre les deux langages est de taille.  
En terme de nombre de lignes, F# est déjà beaucoup plus concis, mais en plus l'égalité par référence de C# oblige à écrire une quantité de code supplémentaire non négligeable.  
Ce surplus de code en C#, nuit également à la lisibilité. 

Mathias nous montre, que TDD est évidemment incontournable dans le processus de développement, mais également tout ce que nous apporte F# : 

* Simplification du code.
* Code compréhensible plus simplement par une personne non technique.
* Approche DDD facilité.
* [F# Interactive][FSI] qui permet d'avoir un retour immédiat.
* ... 

Pour conclure, Mathias nous montre que ce que nous cherchons en faisant du TDD, en écrivant d'abord les types et en utilisant la [REPL][REPL], c'est d'avoir un retour le plus rapide possible.  
Le développement évolue et certains outils/techniques nous facilitent ou donnent accès à cette boucle de feedback alors il ne faut pas s'en priver.

---

[^1]: Ouais, ouais, du Live Coding.
[^2]: Mathias a effectivement eu un problème avec son ordinateur et s'en est fait prêter un avec une configuration très différentes de ses habitudes.

[MathiasBrandewinder]: https://twitter.com/brandewinder
[TDDByExample]: http://www.amazon.fr/Test-Driven-Development-By-Example/dp/0321146530
[REPL]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop
[FSI]: https://msdn.microsoft.com/fr-fr/library/dd233175.aspx