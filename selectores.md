# Guía de referencia para CSS vanilla
## Selectores
#### Selector universal
El selector universal es el *
Con este, seleccionamos todos los elementos html.
Ejemplo: Todos los elementos html tendrán el texto rojo.
```css
* {
    color : red;
}
```
#### Selector de tipo
Para el selector de tipo, usamos el nombre del elemento html.
De esta manera, se afecta solamente a ese elemento.
```css
h1 {
    color: red;
}
```
#### Selector de clase
Para seleccionar por clase, primero debemos indicar la class en el o los elementos html (Pude usarse en varios elementos).
```html
<h1 class="title">
<h2 class="title">
```
Con este agregado de clase, ya podemos seleccionarlo desde CSS anteponiendo el punto delante del nombre de la clase.
En el siguiente ejemplo se modificarán los elementos h1 y h2 ya que comparten la misma clase "title"
```css
.title {
    color: red;
}
```
#### Selector de identificador
Para seleccionar por identificador, primero debemos indicar el id en el elemento html (Pude usarse solamente en un elemento ya que un id siempre debe ser único).
```html
<p id="texto">texto de prueba</p>
<p>texto de prueba</p>
```
Con este agregado de id, ya podemos seleccionarlo desde CSS anteponiendo el símbolo numeral delante del nombre del id dado.
En el siguiente ejemplo se modificará solamente el elemento "p" con el id texto.
```css
#texto {
    color: red;
}
```
#### Selector de atributo
Para este selector podemos indicar un atributo personalizado en el elemento html.
```html
<h1 cualquier-cosa="cualquier-cosa"></h1>
```
Como se observa, podemos colocar el atributo y valor que querramos. Para seleccionarlo desde css, deberemos poner ese atributo entre corchetes, como se muestra a continuación.
```css
[cualquier-cosa="cualquier-cosa"] {
    color: red;
}
```
#### Selector de descendiente
En este caso, podemos seleccionar un elemento hijo html para poder modificarlo.
```html
<p>Este es un <b>elemento hijo</b></p>
```
El elemento "p" tiene de hijo a un elemento "b". Desde css, podemos seleccionarlo indicando el contenedor ("p") y luego el hijo ("b").
```css
p b {
    color: red;
}
```
Veamos otro ejemplo en donde haya más niveles de hijos.
```html
<div id="bloque">
    <ul>
        <li>item 1</li>
        <li>item 2</li>
        <li>item 3</li>
    </ul>
</div>
```
Podemos combinar con lo selectores de id. Con esta seleccionamos todos los hijos "li" de "ul" que a su vez es hijo del elemento con el id "bloque".
```css

#bloque ul li {
    color: blue;
}
```
#### Selector de pseudo-clases
Las pseudo-clases son una serie de términos a los que se les antepone ":"
En el siguiente ejemplo, cuando pasemos el puntero del mouse sobre el elemento "p", este cambiará su color a rojo.
```css
p:hover {
    color: red;
}
```
Para más información sobre las pseudo-clases, dirigirse a la siguiente
[web](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes)
#### Selector de pseudo-elemento
Las pseudo-clases son una serie de términos a los que se les antepone "::"
Ejemplo:
En el siguiente ejemplo, se selecciona solamente la primera línea de texto dentro del elemento "p". Esto es relativo a la pantalla, ya que solamente selecciona la 1era línea de texto que se ve en la pantalla usada. 
```css
p::first-line{
    color: red;
}
```
Para más información sobre los pseudo-elementos, dirigirse a la siguiente
[web](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Selectores_CSS/Pseudo-clases_y_pseudo-elementos#%C2%BFQu%C3%A9_es_un_pseudoelemento)
