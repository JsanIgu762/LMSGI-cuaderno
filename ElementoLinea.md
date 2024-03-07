# Elementos de Línea
En este apartado, vamos ver algunos de los elementos de línea que tiene HTML:
## abbr
La etiqueta abbr, permite indicar que un texto es una abreviatura o un acrónimo.
Se representa subrayado con una línea de puntos.
EL atributo title, permite establecer el significado del mismo que podrá
mostrarse al pasar el ratón por encima.
```HTML
<abbr title=”Hypertext Markup Language”>HTML</abbr>
```
## bdi y bdo
Las etiquetas bdi y bdo, permiten establecer la dirección del texto, o anular el mismo esto permitirá establecer el valor
de la dirección del texto utilizando el atributo dir.
```HTML
<h1>World wrestling championships</h1>
<ul>
 <li><bdi class="name">Evil Steven</bdi>: 1st place</li>
 <li><bdi class="name">François fatale</bdi>: 2nd place</li>
 <li><span class="name"> سما>/span>: 3rd place</li>
 <li><bdi class="name"> إيان القوي الرجل>/bdi>: 4th place</li>
 <li><span class="name" dir="auto"> سما>/span>: 5th place</li>
</ul>
```
## Cite
La etiqueta cite permite mostrar una referencia a un autor o una cita; el texto
normalmente se mostrará en cursiva.
```HTML
<p>Napoleón Dijo: <cite>Los sabios son los que buscan la
sabiduria; los necios piensan ya haberla
encontrado.</cite></p>
```
## Code
La etiqueta code, permite mostrar un código fuente en otro lenguaje de programación; por ejemplo java, python,etc…
```HTML
<p>Hola Mundo en C
    <code>
        #include<stdio.h>
        int main(){
        printf(“Hola Mundo”);
        return 0;
        }
    </code>
```
## Data
El elemento data, nos permite asignar valores a distintos elementos, para que
puedan ser procesados por una máquina.
```HTML
<data value=”10500300”>10500300</data>
```
## Del
El elemento del, permite establecer una trazabilidad a un elemento; es decir que el elemento es
tachado y contiene información de por qué ha sido tachado; tiene los siguientes atributos:
* cite: contiene la URL con la explicación del cambio.
* Datatime: contiene la fecha o la hora del cambio.
```HTML
<p> El lenguaje de programación más utilizado es <del
datetime=”2020-03-04 0:00:00” cite=”lenguajes.html”>Java</del>Python</p>
```
## Dfn
El elemento dfn permite definir un término o definición. Representa el término en
letra cursiva.
```HTML
<p><dfn>Los lenguajes de marcas</dfn> permiten almacenar
información junto a su contexto a través del uso de
etiquetas.</p>
```
## Ins
El elemento ins, es el antagonista de del; permite identificar elementos que se han añadido al documento, mostrando información de trazabilidad; al igual que del, tiene los siguientes atributos:
* cite: Contiene la URL con la explicación del cambio.
* Datetime: contiene la fecha o la hora del cambio.
```HTML
<p>Los lenguajes de programación más demandados son: java,
python, c# y <ins>Kotlin</ins></p>
```
## Kbd
El elemento kbd indica un atajo de teclado o combinación de teclas; esto permite
mejorar la usabilidad de la web.
```HTML
<p> Para arrancar el servidor podemos usar
<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>p</kbd> y pulsar la
opción <em>Live Server: Open With Live Server</em></p>
```
## Mark
El elemento mark, restalta un texto con color amarillo (u otro color si se establece
usando css)
```HTML
<p>Es importante a la hora de trabajar con HTML saber
<mark>utilizar las herramientas disponibles<mark></p>
```
## q
El elemento q (de quote); presenta una cita literal que puede ir acompañado del atributo cite; que permite establecer de donde se ha obtenido dicha cita.
```HTML
<p>Como se indica en wikipedia <q
cite=”https://wikipedia.es/”>XML es un metalenguaje de
marcas</q></p>
```
## Samp
La etiqueta samp indica que el texto delimitado por la etiqueta es un mensaje
proporcionado por un ordenador; diferencia el texto por otra fuente
monoespaciada.
```HTML
<p><samp>Presione F5 para continuar </samp></p>
```
## Slot y small
La etiqueta slot permite definir componentes reutilizables de tal forma que se puedan reutilizar posteriormente.

Además, la etiqueta small permite que un texto tenga una fuente más pequeña
```HTML
<p>Hola <small>que tal </small></p>
```
## Span
La etiqueta span delimita un fragmento de texto para poder posteriormente
establecer un formato personalizado usando CSS; esto es interesante a la hora de
dar importancia o valor a algo en concreto siempre que no haya otra etiqueta que
pueda darle valor.

```HTML
<p>Hola <span class="miclase">que tal </span></p>
```

## Sub y sup
Las etiquetas sub y sup permiten establecer un superindice y un subindice; por lo que se pueden utilizar para definir expresiones matemáticas.
```HTML
<p>0=ax<sup>2</sup>+bx+c</p>
```
## Template y time
La etiqueta template permite crear fragmentos de documento a través del uso de javascript.

Por otro lado, la etiqueta time, permite establecer de forma semántica un tiempo, tiene el atributo datetime que contiene información de la hora o fecha para ser leída por un una máquina.
```HTML
<p> La fecha de finalización es el <time
datetime=”2024-06-22”>22 de Junio de 2024</time></p>
```
## Var y wbr
La etiqueta var, permite establecer dicho contenido como una variable de
ordenador por lo que la establece como cursiva (u otro formato si ponemos css).
```HTML
<p> La variable <var>edad</var> contiene la edad como entero</p>
```
Por otra parte, la etiqueta wbr, indica que el texto tenga un salto de línea si éste sobrepasa el espacio asignado.