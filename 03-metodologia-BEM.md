# Metodología BEM - guía básica

### Características generales:
Esta metodología utiliza únicamente clases para seleccionar los elementos html. Los nombres de clase deben ser específicos para cada bloque html.
Ejemplo:
```html
<div class="login-form"></div> <!--Nombre específco para el bloque-->
<div class="register-form"></div> <!--Nombre específco para el bloque-->

```
Para indicar un hijo dentro del contenedor, se utiliza doble guión bajo.
```html
<div class="login-form">
    <p class="login-form__p"></p><!-- contenedor__1erhijo -->
</div>

<div class="register-form">
    <p class="register-form__p"></p><!-- contenedor__1erhijo -->
</div>
```
Para indicar otros elementos anidados se utiliza el guión medio.
```html
<div class="login-form">
    <p class="login-form__p">
        <strong class="login-form__p-strong"></strong>
    </p><!-- contenedor__1erhijo-subhijo -->
</div>

<div class="login-form">
    <h1 class="login-form__h1">
        <p class="login-form__h1-p">
            <strong class="login-form__h1-p-strong"></strong>
        </p>
    </h1><!-- contenedor__1erhijo-subhijo-sub subhijo -->
</div>
```
Para indicar que uno de los hijos del conetendor con la misma clase, va a ser especial se utiliza el doble guión medio.
```html
<div class="register-form">
    <input type="text"class="register-form__input--active"/>
    <input type="text"class="register-form__input"/>
    <input type="text"class="register-form__input"/>
    <input type="text"class="register-form__input"/>
</div>
```
Esto facilita poder cambiarle la clase con javascript con claridad del selector para cuando, por ejemplo, se produce un evento de clic.
```html
<div class="register-form">
    <input type="text"class="register-form__input"/>
    <input type="text"class="register-form__input"/>
    <input type="text"class="register-form__input--active"/>
    <input type="text"class="register-form__input"/>
</div>
```


