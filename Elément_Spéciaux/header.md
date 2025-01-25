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