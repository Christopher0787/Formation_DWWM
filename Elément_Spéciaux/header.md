# **<header**

---



    L'élément HTML <header> représente du contenu introductif, 
    généralement un groupe de contenu introductif ou de contenu aidant à la navigation. 
    Il peut contenir des éléments de titre, mais aussi d'autres éléments tels qu'un logo, 
    un formulaire de recherche, le nom d'auteur, etc.

---



## **Exemple interactif en HTML**

    <header>
        <a class="logo" href="#">Cute Puppies Express!</a>
    </header>

    <article>
        <header>
            <h1>Beagles</h1>
            <time>08.12.2014</time>
        </header>
        <p>I love beagles <em>so</em> much! Like, really, a lot. They’re adorable and their ears are so, so snugly soft!</p>
    </article>

---



## **Exemple interactif en CSS**

    .logo {
        background: left / cover url('/media/examples/puppy-header-logo.jpg');
        display: flex;
        height: 120px;
        align-items: center;
        justify-content: center;
        font:
            bold calc(1em + 2 * (100vw - 120px) / 100) 'Dancing Script',
            fantasy;
        color: #ff0083;
        text-shadow: #000 2px 2px 0.2rem;
        }

        header > h1 {
            margin-bottom: 0;
        }

        header > time {
            font: italic 0.7rem sans-serif;
        }

---



## **Résumé Technique**

### **Contenu autorisé :**
    Contenu de flux mais sans élément descendant qui soit <header> ou <footer>.

---

### **Omission de balises :** 
    Aucune, les balises d'ouverture et de fermeture sont obligatoires.

---

### **Parents autorisés :** 
    Tout élément acceptant du contenu de flux. 
    Il est à noter qu'un élément <header> ne doit pas descendre d'un élément <address>, <footer> ou d'un autre élément <header>.

---

### **Rôle ARIA implicite :** 
    banner, ou aucun rôle correspondant si l'élément <header> descend d'un 
    élément <article>, <aside>, <main>, <nav> ou <section>, ou d'un élément 
    ayant le rôle article, complementary, main, navigation ou region

---

### **Rôle ARIA autorisés :** 
    roup, presentation ou none

---



# **Note d'utilisation**

    L'élément <header> n'est pas une section de contenu et n'introduit donc pas de nouvelle section dans la structure. 
    Cela dit, un élément <header> est généralement destiné à contenir l'en-tête de la section environnante 
    (un élément <h1> à <h6>), mais ce n'est pas obligatoire.

## Usage historique

    Bien que l'élément <header> ne fasse pas partie de la spécification HTML avant HTML5, 
    il existait de façon implicite depuis les premières versions. 
    Comme on le voit sur le premier site web, il était initialement utilisé comme l'élément <head>. À un moment donné, 
    il a été décidé d'utiliser un nom différent. 
    Cela a permis à <header> d'être libre de remplir un rôle différent par la suite.

---



## **Attributs**

**Cet élément ne possède que les attributs universels.**

---



## **Exemples**

## En-tête de page

    <header>
        <h1>Titre principal</h1>
        <img src="mdn-logo-sm.png" alt="Logo de MDN" />
    </header>

### Résultat

**must be provided**

## En-tête d'un article

    <article>
        <header>
            <h2>La planète Terre</h2>
            <p>
                Publié le mercredi <time datetime="2017-10-04">4 octobre 2017</time> par
                Jeanne Smith
            </p>
        </header>
        <p>Nous vivons sur une planète bleue et verte</p>
        <p>
             <a href="https://example.com/the-planet-earth/">Poursuivre la lecture…</a>
        </p>
    </article>

### Résultat

**must be provided**

---