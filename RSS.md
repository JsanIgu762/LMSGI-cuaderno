# RSS
![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/43/Feed-icon.svg/1200px-Feed-icon.svg.png)
## ¿Que es RSS?
Es un dialecto XML, que permite distribuir contenidos a través de la web,
Está mantenido por la W3C.

Normalmente se utilizan ficheros con extensión .rss o .xml.
## Sintaxis de RSS
* El elemento raíz siempre será ```<rss>``` que tendrá el atributo version con el valor 2.0
* Este elemento tendrá un subelemento llamado ```<channel>``` por cada canal de suscripción que tenga la web.

En los elementos channel, tendremos los siguientes elementos obligatorios.

 | Entidad |   Descripción  |
|:-------:|:--------------:|
| ```<title>```    | Título del canal      |
|```<link>```     | Enlace al sitio web|
|```<description>```   |Descripción del contenido     |
|```<language>```  | Idioma en el que está escrito el canal |
|```<copyright>```  | Aviso relativo a los derecgis de autor  |
|```<category>```  | Una o más categorias a la que pertenece el canal.  |
|```<generator>```  | Nombre del programa que ha generado el canal  |

Además de estos elementos, podemos encontrar una o más entradas definidas con el elemento ```<item>```. Cada elemento contiene:
 | Entidad |   Descripción  |
|:-------:|:--------------:|
| ```<title>```    | Título del canal      |
|```<link>```     | Enlace al sitio web|
|```<description>```   |Descripción del contenido     |
|```<pubDate>```  | Fecha de publicación en formato RFC-822 |
|```<comments>```  | Contiene la URL con los comentarios de la entrada  |
|```<author>```  | Dirección electrónica (email) del autor.  |


## Ejemplo de RSS
```XML
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">

<channel>
    <title>W3Schools Home Page</title>
    <link>htpps://www.w3schools.com</link>
    <description>Free web building tutorials</description>
    <item>
        <title>RSS Tutorial</title>
        <link>https://www.w3schools.com/xml/xml_rss.asp</link>
        <description>New RSS tutorial on W3Schools</description>
    </item>
</channel>

</rss>
```