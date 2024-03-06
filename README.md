# Cuaderno lenguaje de marcas
## Tabla de contenidos
* ### [¿Qué es un lenguaje de marcas?](#qué-es-un-lenguaje-de-marcas-1) 
* ### [Evolución de los lenguajes de marcas](#evolución-de-los-lenguajes-de-marcas-1)
* ### [Características de los lenguajes de marcas](#características-de-los-lenguajes-de-marcas-1)
* ### [Ejemplos y características de diferentes lenguajes de marcas](#ejemplos-y-características-de-diferentes-lenguajes-de-marcas-1)
* ### [XML: definición y caracteristicas del metalenguaje](#xml-definición-y-caracteristicas-del-metalenguaje-1)
* ### [Documento XML](#documento-xml-parte-del-tema-2)
* ### [Sistemas de Gestión de Información](#sistemas-de-gestión-de-información-1)

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
    * Acaba con ``` ]]>```

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

## Sistemas de Gestión de Información
Un sistema de gestión de infotmación, son esos programas informáticos, diseñados para dar soporte a cualquier de los procesos que se realizan en una empresa.
Esto permite poder mejorar sus procesos y obtener un mayor beneficio en su actividad.


### En un sistema de gestión de Información existen:
* Sistema de gestíon de información local 
* Sistema de gestíon de información en la nube

### Hay distintos tipos de Sistemas de Gestión de Información:
* [ERP](ERP.md)
* [CRM](CRM.md)
* [BI (Busine Intelligence)](BI.md)

## HTML
### HTML y su evolución
HTML fe diseñado inicialmente en el año 1991 como parte del CERN, ha tenido varias versiones y diferentes implementaciones;

 | año |   Versión  | Observaciones |
|:-------:|:--------------:|:--------:|
| 1991    | Diseño inicial  |Incluye 18 etiquetas se considera dialecto SGML.|
| 1992    | HTML 1.1      |Primer Borrador|
| 1995   | HTML 2.0      |Recomendación W3C|
| 1997  | HTML 3.2 |Recomendación W3C|
| 1997  | HTML 4.0  |Recomendación W3C|
| 1999  | HTML 4.1  |Recomendación W3C|
| 2000    | XHTML     |Publicado como  recomendación del W3C. Tiene como objetivo sustituir a HTML pero se desarrolló el estándar HTML 5 por otro lado.|
| 2014   | HTML 5.0      |Recomendación W3C|
| 2016  | HTML 5.1 |Recomendación W3C|
| 2017  | HTML 5.2 |Recomendación W3C|
## XHTML
XHTML es un estándar que extiende HTML con las propias caracterísitcas del metalenguaje XML. Por ello, sigue las mismas reglas del mismo a diferencia de HTML.

Tiene una estructura similar al propio HTML pero con algunas diferencias:
* Las etiquetas deben estar bien anidadas.
* Todas las etiquetas deben estar cerradas.
* Todas las etiquetas y atibutos van en minúscula.
* No puede haber texto sin estar dentro de una etiqueta.
* Los scripts y estilos deben ir dentro de un CDATA.

# HTML
## Estructura de HTML 
Veamos la estructura de un documento HTML: 
```HTML
<!DOCTYPE html>
<html>
<head>
 <meta charset='utf-8'>
 <meta http-equiv='X-UA-Compatible'
content='IE=edge'>
 <title>Page Title</title>
 <meta name='viewport'
content='width=device-width,
initial-scale=1' >
 <link rel='stylesheet' type='text/css'
media='screen' href='main.css'>
 <script src='main.js'></script>
</head>
<body>

</body>
</html>
```
Podemos Observar:
* Doctype para validar el documento.
* Cabecera.
* Cuerpo.
* Etiquetas tanto de apertura como de cierre.

### Cabecera HTML
**Title**
Indica el título de la página; esto es importante para informar al usuario de que contenido tiene y visualizarlo en el navegador. Esta etiqueta es Opcional.
```HTML
<html>
    <head>
        <title> Mi página </title>
    <head>
</html>
```
**Meta 1**
* charset: Codificación del juego de caracteres. Por ejemplo UTF-8.
* http-equiv: Especifica una directiva. Lo veremos en la siguiente diapositiva.
* name: Nombre del metadato.
* content: Valor asociado a atributos como name y http-equiv; depende del nombra del atributo.
* Content-Type: Indica el tipo de contenido, y el juego de caracteres.
* Cache-control: Especifica cómo ha de gestionar el navegador la caché de la web.
* refresh: Indica al navegador que pasado un tiempo ha de refrescar la página.
* robots: Indica al nave


## Enlaces de interés 
* [Enlace a W3C](https://www.w3.org/) 
* [Enlace a W3C school](https://www.w3schools.com/) 

