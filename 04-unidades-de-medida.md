# Unidades de medida en CSS
Existen dos tipos de unidades, las unidades fijas y las relativas.
### Unidades de medida fijas:
No dependen de nada, una vez establecidas no varían, por más que se cambie el tamaño de pantalla o su contenedor.
Las más usadas son px (píxeles), cm (centímetros), mm (milímetros), pt(puntos).
```css
p {
    font-size: 15px;
}
.box {
    width: 1cm;
    heigth: 1cm;
}
.container{
    width: 25pt;
    heigth: 25pt; 
}
```
### Unidades de medida relativas:
Varían según el tamaño de pantalla o su contenedor. 
El más usado es **"em"**. Su valor inicial es establecido al inicio. Si no se establece, su valor por defecto es, en general, **16px**, pero esto lo decide el navegador por lo que no es recomendable dejar la unidad em sin definir.
```css
p{
    font-size:2em;/*2 x 16 = 32px*/
}
h3{
    font-size:5em;/*5 x 16 = 80px*/
}
```
El valor **"em"** se hereda del contenedor. Cuando se establece una medida fija (px) a una determinada propiedad, cuando modifiquemos esa propiedad en los hijos contenidos, el valor de **"1em"** será igual a la medida fija en px del padre, en esa propiedad.

```css
.login-form{
    font-size: 10px;/*Se establece el valor de 1em*/
}

.login-form__h2{/*hijo de .login-form*/
    font-size: 2em; /*2 x 10 = 20px*/
}
```
Esto sirve para cualquier propiedad CSS que utilice unidades de medida como margin, padding, height, width, etc.
### Viewport height (vh) y viewport width(vw):
Para indicar que un elemento va a ocupar todo el ancho de la pantalla se da el valor de 100vw y para todo el alto de la pantalla, 100vh
```css
* {/*Esto se llama "Normalize", se hace para resetear
las propiedades que son alteradas por los navegadores*/
    margin: 0;
    padding: 0;
}

.box{
    width: 100vw;/*todo el ancho de la pantalla*/
    height: 100vh;/*todo el alto de la pantalla*/
}

.box2 {
    width: 50vw;/*la mitad del ancho de la pantalla*/
    height: 50vh;/*la mitad del alto de la pantalla*/
}
```
Este tipo de medida relativa depende del tamaño de pantalla.
Existe otra unidad de medida relativa que se establece a partir de %, pero esto va a depender de su contenedor y no de la pantalla, por lo que hay que tener cuidado para no romper el diseño si se cambia el tamaño de pantalla.

