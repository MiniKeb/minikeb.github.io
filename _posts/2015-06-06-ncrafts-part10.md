---
layout: post
title: Et si je vous faisais un retour sur NCrafts... (dixième partie)
---

## Jour 2 - Enterprise Tic-Tac-Toe - [*Scott Wlaschin*][ScottWlaschin]

Scott nous explique qu'il espère cette version *entreprise* de son cas d'utilisation de F#, plus parlante que les habituels projets demo *entreprise* que [l'on trouve][PlusPHP] [sur le net][FizzBuzzEnterprise].

Il débute donc sa session par quelques notions de base de F# avant de s'attaquer à son sujet :  
Développer un Tic-Tac-Toe client/serveur en mode entreprise.

Derrière le terme *entreprise*, se trouve en fait : 

* La **séparation des aspects**[^1] pour que des équipes spécialisées puissent travailler sur différentes parties du code en même temps.
* Une **API documentée**.
* Un **modèle sécurisé** pour éviter des actions non autorisées.
* Du **code bien documentée** pour que les architeces soient content de voir que cela correspond au diagramme UML.
* De la **journalisation** *(log)*.
* De la **scalability**[^2].

Scott nous montre donc comment il va définir son domaine.  
Il commence par les types et fait apparaitre chaque cas d'utilisation sous forme d'une fonction (avec une seule entrée et une seule sortie).

Je ne vais pas poursuivre plus en détail puisque vous trouverez très clairement toutes les informations sur les [posts de F# for fun and profit][TicTacToe], jusqu'à la très intéressante petite[^3] digression à propos de [Rest/Hateoas][Hateoas].

En bref, Scott nous fait une présentation captivante et ludique. Son site [F# for fun and profit][FSharpForFunAndProfit] l'est tout autant et je vous encourage vivement à vous y attarder si ce langage vous intrigue.

---

[^1]: Ok, je ne sais pas trop comment traduire *Separation of concerns*.
[^2]: Bon, celui-ci je n'ai même pas essayé de le traduire en *évolutivité*.
[^3]: C'est moi ou ça fait beaucoup d'adjectifs d'un coup?

[ScottWlaschin]: https://twitter.com/scottwlaschin
[TicTacToe]: http://fsharpforfunandprofit.com/posts/enterprise-tic-tac-toe/
[FSharpForFunAndProfit]: http://fsharpforfunandprofit.com/
[PlusPHP]: https://github.com/Herzult/SimplePHPEasyPlus
[FizzBuzzEnterprise]: https://github.com/EnterpriseQualityCoding/FizzBuzzEnterpriseEdition
[Hateoas]: https://en.wikipedia.org/wiki/HATEOAS