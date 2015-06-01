---
layout: post
title: Et si je vous faisais un retour sur NCrafts... (cinquième partie)
---

## Jour 1 - TDD is dead?!? Let's do an autopsy - [*Bruno Boucard*][BrunoBoucard] et [*Thomas Pierrain*][ThomasPierrain]

Dans cette [session][Slides], Bruno et Thomas essayent de répondre à la question :

> Pourquoi si peu de monde utilise TDD[^1] quotidiennement dans son travail ?

La première raison est probablement que le mantra de TDD n'est pas suffisant.

![Red-Green-Refactor][RedGreenRefactor]

On ne peut pas faire du TDD sans avoir une vue d'ensemble, et pour cela Bruno et Thomas nous font prendre un peu de recul.  

Tout d'abord nos orateurs nous parlent de la règle des [10K heures][10KHours], selon laquelle il est possible d'avoir un très bon niveau dans de nombreux domaines à partir de 10000 heures de pratique.  

Le TDD, c'est pareil!  
Si vous ne le pratiquez pas, vous ne risquez pas de vous améliorer. Pour cela, il faut pratiquer : faire des [Katas][KataCatalog] ou participer à des [Coding Dojo][CodingDojo].

Bruno et Thomas poursuivent leur session en répondant aux différentes idées reçues pouvant démoraliser les personnes se mettant à TDD.

> On m'a dit qu'avec TDD, le design allait émerger tout seul. Pourtant ... :(

Ce peut être vrai, mais il faut s'être préparé en amont : 

* Avoir creusé et approfondit son sujet : On ne peut pas faire émerger un bon design lorsqu'on y connait rien en design. En POO par exemple, l'utilisation des [patrons de conception][DesignPattern] nécessite de les connaitre.
* Échanger avec d'autres développeurs : Je crois que l'on apprend jamais mieux qu'en partageant et échangeant avec ses pairs.
* Nommer ses tests avec "Should" : En indiquant dans le nom du test ce qu'il **DOIT** faire, il devient facile d'identifier le comportement et on se pousse à ne tester **QUE** le comportement.

> Oui, mais avec TDD, on avance pas aussi vite.  

La qualité a effectivement un prix, mais sérieusement vous vous rendez compte que vous mettez du code **non testé en production**?  
Cela va probablement vous surprendre, mais écrire le code n'est pas la partie la plus lente de notre travail.  
Effectivement, comme nous l'a présenté Laurent Bossavit dans sa [Keynote][Keynote], notre cerveau fonctionne à 2 vitesses :

* Le système 1 qui est rapide, nous donne des réponses instantannées. Si on vous dit "Winter is ... " votre réponse sera probablement "...coming" dans la seconde. C'est ce système que l'on utilise pour écrire le code.
* Le système 2 qui est plus lent, nous donne des réponses nécessitant réflexion. Si on vous demande le résultat d'une multiplication (17 x 24), il vous faudra très certainement plusieurs secondes pour y répondre. C'est le système que l'on utilise pour concevoir.

Avec TDD, vous ne pissez plus du code, mais vous prenez le temps de réfléchir à votre code. Il apparait donc normal que cela soit plus lent.

> On a fait du TDD, mais on devient de plus en plus lent.  
> Ca devient un problème pour l'équipe.

L'une des erreurs fréquentes lorsque l'on débute en TDD est de tester l'implémentation au lieu du comportement.   L'implémentation peut et VA changer (ne serait ce que l'étape Refacto du mantra), en revanche le comportement lui devrait rester le même.

Ci-dessous, en dehors du fait que les tests soient mal nommées, ils testent l'implémentation.  
C'est ce genre de tests qui finit par mettre des épines dans les pieds des développeurs et les empêche d'avancer.

	[Test]
	public void Test1()
	{
		BasketManager.Set("Cerises", 2);
		Assert.AreEqual(2, BasketManager.GetItem("Cerises"));
	}

	[Test]
	public void Test2()
	{
		Assert.AreEqual(0, BasketManager.GetValue());
	}

Ci-dessous, on teste uniquement comportement :

	[Test]
	public void Should_provide_total_price_when_a_customer_adds_few_articles()
	{
		basket.Add("Cerises", 2);
		basket.Add("Pommes", 2);
		basket.Add("Bananes", 1);
		Assert.That(basket.Price(), Is.EqualTo(500));
	}

> TDD, c'est vraiment efficace?

Bien sûr, ca permet de ne faire (et tester) que ce dont on a besoin. De plus TDD est un outil fantastique pour avoir un retour immédiat sur son travail.  

Vous pouvez aussi doubler votre boucle de feedback en faisant de l'ATDD[^2] :

1. Ecrire un test d'acceptation qui échoue
2. Ecrire un test unitaire qui échoue
3. Faire passer le test unitaire
4. Refactorer
5. Goto 2, jusqu'à ce que le test d'acceptation passe
6. Goto 1

Pour conclure, si une équipe échoue en utilisant TDD, c'est bien souvent parce qu'il est mal utilisé.
Ne vous contentez pas de suivre le mantra *Red > Green > Refactor*, mais étudiez et pratiquez régulièrement.

---

[^1]: Test Driven Development
[^2]: Acceptance Test Driven Development

[BrunoBoucard]: https://twitter.com/brunoboucard
[ThomasPierrain]: https://twitter.com/tpierrain
[Slides]: http://fr.slideshare.net/ThomasPierrain/if-tdd-is-dead-then-do-an-autospy-16-9-v24
[10KHours]: http://en.wikipedia.org/wiki/Outliers_(book)
[CodingDojo]: http://fr.wikipedia.org/wiki/Coding_dojo
[KataCatalog]: http://www.codingdojo.org/cgi-bin/index.pl?KataCatalogue
[DesignPattern]: http://fr.wikipedia.org/wiki/Patron_de_conception
[Keynote]: /2015/05/28/ncrafts-part1/

[RedGreenRefactor]: https://manojjaggavarapu.files.wordpress.com/2012/07/redgreenrefacor.png