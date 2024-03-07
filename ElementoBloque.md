# Elementos de Bloque
Existen diferentes elementos de bloque en HTML 5:
## Header 
La etiqueta header, indica la cabecera de la web; normalmente almacena el encabezado de una web o sección; suele ser común añadir un logo y título (encabezado) de la web.
```HTML
<header>
    <div class="container">
        <p><img src="images/logo.png" alt="Logo Centro Deportivo
Aguadulce"></p>
        <h1>Centro Deportivo Aguadulce </h1>
    </div>
</header>
```
## Nav
La etiqueta nav está concebida para albergar enlaces de navegación; estos enlaces pueden ser internos o externos. Suelen encontrarse después de la etiqueta header.

Normalmente se incluyen una lista para dichos enlaces.
```HTML
<nav>
    <div class="enlaces">
        <a href="#inicio">Inicio</a>
        <a href="#actividades">Actividades</a>
        <a href="#galeria">Galeria</a>
        <a href="#contacto">Contacto</a>
    </div>
 </nav>
```
## Main 
La etiqueta main delimita el espacio del contenido principal; dentro puede haber distintas secciones y artículos.

Es importante que haya una única etiqueta main para delimitar este espacio, y que esté bien estructurada, con distntas secciones.

Dentro de esta etiqueta podemos encontrar las etiquetas section y article.
## Aside
La etiqueta aside, permite definir un contenido auxiliar dentrp del contenido principal de tal forma que sea un contenido fijo que muestre o un menú o información de interés general de la página.
## Section
La etiqueta section, delimita las distintas secciones de una página; sobre todo se utiliza para separar y dar significado semántico a la web.

```HTML
<section id="inicio">
    <div class="container">
        <img src="images/centrodeportivo.jpg" alt="Centro Deportivo">
            <p>Practicar deporte es esencial para mantener un estilo de
            vida saludable, beneficiando el corazón, la mente y el cuerpo. Nuestro
            centro ofrece instalaciones de vanguardia que incluyen gimnasios bien
            equipados, canchas modernas y piscinas exteriores e interiores. ¡Únete a
            nosotros y vive el deporte!</p>
    </div>
</section>
```

## Article
La etiqueta article, almacena información como una unidad independiente; como puede ser un artículo de una noticia o un comentario. No tiene una representación como tal pero sí es imporatante semánticamente.
```HTML
<article
    <h3>Historia a contar</h3>
    <p> esta es una historia….</p>
</article>
```
## Footer
La etiqueta footer delimita el pie de una página; normalmente delimita enlaces generales de la página o información sobre la misma, como puede ser contacto o dirección de correo.
```HTML
<footer>
    <div class="pie">
        <div class="subpie">
            <p>Pepe perez</p>
            <p>LM | ASIR | 2023/2024</p>
        </div>
        <div class="subpie">
            <a href="https://www.instagram.com/">Siguenos en Instagram</a>
            <p>Teléfono: 954123456</p>
            <p>Dirección: Avda. del deporte, s/n</p>
        </div>
    </div>
 </footer>
```
## Div 
la etiquta div, permite almacenar un contenedor de tal forma que podamos almacenar conjunto de contenedores con un contenido de forma personalizada.
```HTML
<div class="subpie">
        <p>Pepe perez</p>
        <p>LM | ASIR | 2023/2024</P>
</div>
```
## Otras etiqutas
### **address** 
La etiqueta address, permite almacenar una dirección, ya sea física o un correo electrónico.
```HTML
<address>
    Para contactar con la web puede enviar un correo a <a
    href=”mailto:aa@aa.com”>aa@aa.com</a>
</address>
```
### Details
La etiqueta details, permite mostrar un contenido textual cuando se despliega el
componente.
Esta etiqueta contiene el elemento hijo summary; que será el que aparece como
título del detalle.
```HTML
<details>
    <summary>Pincha aqu&iacute;</summary>
Este contenido está desplegado.
</details>
```
### Dialog
La etiqueta dialog, muestra un diálogo al usuario. Esta información estará visible
si tiene el atributo open añadido.
```HTML
<dialog open>
 La compra se ha realizado correctamente.
</dialog>
```
### Figure
La etiqueta figure permite mostrar una imagen con una figura o leyenda. Se
añade dentro de esta etiqueta figcaption; que establece esta leyenda. Veamos
un ejemplo:
```HTML
<figure>
 <img src=”logo.png” alt=”logotipo”
 <figcaption>El logotipo de la web</figcaption>
</figure>
```
### hr
La etiquita hr, establece un delimitador o separador entre secciones, normalmente se muestra como una línea horizontal.
```HTML
<hr/>
```
### pre
La etiqueta pre o texto preformateado, permite mostrar un texto tal y como está escrito en el documento html; representando saltos de página, tabulaciones y espacios.
```HTML
<pre>
 esto 
 esta 
preformateado 
</pre>
```