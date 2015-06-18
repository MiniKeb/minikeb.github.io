---
layout: post
title: Et si je vous faisais un retour sur NCrafts... (sixième partie)
---

## Jour 1 - [Introducing EventStorming][Video] - [*Alberto Brandolini*][AlbertoBrandolini]

Dans cette session d'introduction à l'EventStorming, c'est son inventeur en personne, Alberto Brandolini, qui nous en fait la présentation.

Alberto nous explique en premier lieu les constats qui l'ont poussé à arriver à cette méthode de révélation/communication/clarification/exploration *(choisissez le mot qui vous convient le mieux)* d'un domaine métier. 

Il a effectivement constater que :

* Les réunions traditionnelles sont bien souvent improductives :  
Il y a toujours des personnes qui ne sont pas concernées, qui ne comprennent pas certains points mais ne vont pas poser de questions, d'autres qui s'ennuie et joue à Candy Crash sur leur téléphone, etc.
* Les diagrammes UML sont limités pour communiquer à propos d'un domaine :  
Dessiner un diagramme UML détaillé peut être long et fastidieux. Comment faire tenir mon diagramme sur le tableau blanc de la salle de réunion ou sur le paperboard.

Son idée est en somme assez simple et consiste donc à réunir les bonnes personnes dans un lieu approprié avec le matériel nécessaire pour que chacun puisse participer.

### Les personnes

Ce sont les personnes qui ont des questions à poser et sont curieux de la réponse, ainsi que les personnes qui ont les réponses.

### Le lieu

C'est une pièce pouvant accueillir aisément moins d'une dizaine de personnes, sans chaises pour s'assoir. Le fait de rester debout oblige les personnes à être plus participatives.

### Le matériel

C'est un espace *illimité (limité par la taille de la pièce)* d'affichage. En gros déroullez une énorme bande de papier sur tous les murs de la salle. Un marqueur *qui fonctionne* et un stock de post-it par personne.

### Le fonctionnement

En prenant l'horizontalité de l'affichage comme ligne de temps, les participants commencent par coller un post-it d'une couleur donnée pour chaque **événement** du domaine.  
Certains événements étant la conséquence directe d'une action utilisateur, on choisira alors une couleur de post-it différente pour ces **commandes**.  
Ensuite, on fait apparaître les **utilisateurs** et **systèmes externes**, dans des couleurs différentes.  
Pour finir on définit les **aggrégats** et les **bounded context**.

Pour conclure, avec la méthode d'Alberto : 

* les personnes sont plus participatives puisqu'elles peuvent travailler en petit groupe ou même seule dans leur coin dans un premier temps.
* les échanges sur les problématiques métiers sont facilité.
* la visualisation de l'ensemble est plus aisé et il reste possible de *zoomer* sur une partie spécifique du domaine.
* le métier est au coeur des échanges, contrairement à UML par exemple qui va se centrer sur la technique. On est dans une approche DDD[^1].

Je regrette un peu de ne pas avoir eu l'occasion de participer au workshop qui avait lieu la veille, histoire d'avoir une meilleure idée de cette pratique mais cette approche me semble plus qu'intéressante.  
Après discussion avec Alberto Brandolini, il semble que s'essayer à un EventStorming même *pour du beurre* permet déjà de mieux appréhender l'outils et de se faire la main.  

Peut être qu'essayer l'EventStorming sera l'occasion d'un futur post.

---

[^1]: Domain Driven Design

[Video]: http://videos.ncrafts.io/video/130202708
[AlbertoBrandolini]: https://twitter.com/ziobrando

