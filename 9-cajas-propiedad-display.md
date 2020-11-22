# Display

Para cambiar el tipo de una determinada caja, podemos utilizar la propiedad "display".

**Valores importantes de Display:**
* inline
* block
* inline-block
* inline-table (Ídem al anterior, pero en línea)
* list-item (Se comporta como listas html - **ul** / **ol**)
* table (Se comporta como la tabla que ya conocemos de html) ***deprecated***
* table-cell (Se comporta como una celda de tabla) ***deprecated***
* table-row (Se comporta como una fila de tabla) ***deprecated***
* table-column (Se comporta como una columna de tabla) ***deprecated***
* flex
* grid
* inherit

### inline
Si queremos que un elemento de tipo bloque se comporte como un elemento en línea, se indica  **"display: inline;"**.
Los elementos **inline**, no aceptan cambios en su ancho y alto, por más que se los indiquemos.
```css
b {
    width: 200px;
    height: 500px;
}
```
Una forma de lograr que un elemento **inline** permita cambios de tamaño es dándole un **display block**.
```css
b {
    display: block;
    width: 200px;
    height: 500px;
}
```
### block
Si queremos que un elemento de tipo en línea se comporte como un elemento en bloque, se indica  **"display: block;"**.
Los elementos **block** aceptan cambios en su ancho y alto a partir de las propiedades width y height.
```css
h1 {
    width: 200px;
    height: 500px;
}
```
### inline-block
Si queremos que el comportamiento de un elemento sea inline, pero que admita además cambios de tamaño como lo hace un elemento block, se indica **display: inline-block;**
```css
b {
    display: inline-block;
    width: 200px;
    height: 500px;
}

h1 {
    display: inline-block;
    width: 200px;
    height: 500px;
}
```
