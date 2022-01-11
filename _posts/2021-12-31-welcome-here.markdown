---
layout: post
title:  "Welcome to my blog!"
date:   2022-01-01 13:43:24 +0100
categories: welcome
abstract: Une courte présentation, et un petit tips pour l'installation de <i>Jekyll<i> 
---
### Intro

Hello, je me lance enfin dans l'écriture d'un blog.
J'imagine que dans ce genre d'exercice, l'une des difficultés c'est de rester focus sur une thématique,
well...et bien je dirais simplement que je vais essayer d'écrire à mesure que cela me passe par la tête.
Concernant les sujets, je vais essayer d'aborder les quelques travaux que j'ai déjà réalisés, et partager d'autres choses notamment sur la tech, et des sujets plus vastes comme le heavy metal, voire du bricolage, voire les 3 à la fois.

### Premier problème

Pour entrer dans le détail, j'ai donc utilisé [GitHub Pages](https://docs.github.com/en/pages), et [Jekyll](https://jekyllrb.com/) (générateur de page statique).
Etant un peu boulet, et beaucoup un aimant à "ennuis", j'ai été confronté à une erreur :  

```batch
undefined method `delegate_method_as' for Jekyll::Drops::CollectionDrop:Class (NoMethodError) Did you mean? DelegateClass
```

Merci à [StackoverFlow](https://stackoverflow.com/questions/68220028/undefined-method-delegate-method-as-for-jekylldropscollectiondropclass-n), après une désinstallation, et réinstallation via `gem`, tout fonctionne bien. La commande décrite par le site officiel de `Jekyll` n'est donc pas conseillée (...) : 

```batch
#uninstall : 
PACKAGES="$(dpkg -l |grep jekyll|cut -d" " -f3|xargs )"
sudo apt remove --purge $PACKAGES 
sudo apt autoremove
#install : 
sudo gem install jekyll jekyll-feed jekyll-gist jekyll-paginate jekyll-sass-converter jekyll-coffeescript
#finalize
bundle update
```

N'étant pas un grand expert UI, j'ai pris le premier style qui me plaisait, après 1 jour de bidouille, ça a l'air de ressembler 
à quelque chose. Je vous vois déjà venir, oui je n'ai pas une grande fibre graphique, je suis un dev back, ne l'oubliez pas!

### Remerciements

Merci à [Shangzhi Huang](https://ngzhio.github.io), je lui ai piqué plusieurs choses pour appliquer le thème que je voulais.

Merci aussi à la team des twittos : 
[idriss_neumann](https://twitter.com/idriss_neumann), 
[k33g_org](k33g_org), 
[BillyTheTroll](https://twitter.com/BillyTheTroll),
[titimoby](https://twitter.com/titimoby), 
[zigazou](https://twitter.com/zigazou),
[allema_s](https://twitter.com/allema_s),
[KajanSiva](https://twitter.com/KajanSiva),
[ponceto91](https://twitter.com/ponceto91),
[_Akanoa_](https://twitter.com/_Akanoa_),
[dadideo](https://twitter.com/dadideo),
[manekinekko](https://twitter.com/manekinekko),
[teamdevops](https://twitter.com/teamdevops)


Bonne lecture.
