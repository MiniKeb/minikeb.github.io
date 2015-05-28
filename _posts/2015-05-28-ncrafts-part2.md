---
layout: post
title: Et si je vous faisais un retour sur NCrafts... (deuxième partie)
---

## Jour 1 - Continuous delivery - the missing parts - [**Paul Stack**][PaulStack]

Paul est probablement l'un des rares intervenants dont je n'avais pas entendu parler avant ce jour, mais fut une réelle et agréable surprise. Sa [session][Slides] pleine d'énergie parlait de DevOps et plus particulièrement de livraison continue (Continuous Delivery).

En premier lieu, Paul nous rappelle que le but du CD[^1] est de <s>builder</s> construire, tester et déployer un projet de manière automatique et fréquente.

Pour cela, il existe les 8 principes du CD[^1] :

1. **The process for releasing/deploying software MUST be repeatable and reliable.**[^2]  
Ce qui nous mène vers le deuxième principe...
2. **Automate everything!**[^3]  
On dit souvent que les bons développeurs doivent être fainéants car ils chercheront à automatiser leurs tâches récurrentes. Pourquoi ne pas automatiser nos processus de livraison?
3. **If somethings difficult or painful, do it more often.**[^4]  
Ca peut paraitre surprenant mais faire et refaire quelque chose de pénible nous pousse naturellement à trouver une solution pour que ce le soit moins. 
4. **Keep everything in source control.**[^5]  
Ceci peut sembler normal aujourd'hui, mais quand on dit tout, c'est tout! Même vos scripts SQL (pour ceux qui en ont encore :) ).
5. **Done means “released”.**[^6]  
Dans les méthodes agiles, on cherche souvent la DoD[^7] pour une fonctionnalité. Pourtant une fonctionnalité n'a de valeur qu'une fois dans les mains de l'utilisateur et qu'elle fonctionne correctement. Dire que la fonctionnalité X est terminé parce qu'on l'a faite tourner sur sa machine et qu'on l'a bien déposé sur le contrôle de code source n'est pas suffisant car elle n'apporte aucune valeur à quiconque.
6. **Build quality in!**[^8]  
Il faut prendre le temps de faire de la qualité et trouver des métriques pour la mesurer. Paul nous renvoie ici vers le premier principe du [manifeste Software Craftmanship][SoftwareCraftmanshipManifesto] : *Pas seulement des logiciels opérationnels, mais aussi des logiciels bien conçus.*.
7. **Everybody has responsibility for the release process.**[^9]  
Le cinquième principe indique qu'une fonctionnalité n'est terminé qu'une fois qu'elle fonctionne correctement en production, simplement parce qu'elle n'a de valeur et ne rapporte d'argent qu'à partir de ce moment. C'est pour cette raison que chacun doit être impliqué dans son cycle de vie et sa livraison en production : les développeurs, les chefs de projets, les testeurs, etc.
8. **Improve continuously.**[^10]  
N'attendez pas que votre système soit dépassé. L'amélioration continue du CD[^1] signifie faire évoluer les processus et les outils de manière à rendre la livraison plus rapide, plus simple à faire évoluer et maintenir.

... et 4 pratiques du CD[^1] :

1. **Build binaries only once.**[^11]  
Si vous recompilez votre logiciel pour votre recette et une fois encore pour votre production, vous avez de forte chance d'avoir des versions divergeantes. Au lieu de cela, ne compilez qu'une fois et déployez ce binaire sur vos différents environnements.
2. **Use precisely the same mechanism to deploy to every environment.**[^12]  
Faites simple, avoir un seul processus pour vos déploiement est plus simple à maintenir, à automatiser et répéter qu'un processus par environnement. Les principes [KISS][KISS] et [DRY][DRY] appliqués au CD[^1] en quelques sortes. :)
3. **Smoke test your deployment.**[^13]  
Après votre déploiement, vérifiez que votre système fonctionne à minima évite bien des désagréments. 
4. **If anything fails, stop the line!**[^14]  
Il me semble que cette pratique nous vient de Toyota, qui s'il y a un problème sur la chaine de production arrete tout, concentre ses efforts sur la résolution de ce problème avant de relancer la production. En gros, si vous rencontrez un problème n'essayez pas de le patcher à la volée, ceci ne fera que vous donner du travail en plus pour une qualité moindre.

Avec ces principes et pratiques en tête, Paul continue sa présentation sur les idées reçues, qu'il a pu entendre.  
J'ai particulièrement retenu et apprécié celle-ci : 

> CD[^1] is simple as hooking github to Azure

Notre orateur nous explique ensuite ce qu'est le DevOps, à savoir un buzzword qui a été collé sur le rapprochement et l'étroite collaboration entre les développeurs et les opérationnels. Ce n'est ni un rôle, ni un poste, ni une personne mais juste une manière de travailler.

D'ailleurs, dans le [manifeste agile][AgileManifesto], on trouve les notions de CD[^1] et rapprochement développement/déploiement, bien avant que le terme *DevOps* n'existe (suite au nom donné à une conférence).

> Notre plus haute priorité est de satisfaire le client en **livrant rapidement et régulièrement** des fonctionnalités à grande valeur ajoutée.

Paul poursuit en nous expliquant que le "DevOps" repose donc sur : 

* Une culture
* L'automatisation
* Des <s>mesures</s> métriques
* Le partage

Il met aussi en avant que l'infrastructure a un impact important et qu'elle ne doit pas être considérée comme un animal de compagnie mais plutôt comme du bétail. Il met en balance l'infrastructure <s>immutable</s> immuable qui rigidifie le process et l'infrastructure <s>disposable</s> disponible qui est utilisable au besoin.

Pour conclure, le déploiement continu fait partie intégrante de notre travail de développeurs. 

Paul nous invite également à lire [The Goal][Book_TheGoal] et plus particulièrement [The Phoenix Project][Book_PhoenixProject] si l'on souhaite approfondir le sujet.

---

[^1]: Continuous Delivery ... suivez un peu.
[^2]: Les processus pour sortir/déployer un logiciel DOIVENT être répétable et fiable.
[^3]: Automatisez tout!
[^4]: Si quelque chose est difficile ou douloureux, faites le plus souvent.
[^5]: Gardez tout sur un contrôle de code source.
[^6]: Terminé signifie "Livré en production".
[^7]: DoD - Definition of Done - Définition du terminé.
[^8]: Construisez avec de la qualité.
[^9]: Tout le monde est responsable de processus de livraison.
[^10]: Amélioration continue.
[^11]: Ne construisez les binaires qu'une fois.
[^12]: Utilisez les mêmes mécanismes pour déployer sur chaque environnement.
[^13]: Smoke tester vos déploiements.
[^14]: Si quelque chose échoue, arrêtez tout!

[PaulStack]: https://twitter.com/stack72
[Slides]: https://speakerdeck.com/stack72/continuous-delivery-the-missing-parts
[SoftwareCraftmanshipManifesto]: http://manifesto.softwarecraftsmanship.org/#/fr-fr
[AgileManifesto]: http://agilemanifesto.org/iso/fr/principles.html
[KISS]: http://fr.wikipedia.org/wiki/Principe_KISS
[DRY]: http://fr.wikipedia.org/wiki/Ne_vous_r%C3%A9p%C3%A9tez_pas
[FunctionalProgDemo]: https://github.com/tjaskula/Talks/

[Book_TheGoal]: http://www.amazon.com/The-Goal-Process-Ongoing-Improvement/dp/0884270610
[Book_PhoenixProject]: http://www.amazon.com/Phoenix-Project-DevOps-Helping-Business/dp/0988262509