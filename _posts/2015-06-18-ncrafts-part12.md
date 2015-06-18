---
layout: post
title: Et si je vous faisais un retour sur NCrafts... (douzième partie)
---

## Jour 2 - When DDD meets Documentation - [*Cyrille Martraire*][CyrilleMartraire]

La session de Cyrille traite d'un sujet qui ne fait généralement pas le bonheur des développeurs : **La documentation**.

En tant que développeurs, lorsqu'on nous parle *documentation*, on pense à la rédaction d'un document word, la schématisation par un diagramme UML ou encore des commentaires dans le code. Bref à quelque chose de fatidieux à maintenir en cohérence avec le code, qui prend du temps et qui ne sera probablement jamais lu par personne *ou presque*.

Pourtant la documentation a pour but de **communiquer des connaissances**.  
Bien sûr, il y a des moyens bien plus efficace de transmettre la connaissance, le pair-programming est l'un de ces moyens, mais comment faire pour avoir de la documentation qui soit en synchrone avec ce que fait le code ? La réponse est simple faire de la **documentation vivante**.

BDD[^1] fait partie de ce type de documentation restant à jour. Néanmoins, pour avoir une documentation la plus vivante possible, la meilleure solution reste encore d'exploiter directement le code.  

Et c'est ce que nous montre Cyrille : 
* en annotant son code pour identifier les *DDD[^2] building blocks*, il est possible de générer un glossaire du métier. De plus le glossaire permettra de mettre en exergue si vous faites mal du DDD[^2].
* en prenant soin de son architecture[^3] et avec quelques convention de nommage, il est possible de générer un diagramme qui de surcroit nous donne l'occasion de visualiser rapidement les complexités ou problèmes d'architecture.

La grande difficulté de cette activité de documentation vivante est le filtrage des informations inutiles, mais le retour est énorme car cette documentation donne du feedback sur la qualité du code.  

Pour faire court, simplifiez votre code et votre architecture et la documentation sera déjà à moitié faite.

Cyrille termine sa session par une autopromotion de son livre [*Living Documentation*][LivingDocumentation] qui semble approfondir le sujet.

En conclusion, cette session donne envie de se (re)mettre à la documentation pourvu qu'elle soit vivante.  
Cyrille est orateur que j'apprécie beaucoup pour l'accessibilité et l'énergie qu'il peut mettre dans ses présentations, je vous invite donc à regarder celle dont je viens de vous parler sur [SkillsMatter][SkillsMatter].

---

[^1]: Behavior Driven Development.
[^2]: Domain Driven Design.
[^3]: Avec une architecture hexagonale par exemple.

[CyrilleMartraire]: https://twitter.com/cyriux
[LivingDocumentation]: https://leanpub.com/livingdocumentation
[SkillsMatter]: https://skillsmatter.com/skillscasts/6273-cyrille-martraire
