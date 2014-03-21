---
layout: post
title:  "LinuQ - Utilisateur XiVO"
date:   2014-03-20
---

Configurer XiVO
===============

La configuration de la machine se fait en quelques étapes guidées :

![Page d'accueil de l'assistant]({{ site.url }}/assets/wizard/01.png)

Ne pas entrer de mot de passe sensible pour la présentation, il pourra être
utile à d'autres pour vous dépanner.

![Première page de configuration]({{ site.url }}/assets/wizard/02.png)

Les informations données ici sont à titre d'exemple, mais conseillées.

![Deuxième page de configuration]({{ site.url }}/assets/wizard/03.png)


Configurer un utilisateur
=========================

![Page de supervision]({{ site.url }}/assets/user/01.png)

![Page IPBX]({{ site.url }}/assets/user/02.png)

![Page d'ajout utilisateur]({{ site.url }}/assets/user/03.png)

![Page des lignes de l'utilisateur]({{ site.url }}/assets/user/04.png)

Vous pouvez enregistrer votre utilisateur.

-------------------------------------------------------------------------------

Allons maintenant récupérer les informations nécessaires pour enregistrer un
téléphone logiciel pour cet utilisateur. Il nous faut éditer la ligne créée
automatiquement pour l'utilisateur.

![Page des lignes]({{ site.url }}/assets/user/05.png)

Copiez les informations de la ligne ...

![Page d'édition de la ligne]({{ site.url }}/assets/user/06.png)

Ajoutez un compte dans votre téléphone logiciel (ici SFLphone) ...

![Menu de gestion des comptes]({{ site.url }}/assets/user/07.png)

Et collez-y les informations de la ligne. L'adresse IP du serveur est celle de XiVO.

![Formulaire d'ajout de compte SIP]({{ site.url }}/assets/user/08.png)

Votre téléphone logiciel devrait indiquer qu'il s'est enregistré. Vous pouvez
essayer vérifier s'il fonctionne en composant *10, qui devrait vous annoncer
l'état des services activés sur le poste de l'utilisateur auprès de XiVO.
