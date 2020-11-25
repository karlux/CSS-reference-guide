# Responsive design - Mobile first
Cuando hablamos de **responsive design**, nos referimos a un diseño que puede adaptarse a diferentes resoluciones para dar al usuario una buena experiencia de uso. 
Por otro lado, **mobile first** tiene que ver con comenzar siempre con el diseño para los móviles, después pasar a adaptar esto a las tablets, después a ordenadores, etc. Dar prioridad e iniciar siempre por las pantallas más pequeñas. 
**Importante:** Google posiciona mejor las web que respondan a esta forma de diseño, es decir, ayuda al SEO (posicionamiento orgánico).

### Responsive design
Para trabajar con esto, se utiliza las llamadas media querys de CSS. Esto detecta la resolución y de acuerdo a eso, cambia los estilos.
```html
<body>
    <div class="caja">
        <h1 class="titulo">Este es el título</h1>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ullam,
           id nisi. Velit nostrum sed modi esse ipsam quo ratione ex 
           placeat? Incidunt accusamus molestiae aspernatur dolore 
           necessitatibus ratione reiciendis animi.
        </p>
    </div>
    <div class="caja2">
        <h2 class="subtitulo">Este es un subtítulo</h2>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ullam,
           id nisi. Velit nostrum sed modi esse ipsam quo ratione ex 
           placeat? Incidunt accusamus molestiae aspernatur dolore 
           necessitatibus ratione reiciendis animi.
        </p>
    </div>
</body>
```
#### Utilizamos @media para indicar en qué resolución cambiar los estilos
Con esto, cada vez que las resoluciones sean menores a 800px, cambiará los estilos por los indicados.
```css
div {
    display: inline-block;
    width: 45%;
    padding: 20px;
    background: #ddd;
}

h1 {
    font-size: 24px;
}

.caja2 {
    background: #bbb;
}

@media only screen and (max-width: 800px) {
    div {
        display: block;
        width: 100%;
    }

    h1 {
        font-size: 18px;
    }
}
```