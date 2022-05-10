# Ethernet - Trame
https://www.root-me.org/fr/Challenges/Reseau/ETHERNET-trame

On nous demande de retrouver les données confidentielles contenues dans la trame :
![3](https://user-images.githubusercontent.com/91454016/167725760-cde56f76-8cbe-49a6-9cb7-41fc41429314.png)

Je sais que ce sont des caractères écrits en hexadécimal, donc je le convertis en texte avec un convertisseur quelqconque sur internet :

![1](https://user-images.githubusercontent.com/91454016/167726030-d29e7bbe-e824-4611-89c8-153578fc4803.png)
*Ici, une ligne nous interpèle : **"Authorization: Basic Y29uZmk6ZGVudGlhbA=="***

J'en déduis que ce que je cherche doit avec un lien avec ce "Y29uZmk6ZGVudGlhbA==" (qui ressemble à du base64) et le basic juste avant :
on repasse ce texte dans un convertisseur cette fois de base64 à texte et on obtient un mot : "confidential" !

![2](https://user-images.githubusercontent.com/91454016/167726692-d6cbdea5-0876-4197-92c0-54a6480d275a.png)

![image](https://user-images.githubusercontent.com/91454016/167726944-c14e7e16-6066-463b-8224-8d04c8ae9c47.png)

## Challenge terminé !
