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


## **Formats d'image pris en charge**

    Le standard HTML n'indique pas les formats d'image qui doivent être pris en charge, 
    les agents utilisateurs peuvent prendre en charge différents formats.


    Les formats d'image qu'on rencontre le plus fréquemment sur le Web sont :

        APNG 
        (Animated Portable Network Graphics) pour les séquences animées avec 
        une compression sans perte (le format GIF est moins performant)

        AVIF 
        (AV1 Image File Format) pour les images et les images animées avec de hautes performances

        GIF 
        (Graphics Interchange Format) pour les images et animations simples

        JPEG 
        (Joint Photographic Expert Group image) pour une compression avec pertes 
        d'images statiques, il s'agit du format le plus utilisé

        PNG 
        (Portable Network Graphics) pour une compression sans perte d'images statiques, 
        de meilleure qualité que le JPEG

        SVG 
        (Scalable Vector Graphics) pour un format d'image vectorielle 
        (qui permet de dessiner une image précisément à différentes échelles)

        WebP 
        (Web Picture format) pour les images statiques et animées


    Les formats comme WebP et AVIF sont recommandés, car avec de meilleures performances 
    que PNG, JPEG, GIF tant pour les images animées que statiques. 
    WebP dispose d'une large prise en charge tandis qu'AVIF n'est pas pris en charge par Safari.

    SVG reste le format recommandé pour les images qui doivent être dessinées avec précision quelle que soit la taille.

---

## **Erreur de chargement d'une image**

    Si une erreur se produit lors du chargement ou du rendu de l'image 
    et qu'un gestionnaire d'évènement onerror a été défini pour intercepter 
    l'évènement error, le gestionnaire sera appelé. 
    Cela peut arriver pour plusieurs raisons :


        L'attribut src est vide ("") ou absent (null pour le DOM).

        L'URL utilisée pour l'attribut src est la même que celle de la page courante.

        L'image est corrompue et ne peut être chargée ainsi.

        Les métadonnées associées à l'image sont corrompues de telle façon qu'il est impossible 
        de connaître ses dimensions et qu'aucune dimension n'a été fournie pour les attributs 
        de l'élément <img>.

        Le format de l'image n'est pas pris en charge par l'agent utilisateur (généralement le navigateur).


---


## **Attributs**

    On peut utiliser les attributs universels sur cet élément.

        alt

    Définit une description textuelle alternative pour l'image.

    Utiliser la chaîne de caractères vide comme valeur pour cet attribut (alt="") 
    indique que cette image n'est pas importante pour le contenu 
    (par exemple une décoration ou un pixel de pistage), dans ce cas, les navigateurs 
    non-visuels peuvent ne pas la traiter pour le rendu. 
    Les navigateurs visuels masqueront l'icône de l'image cassée si alt est vide et 
    que le chargement de l'image a échoué.

    Cet attribut est également utilisé pour copier/coller l'image vers du texte ou 
    pour enregistrer un marque-page avec l'image associée.

        attributionsrc :Expérimental

    Indique au navigateur d'envoyer un en-tête Attribution-Reporting-Eligible avec 
    la requête pour l'image.

    Côté serveur, cela sert à déclencher l'envoi d'un en-tête 
    Attribution-Reporting-Register-Source ou Attribution-Reporting-Register-Trigger 
    dans la réponse afin d'enregistrer une source d'attribution ou un déclencheur d'attribution.

    L'en-tête de réponse renvoyé dépend de la valeur de l'en-tête Attribution-Reporting-Eligible ayant déclenché l'enregistrement.

    La source ou le déclencheur correspondant est éteint lorsque le navigateur reçoit la réponse contenant le fichier image.
