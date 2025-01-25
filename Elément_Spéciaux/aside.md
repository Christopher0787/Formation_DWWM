    <aside> 
# **: l'élément aparté**

---


    L'élément <aside> (en français, « aparté ») représente une partie d'un document dont 
    le contenu n'a qu'un rapport indirect avec le contenu principal du document. 
    Les apartés sont fréquemment présents sous la forme d'encadrés ou de boîtes de légende.

---

## **Exemple interactif**
    HTML Demo: <aside>

## **Exemple interactif en HTML**
    <p>
        Salamanders are a group of amphibians with a lizard-like appearance, including short legs and a tail in both larval
        and adult forms.
    </p>

    <aside>
        <p>The Rough-skinned Newt defends itself with a deadly neurotoxin.</p>
    </aside>

    <p>
        Several species of salamander inhabit the temperate rainforest of the Pacific Northwest, including the Ensatina, the
        Northwestern Salamander and the Rough-skinned Newt. Most salamanders are nocturnal, and hunt for insects, worms and
        other small creatures.
    </p>
---
## **Exemple interactif en CSS**
    aside {
        width: 40%;
        padding-left: 0.5rem;
        margin-left: 0.5rem;
        float: right;
        box-shadow: inset 5px 0 5px -5px #29627e;
        font-style: italic;
        color: #29627e;
    }

    aside > p {
        margin: 0.5rem;
    }

---

## **Attributs**
    Cet élément ne comprend que les attributs universels.
---
## **Notes d'utilisation**
    On ne doit pas utiliser l'élément <aside> pour marquer du texte entre parenthèses, 
    ce type de texte est considéré comme faisant partie du flux principal.
---
## **Exemples**
    Dans cet exemple, on utilise <aside> afin de baliser un paragraphe d'un article. 
    Ici, le paragraphe n'est pas directement lié au contenu principal de l'article et 
    c'est pour cela qu'on utilise cet élément.

---
    HTML

    <article>
        <p>
            Le film Disney <cite>La petite Sirène</cite> est sorti en salles en 1989.
        </p>
        <aside>
            <p>Le film a gagné 87 millions de dollars pendant sa sortie initiale.</p>
        </aside>
        <p>Plus d'informations sur le film…</p>
    </article>
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