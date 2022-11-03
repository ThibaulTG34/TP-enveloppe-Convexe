# TP-enveloppe-Convexe
>Le but de ce TP était de calculer des enveloppes convexes à partir d'ensembles de points en implémentant trois algorithmes, demi-plan, Jarvis et Graham.

+ <span style="color: #b20238"> **Exercice 1 :** </span> 
  + <span style="color: #039bde"> Déterminant </span>: Pour la première partie, on devait implémenter la fonction ***déterminant***, qui permettait de calculer le déterminant entre deux vecteurs.

  + <span style="color: #039bde"> Signe du déterminant </span>: Ensuite, on devait faire la fonction ***detSing*** qui retournait le signe du déterminant. 

  + <span style="color: #039bde"> Tour </span>: Et enfin, l'implémentation de la fonction ***tour*** qui retournait *+1* si les trois points sont orientés dans le sens trigo (tour gauche), *-1* si les points sont orientés dans le sens indirect (tour droit) ou *0* si les points sont alignés.

  + <span style="color: #039bde"> résultat de l'exercice 1 </span>:

    <img src="tour_gauche.png" style="zoom:36%" >
    <img src="tour_droit.png" style="zoom:36%">
    <img src="tour_aligne.png" style="zoom:36%">

+ <span style="color: #b20238"> **Algo de Jarvis (Exo 3)** </span> :
    + <span style="color: #039bde"> explication </span>: \
    Cette algorithme retourne un tableau de points qui constitue l'enveloppe convexe. Le principe est de partir du point le plus "bas" et de trouver le point le plus à droite du point courant, c'est pourquoi, pour l'implémenter, il fallait créer deux autres fonctions : ***findNextIdx*** et ***findMinIdy***.

        + <span style="color: #0bde"> findMinIdy </span> : Cette fonction permet de trouver le point le plus en "bas", c'est-à-dire, le point qui a le minimum en y.

        + <span style="color: #0bde"> findNextIdx </span> : 
        Cette fonction trouve le point qui est le plus à droite du point courant. Elle utilise la fonction ***tour***.
    
    + <span style="color: #039bde"> résultat de l'algo </span>:
        
        <img src="jarvis.png" style="zoom:45%"> 
        <img src="jarvis_8points.png" style="zoom:50.3%">
    

+ <span style="color: #b20238"> **Ajout/Suppression d'un point (Exo 7)**</span> :
    + <span style="color: #039bde"> Ajout </span>: \
    Cette fonction permet d'ajouter un point à l'ensemble de départ. Elle retourne le nouvel ensemble contenant les points initiaux et le nouveau point. Sur l'image ci-après, le point ajouté est nommé ***NP***. 
        
        <img src="jarvis_apres_add.png" style="zoom:45%"> 


    + <span style="color: #039bde"> Suppression </span>: \
    Cette fonction permet de supprimer un point de l'ensemble résultant de l'algo de Jarvis. Elle retourne le nouvel ensemble sans le point que l'on a supprimé. Pour l'exemple, j'ai choisi de supprimé le point que j'avais ajouté au-dessus. On s'aperçoit que l'on obtient le même résultat que le résultat par l'algo de Jarvis.

        <img src="jarvis.png" style="zoom:48%"> 
