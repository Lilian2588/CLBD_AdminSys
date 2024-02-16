#TP1

##Exercice 1 

Pour répartir efficacement les machines en utilisant du VLSM (Variable Length Subnet Mask), nous devons d'abord déterminer le nombre de bits de masque de sous-réseau nécessaires pour chaque sous-réseau en fonction du nombre de machines.

    Calcul du nombre de bits de masque de sous-réseau nécessaires :
        Sous-réseau 1 : 38 machines → 2^6 = 64 (6 bits)
        Sous-réseau 2 : 33 machines → 2^6 = 64 (6 bits)
        Sous-réseau 3 : 52 machines → 2^6 = 64 (6 bits)
        Sous-réseau 4 : 35 machines → 2^6 = 64 (6 bits)
        Sous-réseau 5 : 34 machines → 2^6 = 64 (6 bits)
        Sous-réseau 6 : 37 machines → 2^6 = 64 (6 bits)
        Sous-réseau 7 : 25 machines → 2^5 = 32 (5 bits)

    Répartition des sous-réseaux :

    Sous-réseau 1 :
        Adresse de sous-réseau : 172.16.0.0
        Masque de sous-réseau : /26 (255.255.255.192)
        Adresse de broadcast : 172.16.0.63
        Première adresse IP utilisable : 172.16.0.1
        Dernière adresse IP utilisable : 172.16.0.62

    Sous-réseau 2 :
        Adresse de sous-réseau : 172.16.0.64
        Masque de sous-réseau : /26 (255.255.255.192)
        Adresse de broadcast : 172.16.0.127
        Première adresse IP utilisable : 172.16.0.65
        Dernière adresse IP utilisable : 172.16.0.126

    Sous-réseau 3 :
        Adresse de sous-réseau : 172.16.0.128
        Masque de sous-réseau : /26 (255.255.255.192)
        Adresse de broadcast : 172.16.0.191
        Première adresse IP utilisable : 172.16.0.129
        Dernière adresse IP utilisable : 172.16.0.190

    Sous-réseau 4 :
        Adresse de sous-réseau : 172.16.0.192
        Masque de sous-réseau : /26 (255.255.255.192)
        Adresse de broadcast : 172.16.0.255
        Première adresse IP utilisable : 172.16.0.193
        Dernière adresse IP utilisable : 172.16.0.254

    Sous-réseau 5 :
        Adresse de sous-réseau : 172.16.1.0
        Masque de sous-réseau : /26 (255.255.255.192)
        Adresse de broadcast : 172.16.1.63
        Première adresse IP utilisable : 172.16.1.1
        Dernière adresse IP utilisable : 172.16.1.62

    Sous-réseau 6 :
        Adresse de sous-réseau : 172.16.1.64
        Masque de sous-réseau : /26 (255.255.255.192)
        Adresse de broadcast : 172.16.1.127
        Première adresse IP utilisable : 172.16.1.65
        Dernière adresse IP utilisable : 172.16.1.126

    Sous-réseau 7 :
        Adresse de sous-réseau : 172.16.1.128
        Masque de sous-réseau : /27 (255.255.255.224)
        Adresse de broadcast : 172.16.1.159
        Première adresse IP utilisable : 172.16.1.129
        Dernière adresse IP utilisable : 172.16.1.158

Cela permet de gérer efficacement les 254 machines réparties en 7 sous-réseaux avec le minimum de gaspillage d'adresses IP.

##Exerice 2
