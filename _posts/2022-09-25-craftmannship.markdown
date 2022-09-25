---
layout: post
title:  "Bricolage et développement informatique"
date:   2022-09-25 10:00:00 +0100
categories: developement
abstract: Comment le bricolage m'a permis d'être un meilleur développeur, ou l'inverse. 
---
### Avertissement
L'auteur décline toute réponsabilité quant aux éventuels préjudices matériels ou blessures physiques, 
si un tiers, personne morale ou physique, 

### Introduction
Dans la vie, j'ai quelques passions, ou du moins des passes temps, et le bricolage en fait partie.
Je suis littérallement né dedans, mon père ayant rénové la maison familliale pendant de mon enfance jusqu'à l'adolescence.
J'avais donc comme terrain de jeu, des parpaings à la place de Lego, et des rivets pour remplacer les épées Playmobil.
Et donc durant l'hiver 2008, suite à l'achat de notre appartement, j'ai mis le doigt dans l'engrenage de la rénovation immobilière.
Depuis, je n'ai pas réussi à en sortir.
Parallèlement, j'ai débuté ma carrière de développeur, et après presque 15 ans, je vais vous partager mon analyse sur ces deux domaines, mes astuces, mes réussites et mes quelques échecs, avec comme fil conducteur ces deux questions :
Doit-on considérer un chantier de rénovation comme un projet informatique? Si oui, l'inverse est-il vrai ?

### Avant de débuter
Avec les méthodes agiles, le client, et ses besoins sont revenus au centre des problématiques.
Pourquoi doit-on développé service multi threadé de mise à jour de fichiers?
Pour le fun? Pour dépasser notre condition humaine?
Non, pour répondre à un besoin d'un client.
Quand on double une cloison, c'est pour isoler un mur le plus souvent, ce n'est surement pas pour le plaisir.
Donc comme n'importe quel projet informatique, il y a un besoin client, la plus part du temps heureusement on fait parti de cette entité,
de ce fait on peut être "exigent" et râler sur les demandes débiles.
En allant plus loin, la rénovation d'une maison peut s'apparenter à de l'édition software
des epics par ex. Rénovation du premier étage
des stories, par ex. En tant qu'invité j'aimerais prendre une douche sans avoir l'impression d'être dans un pays du tier monde
des tâches, enlever l'ancienne baignoire   

### Les résources humaines et matérielles 
Après plus d'une décennie, j'en suis arriver à la conclusion que le bricolage consiste à remplacer des matériaux, par d'autres.
En gros, c'est juste du remplacement, on casse un mur de brique pour le remplacer par une cloison en placoplâtre. Les gravats vont à la déchetterie, et la nouvelle cloison remplace l'ancienne. Si j'était tordu, je dirais que c'est la parfaite illustratrion de la fameuse phrase de Lavoisier "Rien ne se créé, rien ne se perd tout se transforme".
Et bien pour le developpement, je trouve que c'est difficilement comparable pour une fois.
On part généralement d'une absence de code pour une nouvelle fonctionnalité, et on se rapproche peut etre plus de la correction de bug, à savoir
remplacer du mauvais code par du bon code.

"image les inconnus"
"Tu vois le bon code ben il fait un truc, mais il est bon. Le mauvais code, il fait un truc mais c'est un mauvais code, tu vois?"

Une phase primordiale du bricolage, c'est le choix, et l'achat des matériaux. A cette étape là, il faut déjà avoir une vue bien définie du projet, car une ressource non infinie et donc l'usage doit se faire avec parcimonie est le temps. 
Passer du temps en magasin à choisir, ou revenir pour la seconde ou troisième fois par oubli ou mauvais choix, peut nuire à la réussite d'un projet. 
Mon astuce, c'est de faire des schémas, en partant du besoin (encore une fois), et je commence par dessiner la solution la meilleure, puis je modifie en intégrant les contraintes techniques (par ex. surface au sol, distance des habitations voisines).
Quand j'arrive à une solution, répondant aux besoins tout en étant conforme aux exigences, ben là je vais sur le site web de ma grande surface de bricolage. Généralement, l'étape du chiffrage m'a rarement réservé des surprises mais si c'est le cas, il faut reconsidérer les étapes précédentes, voir diminuer les fonctionnalités.

Là normalement, vous voyez les similitudes avec la gestion de projet, comme la conversion du besoin client en cahier des charges, puis chiffrage.
Par contre en développement on va rarement à la pêche au code sur étagère...quoiqu'effectivement quand on a une problématique insoluble, l'un des premiers reflexes c'est d'utiliser le fameux moteur de recherche, et de piocher les solutions les mieux notées sur StackOverFlow.

Quand on aborde le sujet des ressources humaines, on retrouve des similitudes. Pour appel à un prestataire, peut s'avérer être réel gain de temps, et de qualité. On pourrait se dire la même chose pour le développement, même la qualité des prestataires des ESN varie autant que celle des artisans. C'est à double tranchant, en informatique suite à une mauvaise prestation on peut se trainer un historique lourd à maintenir, idem pour un carrelage mal posé ou un mur pas droit.


### Savoir gérer les aléas
Alors, là c'est THE point important, et qui a fait que vous lisez cette article. Durant les différentes taĉhes de rénovation auxquelles j'ai participé, j'ai développé une méthodologie où je déroule dans ma tête tous les scénarios, surtout les plus catastrophiques.
Car il y a un seul scénario où tout se passe bien et un bon millier d'autres où ça déconne, à différents dégrés de criticité.
L'exemple le plus répresentatif, est quand nous avons voulu créé une extension à notre maison, il fallait donc faire de la maçonnerie, ce que je n'avais jamais fait seul. Pour ce genre de travaux, il faut d'abord commencer par la base à savoir, la dalle de béton, et ça ne s'improvise pas.
Après plusieurs phases d'intense réflexion, j'ai réussi à obtenir ma liste de fournitures, et aussi à la conclusion que je n'y arriverais pas seul, et donc que j'aurais besoin de l'aide de mes amis. On retrouve là aussi un pan important de la gestion de projet informatique, la gestion humaine des ressources. 
"Qui va faire quoi, quand et comment."
Ne voulant pas non plus, bloquer mes amis plus d'une journée, je devais donc être sûr de la marche à suivre pour couler la dalle, et donc c'est là où j'ai déroulé le scénario de la journée avec à chaque étape le meme schéma : 
- si ça bloque sur tel truc, qu'est ce que je dois faire si ça arrive
- qu'est ce que je dois faire pour que cela n'arrive pas.  
J'avais donc une liste de solutions alternatives à chaque problème identifié. J'ai même poussé le vice jusqu'à gérer les traces de chats sur la dalle.

ce qui permet dé prévoir les alternatives, les extensions

### Les cérémonies, surtout la célébration

le mieux est l'ennemi du bien