# Propiedad de cajas: overflow
Esta propiedad, nos permite controlar qué hacer con el contenido que se desborda de la caja.
Valores posibles:
* **visible** (valor por default)
* **hidden** (oculta lo que se desborda)
* **scroll** (muestra las barras de scroll **x** e **y** para ver el contenido)
* **auto** (Agrega las barras de scroll **x** e **y** solamente si se necesita)

### A tener en cuenta
Los elementos img no se desbordan, se ajustan a su contenedor por más que le cambiemos su tamaño. 
Para lograr desbordamiento, se le debe indicar una position relative y darle posicionado con top y left.