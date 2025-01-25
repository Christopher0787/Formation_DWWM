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

---

        Utiliser la chaîne de caractères vide comme valeur pour cet attribut (alt="") 
        indique que cette image n'est pas importante pour le contenu 
        (par exemple une décoration ou un pixel de pistage), dans ce cas, les navigateurs 
        non-visuels peuvent ne pas la traiter pour le rendu. 
        Les navigateurs visuels masqueront l'icône de l'image cassée si alt est vide et 
        que le chargement de l'image a échoué.

        Cet attribut est également utilisé pour copier/coller l'image vers du texte ou 
        pour enregistrer un marque-page avec l'image associée.

---

    attributionsrc :Expérimental

        Indique au navigateur d'envoyer un en-tête Attribution-Reporting-Eligible avec 
        la requête pour l'image.

        Côté serveur, cela sert à déclencher l'envoi d'un en-tête 
        Attribution-Reporting-Register-Source ou Attribution-Reporting-Register-Trigger 
        dans la réponse afin d'enregistrer une source d'attribution ou un déclencheur d'attribution.

        L'en-tête de réponse renvoyé dépend de la valeur de l'en-tête Attribution-Reporting-Eligible 
        ayant déclenché l'enregistrement.

        La source ou le déclencheur correspondant est éteint lorsque le navigateur reçoit la réponse contenant le fichier image.

---


    Il existe deux versions de cet attribut :

        Une forme booléenne (c'est-à-dire l'utilisation du nom attributionsrc seul) 
        qui indique qu'on souhaite envoyer l'en-tête Attribution-Reporting-Eligible 
        au même serveur que celui vers lequel pointe l'attribut src. 
        Cela fonctionne quand la source d'attribution ou le déclencheur d'enregistrement 
        sont gérés sur le même serveur. Lors de l'enregistrement d'un déclencheur d'attribution, 
        cette propriété est optionnelle et une valeur booléenne sera utilisée si elle est absente.

        Une valeur contenant une ou plusieurs URL, comme :

---

## HTML

    <img
        src="image-file.png"
        alt="Ma description d'image"
        attributionsrc="https://a.example/register-source
                            https://b.example/register-source" />

---

        Cette forme s'avère utile lorsque la ressource demandée n'est pas située sur un serveur 
        que vous contrôler, ou si vous souhaitez gérer l'enregistrement de la source d'attribution 
        sur un serveur différent. 

        Dans ce cas, on indique une ou plusieurs URL pour la valeur de attributionsrc. 

        Lorsque la requête pour la ressource est émise, l'en-tête Attribution-Reporting-Eligible 
        sera envoyé aux URL indiquées dans attributionSrc, ainsi qu'à l'origine de la ressource. 

        Ces URL pourront ensuite répondre avec un en-tête Attribution-Reporting-Register-Source 
        ou Attribution-Reporting-Register-Trigger afin de finaliser l'enregistrement.


    crossorigin

        Indique que la récupération de l'image doit être effectuée avec une requête CORS. 
        Les données provenant d'une image chargée via une requête CORS peuvent être réutilisées 
        dans un élément <canvas> sans que celui-ci soit considéré comme corrompu (tainted).

        Si l'attribut crossorigin n'est pas indiqué, une requête sans CORS sera effectuée 
        (c'est-à-dire sans l'en-tête de requête Origin) et le navigateur marquera la page 
        comme potentiellement corrompue, empêchant d'accéder aux données de l'image et empêchant
        son utilisation dans les éléments <canvas>.

        Si l'attribut crossorigin est présent, une requête CORS est envoyée 
        (avec l'en-tête de requête Origin) ; si le serveur ne gère pas l'accès depuis les origines 
        tierces (c'est-à-dire qu'il n'envoie aucun en-tête de réponse Access-Control-Allow-Origin 
        ou qu'il n'inclut pas l'origine du site dans l'en-tête Access-Control-Allow-Origin), 
        le navigateur bloquera le chargement de l'image et affichera une erreur CORS dans la console de développement.

        Les valeurs autorisées pour cet attribut sont :

    anonymous
        Une requête CORS est envoyée sans informations d'authentification 
        (c'est-à-dire sans cookie, certificat X.509, ou en-tête de requête Authorization).

    use-credentials
        La requête CORS est envoyée avec les informations d'authentification 
        (cookies, certificat X.509 et/ou en-tête Authorization).

        Si le serveur ne permet pas le partage des informations d'authentification 
        avec le site d'origine 
        (avec Access-Control-Allow-Credentials: true comme en-tête de réponse), 
        le navigateur marque l'image comme potentiellement 
        corrompue et restreint l'accès à ses données.

### Si la valeur de l'attribut est invalide, les navigateurs considèrent que la valeur anonymous a été utilisée. Voir les attributs de paramétrage du CORS pour plus d'informations.

    decoding
        Fournit au navigateur une indication pour décoder l'image. 
        Les valeurs autorisées sont :

    sync
        L'image est décodée de façon synchrone afin d'être présentée de façon atomique 
        avec le reste du contenu.

    async
        L'image est décodée de façon asynchrone afin de réduire le temps nécessaire à 
        l'affichage du reste du contenu.

    auto
        La valeur par défaut qui indique qu'il n'y a pas de préférence. C'est le navigateur 
        qui décide alors ce qui est le mieux.

    elementtiming
        Indique que l'image doit être observée par l'API PerformanceElementTiming. 
        La valeur fournie devient un identifiant pour l'élément observé. 
        Voir aussi la page de l'atttribut elementtiming.

    fetchpriority
        Fournit une indication de la priorité relative à utiliser pour la récupération 
        de l'image. Les valeurs autorisées sont :

    high
        L'image est récupérée avec une priorité plus élevée que les autres images.

    low
        L'image est récupérée avec une priorité plus faible que les autres images.

    auto
        La valeur par défaut. Il n'y a pas de préférence pour la priorité.

### Voir HTMLImageElement.fetchPriority pour plus d'informations.

    height
        La hauteur intrinsèque de l'image, exprimée en pixels. Cette valeur doit 
        être un nombre entier, sans unité.

    ismap
        Cet attribut booléen indique que l'image fait partie d'une carte côté serveur.
        Dans ce cas, les coordonnées du clic sur l'image sont envoyés au serveur.

    loading
        Indique comment le navigateur devrait charger l'image :

    eager

        : L'image est chargée immédiatement, que l'image soit située dans la zone 
        d'affichage (viewport) visible ou non. Il s'agit de la valeur par défaut.
    lazy

        : Le chargement de l'image est retardé jusqu'à ce que celle-ci soit située 
        à une certaine distance, définie par le navigateur, de la zone d'affichage. 
        L'idée est d'éviter de consommer de la bande passante et des ressources réseaux 
        avant d'être relativement certain que l'image est nécessaire. 
        Pour la plupart des cas d'usage, cela permet d'améliorer les performances.

---