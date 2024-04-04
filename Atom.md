# ATOM
## ¿Qué es Atom?
Atom es otro formato de sindicación de contenidos basado en XML. Los ficheros Atom suelen tener extensión .xml o .atom.
## Sintaxis de Atom 
El elemento raíz ```<feed>``` que se le indica el espacio de nombres xmlns=http://www.w3.org/2005/Atom
 | Entidad |   Descripción  |
|:-------:|:--------------:|
| ```<id>```    | Identifica el canal utilizando una URI      |
|```<title>```     |Título del canl|
|```<updated>```   |Fecha de la última actualización |
|```<author>```  | Indica el autor, contiene la etiqueta ```<name>``` y opcionalmente ```<email>``` y ```<uri>``` |
|```<link>```  | Enlace mediante el atributo *href* al canal  |
