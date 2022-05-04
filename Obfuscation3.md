
obfuscation 3 -  https://www.root-me.org/fr/Challenges/Web-Client/Javascript-Obfuscation-3?lang=fr 

Dans un premier temps, nous avons pensé que la variable pass contenait le mot de passe. On a jugé bon de transformer la suite de nombres qu’elle contenait en caractères grâce à la table ASCII, comme on l’avait fait précédemment dans l’exercice obfuscation 2. Nous avons donc réalisé la commande suivante dans la console :

String.fromCharCode(70,65,85,88,32,80,65,83,83,87,79,82,68,32,72,65,72,65)

String.fromCharCode() permettant de transformer rapidement en caractères ces nombres, cette fonction se basant donc sur la table ascii. 
Malheureusement, cela nous a renvoyé "FAUX PASSWORD AHAH!" qui est le message renvoyé lorsque l'on se trompe dans la saisie du mot de passe. On en a déduit qu'il ne s'agissait pas du mot de passe et qu'il fallait se pencher sur d'autres possibilités.

![image](https://user-images.githubusercontent.com/91453689/166659897-973b175b-6b82-4fd5-9781-795b8aa31be3.png)

La chaine de caractère suivante n’a pas tardé à éveiller notre curiosité: "\x35\x35\x2c\x35\x36\x2c\x35\x34\x2c\x37\x39\x2c\x31\x31\x35\x2c\x36\x39\x2c\x31\x31\x34\x2c\x31\x31\x36\x2c\x31\x30\x37\x2c\x34\x39\x2c\x35\x30"

Tout d’abord nous avons réessayé la commande précédente, avec cette chaine de caractère en paramètres :

String.fromCharCode(\x35\x35\x2c\x35\x36\x2c\x35\x34\x2c\x37\x39\x2c\x31\x31\x35\x2c\x36\x39\x2c\x31\x31\x34\x2c\x31\x31\x36\x2c\x31\x30\x37\x2c\x34\x39\x2c\x35\x30)

Cela ne nous a renvoyé l’erreur « Uncaught SyntaxError: Invalid or unexpected token »

![image](https://user-images.githubusercontent.com/91453689/166660002-f58fa131-55fe-4da0-8b3b-add82c76bdda.png)

Il était évident qu'il ne s'agissait là pas de caractères ascii donc cela ne pouvait fonctionner. On s'est renseigné notamment en utilisant des tags de recherche assez abstraits en raison de notre manque d'informations (par exemple le tag de recherche "\x34\ to ascii" qui s’est révélé bien plus utile que ce qu’on pouvait l’imaginer) ce qui nous a permis de comprendre qu'il s'agissait en réalité de caractères hexadécimaux. Nous avons donc trouvé assez rapidement un convertisseur en ligne de chaines de caractères hexadécimaux en chaine de caractères ascii qui nous a permis de convertir notre chaine de caractères hexadécimaux. (nous avons donc utilisé le site https://www.rapidtables.com/convert/number/hex-to-ascii.html) 

En entrant \x35\x35\x2c\x35\x36\x2c\x35\x34\x2c\x37\x39\x2c\x31\x31\x35\x2c\x36\x39\x2c\x31\x31\x34\x2c\x31\x31\x36\x2c\x31\x30\x37\x2c\x34\x39\x2c\x35\x30 le site nous a renvoyé 55,56,54,79,115,69,114,116,107,49,50

![image](https://user-images.githubusercontent.com/91453689/166660099-215b80bb-97b7-4e89-a71d-2e601ffe2c59.png)

Nous avons réutilisé cette suite de caractères ASCII avec notre commande String.fromCharCode() :

String.fromCharCode(55,56,54,79,115,69,114,116,107,49,50) 

Ce qui nous a renvoyé le flag '786OsErtk12'.

![image](https://user-images.githubusercontent.com/91453689/166660180-877334bc-3862-464f-a710-da92228ab071.png)

