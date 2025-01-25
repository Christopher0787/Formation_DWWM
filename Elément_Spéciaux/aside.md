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