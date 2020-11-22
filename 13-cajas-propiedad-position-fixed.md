# Propiedad de caja: position
El flujo normal html lee línea a línea cada instrucción y se posiciona en la página de esa forma. Position viene a alterar ese flujo.

**Valores posibles:**
* static (valor por default - con esto no está posicionado)
* relative
* absolute
* **fixed**
* sticky
## Fixed
**Fixed** es igual a **absolute** (pierde su espacio), con la única salvedad de que el elemento queda fijo. No se mueve. Muy usado en menú fijo, barras de navegación al estilo facebook que siempre se ve, publicidades o elementos que queremos que siempre se vean a pesar de hacer scroll.

Un hack muy usado para dar lugar a un menú fijo arriba, es darle un padding-top al body. Para que el elemento fixed tome ese lugar, le ponemos un margin negativo con el mismo valor al padding-top que se le dio antes al body.
```css
body {
    padding-top: 100px;/*dejamos lugar para el menú*/
}

p {/*Contenido común*/
    background-color: lightblue;
}

.texto-fixed {
    background: red;
    position: fixed;/*Elemento fijado*/
    margin: -100px auto;
    /*Le damos margin negativo con el valor que se le dio
    al padding-top del boy*/
}
```






