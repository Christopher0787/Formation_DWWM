    <audio> 
---
# **: l'élément audio embarqué**

---
    L'élément HTML <audio> est utilisé afin d'intégrer un contenu sonore dans un document. 
    Il peut contenir une ou plusieurs sources audio représentées avec l'attribut src ou 
    l'élément <source> : le navigateur choisira celle qui convient le mieux. 
    Il peut également être la destination de médias diffusés en continu, en utilisant un MediaStream.
---
## **Exemple interactif**
    HTML Demo: <audio>

## **Exemple interactif en HTML**
    <figure>
        <figcaption>Listen to the T-Rex:</figcaption>
        <audio controls src="/media/cc0-audio/t-rex-roar.mp3"></audio>
        <a href="/media/cc0-audio/t-rex-roar.mp3"> Download audio </a>
    </figure>
---
## **Exemple interactif en CSS**
    figure {
        margin: 0;
    }
---

    L'exemple qui précède illustre le fonctionnement simple d'un élément <audio>, à la façon de ce qui peut être fait pour une image avec l'élément <img> : 
    on inclut un chemin vers la ressource grâce à l'attribut src et on peut ajouter d'autres attributs afin de fournir d'autres informations : 
    lecture automatique, lecture en boucle, utilisation des contrôles par défaut du navigateur, etc.

    Le contenu présent à l'intérieur des balises <audio></audio> est affiché comme contenu alternatif lorsque le navigateur ne prend pas en charge l'élément.
---