# Bluetooth - Fichier inconnu
https://www.root-me.org/fr/Challenges/Reseau/Bluetooth-Fichier-inconnu

*On nous demande le "hash SHA1 de la concaténation de l’adresse MAC (en majuscules) et du nom du téléphone".*

J'ouvre donc le fichier avec WireShark pour analyser en détail son contenu, et je cherche un nom de téléphone.
Ici il n'y a pas beaucoup de requêtes, donc on peut se permettre de chercher un par un à la main.

Les requêtes qui vont attirer notre attention sont les deux plus "gros" et qui sont nommés **"Remote Name Request Complete"**.

![1](https://user-images.githubusercontent.com/91454016/167723432-df259f7f-3716-403b-bc43-de2a266520f7.png)
*On retrouve l'adresse mac et le nom du téléphone au même endroit*

L'adresse Mac est donc : **0c:b3:19:b9:4f:c6** => **0C:B3:19:B9:4F:C6**
Le nom du téléphone est donc : **GT-S7390G**

Pour répondre à la question il faut donc faire une conversion hash SHA1 de la concaténation de ces deux éléments : **"0C:B3:19:B9:4F:C6GT-S7390G"**

![1](https://user-images.githubusercontent.com/91454016/167724253-40a87e08-00fe-437e-9583-c5ef5782e7b0.png)
*Je me rends donc sur un site internet pour faire la conversion*

Ce qui nous donne : **c1d0349c153ed96fe2fadf44e880aef9e69c122b**

# Challenge terminé !

![1](https://user-images.githubusercontent.com/91454016/167724533-d7e2be9f-b470-485a-a371-9e45da35f19c.png)
