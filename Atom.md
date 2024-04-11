# ATOM
## ¿Qué es Atom?
Atom es otro formato de sindicación de contenidos basado en XML. Los ficheros Atom suelen tener extensión .xml o .atom.
## Sintaxis de Atom 
### El elemento raíz ```<feed>``` 
que se le indica el espacio de nombres *xmlns=http://www.w3.org/2005/Atom*
 | Elemento |   Descripción  |
|:-------:|:--------------:|
| ```<id>```    | Identifica el canal utilizando una URI      |
|```<title>```     |Título del canal|
|```<updated>```   |Fecha de la última actualización |
|```<author>```  | Indica el autor, contiene la etiqueta ```<name>``` y opcionalmente ```<email>``` y ```<uri>``` |
|```<link>```  | Enlace mediante el atributo *href* al canal  |

En el  elemento feed puede contener los siguientes elementos opcionales.

 | Elemento |   Descripción  |
|:-------:|:--------------:|
| ```<category>```    | Categoría del canal, puede tener múltiples elementos.    |
|```<contributor>```     |Nombre o nombres del colaborador; contiene las etiquetas ```<name>``` y opcionalmente ```<email>``` o ```<uri>```|
|```<generator>```   |Programa que ha generado este feed. |
|```<rights>```  | Contiene información acerca de los derechos de propiedad del canal.|
|```<subtitle>```  | Contiene la disposición final.  |


Dentro del propio Feed, pueden aparecer una o varias entradas, estas se identifican por 
### El elemento *```<entry>```* 
en el que pueden aparecer los siguientes elementos:

 | Elemento |   Descripción  |
|:-------:|:--------------:|
| ```<id>```    | Identificador de la entrada debe ser una URI.    |
|```<title>```     |Título de la entrada|
|```<update>```   |Fecha de actualización. |
|```<content>```  | Descripción del contenido.|
|```<author>```  | Autor de la entrada, debe contener el elemento ```<name>``` y opcionalmente los elementos ```<email>``` o ```<URI>``` |
|```<link>```  | Enlace a la entrada con el atriburo  *href* |
|```<summary>```  | Resumen de la entrada.  |

### Elementos de entry II:

| Elemento |   Descripción  |
|:-------:|:--------------:|
| ```<category>```    | Categoría de la entrada    |
|```<contributor>```     |Colaborador de la entrada, debe contener el elemento ```<name>``` y opcionalmente los elementos ```<email>``` o ```<URI>```|
|```<published>```   |Fecha de publicación. |
|```<rights>```  | Información acerca de la propiedad o los derechos de la entrada.|

## Ejemplo de Atom
```XML
<?xml version="1.0" encoding="utf-8"?>

<feed xmlns="http://www.w3org/2005/Atom">

    <title>Example Feed</title>
    <subtitle>A subtitle.</subtitle>
    <link href="http://example.org/feed/" rel="self"/>
    <link href="http://example.org" />
    <id> urn:uuid:60a76c80-d399-11d9-b91C-0003939e0af6</id>
    <updated>2003-12-13T18:30:02Z</updated>

    <entry>
        <title>Atom-Powered Robots Run Amok</title>
        <link href="http://example.org/2003/12/13atom03"/>
        <link rel="alternate" type="text/html" href="http://example.org/2003/12/13/atom03/edit"/>
        <link rel="edit" href="http://example.org/2003/12/13/atom03/edit"/>
        <id>urn:uuid:1225c695-cfb8-4ebb-aaaa-80da344efa6a</id>
        <published>2003-11-09T17:23:02Z</published>
        <updated>2003-12-13T18:30:02Z</updated>
        <summary>Some text.</summary>
        <content type="xhtml">
            <div xmlns="http://wwww.w3.org/1999/xhtml">
                <p>This is the entry content.</p>
            </div>
        </content>
        <author>
            <name>John Doe</name>
            <email>johndoe@example.com</email>
        </author>
    </entry>
</feed>
```