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