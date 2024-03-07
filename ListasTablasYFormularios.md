# Listas, Tablas y Formularios.
## Listas 
Las listas, son elementos que permiten mostrar información de forma estructurada
normalmente para diferenciar diferentes elementos o características. En HTML,
podemos diferenciar 3 tipos:
* Desordenadas
* Ordenadas
*  De Definición
### Desordenadas
Las listas desordenadas (Elemento ul) permiten mostrar información de forma
estructurada mostrando las llamadas viñetas Aunque se puede cambiar el
formato de estas utilizando CSS.
```HTML
<ul>
 <li>Elemento 1</li>
 <li>Elemento 2</li>
 <li>Elemento 3</li>
</ul>
```
### Ordenadas 
Una lista ordenada (ol), si tiene una numeración para cada elemento. Esta
numeración puede cambiarse utilizando los siguientes atributos:
* _start_: indica el inicio de la lista.
* _reversed_: indica si es ascendente (valor false por defecto) o descendente
(valor true).
* _type_: Indica el tipo de lista.
    * a: Letras Minúsculas.
    * A: Letras Mayúsculas.
    * i: Números Romanos en Minúsculas.
    * I: Número Romanos en Mayúsculas.
    * 1: Para Números.
```HTML
<ol type=”a”>
 <li>Elemento a</li>
 <li>Elemento b</li>
 <li>Elemento c</li>
</ol>
```
### Listas 
**Definición**
Las listas de definición permiten mostrar diferentes definiciones de términos a partir de claves y su correspondiente valor. Se componen de los siguientes elementos:
* dt: Término de la definición; en una lista puede haber varios términos para
una definición.
* dd: Definición; indica la definición de los diferentes términos
```HTML
<dl>
    <dt>PalWorld</dt>
    <dd>Palworld es un videojuego…</dd>
</dl>
```
### Tablas
Una tabla es un contenedor de distintos elementos que permite mostrar elementos por filas y columnas.
Una tabla permite mostrar información dependiendo de los elementos de filas y columnas.
```HTML
<table>
    <thead>
        <th>Cabecera1</th>
        <th>Cabecera2</th>
    </thead>
<tbody>
    <tr>
        <td>Elemento 1</td>
        <td>Elemento 2</td>
    </tr>
</tbody>
</table>
```
Los elementos de una tabla:
* Thead: Indica el encabezado de la tabla.
    * th: indica las columnas del encabezado de la tabla.
* Tbody: Indica el cuerpo de la tabla.
    * tr: cada una de las filas de la tabla.
* td: Cada una de la columna de cada fila.
    * Tfoot: Indica el pie de una tabla; los elementos de cada fila y columna se usan de forma análoga al encabezado.
* Caption: Indica el título de la tabla.

Es importante combinar las distintas celdas de una columna o fila utilizando dos atributos del elemento td.
* colspan: Indica cuántas columnas forman dicha celda.
* rowspan: Indica cuántas filas forman dicha celda.
## Formulario
Un formulario es uno de los elementosmás importantes de la web, en este caso
sirve para que el usuario envíe información a la web a través de
distintos elementos de entrada.

Un formulario se compone de la etiqueta form, seguido de una serie de elementos de entrada. Cada uno de estos elementos pueden tener diferentes métodos de entrada.

La etiqueta form, tiene los siguientes atributos:
* action: indica la URL de destino.
* method: indica el método a utilizar para enviar la petición HTTP (HyperText
Transport Protocol). Normalmente GET o POST.
* target: india donde se abrirá el nuevo contenido _self o _blank (igual que
para enlaces).
* autocomplete: indica si se puede auto rellenar el formulario o no.

un formulario se compone de elementos de entrada. Un
elemento de entrada se define por la etiqueta ```<input>```, esta etiqueta permite
recoger un valor y enviarlo con el formulario.

El elemento input tiene un atributo especial type, que permite definir el tipo, cada tipo obtiene un dato que puede ser después procesado.

* button: Es un botón que se puede pulsar.
* checkbox: Un botón con casilla de selección.
* color: Selecciona un color utilizando la notación RGB(Red Green Blue).
* date: Selecciona una fecha.
* datetime-local: Selecciona una Fecha y una Hora.
* email: Inserta un email.
* file: selecciona un fichero.
* hidden: Elemento no visible.
* image: es un botón que envía el formulario pero con una imagen.
* month: Selecciona un mes y un año.
* number: Permite seleccionar un valor numérico.
* password: Inserta una contraseña; no mostrando el valor por pantalla.
* radio: Casilla de selección de un elemento.
* range: Selección visual de un elemento a través de un rango.
* reset: Resetea el formulario.
* search: Permite realizar una búsqueda.
* submit: Envía toda la información del formulario; normalmente representado por un botón.
* tel: Inserta un número de teléfono.
* text: Texto libre.
* time: Hora.
* url: URL
* week: Año y ordinal de la semana del año.

Además, el elemento input tiene los siguientes atributos:
* autocomplete: Indica si se puede autocompletar o no (a nivel de elemento).
* autofocus: Indica si este elemento tendrá el foco cuando cargue la página.
* disabled: desactiva el componente.
* form: Referencia al id del formulario.
* list: asocia el componente con una lista de opciones.
* name: nombre del elemento que se enviará en la información del formulario.
* placeholder: indica un valor que aparecerá para indicar información extra.
* readonly: el elemento es de solo lectura.
* required: El elemento es obligatorio.
* type: Tipo de elemento
* value: Valor por defecto.

Por otro lado, existe otro elemento de entrada llamado select, este elemento
permite seleccionar una opción de una lista de opciones.

* Cada opción del elemento select, se utiliza el elemento option; que tiene el atributo value y como texto, el texto que aparecerá.
```HTML
<select name=”deporte”>
 <option value=”futbol”>Futbol</option>
 <option value=”baloncesto”>Baloncesto</option>
 <option value=”VoleiBol”>VoleyBol</option>
</select>
```
Por último, vamos a ver algunos otros elementos relacionados con los formularios:
* fieldset: agrupa un conjunto de campos.
* label: indica una etiqueta de un campo. tiene el atributo for que indica el id del elemento de entrada asociado.

Además, cada elemento de entrada tiene una serie de atributos que se pueden utilizar para realizar validaciones:
* required: indica si es obligatorio.
* minlength y maxlength: indica la longitud en caracteres de un texto.
* min y max: indica el valor mínimo y máximo de un valor numérico.
* pattern: Indica un patrón (expresión regular) que debe cumplir el elemento
(utiliza la misma sintaxis que para XML Schema).
