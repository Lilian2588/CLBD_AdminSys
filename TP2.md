# TP4

## Exercice 1. Commandes de bases

2) 
Lorsque vous définissez un alias dans un fichier de configuration de shell tel que ~/.bashrc, le shell interprète ces alias directement sans nécessiter qu'ils soient situés dans un répertoire inclus dans votre variable PATH. Le shell effectue une recherche interne pour trouver des alias correspondant aux commandes entrées.

Ainsi, lorsque vous entrez la commande maj, le shell recherche dans sa liste d'alias et trouve celui que vous avez défini dans ~/.bashrc. Il exécute ensuite la commande associée à cet alias.

3) `apt-cache stats | grep "Total package names"`permet d'afficher tous les paquets dispo sur ubuntu

4) `dpkg -l | wc -l` renvoie 640 
   `apt list --installed | wc -l` renvoie 636
   
5) `grep "install" /var/log/dpkg.log | tail -n 5`

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

