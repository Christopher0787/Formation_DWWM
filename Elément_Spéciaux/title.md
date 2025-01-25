# **<title : l'élément de titre du Document**
---



## **L'élément <title définit le titre du document (qui est affiché dans la barre de titre du navigateur ou dans l'onglet de la page). Cet élément ne peut contenir que du texte, les balises qu'il contiendrait seraient ignorées.**

---



## **Attributs**
**Cet élément inclut uniquement les attributs universels.**

---


## **Notes d'utilisation**

**L'élément <title est toujours utilisé au sein de l'élément <head de la page.**

## Référencement (SEO)

**Le titre d'une page fait partie des éléments principaux qui sont scannés lors de l'indexation d'une page. C'est aussi le texte qui est affiché parmi les résultats du moteur de recherche, de façon proéminente et donc visible par les utilisateurs qui trouvent votre site grâce à un moteur de recherche.**

**Aussi, mieux vaudra avoir des titres descriptifs plutôt que des titres trop courts ou vagues.**

**Quelques observations :**

    * On pourra éviter les titres sur un ou deux mots.

    * La longueur affichée pour les titres dans les résultats d'un moteur de recherche se situe entre 55 et 60 caractères. 
    Si le titre est plus long, on veillera à ce que les concepts majeurs apparaissent avant cette longueur.

    * Attention aux entités (les chevrons HTML pourront être affichés différemment entre les navigateurs).

    * Le titre doit être intelligible et pas une simple concaténation de mots-clés.

    * Le titre devra être unique pour un même site.

---



## **Exemples**

**<title Et voici le titre de ma page !</title**

---



## **Accessibilité**

**Il est important de fournir une valeur pour l'attribut title qui décrit le but de la page de façon claire et concise.**

**Les personnes utilisant des outils d'assistance peuvent utiliser le titre de la page afin de déterminer rapidement ce qu'elle contient.** 

**Ainsi, il peut ne pas être nécessaire de naviguer « dans » la page, ce qui peut prendre du temps et être source de confusion si, ce faisant, on doit déterminer le but de la page.**

### **Exemple**

**<title Menu - Restaurant chinois Maison bleue - Commande en ligne</title**

**Mettre à jour la valeur de title afin de refléter un changement d'état important (un problème de validation d'un formulaire par exemple) peut également s'avérer utile :**

    <title
        2 erreurs sur votre commande - Restaurant chinois Maison bleue - Commande en
        ligne
    </title
