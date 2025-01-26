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

    L'exemple qui précède illustre le fonctionnement simple d'un élément <audio>, 
    à la façon de ce qui peut être fait pour une image avec 
    l'élément <img> : on inclut un chemin vers la ressource grâce à l'attribut src et on 
    peut ajouter d'autres attributs afin de fournir d'autres informations : lecture automatique, lecture en boucle, 
    utilisation des contrôles par défaut du navigateur, etc.

    Le contenu présent à l'intérieur des balises <audio></audio> est affiché comme 
    contenu alternatif lorsque le navigateur ne prend pas en charge l'élément.
---

## **Attributs**
    Cet élément inclut les attributs universels.
---

    autoplay
        Un attribut booléen : s'il est spécifié, l'audio commencera automatiquement la lecture dès qu'il pourra le faire, 
        sans attendre la fin du téléchargement de l'ensemble du fichier audio.
---

    controls
        Si l'attribut est présent, le navigateur affichera des contrôles pour que l'utilisateur puisse gérer la lecture, 
        le volume, et le déplacement du curseur de lecture.

        Cet attribut à valeur contrainte indique comment le CORS doit être utilisé afin de récupérer la ressource. 
        Les ressources utilisant le CORS peuvent être réutilisées dans un élément <canvas> sans corrompre celui-ci. 
        Les valeurs autorisées pour cet attribut sont :
---

    anonymous
        Une requête multi-origine est envoyée sans information d'authentification. 
        Autrement dit, l'en-tête HTTP Origin est envoyé sans cookie, certificat X.509 ou sans authentification HTTP. 
        Si le serveur ne fournit pas d'information d'authentification au site d'origine 
        (sans indiquer l'en-tête Access-Control-Allow-Origin), 
        la ressource sera corrompue (tainted) et son utilisation sera restreinte.
---
    use-credentials
        Une requête multi-origine est envoyée avec une information d'authentification 
        (c'est-à-dire avec un en-tête HTTP Origin: 
        qui contient un cookie, un certificat ou effectuant une authentification HTTP).

        Lorsque cet attribut n'est pas présent, la ressource est récupérée sans requête 
        CORS et empêche ainsi d'utiliser la ressource dans un <canvas>. 
        Si la valeur fournie est invalide, elle sera considérée comme anonymous. 
        Voir Paramétrage des attributs relatifs au CORS pour plus d'informations.
---
    disableRemotePlayback Expérimental
        Un attribut booléen utilisé pour désactiver la capacité de lecture à distance dans les appareils qui sont connectés 
        à l'aide de câbles (HDMI, DVI, etc.) et sans fil 
        (Miracast, Chromecast, DLNA, AirPlay, etc.). 
        Voir cette proposition de spécification pour plus d'informations.
---
    loop
        Un attribut booléen. S'il est renseigné, la lecture du fichier se fera en boucle.
---
    muted  
        Un attribut booléen, indiquant si le son de l'élément audio est initialement coupé. 
        Sa valeur par défaut est false.
---
    preload
        Cet attribut indique au navigateur ce que l'auteur du code html pense de l'utilisation optimale de cet élément. 
        Il accepte uniquement les valeurs suivantes :

            none : Indique que l'élément audio ne devrait pas être mis en cache

            metadata : Indique que seules les méta-données (comme la durée) sont préchargées

            auto : Indique que tout le fichier peut être téléchargé, même s'il n'est pas certain que l'utilisateur le lira

            "" (chaîne de caractères vide) : Un synonyme de auto

        La valeur par défaut peut varier d'un navigateur à l'autre. 
        Les spécifications recommandent la valeur metadata.
---
    src
        L'URL du fichier audio à intégrer. Cet élément est soumis aux contrôles d'accès HTTP. 
        Cet attribut est facultatif ; vous pouvez utiliser l'élément <source> dans le 
        bloc audio pour spécifier l'audio à intégrer.
---





































































