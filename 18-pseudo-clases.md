# Pseudo-clases
Las pseudo-clases son listeners de eventos. Entran en funcionamieto cuando en un elemento, al cual se aplica la pseudo-clase, se produce un evento como clic, doble clic, pasar por arriba del elemento, activarlo, darle foco, etc.

**Los más usados son:**
* :hover (se dispara cuando el puntero pasa por arriba del elemento afectado)
* :link (estado inicial de un enlace)
* :visited (estado visitado de un enlace)
* :active (estado activo de un enlace)
* :focus (se dispara cuando se hace foco en el elemento afectado)
* :lang
### :hover
Esta pseudo-clase nos permite manipular el estilo de aquellos elementos afectados donde el puntero del mouse pase por arriba. Es muy usado para enlaces, botones, animaciones, etc.
```html
<html>
    <button>clic aquí</button>
</html>
```
```css
button {
    background: darkslateblue;
    color: #fff;
    transition: background .5s, color .5s;
}

button:hover {
    background: slateblue;
    color: #000;
}
```
### :link
Esta pseudo-clase nos permite cambiar el estilo de aquellos enlaces que todavía no han sido visitados.
```html
<html>
    <a href="#">clic aquí</a>
</html>
```
```css
a:link {
    background: black;
    color: white;
}
```
### :visited
Esta pseudo-clase nos permite cambiar el estilo de aquellos enlaces que ya han sido visitados. Para cambiar las propiedades desde afuera del enlace:visited, deberemos tener en cuenta los niveles de prioridad. Podríamos usar un ID o un !important para tener el dominio de sus estilos.
```html
<html>
    <div>clic aquí</div>
</html>
```
```css
a:visited {
    background: red;
    color: blue;
}
```
### :active
Esta pseudo-clase nos permite cambiar el estilo de aquellos elementos que reciben clic. Este estilo se va a mantener mientras se mantenga el clic presionado.
```css
div {
    background: red;
    width: 250px;
    height: 250px;
    margin: 50px;
}

div:active {
    background: green;
}
```
### :focus
Esta pseudo-clase nos permite cambiar el estilo de aquellos elementos que han tomado el foco. Se aplica generalmente a los inputs.
```css
input {
    /*Todos los cambios en input:focus van a aparecer de a poco,
    es una transición de 1 segundo*/
    transition: all 1s;
}

input:focus {
    background: black;
    color: white;
}
```
### :lang
Esta pseudo-clase nos permite cambiar el estilo de aquellos elementos que respondan al lenguaje establecido. Para esto, se debe establecer primero en la etiqueta html la propiedad lang="colocamos en, es, etc.". Después, desde CSS, se le debe aplicar esta pseudo-clase al elemento en cuestión para modificar su estilo o directamente, para aplicarlo a todos los elementos que respondan a un determinado lenguaje, ponemos en CSS **:lang(es){...estilos}**.
Esta pseudo-clase casi no se usa en la actualidad.
```html
<body>
    <b lang="en">Hello world!!!</b>
    <b lang="es">Hola mundo!!!</b>
</body>
```
```css
b:lang(es) {
    background: red;
    color: white;
}

b:lang(en) {
    background: white;
    color: red;
}
```