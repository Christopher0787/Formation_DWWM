    <div> 
# **: l'élément de division du contenu**

---


    L'élément HTML <div> (ou division) est le conteneur générique du contenu du flux. 
    Il n'a aucun effet sur le contenu ou la mise en page tant qu'il n'est pas mis en forme 
    d'une manière quelconque à l'aide de CSS.

---


## **Exemple interactif**

### **Exemple interactif**
    HTML Demo: <div>
### **Exemple interactif en HTML**
    <div class="warning">
        <img src="/media/examples/leopard.jpg" alt="An intimidating leopard." />
        <p>Beware of the leopard</p>
    </div>


### **Exemple interactif en CSS**
    .warning {
        border: 10px ridge #f00;
        background-color: #ff0;
        padding: 0.5rem;
        display: flex;
        flex-direction: column;
    }

    .warning img {
        width: 100%;
    }

    .warning p {
        font: small-caps bold 1.2rem sans-serif;
        text-align: center;
    }

---