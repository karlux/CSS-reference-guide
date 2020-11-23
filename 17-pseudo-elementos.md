# Pseudo-elementos
Los pseudo-elementos no forman parte del DOM como un elemento convencional, a excepción de ::first-line y ::first-letter qué sí podemos seleccionar y manipular en la vista. Los pseudo-elementos que requiren de la etiqueta content, no forman parte del DOM.
Se utilizan para implementar cambios visuales sin afectar al DOM.
Las pseudo-clases **NO funcionan** en los elementos de tipo **inline**. Sí funcionan en elementos de tipo block, inline-block, grid, flex, etc.
Un pseudo-elemento se aplica a un elemento.
```css
elemento::pseudo-elemento {
    /*código*/
}
```

Los más usados son:
 * ::first-line (funciona con block) - forma parte del DOM.
 * ::first-letter (funciona con block) - forma parte del DOM.
 * ::placeholder (permite modificar placeholder de inputs de tipo texto)
 * ::selection (hijos - content (necesario) - inline)
 * ::after
 * ::before (hijos - content (necesario) - inline)

### ::first-line
Este pseudo-elemento representa la primera línea del texto y sigue haciéndolo a pesar de que se cambie el tamaño de pantalla. Solamente toma la primera línea (responsive)
```css
.texto::first-line {
    color: red;
}
```
### ::first-letter
Este pseudo-elemento representa la primera letra de un texto.
```css
.texto::first-letter {
    font-size: 2em;
    color: red;
}
```
### ::placeholder
Este pseudo-elemento representa al placeholder de un input de tipo texto.
```css
input::placeholder {
    color: grey;
    opacity: .7;
}
```
### ::selection
Este pseudo-elemento representa a la selección que se haga (haciendo doble clic sobre una palabra, seleccionando parte del texto o elementos, etc.).
Muy útil para el efecto de resaltado (marcador) de texto en apuntes.
Por default el background es celeste y el color de fuente es blanco.
La contra es que la selección se comporta como un elemento en línea y por eso pierde muchas propiedades como margin, padding, width, height, etc.
```css
.texto::selection {
    color: yellow;
}
```

### ::before y ::after
Estos pseudo-elementos permiten insertar contenido antes o después del elemento al que afecten. Requiere la propiedad content para funcionar y se comporta como un elemento en línea. 
No pertenecen al DOM y por esto no lo podemos seleccionar o interactuar con él.

```html
<body>
    <p>Luciano</p>
</body>    
```

```css
p::before {
    content: "Hola ";
}
p::after {
    content: ", bienvenido!"
}
```
