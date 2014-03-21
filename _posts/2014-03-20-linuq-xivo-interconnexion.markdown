---
layout: post
title:  "LinuQ - Interconnexion XiVO"
date:   2014-03-20
---

Nous allons construire le réseau suivant :

![Schéma d'interconnexion]({{ site.url }}/assets/interconnections.svg)

Configurer une interconnexion
=============================

![]({{ site.url }}/assets/trunk/01.png)

* L'adresse IP donnée est celle du XiVO passerelle, sur lequel les différents XiVO
vont venir s'enregistrer.
* Le nom et l'identifiant d'authentification doivent impérativement être les mêmes.

![]({{ site.url }}/assets/trunk/02.png)

![]({{ site.url }}/assets/trunk/03.png)

Enregistrez l'interconnexion.

-------------------------------------------------------------------------------

Nous allons configurer le nécessaire pour recevoir des appels.

![]({{ site.url }}/assets/trunk/04.png)

![]({{ site.url }}/assets/trunk/05.png)

Enregistrez l'appel entrant.

-------------------------------------------------------------------------------

Nous allons configurer le nécessaire pour émettre des appels.

![]({{ site.url }}/assets/trunk/06.png)

![]({{ site.url }}/assets/trunk/07.png)

L'extension "X." dit au XiVO : "fais passer tous les appels vers une destination
inconnue par cette interconnexion".

![]({{ site.url }}/assets/trunk/08.png)

Enregistrez l'appel sortant.
