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


###  crossorigin

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
---
###  anonymous
        Une requête CORS est envoyée sans informations d'authentification 
        (c'est-à-dire sans cookie, certificat X.509, ou en-tête de requête Authorization).
---
###  use-credentials
        La requête CORS est envoyée avec les informations d'authentification 
        (cookies, certificat X.509 et/ou en-tête Authorization).

        Si le serveur ne permet pas le partage des informations d'authentification 
        avec le site d'origine 
        (avec Access-Control-Allow-Credentials: true comme en-tête de réponse), 
        le navigateur marque l'image comme potentiellement 
        corrompue et restreint l'accès à ses données.
---
## Si la valeur de l'attribut est invalide, les navigateurs considèrent que la valeur anonymous a été utilisée. 
## Voir les attributs de paramétrage du CORS pour plus d'informations.
---
###  decoding
        Fournit au navigateur une indication pour décoder l'image. 
        Les valeurs autorisées sont :
---
###  sync
        L'image est décodée de façon synchrone afin d'être présentée de façon atomique 
        avec le reste du contenu.
---
###  async
        L'image est décodée de façon asynchrone afin de réduire le temps nécessaire à 
        l'affichage du reste du contenu.
---
###  auto
        La valeur par défaut qui indique qu'il n'y a pas de préférence. C'est le navigateur 
        qui décide alors ce qui est le mieux.
---
###  elementtiming
        Indique que l'image doit être observée par l'API PerformanceElementTiming. 
        La valeur fournie devient un identifiant pour l'élément observé. 
        Voir aussi la page de l'atttribut elementtiming.
---
###  fetchpriority
        Fournit une indication de la priorité relative à utiliser pour la récupération 
        de l'image. Les valeurs autorisées sont :
---
###  high
        L'image est récupérée avec une priorité plus élevée que les autres images.
---
###  low
        L'image est récupérée avec une priorité plus faible que les autres images.
---
###  auto
        La valeur par défaut. Il n'y a pas de préférence pour la priorité.
---
### Voir HTMLImageElement.fetchPriority pour plus d'informations.

###  height
        La hauteur intrinsèque de l'image, exprimée en pixels. Cette valeur doit 
        être un nombre entier, sans unité.
---
###  ismap
        Cet attribut booléen indique que l'image fait partie d'une carte côté serveur.
        Dans ce cas, les coordonnées du clic sur l'image sont envoyés au serveur.
---
###  loading
        Indique comment le navigateur devrait charger l'image :

             eager

                : L'image est chargée immédiatement, que l'image soit située dans 
                la zone d'affichage (viewport) visible ou non. Il s'agit de la valeur 
                par défaut.
            lazy

                : Le chargement de l'image est retardé jusqu'à ce que celle-ci soit située 
                à une certaine distance, définie par le navigateur, de la zone d'affichage.

                L'idée est d'éviter de consommer de la bande passante et des ressources réseaux 
                avant d'être relativement certain que l'image est nécessaire. 

                Pour la plupart des cas d'usage, cela permet d'améliorer les performances.

---


###  referrerpolicy
        Une chaîne de caractères qui indique le référent à utiliser lors de la récupération 
        de la ressource :
---
###  no-referrer
        L'en-tête Referer n'est pas envoyé.
---
###  no-referrer-when-downgrade
        L'en-tête Referer ne sera pas envoyé aux origines sans TLS/HTTPS.
---
###  origin:
        Le référent envoyé sera limité à l'origine de la page référente, c'est-à-dire 
        qu'il ne contiendra que le schéma, l'hôte et le port.
---
###  origin-when-cross-origin
        Le référent envoyé aux autres origines sera limité au schéma, à l'hôte et au port. 
        La navigation vers la même origine contiendra le chemin.
---
###  same-origin
        Un référent sera envoyé vers les mêmes origines mais les requêtes vers d'autres 
        origines ne contiendront pas de référent.
---
###  strict-origin
        N'envoie l'origine du document comme référent que lorsque le niveau de sécurité du protocole reste le même (HTTPS→HTTPS) 
        et pas lorsque la destination est moins sécurisée (HTTPS→HTTP).
---
###  strict-origin-when-cross-origin (la valeur par défaut)
        Envoie l'URL complète lors d'une requête vers la même origine, n'envoie que l'origine 
        pour les requêtes vers d'autres origines si le niveau de sécurité du protocole reste 
        le même (HTTPS→HTTPS), n'envoie aucun en-tête correspondant vers une destination moins sécurisée (HTTPS→HTTP).
---
###  unsafe-url
        Le référent inclut l'origine et le chemin (mais pas le fragment, le mot de passe ou 
        le nom d'utilisateur). Cette valeur n'est pas sécurisée, car elle diffuse l'origine 
        et les chemins de ressources protégées par TLS vers des origines non-sécurisées.

###  sizes
        Une ou plusieurs chaînes de caractères séparées par des virgules et qui indiquent 
        un ensemble de tailles de source possible. Chaque taille de source consiste en :

        Une condition de média. Celle-ci doit être absente pour le dernier élément de la liste.

        Une valeur de taille de source.

        La condition de média décrit les propriétés de la zone d'affichage et pas de l'image. Ainsi, (max-height: 500px) 1000px 
        proposera d'utiliser une source de largeur 1000px, 
        si la zone d'affichage n'est pas plus haute que 500px.

        Les valeurs pour les tailles de source indiquent la taille d'affichage souhaitée 
        de l'image. Le navigateur utilise la taille de source courante correspondante pour sélectionner une des sources fournies 
        par l'attribut srcset lorsque les sources y 
        sont décrites avec un descripteur de largeur (w). 
        La taille de source sélectionnée affecte la taille intrinsèque de l'image 
        (c'est-à-dire la taille occupée à l'écran si aucun style CSS n'est appliqué). 
        Si l'attribut srcset est absent ou qu'il ne contient pas de valeur 
        avec un descripteur de largeur, l'attribut sizes aura aucun effet.
---
###  src
        L'URL de l'image. Cet attribut est obligatoire. 
        Pour les navigateurs qui prennent en charge srcset, l'image fourni par src est considérée comme une candidate 
        avec un descripteur de densité de pixel à 1x, sauf si une image avec 
        un tel descripteur est déjà définie dans srcset, ou si srcset contient des descripteurs w.
---
###  srcset
        Une ou plusieurs chaînes de caractères séparées par des virgules, qui indiquent des 
        sources possibles pour l'image que le navigateur pourra utiliser. Chaque chaîne de caractères se compose :

            D'une URL vers l'image

            Éventuellement, d'un espace suivi :

                 D'un descripteur de largeur (un entier positif suivi par w). Le descripteur de largeur est divisé 
                 par la taille de source fournie par l'attribut sizes afin de calculer la densité de pixel effective.

                D'un descripteur de densité de pixel (un nombre décimal positif suivi par x).

        Si aucun descripteur n'est indiqué, la source se voit affecter un descripteur par 
        défaut de 1x.

        Toute combinaison des deux types de descripteur sera invalide. De même, indiquer 
        deux sources avec le même descripteur sera invalide.

        L'agent utilisateur sélectionne une des sources disponibles comme il l'entend. 
        Cette liberté permet de baser le choix sur d'autres facteurs comme les préférences 
        de l'utilisateur ou les conditions réseau. 
        Voir le tutoriel sur les images adaptatives pour un exemple.

###  width
        La largeur intrinsèque de l'image, exprimée en pixels. La valeur doit être un nombre 
        entier sans unité.
---
###  usemap
        L'URL partielle (commençant par #) d'une carte d'image associée à l'élément.

---

## **Attributs dépréciés**

    top

        Équivalent à vertical-align: top ou vertical-align: text-top
---
    middle

        Équivalent à vertical-align: -moz-middle-with-baseline
---
    bottom

        La valeur par défaut, équivalent à vertical-align: unset ou vertical-align: initial
---
    left

        Équivalent à float: left
---
    right

        Équivalent à float: right

---


## **Mettre en forme avec CSS**

    <img> est un élément remplacé. Sa propriété display par défaut vaut inline, 
    mais ses dimensions par défaut sont définies par les valeurs intrinsèques de 
    l'image, à la façon de inline-block. 
    Il est tout à fait possible d'utiliser les propriétés border/border-radius, 
    padding/margin, width, et height sur une image.

    <img> n'a pas de ligne de base, donc lorsque les images sont utilisées dans 
    un contexte de mise en forme en ligne avec vertical-align: baseline, 
    le bas de l'image sera placé sur la ligne de base du texte.

    La propriété object-position peut être utilisée afin de positionner l'image 
    au sein de la boîte fournie par l'élément. La propriété object-fit peut être 
    utilisée pour ajuster le dimensionnement de l'image au sein de la boîte 
    (par exemple pour étirer ou rogner l'image dans la boîte si nécessaire).

    Selon son type, une image peut avoir une largeur et une hauteur intrinsèque. 
    Pour certains types d'image en revanche, de telles dimensions intrinsèques ne 
    sont pas nécessaires. Ainsi, les images vectorielles (en SVG par exemple) n'ont 
    pas de dimensions intrinsèques si leur racine (l'élément <svg>) n'a pas d'attribut 
    width ou height défini.

---


## **Exemples**

## Fournir un texte alternatif

    Dans l'exemple qui suit, l'image est accompagnée d'un texte alternatif qui sert l'accessibilité.

---
    HTML

    <img src="favicon144.png" alt="Logo de MDN" />
---

## Créer un lien avec une image

    Cet exemple intègre l'image précédente et la transforme en lien. Pour cela, 
    l'élément <img> est placé au sein d'un élément <a>. Ici, le texte alternatif 
    devrait décrire la ressource vers laquelle pointe le lien.
---
    HTML

    <a href="https://developer.mozilla.org">
        <img src="favicon144.png" alt="Visiter le site MDN" />
    </a>
---

## Utiliser l'attribut srcset

    Dans cet exemple, on utilise l'attribut srcset avec une référence vers une 
    version du logo en haute résolution. Pour les appareils avec une haute résolution, 
    celle-ci sera chargée à la place à la place de l'image indiquée par src. 
    Pour les agents utilisateurs qui prennent en charge l'attribut srcset, l'image référencée 
    par l'attribut src sera considérée comme une candidate avec le descripteur 1x.
---
    HTML

    <img src="favicon72.png" alt="Logo MDN" srcset="favicon144.png 2x" />
---

## Utiliser les attributs srcset et sizes

    L'attribut src est ignoré par les agents utilisateurs qui le prennent en charge lorsque 
    les descripteurs w sont présents. Lorsque la condition (max-width: 600px) est 
    respectée, l'image large de 200 pixels sera chargée 
    (car c'est celle qui est la plus proche de 200px). 
    Dans les autres cas, c'est l'autre image qui est chargée.
---
    HTML

    <img
        src="clock-demo-200px.png"
        alt="Clock"
        srcset="clock-demo-200px.png 200w, clock-demo-400px.png 400w"
        sizes="(max-width: 600px) 200px, 50vw" />
---

## **Sécurité et vie privée**

    Bien que les éléments <img> puissent être utilisés innocemment, 
    ils peuvent également avoir des effets indésirables en termes de sécurité et de vie privée. 
    Voir cet article quant à l'en-tête Referer pour plus de détails.


---



## **Accessibilité**

## Écrire des descriptions alternatives significatives 

    La valeur d'un attribut alt devrait toujours décrire le contenu de l'image de façon claire
    et concise. 
    Elle ne doit pas décrire la présence de l'image ou le nom du fichier de l'image. 
    Si l'attribut alt est omis volontairement, car l'image n'a pas d'équivalent textuel, utilisez d'autres méthodes afin 
    d'indiquer le message véhiculé par l'image.

---
### Mauvaise pratique
    <img alt="image" src="pingouin.jpg" />
---
### Bonne pratique
    <img alt="Un manchot Rockhopper sur une plage." src="pingouin.jpg" />
---

    Un test important pour l'accessibilité consiste à lire le contenu de l'attribut alt 
    avec le contenu texte précédent afin de voir si cela fournit les mêmes informations que l'image. 
    Ainsi, si l'image était précédée de la phrase « Lors de mon voyage, j'ai vu un animal mignon : ». 
    Dans l'exemple de la mauvaise pratique, cela aurait donné « Lors de mon voyage, 
    j'ai vu un animal mignon : image », ce qui n'a pas de sens. 
    Avec la bonne pratique et cet exemple, on aurait obtenu « Lors de mon voyage, 
    j'ai vu un animal mignon : Un manchot Rockhopper sur une plage. », ce qui est plus parlant.

    Pour les images déclenchant une action, par exemple celles incluses dans 
    un lien <a> ou un bouton <button>, il faut penser à décrire l'action déclenchée dans alt. 
    On peut ainsi écrire alt="page suivante" plutôt que alt="flèche droite". 
    Vous pouvez inclure une description complémentaire dans l'attribut title, 
    qui pourra être lu par les lecteurs d'écrans si l'utilisatrice ou l'utilisateur 
    en fait la demande.

    Lorsque l'attribut alt n'est pas présent sur une image, certains lecteurs d'écran pourront 
    annoncer le nom du fichier de l'image. 
    Cela peut être source de confusion si le nom du fichier n'est pas représentatif du contenu 
    de l'image.


---


## Identifier le contenu SVG comme image

    En raison d'un bug VoiceOver, ce dernier n'annonce pas correctement 
    les images SVG comme étant des images. 
    Il faut inclure role="img" pour les éléments <img> basés sur des fichiers 
    sources SVG afin de s'assurer que les outils d'assistance annoncent le contenu 
    SVG comme une image.


---


## L'attribut title

    L'attribut title n'est pas un remplaçant acceptable pour l'attribut alt. 
    Il vaut également mieux éviter de dupliquer la valeur de l'attribut alt dans 
    un attribut title pour la même image. 
    En effet, un tel doublon entraînera les lecteurs d'écran à annoncer deux fois 
    la description, ce qui pourra être une source de confusion.

    L'attribut title ne devrait pas être utilisé afin de compléter les informations 
    de légende de l'image pour accompagner la description fournie par alt. 
    Si une image a besoin d'une légende, on utilisera les éléments figure et figcaption.

    La valeur de l'attribut title est généralement affichée via une bulle d'information 
    qui apparaît au survol du curseur sur l'image. Bien que cet attribut puisse fournir 
    des informations supplémentaires, on ne doit pas s'attendre à ce que toute personne le voit : 
    par exemple lorsque la navigation est effectuée au clavier ou sur un écran tactile. 
    Si les informations à afficher sont particulièrement importantes ou utiles, on utilisera 
    les méthodes évoquées ci-avant plutôt que title.

---


## **Compatibilité des navigateurs**

| Navigateur          | Compatibilité Ordinateur | Compatibilité Mobile |
|---------------------|--------------------------|----------------------|
| Google Chrome       | ✅ (Très fiable)         | ✅ (Très fiable)     |
| Mozilla Firefox     | ✅ (Très fiable)         | ✅ (Très fiable)     |
| Safari              | ✅ (Très fiable)         | ✅ (Très fiable)     |
| Microsoft Edge      | ✅ (Très fiable)         | ✅ (Très fiable)     |
| Opera               | ✅ (Très fiable)         | ✅ (Très fiable)     |
| Samsung Internet    | N/A                      | ✅ (Très fiable)     |
| Internet Explorer   | ⚠️ (Moins fiable)        | N/A                  |

---