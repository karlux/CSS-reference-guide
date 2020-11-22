# Propiedades para textos
A continuación, se describen las propiedades que podemos manipular en un texto desde CSS. 
Existen otras propiedades, pero no son útiles para nada, prácticamente.
```css
.login-form__p{
    font-size: 2em;/*Si no se setea un valor en el contenedor, 1em = 16px*/
    font-family: Georgia;
    /*Para conseguir más tipografías vamos a google fonts.
    Ahí elegimos una y copiamos el enlace que nos dan
    para pegarlo en el head del html. 
    Luego, copiamos la regla que nos dan para la propiedad
    font-family del elemento en CSS y listo!*/
    color: rgba(0,0,0,0.5);
    line-height: 2;/*Interlineado*/
    font-weight: 900;/*grosor de letra. De 100 a 900. No muy usado*/
    text-shadow: 2px 2px 3px rgba(0, 0, 0, 0.5);
    /*Si se quiere mayor intensidad del efecto shadow, 
    se puede volver a pegar los mismos parámetros varias veces:
    2px 2px 3px rgba(0, 0, 0, 0.5), 2px 2px 3px rgba(0, 0, 0, 0.5),
    2px 2px 3px rgba(0, 0, 0, 0.5);
    */
    text-decoration: none;/*útil para enlaces, quita el subrayado*/
    list-style: none; /*útil para listas*/
    opacity: .5; /*Se puede aplicar a cualquier caja*/
}
```