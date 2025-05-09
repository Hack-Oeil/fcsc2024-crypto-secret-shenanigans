
# FCSC 2024 Secret SHenanigans

Un malfrat, versé dans la technique, se méfie des protocoles de canaux sécurisés éprouvés comme SSH ou TLS : “ils sont tous certainement backdoorés” pense t’il. Comme il doit régulièrement recevoir des informations confidentielles de collègues à lui, il a développé son propre protocole d’établissement de canal sécurisé permettant à des clients anonymes d’envoyer à son serveur ces informations confidentielles.

Vous avez accès à un TAP réseau vous positionnant en Man-in-the-Middle entre un client et le serveur, et vous avez par ailleurs réussi à dérober le code source de l’application (sans la clé privée du serveur malheureusement …). Saurez-vous récupérer le secret que le client envoie au serveur ?


![secret_shenanigans.png](secret_shenanigans.png)


### Présentation générale du TAP

Le TAP est placé entre un client et un serveur et bloque les deux canaux de connexion (serveur vers client et client vers serveur) dès que l'un des deux envoie un paquet.
En mode TAP, l'attaquant peut :

- Lire les deux tampons de communication avec « R0 » (serveur vers client) ou « R1 » (client vers serveur).
La ​​sortie est la valeur hexadécimale du tampon.
- Modifier ces deux tampons de communication avec « E0 » et « E1 » avec une valeur hexadécimale.
- Activer le « mode toujours transparent à partir de maintenant » pour éviter toute invocation ultérieure du TAP avec « T ».
- Quitter ce hook TAP avec « Q » ; le hook TAP sera réactivé lors du prochain envoi de paquet serveur ou client (sauf si le « mode toujours transparent » a été configuré précédemment).

Attention : toute altération des canaux de communication peut bloquer le client et le serveur, voire les faire paniquer. À utiliser avec précaution :-)




Fichiers :
- [secret-shenanigans.tar.xz](secret-shenanigans.tar.xz)



Auteur : rbe

Origine : [Secret SHenanigans](https://hackropole.fr/fr/challenges/crypto/fcsc2024-crypto-secret-shenanigans/)



-----------

## Connectez vous en WEBSSH
> http://localhost

#### tentez 
> nc secret-shenanigans.cyrhades.fr 4000

-----------

## Ou directement avec netcat
> nc localhost 4000

-----------


## Installation manuel
Vous n'utilisez pas l'application **les CTFs de Cyrhades** ? C'est dommage !
Mais voici comment installer ce CTF manuellement :

> git clone https://github.com/Hack-Oeil/fcsc2024-crypto-secret-shenanigans.git

> cd fcsc2024-crypto-secret-shenanigans


-----------

## Sur le site officiel hackropole.fr
> https://hackropole.fr/fr/challenges/crypto/fcsc2024-crypto-secret-shenanigans/

