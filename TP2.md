# TP4
début du script : `#!/bin:bash`

## Exercice 1. Commandes de bases

2) 
Lorsque vous définissez un alias dans un fichier de configuration de shell tel que ~/.bashrc, le shell interprète ces alias directement sans nécessiter qu'ils soient situés dans un répertoire inclus dans votre variable PATH. Le shell effectue une recherche interne pour trouver des alias correspondant aux commandes entrées.

Ainsi, lorsque vous entrez la commande maj, le shell recherche dans sa liste d'alias et trouve celui que vous avez défini dans ~/.bashrc. Il exécute ensuite la commande associée à cet alias.

3) `apt-cache stats | grep "Total package names"`permet d'afficher tous les paquets dispo sur ubuntu

4) `dpkg -l | wc -l` renvoie 640 ou plutôt `dpkg -l | grep "^ii" | wc -l`
   `apt list --installed | wc -l` renvoie 636
La différence s'explique seulement par les quelques lignes de texte informatif affichées par dpkg -l 

5) `grep "install" /var/log/dpkg.log | tail -n 5 | cut /var/log/dpkg.log -f4-5 -d" " | cut -f2 -d" "`

Voici les 5 derniers paquets installés basés sur les entrées fournies :

    ufw:all 0.36.2
    man-db:amd64 2.11.2
    plymouth-theme-ubuntu-text:amd64 22.02.122
    dbus:amd64 1.14.10
    linux-image-6.5.0


6) `grep "apt" /var/log/dpkf.log`
```bash
2023-10-11 00:41:08 status unpacked apt-utils:amd64 2.7.3
2023-10-11 00:41:11 configure apt-utils:amd64 2.7.3 <none>
2023-10-11 00:41:11 status unpacked apt-utils:amd64 2.7.3
2023-10-11 00:41:11 status half-configured apt-utils:amd64 2.7.3
2023-10-11 00:41:11 status installed apt-utils:amd64 2.7.3
```

7)  
**Glances** : Glances est un moniteur système en temps réel qui permet de surveiller diverses ressources système telles que l'utilisation du processeur, la mémoire, le réseau, etc. Il fournit une vue d'ensemble facile à lire de la santé de votre système.

**tldr** : tldr (abrégé de "too long; didn't read") est une interface en ligne de commande qui fournit des pages de manuel simplifiées pour diverses commandes Unix. Il fournit des exemples succincts et faciles à comprendre sur la façon d'utiliser une commande donnée, ce qui est particulièrement utile pour les débutants ou pour se rappeler rapidement la syntaxe d'une commande.

**Hollywood** : Hollywood est un script qui transforme votre terminal en un spectacle cinématographique simulé. Il affiche une série de fenêtres de terminal qui défilent avec des animations et des effets sonores pour donner l'apparence d'une scène de piratage informatique ou d'un centre de commandement informatique sophistiqué, similaire à ce que l'on voit dans les films d'action ou de science-fiction

8) `apt search sudoku`

## Exercice 2
`which ls` donne le chemin de la commande ls


```bash
which -a ls | xargs dpkg -S 2> /dev/null | cut -f1 -d
```



