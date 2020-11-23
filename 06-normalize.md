# Normalize

La normalización en CSS tiene que ver con resetear todas las reglas que cargan por defecto los diferentes navegadores.
Al resetearlas, nuestros estilos se verán siempre igual en cualquier lugar. Para normalizar, se seleccionan todos los elementos con "*" y se procede a resetear todas las propiedades que necesitemos.
```css
*{
    margin: 0;
    padding: 0;
    /*css*/
}
```
Podemos hacer esto de forma manual, pero ya existen herramientas que resetean absolutamente todos los elementos que pueden llegar a ser modificados por los navegadores.
Podemos descargar ese código de la siguiente [web](https://necolas.github.io/normalize.css/). Luego, lo linkeamos al html.
```html
<head>
    <!--  otro código -->
    <link rel="stylesheet" href="normalize.css">
    <!--  otro código -->
</head>
```

O podemos instalarlo usando el gestor de paquetes npm
```sh
npm install normalize.css
```
Recordar iniciar antes npm con:
```sh
npm init
```

# Importante!!!

### "margin y padding a cero"
Debemos agregar a todos los elementos **margin: 0** y **padding: 0** ya que eso no lo hace normalize.css
También, tenemos que buscar con ctrl+f el elemento **h1** para quitarle el magin que le da normalize.css
```css
*{
    margin: 0;
    padding: 0;
}

/* más código css*/

/*h1 {
    font-size: 2em;
    margin: 0.67em 0;
}*/

h1 {
    font-size: 2em;
}
```
### "box-sizing: border-box" a todos (*) los elementos
Además, debemos agregar la regla para box-sizing con el valor border-box a todos los elementos.
Esto se hace para que las cajas en las que se define un tamaño fijo, no lo cambien a pesar de agregarle padding.
Si una caja tiene **width: 50px** y **height: 50px** y le agregamos **padding: 20px**, El resultado va a ser que se va a sumar 20 más al tamaño de la caja para dar lugar al padding agregado, quedando una caja de **70px** de ancho y alto. Pero , si agregamos esta regla, evitamos eso y el padding se hace interno, si se puede.
```css
/*Seleccionamos todos los elementos con el "*" */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
### "max-with: 100%" en el elemento img
A pesar de tener todo reseteado, necesitamos establecer el valor 100% a los elementos img. Con esto se logra que las imágenes se vean bien en el navegador, tablet, móvíl, etc. ya que van a ocupar solamente lo que le permite el contenedor.
```css
img {
    border-style: none;
    max-with: 100%;
}
```