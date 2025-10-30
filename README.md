# Secret SHenanigans

Un malfrat, versé dans la technique, se méfie des protocoles de canaux sécurisés éprouvés comme SSH ou TLS : “ils sont tous certainement backdoorés” pense t’il. Comme il doit régulièrement recevoir des informations confidentielles de collègues à lui, il a développé son propre protocole d’établissement de canal sécurisé permettant à des clients anonymes d’envoyer à son serveur ces informations confidentielles.

Vous avez accès à un TAP réseau vous positionnant en Man-in-the-Middle entre un client et le serveur, et vous avez par ailleurs réussi à dérober le code source de l’application (sans la clé privée du serveur malheureusement …). Saurez-vous récupérer le secret que le client envoie au serveur ?

![secret_shenanigans.png](secret_shenanigans.png)

Fichiers :
- [README_FCSC.md](README_FCSC.md)
- [secret-shenanigans.tar.xz](secret-shenanigans.tar.xz)



Auteur : rbe

Origine : [SHenanigans](https://hackropole.fr/fr/challenges/crypto/fcsc2024-crypto-secret-shenanigans/)



-----------

## Installation manuel
Vous n'utilisez pas l'application **les CTFs de Cyrhades** ? C'est dommage !
Mais voici comment installer ce CTF manuellement :

> git clone https://github.com/Hack-Oeil/fcsc2024-crypto-secret-shenanigans.git

> cd fcsc2024-crypto-secret-shenanigans


-----------

## Sur le site officiel hackropole.fr
> https://hackropole.fr/fr/challenges/crypto/fcsc2024-crypto-secret-shenanigans/