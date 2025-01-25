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



## **Attributs**

**Comme tous les éléments HTML, cet élément accepte les attributs universels.**

---



## **Notes d'utilisation**

    Les informations sur l'autrice ou l'auteur doivent être placées dans un élément <address> 
    et incluses dans l'élément <footer>.
    L'élément <footer> n'a pas de contenu sectionnant et ne peut donc pas introduire une 
    nouvelle section dans le plan.

---



## **Exemples**

    HTML

    <body>
        <h3>Les écrivains français du XIX<sup>ème</sup> siècle</h3>
        <ul>
            <li>Hugo</li>
            <li>Flaubert</li>
            <li>Zola</li>
            <li>Maupassant</li>
        </ul>

        <footer>
            <small>Copyright © 2023 Littérature.com. Tous droits réservés.</small>
        </footer>
    </body>

---

    CSS

    footer {
        text-align: center;
        padding: 5px;
        background-color: #abbaba;
        color: #000;
    }

### Résultat

**must be provided**

---



## **Accessibilité**

    Avant la publication de Safari 13, le rôle de repère contentinfo n'était pas correctement exposé par VoiceOver. 
    Si vous devez prendre en charge les anciens navigateurs Safari, 
    ajoutez role="contentinfo" à l'élément footer pour vous assurer que le landmark sera correctement exposé.

        En rapport : WebKit Bugzilla : 146930 - AX : Les éléments natifs HTML 
        (header, footer, main, aside, nav) devraient fonctionner de la même manière 
        que les points de repère ARIA, parfois ce n'est pas le cas.

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