    <footer> 
# **: l'élément de pied de page ou de section**

---



    L'élément HTML <footer> représente le pied de page de la section 
    ou de la racine de sectionnement la plus proche. 
    Un élément <footer> contient habituellement des informations sur l'autrice 
    ou l'auteur de la section, les données relatives au droit d'auteur (copyright) 
    ou les liens vers d'autres documents en relation.

---



## **Exemple interactif en HTML**

    HTML Demo: <footer>

    <article>
        <h1>How to be a wizard</h1>
        <ol>
            <li>Grow a long, majestic beard.</li>
            <li>Wear a tall, pointed hat.</li>
            <li>Have I mentioned the beard?</li>
        </ol>
        <footer>
            <p>© 2018 Gandalf</p>
        </footer>
    </article>

## **Exemple interactif en CSS**

    article {
        min-height: 100%;
        display: grid;
        grid-template-rows: auto 1fr auto;
    }

    footer {
        display: flex;
        justify-content: center;
        padding: 5px;
        background-color: #45a1ff;
        color: #fff;
    }

---



## **Résumé Technique**
   
### **Contenu autorisé :**
    Contenu de flux sans élément descendant qui soit <footer> ou <header>.

### **Omission de balises :** 
    Aucune, la balise ouvrante et la balise fermante sont toutes les deux obligatoires.

### **Parents autorisés :** 
    Tout élément qui accepte du contenu de flux. 
    Un élément <footer> ne doit pas descendre d'un élément <address>, <header> 
    ou d'un autre élément <footer>.

### **Rôle ARIA implicite :** 
    contentinfo, ou pas de rôle correspondant si un descendant d'un élément <article>, <aside>, <main>, <nav> ou <section>, 
    ou un élément avec role=article, complementary, main, navigation ou region.

### **Rôle ARIA autorisés :** 
    group, none, presentation

---