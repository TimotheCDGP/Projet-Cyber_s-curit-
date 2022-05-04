Exercice « directory indexing » https://www.root-me.org/fr/Challenges/Web-Serveur/HTTP-Directory-indexing

Dans un premier temps, nous avons comme toujours regardé ce qu’il y avait dans l’onglet « sources » à l’inspection de la page.
Un commentaire dans le index.html a largement suscité notre intérêt. Le commentaire était le suivant :

![image](https://user-images.githubusercontent.com/91453689/166661183-a4838904-6518-4dac-8f22-0985f795c67e.png)

Nous avons immédiatement pensé qu’il fallait rajouter ce bout de code dans notre url.
L’url que nous avions de base (challenge01.root-me.org/web-serveur/ch4/) devenant donc
(http://challenge01.root-me.org/web-serveur/ch4/admin/pass.html).
Malheureusement, il s’est avéré qu’il s’agissait d’un leurre du créateur de l’exercice. La page arborait désormais le message suivant :
![image](https://user-images.githubusercontent.com/91453689/166659096-d41d1e4d-433a-4b6c-85ac-461a8c846abe.png)

Nous avons donc tenté de chercher dans les autres fichiers disponibles, par exemple le fichier css, qui ne contenait malheureusement rien d’intéressant.

Nous avons tenté d’utiliser l’url http://challenge01.root-me.org/web-serveur/ch4/admin/  en enlevant juste « /pass.html » afin de voir le contenu précédant le rickroll.
Nous sommes tombés sur la page suivante

![image](https://user-images.githubusercontent.com/91453689/166659142-16781584-f79e-4d63-81b4-8b0faa2d7b4e.png)

Dans un premier lieu, nous avons cru que ce n’était pas la solution, car l’interface était similaire à celle du site Root Me de base, par conséquent nous pensions être sortis de l’exercice en lui-même. Malgré tout, nous avons tout de même cliqué sur les liens disponibles au cas où ils contiendraient quelque chose (de toute façon nous n’avions pour être honnête aucune autre piste.)

En cliquant sur « parent directory » nous sommes retombés sur notre page initiale, ce qui semblait faire sens puisqu’il s’agissait justement du parent de cette page.
Aussi, nous savions que cliquer sur « pass.html » ne nous apporterait rien, puisqu’il nous redirigerait sur la page troll que nous avions exploré auparavant. 
Par conséquent, nous avons donc cliqué sur le dernier fichier disponible « backup/ » qui contenait un fichier admin.txt, et en l’ouvrant il y avait le flag dedans.  

![image](https://user-images.githubusercontent.com/91453689/166659171-ae5238c8-36ea-4e46-a4e0-6aaf0f54f90e.png)
