# FABRICH--STD22096--WriteUpChallenges

# Dillinger

## Root-me

Root-Me est un jeu de hacking en ligne qui vous met au défi de tester vos compétences en matière de sécurité informatique de manière légale et éthique. Le jeu propose différents scénarios réalistes où vous devez trouver et exploiter des failles de sécurité.

Vous pouvez choisir parmi diverses catégories de défis, comme la cryptographie, le web, les réseaux, la programmation et les failles de sécurité. En résolvant ces défis, vous apprenez à identifier les vulnérabilités des systèmes informatiques et à les sécuriser.

## Objectif

- Le but de Root-Me est d'aider les joueurs à développer leurs compétences en matière de sécurité informatique de manière légale et éthique.
- En résolvant les défis proposés dans les différentes catégories, les joueurs peuvent acquérir une compréhension approfondie des vulnérabilités des systèmes informatiques et apprendre à les prévenir.

- Le jeu vise à sensibiliser les joueurs aux risques de sécurité et à promouvoir de bonnes pratiques pour assurer la protection des données et des systèmes.


# TUTORIAL
## FTP - Authentification
On ouvre le fichier telecharger la WireShark.
On suit le flux TCP de la priemiere protocole FTP qui s'affiche, et on devrait voir ces lignes ci-dessous
```sh
220-QTCP at fran.csg.stercomm.com.
220 Connection will close if idle more than 5 minutes.
USER cdts3500
331 Enter password.
PASS cdts3500
230 CDTS3500 logged on.
SYST
215  OS/400 is the remote operating system. The TCP/IP version is "V5R2M0".
SITE NAMEFMT
250  Now using naming format "0".
PWD
257 "CDTS3500" is current library.
PASV
227 Entering Passive Mode (10,20,144,151,62,141).
RETR qgpl/apkeyf.apkeyf
150 Retrieving member APKEYF in file APKEYF in library QGPL.
250 File transfer completed successfully.
QUIT
221 QUIT subcommand received.

```
Dans le troisieme ligne, on a le mot de passe de l'user
```sh
USER cdts3500
```

Le mot de passe est donc : ```cdts3500```

## TELNET - authentification
On ouvre le fichier telecharger la WireShark.
On suit le flux TCP de la priemiere protocole FTP qui s'affiche, et on devrait voir ces lignes ci-dessous
```sh
........... ..!.."..'.....#..%..%........... ..!..".."........P. ....".....b........b....	B.
........................"......'.....#..&..&..$..&..&..$.. .....#.....'........... .9600,9600....#.bam.zing.org:0.0....'..DISPLAY.bam.zing.org:0.0......xterm-color.............!.............."............
OpenBSD/i386 (oof) (ttyp1)

login: .."........"ffaakkee
.
Password:user
.
Last login: Thu Dec  2 21:32:59 on ttyp1 from bam.zing.org
Warning: no Kerberos tickets issued.
OpenBSD 2.6-beta (OOF) #4: Tue Oct 12 20:42:32 CDT 1999

Welcome to OpenBSD: The proactively secure Unix-like operating system.

Please use the sendbug(1) utility to report bugs in the system.
Before reporting a bug, please try to reproduce it with the latest
version of the code.  With bug reports, please try to ensure that
enough information to reproduce the problem is enclosed, and if a
known fix for it exists, include that as well.

$ llss
.
$ llss  --aa
.
.         ..        .cshrc    .login    .mailrc   .profile  .rhosts
$ //ssbbiinn//ppiinngg  wwwwww..yyaahhoooo..ccoomm
.
PING www.yahoo.com (204.71.200.74): 56 data bytes
64 bytes from 204.71.200.74: icmp_seq=0 ttl=239 time=73.569 ms
64 bytes from 204.71.200.74: icmp_seq=1 ttl=239 time=71.099 ms
64 bytes from 204.71.200.74: icmp_seq=2 ttl=239 time=68.728 ms
64 bytes from 204.71.200.74: icmp_seq=3 ttl=239 time=73.122 ms
64 bytes from 204.71.200.74: icmp_seq=4 ttl=239 time=71.276 ms
64 bytes from 204.71.200.74: icmp_seq=5 ttl=239 time=75.831 ms
64 bytes from 204.71.200.74: icmp_seq=6 ttl=239 time=70.101 ms
64 bytes from 204.71.200.74: icmp_seq=7 ttl=239 time=74.528 ms
64 bytes from 204.71.200.74: icmp_seq=9 ttl=239 time=74.514 ms
64 bytes from 204.71.200.74: icmp_seq=10 ttl=239 time=75.188 ms
64 bytes from 204.71.200.74: icmp_seq=11 ttl=239 time=72.925 ms
...^C
.--- www.yahoo.com ping statistics ---
13 packets transmitted, 11 packets received, 15% packet loss
round-trip min/avg/max = 68.728/72.807/75.831 ms
$ eexxiitt
.
```
Dans le huitieme ligne, on a le "password":
```sh
Password:user
```
Le mot de passe qu'on doit chercher est alors: ```user```

## ______________________________________________
## ETHERNET - trame

En cliquant sur le button "Demmarer le challenge", il y a une nouvelle onglet qui s'ouvre, et qui contient:

```sh
00 05 73 a0 00 00 e0 69 95 d8 5a 13 86 dd 60 00
00 00 00 9b 06 40 26 07 53 00 00 60 2a bc 00 00
00 00 ba de c0 de 20 01 41 d0 00 02 42 33 00 00
00 00 00 00 00 04 96 74 00 50 bc ea 7d b8 00 c1
d7 03 80 18 00 e1 cf a0 00 00 01 01 08 0a 09 3e
69 b9 17 a1 7e d3 47 45 54 20 2f 20 48 54 54 50
2f 31 2e 31 0d 0a 41 75 74 68 6f 72 69 7a 61 74
69 6f 6e 3a 20 42 61 73 69 63 20 59 32 39 75 5a
6d 6b 36 5a 47 56 75 64 47 6c 68 62 41 3d 3d 0d
0a 55 73 65 72 2d 41 67 65 6e 74 3a 20 49 6e 73
61 6e 65 42 72 6f 77 73 65 72 0d 0a 48 6f 73 74
3a 20 77 77 77 2e 6d 79 69 70 76 36 2e 6f 72 67
0d 0a 41 63 63 65 70 74 3a 20 2a 2f 2a 0d 0a 0d
0a
```
C'est une notation en hexadecimal, et en le decodant on obtient:
```sh
Authorization: Basic Y29uZmk6ZGVudGlhbA==
User-Agent: InsaneBrowser
Host: www.myipv6.org
Accept: */*
```
On s'interesse seulement la premiere ligne.
Apres un reflexion et de recherche profonde sur le cryptographie, on a compris que c'est une notation en base64.
On le decode et on obtient : ```confi:dential```, et c'est belle et bien le mot de passe.

## ______________________________________________

## Authentification twitter
Il n'y a qu'une seule ligne dans ce fichier donc on le analyse le flux TCP, et on a ca:

```sh
GET /statuses/replies.xml HTTP/1.1
User-Agent: CFNetwork/330
Cookie: _twitter_sess=BAh7CDoJdXNlcjA6B2lkIiVmZGQ2ODc5MTMwMWFhOTFiMWExZDViZmQwMGEz%250AOWNkMyIKZmxhc2hJQzonQWN0aW9uQ29udHJvbGxlcjo6Rmxhc2g6OkZsYXNo%250ASGFzaHsABjoKQHVzZWR7AA%253D%253D--ea12e7bc090d05202cd7e3f972c2b4414a97f657
Accept: */*
Accept-Language: en-us
Accept-Encoding: gzip, deflate
Authorization: Basic dXNlcnRlc3Q6cGFzc3dvcmQ=
Connection: keep-alive
Host: twitter.com

```

Sur la ligne Authorization, juste apres le mot "Basic" est une code en base64. On le decode et on a ```usertest:password```.
Le mot de passe est donc ```password```

### ______________________________________________________

### Bluetooth - Fichier inconnu
On ouvre le fichier ISO avec Wireshark.
Puis on clique sur 'wireless', apres sur 'equipement bleutooh'.
Et il y a une tableau qui s'affiche et montre le nom de l'appareil ainsi que l'addresse mac.
On suis juste les conseilles de jeu, on transforme les lettres de l'addresse Mac en majuscule , on fais le concatenation avec le nom de l'appareil.
Et finallement, on encode le tous en sha1, et obtient : ```c1d0349c153ed96fe2fadf44e880aef9e69c122b```
