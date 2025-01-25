# **<head : l'élément de métadonnées (en-tête) du document**
---



## **L'élément HTML <head fournit des informations générales (métadonnées) sur le document, incluant son titre et des liens ou des définitions vers des scripts et feuilles de style.**

---



## **Attributs**

**Comme tous les éléments HTML, cet élément prend en charge les attributs universels.**

**profile : Obsolète**

**L'URI d'un ou plusieurs profils de métadonnées, séparés par un espace.**

---



## **Exemples**
    <html>
        <head>
            <title>Titre du document</title>
        </head>
    </html>
---



## **Notes**

**La plupart des navigateurs conformes à HTML5 construisent automatiquement l'élément <head si les balises sont omises dans le balisage.** 
**Cependant, ce comportement n'est pas garanti pour les navigateurs antérieurs.**

---



## **Résumé Technique**

### **Conten autorisé :**

    Si le document est un document source (srcdoc) d'une <iframe ou si l'information pour le titre est disponible 
    via un protocole de plus haut niveau zéro ou plusieurs éléments de méta-données. 
    Sinon un ou plusieurs éléments de méta-données dont un (et un seul) est un élément <title.


### **Omission de balises :** 

    La balise de début peut être absente si le premier contenu est un élément. 
    La balise de fermeture peut être absente si le premier objet suivant 
    l'élément <head n'est pas un caractère blanc ou un commentaire.


### **Parents autorisés :** 

    Cet élément doit être le premier enfant de l'élément <html.

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