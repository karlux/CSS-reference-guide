# Propiedad de caja: position
El flujo normal html lee línea a línea cada instrucción y se posiciona en la página de esa forma. Position viene a alterar ese flujo.

**Valores posibles:**
* static (valor por default - con esto no está posicionado)
* relative
* absolute
* fixed
* **sticky**
### Sticky
Sticky es muy similar a **relative** ya que por más que se mueva de posición, conserva su espacio original (no es ocupado por otros elementos).
 Además, es parecido al **fixed**, pero comienza a comportarse como tal, cuando llegamos a la posición que le establecemos.

### Ejemplo de posicionado sticky
```html
<body>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
        Pariatur sequi numquam vitae deleniti sapiente consequatur dolore
         iste earum! Numquam voluptatum perspiciatis asperiores explicabo
          velit vel. Dolore inventore amet adipisci ipsum.
       Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae
   </p>

   <p class="texto-sticky">Lorem ipsum, dolor sit amet consectetur 
       adipisicing elit. Natus illum accusamus praesentium
   </p>

   <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
        Pariatur sequi numquam vitae deleniti sapiente consequatur dolore
         iste earum! Numquam voluptatum perspiciatis asperiores explicabo
          velit vel. Dolore inventore amet adipisci ipsum.
       Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae
        qui maxime, dolore a, nostrum ex architecto est iusto quasi ut 
        perferendis iste ducimus non sapiente, unde sed rem itaque amet?
       Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequatur
        doloribus natus nostrum molestiae, aut rerum dignissimos enim 
        repudiandae atque hic quo unde ex quidem fugiat magni, sit 
        recusandae qui quia.
   </p>
</body>
```
```css
p {
    background-color: lightblue;
}

.texto-sticky {
    background: red;
    position: sticky;
    top: 0;
    /*Cuando hacemos scroll y llegamos a su posicion top 0,
    este elemento comienza a comportarse como fixed*/
}
```