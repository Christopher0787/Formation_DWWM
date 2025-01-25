    <article> 
# **: l'élément de contenu d'un article**

---



    L'élément <article> représente une composition autonome dans un document, une page, une application ou un site, 
    destinée à être distribuée ou réutilisée de manière indépendante (par exemple, dans le cadre d'une syndication). 
    Exemples : un message de forum, un article de magazine ou de journal, ou un article de blog, une fiche produit, 
    un commentaire soumis par un utilisateur, un widget ou gadget interactif, 
    ou tout autre élément de contenu indépendant.

---



## **Exemple interactif**

### **Exemple interactif en HTML**

    HTML Demo: <article>

    <article class="forecast">
        <h1>Weather forecast for Seattle</h1>
    <   article class="day-forecast">
            <h2>03 March 2018</h2>
            <p>Rain.</p>
        </article>
        <article class="day-forecast">
            <h2>04 March 2018</h2>
            <p>Periods of rain.</p>
        </article>
        <article class="day-forecast">
            <h2>05 March 2018</h2>
            <p>Heavy rain.</p>
        </article>
    </article>



### **Exemple interactif en CSS**

    .forecast {
        margin: 0;
        padding: 0.3rem;
        background-color: #eee;
    }

    .forecast > h1,
    .day-forecast {
        margin: 0.5rem;
        padding: 0.3rem;
        font-size: 1.2rem;
    }

    .day-forecast {
        background: right/contain content-box border-box no-repeat
            url('/media/examples/rain.svg') white;
    }

    .day-forecast > h2,
    .day-forecast > p {
        margin: 0.2rem;
        font-size: 1rem;
    }

---



    Un document donné peut contenir plusieurs articles ; par exemple, 
    sur un blog qui affiche le texte de chaque article l'un après l'autre au fur et à mesure 
    que le lecteur fait défiler, chaque message sera contenu dans un élément <article>,
    avec éventuellement une ou plusieurs <section> à l'intérieur.

---



## **Résumé Technique**

### **Omission de balises :** 
    Aucune, la balise d'ouverture et la balise de fermeture sont obligatoires.

### **Parents autorisés :** 
	Tout élément acceptant du contenu de flux. Un élément <article> ne doit pas être un descendant 
    d'un élément <address>.

### **Rôle ARIA implicite :** 
	article

### **Rôle ARIA autorisés :** 
    application, document, feed, main, none, presentation, region.

---



## **Attributs**

**Cet élément n'a pas d'autres attributs que les attributs universels, communs à tous les éléments.**



## **Notes d'utilisation**

    Chaque <article> autonome, qui n'est pas imbriqué dans un autre élément <article>, 
    devrait être identifié typiquement, en incluant un élément de titre <h1> à <h6>.

    Quand un élément <article> est imbriqué dans un autre, 
    l'élément contenu représente un article relatif à l'élément contenant. 

    Par exemple, les commentaires d'une parution de blog peuvent être un élément <article> inclus dans l'<article> 
    représentant la parution en elle-même.

    Des informations à propos de l'auteur d'un élément <article> peuvent être fournies 
    au travers de l'élément <address>, mais cela ne s'applique pas aux éléments <article> imbriqués.

    La date et l'heure de publication d'un élément <article> peuvent être donnés en 
    utilisant l'attribut datetime d'un élément <time>. 

    Notez que l'attribut pubdate de <time> ne fait plus partie de la norme W3C HTML 5.

---



## **Exemples**
    <article class="film_review">
        <header>
            <h2>Jurassic Park</h2>
        </header>
        <section class="main_review">
            <p>Les dinosaures étaient super !</p>
        </section>
        <section class="user_reviews">
                <article class="user_review">
                    <p>Beaucoup trop effrayant pour moi</p>
                    <footer>
                        <p>
                            Posté le
                            <time datetime="2015-05-16 19:00">16 mai</time>
                            par Lisa.
                        </p>
                    </footer>
                </article>
            <article class="user_review">
                <p>Je suis d'accord, les dinosaures sont mes préférés</p>
                <footer>
                    <p>
                        Posté le
                        <time datetime="2015-05-17 19:00">17 mai</time>
                        par Gilles Stella.
                    </p>
                </footer>
            </article>
        </section>
            <footer>
                <p>
                    Posté le
                    <time datetime="2015-05-15 19:00">15 mai</time>
                    par Staff.
                </p>
            </footer>
    </article>

### Résultat

**must be provided**

---



## **Compatibilité des navigateurs**