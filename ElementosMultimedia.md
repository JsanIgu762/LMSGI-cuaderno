# Elementos Multimedia.
Estos elementos, permiten incrustar información en forma de imagen, audio e incluso vídeo, sin olvidar otros elementos como map que permiten hacer una imagen interactiva.
## Audio
El elemento audio, permite insertar un componente de sonido que esta soportado por la mayoría de navegadores. 

Tiene los siguientes atributos:
* src: URI del recurso; adicionalmente, se puede añadir un elemento source.
* preload: indica cómo se realizará la precarga; los valores son none (no se
precarga), metadata (se precargan los metadatos) y auto (a criterio del
navegador).
* autoplay: reproducción automática.
* loop: reproducción en bucle.
* muted: silencia el componente.
* controls: proporciona una interfaz para el elemento.

## Video
El elemento video, incrusta un elemento visual para reproducir un vídeo. 

Tiene los siguientes elementos:
* src: URI del recurso (también puede utilizarse source).
* poster: URI de la imagen a mostrar mientras se carga.
* playsinline: indica el vídeo dentro de su área de reproducción no a
pantalla completa.
* width y height: indican ancho y alto para la reproducción.

Ademas de tener támbien los atributos hablados en el elemento audio.
## Track
El elemento track, puede utilizarse junto a los elementos audio o video,
permite añadir información a dicho elemento, como pueden ser subtitulos.

Tiene los siguientes atributos:
* default: elemento track a utilizar por defecto.
* kind: tipo de pista. subtitles (subtítulos), captions (transcripciones),
descriptions (descripciones), chapters (capítulos) y metadata
(metadatos no visibles).
* label: título que describe la pista.
* src: URI del elemento
* srclang: idioma del elemento.
## img
Elemento img es el que representa una imagen en HTML: normalmente a partir de un elemento externo representado por el atributo src. 

Permite muchos formatos de imagen como puede ser jpg,png,svg,etc…

Tiene los siguientes atributos:
* alt: texto con información alternativa; este texto es importante para la accesibilidad.
* src: URI del recurso de imagen.
* srcset y sizes: permite asignar diferentes recursos para que el navegador cargue la versión másadecuada.
* usemap: referencia un mapa definido por el elemento map.
* ismap: Indica que la imagen es parte de un mapa del lado del servidor.
* width y height: ancho y alto de la imagen.
* decoding: indica cómo se decodificar la imagen; tiene los valores async(asíncrono),sync(síncrono)
y auto (el navegador decide).
* loading: indica como cargará la imagen; tiene los valores eager (inmediatamente) o lazy (carga a
posteriori).
## Map
El elemento map, permite realizar imágenes interactivas; de tal forma que podemos definir áreas de una imágen con enlaces o elementos los que ir.

Normalmente son referenciados por parte de una imagen, y contienen una serie de elementos area.
```HTML
<map name=”mimapa”>
    <area href=”#intro” alt=”introduccion” shape=”circle”
coords=”205,187,170”/>
</map>
<img src=”imagen.png” usemap=”mimapa” alt=”ejemplo”>
```
El elemento area tiene los siguientes atributos:
* alt: versión textual del área.
* shape: tipo de figura; puede ser circle (círculo), rect (rectangular), poly
(polígono), default (toda el área).
* coords: coordenadas de la figura; depende de la forma seleccionada.
* href: URI al elemento (igual que a).
* target: de forma análoga a los enlaces indica donde se cargará al pulsar.
* download, ping y rel: funcionan igual que para los enlaces.

## Svg
Normalmente, se trabajan con imágenes de mapa de bits (matrices de pixeles),
pero estas tienen un inconveniente y es que se pueden deformar si se escalan. Por eso, se pueden trabajar con imágenes vectoriales.

El elemento svg, permite trabajar con este tipo de imágenes a partir de primitivas expresadas en xml. 
```HTML
<svg xmlns=”http://w3.org/2000/svg/” width=”150”
height=”100”>
    <rect width=”4” height=”1” y=”0” fill=”#00ab39” />
</svg>
```
## Canvas
El elemento canvas, proporciona un lienzo sobre el que mostrar gráficos;
normalmente utilizando lenguajes de script como JavaScript.

Tiene los siguientes atributos:
* width: ancho del elemento.
* height: alto del elemento.

En muchas ocasiones es necesario incrustar contenido a nustra web a través de distintos elementos o incluso programas externos.

## Embed
El elemento embed, representa un contenido incrustado por un plugin o elemento externo, dependiendo del elemento o contenido será más o menos soportado por el navegador.

Tiene los siguientes atributos:
* src: uri del recurso.
* type: indica el tipo MIME del recurso.
* width y height: ancho y alto del elemento.

```HTML
<embed type=”video/webm” src=”trailers/estreno.mov”
width=”640” height=”480”>
```
## iframe
Un iframe, es un contenido de navegación anidado. Es decir, es un documento HTML, externo incrustado.

Tiene los siguientes atributos:
* src: URI del recurso.
* srcdoc: contiene el código HTML a mostrar en el elemento iframe (aunque puede
estar dentro de la etiqueta).
* sandbox: Permite proporcionar restricciones al documento incrustado en el
elemento iframe.
* allow: directivas referentes a permisos.
* allowfullscreen: si existe permite establecer el tamaño a pantalla completa
* width y height: alto y ancho en píxeles.
* loading: puede tomar lazy o eager que se carga se haga visible.

El elemento iframe, es muy utilizado por ejemplo para incrustar vídeos y contenido de webs como youtube u otras páginas.
## Object
El elemento object permite incrustar un elemento externo que puede ser una
imagen u cualquier otro contenido relacionado. 

Puede tener los siguientesatributos:
* data: contiene el recursos que se ha de mostrar.
* type: tipo MIME.
* name: nombre que puede ser utilizado para referenciar a este recurso.
* usermap: referencia al atributo name de un elemento map.
* form: referencia al atributo id de un formulario.
* width y height: ancho y alto del elemento.
