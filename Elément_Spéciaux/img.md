    <img> 
# **: l'élément d'image embarquée**

---

    L'élément HTML <img> permet d'intégrer une image dans un document.

---



## **Exemple interactif**

    HTML Demo: <img>

## **Exemple interactif en HTML**

    <img
        class="fit-picture"
        src="/media/cc0-images/grapefruit-slice-332-332.jpg"
        alt="Grapefruit slice atop a pile of other slices" />

## **Exemple interactif en CSS**

    .fit-picture {
        width: 250px;
    }

---


    L'exemple qui précède illustre l'utilisation de l'élément <img> :

        L'attribut src est obligatoire, et contient le chemin vers l'image qu'on veut intégrer.

        L'attribut alt est obligatoire et contient une description textuelle de l'image, ce qui est extrêmement utile.

        En effet, les outils de lecture d'écran utilisent cette description pour 
        la lire afin que les personnes sachent ce que l'image représente.

        Ce texte alternatif sera également affiché sur la page si l'image ne peut pas être chargée 
        (par exemple s'il y a des erreurs réseau, du blocage de contenu ou un lien périmé).

---

    Il existe de nombreux autres attributs :

        Le contrôle du référent et de la politique de gestion des ressources d'origines multiples 
        (CORS) avec les attributs crossorigin et referrerpolicy.

        width et height qui permettent de définir la taille intrinsèque de l'image, 
        lui permettant ainsi de prendre l'espace nécessaire avant son chargement 
        (évitant ainsi d'avoir des décalages indésirables lors du chargement de la page).

        Des indications responsives avec sizes et srcset (voir également l'élément <picture> 
        et le tutoriel sur les images adaptatives).

---