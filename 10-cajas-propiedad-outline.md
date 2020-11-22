# Propiedad de caja: outline
Esta propiedad se utiliza para darle un "borde" a una caja para **resaltarla**, pero no afecta al tamaño de esta ni del resto de elementos del DOM (Document Object Model) como sí lo hace border.
Esto se da igual, por más que le demos o NO, **box-sizing: content-box;** ó **box-sizing: border-box;**
```css
.caja1 {
    background: rgba(50, 120, 50, 0.9);
    width: 200px;
    height: 200px;
    box-sizing: content-box; /*border-box*/
    outline: 10px solid rgba(0, 50, 50, 1);
}
```
Puede usarse para indicar que elemento tiene el foco al pasar el mouse.
```css
.caja1:hover {
    outline: 10px solid rgba(0, 50, 50, 1);
}
```