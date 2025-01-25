    <p> 
# **: l'élément paragraphe**

---


    L'élément HTML <p> représente un paragraphe de texte. 
    Les paragraphes sont généralement représentés comme des blocs 
    et séparés par un espace vertical, leur première ligne est également parfois indentée. 
    Les paragraphes sont des éléments blocs.

---

## **Exemple interactif**
    HTML Demo: <p>
### **Exemple interactif en HTML**
    <p>
        Geckos are a group of usually small, usually nocturnal lizards. They are found on every continent except Antarctica.
    </p>

    <p>
        Some species live in houses where they hunt insects attracted by artificial light.
    </p>


### **Exemple interactif en CSS**
    p {
        margin: 10px 0;
        padding: 5px;
        border: 1px solid #999;
    }

---


    Étant des éléments de bloc, les paragraphes se fermeront automatiquement si un autre 
    élément de bloc est analysé avant la balise de fermeture </p> 
    (voir Omission de balises dans le tableau qui suit)

---


## **Attributs**

    Cet élément, comme les autres éléments HTML, inclut les attributs universels.

---


## **Exemples**

    HTML

    <p>
        Premier paragraphe du texte. J'aime les licornes beaucoup beaucoup beaucoup.
    </p>

    <p>
        Deuxième paragraphe du texte. Et si j'en avais une apprivoisée je serais très
        contente.
    </p>

---


## **Accessibilité**

    Répartir le contenu entre différents paragraphes permet d'améliorer l'accessibilité d'une page. 
    Les lecteurs d'écran et autres outils d'assistance fournissent des raccourcis qui permettent 
    aux utilisateurs d'accéder rapidement au paragraphe suivant ou précédent et ainsi de naviguer 
    plus rapidement sur la page, comme le permettent les blancs pour la navigation visuelle 
    des autres utilisateurs.

    L'utilisation de paragraphes vides (des éléments HTML <p> sans contenu) est 
    problématique pour les personnes qui naviguent sur une page à l'aide d'outils d'assistance. 
    Les lecteurs d'écran, par exemple, pourraient annoncer l'élément mais pas le contenu associé 
    ce qui peut être frustrant ou source de confusion.

    S'il est nécessaire d'avoir un espace supplémentaire, on pourra utiliser des propriétés 
    CSS comme margin pour obtenir l'effet désiré.

---

    CSS

    p {
        margin-bottom: 2em; // on ajoute un espace après chaque paragraphe
    }

---