# Cuaderno lenguaje de marcas
## Tabla de contenidos
* ### ¿Qué es un lenguaje de marcas? 
* ### Evolución de los lenguajes de marcas
* ### Características de los lenguajes de marcas
* ### Ejemplos y características de diferentes lenguajes de marcas
* ### XML: definición y caracteristicas del metalenguaje

## ¿Qué es un lenguaje de marcas?
* Un lenguaje de marcas, es aquel que permite representar información que contiene, además de los datos, marcas o etiquetas que indican cómo se estructuran estos datos, su significado o cómo debe representar desde un punto de vista gráfico y visual.
![](https://universidadeuropea.com/resources/media/images/que-es-lenguaje-marca-1200x630.original.jpg) 

## Evolución de los lenguajes de marcas
* [GML](GML.md)
* [SGML](SGML.md)
## Características de los lenguajes de marcas
* **Uso del texto plano**: Al ser un texto plano cualquier persona puede leer y editar esa información.
* Es un **lenguaje compacto**: Las etiquetas de marcas se mezclan con el contenido del mismo.
* **Independencia del dispositivo**: Al ser independiente del dispositivo nos permite mostrar el contenido.
* **Facilidad de procesamiento**: Permite el desarrollo de lenguajes especializadas según el tipo de documento que necesitemos procesar.
* **Flexibilidad**: Posibilidad de combinación con otros lenguajes.
* Muy **ordenados**
## Ejemplos y características de diferentes lenguajes de marcas
* [XML](XML.md)
* [HTML](HTML.md)
* [JSON](JSON.md)
* [YAML](YAML.md)

## XML: definición y caracteristicas del metalenguaje
### Prólogo
El prólogo de un documento XML tiene la siguiente estuctura.
``` XML
<?xml version="1.0" encoding="utf-8" standalone="no"?>
```
Aunque no es obligatorio indica informacion relativa al propio documento.

Puede contener los siguientes elementos:
* **version**: indica la versión de XML que estamos usando.
* **encoding**: indica la codificación escrita en el documento
* **standalone**:  indica la existencia de un esquema XML(DTD) en el propio documento o externo.
### Etiquetas
En un lenguaje de marcas se pueden econtrar unas etiquetas
* Una etiqueta en XML debe tener un inicio y un final que será una palabra entre los símbolos "<" ">"
* Siempre debe haber una etiqueta de cierre "</"
* Las etiquetas pueden tener atributos.
* Un elemento es el par de etiqueta de apertura y de cierre.
* Dentro de un elemento puede encontrarse texto u otros elementos.
* En un documento XML solo puede haber un elemento raiz.
* Pueden añadirse comentarios entre los símbolos ```<!-- y -->```.
### Atributos
En una etiqueta XML puede encontrarse atributos.
* Un atributo en XML, es una información adicional que se le da a una etiqueta en concreto
* Comienza con una palabra, seguido del símbolo "=" y la información entre comillas dobles "".
* Una etiqueta puede tener 0 o más atributos.
* Cada atributo tendrá solo información, no puede como contener como tal otros atributos.
### Ejemplos de XML
``` XML
<pizzas>
    <pizza nombre="Barbacoa" precio="8">
        <ingrediente nombre="Salsa Barbacoa"/>
        <ingrediente nombre="Mozzarella"/>
        <ingrediente nombre="Pollo"/>
        <ingrediente nombre="Bacon"/>
        <ingrediente nombre="Ternera"/>
    </pizza>
    <pizza nombre="Margarita" precio="6">
        <ingrediente nombre="Tomate"/>
        <ingrediente nombre="Jamón"/>
        <ingrediente nombre="Queso"/>
    </pizza>
</pizzas>
```
``` XML
<poema fecha="Abril de 1915" lugar="Granada">
    <titulo>Alba</titulo>
    <verso>Mi corazón oprimido</verso>
    <verso>late junto a la alborada</verso>
    <verso>el dolor de sus amores...</verso>
</poema>
```
``` XML
<recetas>
    <receta>
        <tipo definicion="postre"/>
        <dificultad>Fácil</dificultad>
        <nombre>Tarta de chocolate</nombre>
    </recetas>
    <ingredientes>
        <ingrediente nombre="Cola-Cao" cantidad="250 gramos"/>
        <ingrediente nombre="mantequilla" cantidad="200 gramos"/>
        <ingrediente nombre="harina" cantidad="1 vaso"/>
        <ingrediente nombre="azúcar" cantidad="1 vaso"/>
        <ingrediente nombre="huevos" cantidad="3"/>
    </ingredientes>
</recetas>
```
## Documento XML (Parte del tema 2)
* ### Declaración (prólogo)
    Es un elemento opional que se incluye al inicio del documento.
    
    Empezará y acabará por:
    
    ```<?xml y acaba por ?>```
    y podrá contener los siguientes atributos:
    * _Version_: Versión de XML.
    * _encoding_: Codificación del documento.
    * _standalone_: Indica si el documento es independiente o si existe un DTD externo. Admite valores "yes" o "no" para indicar si existe dicho vocabulario.

    DTD: _Document Type Definition_: contiene las reglas que determina que un documento XML es válido.
* ### Elementos 
    Un documento XML se compone por una serie de elementos.
    * Un elemento tiene un nombre que se diferencia entre mayusculas y minusculas.
    * Comienza por ```<nombre>``` y termina por ```</nombre>```. Debe ser iguales en su apertura y cierre.
    * Los nombres de los elementos deben caracteres alfanuméricos, guiones, guines bajos o punto (sin espacios).
    * Debe haber un único elemento inicial llamado raíz (aunque puede llamarse como queramos).
    * Dentro de un elemento, puede haber más elementos o texto.
    * Si un elemento está vacío puede escribirse como ```<nombre/>```

    Existen las siguientes relaciones.
    * Un único elemento raíz (root).
    * Cada uno de los elementos descendientes de un elemento, se llaman hijos (children).
    * El elemento ascedente de un elemento, se llama padre (parent).
    * Los elementos que tienen un padre común se denominan hermanos (sliblinng).
* ### Atributos
    Un documento xml se compone por una serie de elementos.
    * Deben tener asignado un valor.
    * Los valores siempre van entre comillas(simples o dobles).
    * Diferencian entre mayúsculas y minúsculas.
    * Comienzan por una letra o guión bajo.
    * Los atributos siempre están dentro de la etiqueta de apertura de un elemento.
* ### Comentarios
    Un comentario en XML, es un elemento, que no va a ser procesado; sirve para mostrar información al usuario para entender el contexto del documento u otra información.

    ```<!-- y acaba acaban por -->```
* ### Espacios de Nombres
    El espacio de nombres o namespace, es un identificador que se utiliza para resolver las ambigüedades que podrían surgir cuando hay dos o más elementos iguales.

    La declaración de un espacio de nombres se realiza con el atributo xmlnes seguido por el nombre y una URL.
```XML
<?xml version="1.0" encoding="utf-8" ?>
<root xmlns:e="https://example.com/e/">
    <!--Comment-->
    <e:element1>text</e:element1>
    <e:element2>text2</e:element>
</root>
```
* ### Entidades 
    Las entidades en XML, permiten incluir información predefinida en un documento.
    * Pueden ser definidas en el propio DTD o que sean externas.
    * Empiezan por & y finalizan por;
    * Se pueden clasificar por:
        - Generales (Forman parte del documento)
            - Internas (Son predefinidas y mantienen su valor),
            - Externas (Mantienen los valores en un fichero externo).
        - Entidades de parametros (Se transforman en DTD). 
 Existen 5 entidades generales predefinidas internas.
            
 | Entidad |   Descripción  | Carácter |
|:-------:|:--------------:|:--------:|
| &li;    | Menor que      |        < |
| &gt;    | Mayor que      |        > |
| &amp;   | Ampersand      |        & |
| &apos;  | Comilla simple |        ' |
| &quot;  | Comilla doble  |        " |

* ### CDATA
    En XML, una sección CDATA es un conjuto de caracteristicas que no debe ser tratado por el analizador, pero si formará parte de la información (a diferencia de un comentario).
    * Comienza por ```<![CDATA[.```
    * ```Acaba con ]]>```

Ejemplo de CDATA:
```XML
<?XML version="1.0" encoding="utf-8" ?>
<root xmlns:e="https://example.com/e/">
    <!--Comment-->
    <e:element1>text</e:element1>
    <e:element2><![CDATA[
        <html>
            <head>
            </head>
            <body>
                <h1>Encabezado </h1>
            </body>
        </html>
        ]]>
    </e:element2>
</root>
```

## Validación de documentos
Un documento está validado, si además de estar bien formado, si está escrito conforme a las reglas definidas en su DTD o conforme un XML Schema.

* [DTD](DTD.md)
* [XML Schema](XMLSch.md)

## Enlaces de interés 
* [Enlace a W3C](https://www.w3.org/) 
* [Enlace a W3C school](https://www.w3schools.com/) 


