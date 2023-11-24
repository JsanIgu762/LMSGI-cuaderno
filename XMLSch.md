# ¿Que es XMLSchema?
Es una serie de reglas para definir la estructura y las restricciones de un documento XML, atraves de un fichero XSD (XML Schema Definition).
## ¿Cuales son sus funcionalidades?
* Permite determinar qué elementos y atributos admiten un XML.
* Permite determinar los tipo de datos que contiene tanto elementos como atributos.
* Permite asignar valores por defecto.
* Permite determinar cardinalidades más precisas, orden de los elementos u opcionalidad.
* XMLSchema esta escrito en XML a diferencia de DTD.

## **Ejemplo de XMLSchema**

Primero necesitamos un documento XML a validar.

```XML
<?xml version="1.0" encoding="UTF-8"?>
<mensaje xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation="mensaje.xsd">
    <de>Anna</de>
    <para>Rocio</para>
    <mensaje>Llego en 5 minutos</mensaje>
</mensaje>
```
Dentro del ficher "*mensaje.xsd*" encontraremos la definicion en XMLSchema como validación.

¿Como sería la validación para el documento anterior?

```XML
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="mensaje">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="de" type="xs:string"/>
                <xs:element name="para" type="xs:string"/>
                <xs:element name="mensaje" type="xs:string"/>
            </xs:sequence>
        </xs:complexType>
    </xs:element>
</xs:schema>
```
## Enlazar XSD
```XML
<mensaje xmlns:xs="http://www.w3.org/2001/XMLSchema-instance"
    xs:noNamespaceSchemaLocation="mensaje.xsd">
```
Se debe de enlazar el espacio de nombre "xs"; y establecer un esquema por defecto "NoNamespaceSchemaLocation".

El esquema puede estar en local, o utilizando una URL.

## Crear XSD

```XML
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
```
Dentro de este fichero, ya se declararán los distintos elementos y atributos necesarios. Los elementos pueden ser:

* **Locales**: hijos de elementos que no son el elemento raíz y solo se usan una vez.
* **Globales**: son hijos del elemento raíz y pueden ser reutilizados.

## Elementos
Para declarar un elemento en XML SChema se usa la siguiente sintaxis
```XML
<xs:element name="" type="" default="" fixed="" minOccurs="0" maxOccurs="0"/>
```
Donde:
* name: Nombre del elemento.
* *type*: Tipo de dato. Se establece si el elemento es de tipo Simple.
* *default*: Valor por defecto
* minOccurs: Número de veces mínima que puede aparecer. Por defecto 1.
* maxOccurs: Número de veces máxima que puede aparecer. Por defecto 1.

Si un elemento puede aparecer un número indeterminado se establece el valor "unbounded".

Un elemento puede ser dependiendo de su tipo, de dos formas:
* **Simple**: Guarda un texto, número, fecha, etc... Se debe establecer el atributo type o utilizar una restricción.
* **Complejo**: Guarda dentro elementos hijos y se pueden establecer restricciones a las relaciones.

### SimpleType
Ejemplo Elemento Simple
```XML
<xs:element name="fecha" type="xs:date"/>
```
Ejemplo Elemento Simple con restricción 

```XML
<xs:element name="diaSemana">
    <xs:simpleType>
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="1"/>
            <xs:MaxInculsive value="7"/>
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

### ComplexType
Ejemplo Elemento Complejo
```XML
<xs:element name="mensaje">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="para" type="xs:string"/>
        </xs:sequence>
    </xs:complexType>
</xs:element> 
```
Dentro de un tipo complejo se establece:
* SubElementos.
* atributos.

Un subelemento, establece la relación de los elementos contenidos con respecto al padre.

Puede ser:
* *xs:sequence*: Indica una secuencia de elementos obligatorios, y en el mismo orden.
* *xs:choise*: Señala una secuencia de elementos alternativos.
* *xs:all*: Indica una secuencia de elementos opcionales; no es obligatorio que aparezcan todos en el mismo orden.

### Atributos
Se pueden guardar atributos tanto en un elemento complejo como simple.
```XML
<xs:attribute name="" type=""/>
```
Un atributo tiene los siguientes valores:
* name: Nombre del atributo.
* type: Tipo de dato.
* use: indica su obligatoriedad; tiene los siguientes valores:
    * required: es obligatorio.
    * optional: es opcional.
    * prohibited: no se puede utilizar en dicho elemento.
* default: Permite asignar un valor por defecto.
* fixed: Determina el valor del atributo en caso de que exista.

### Restriciones
Se pueden establecer restricciones a elementos y atributos. Su sintaxis es:
```XML 
<xs:restricition base="xs:integer">
....
</xs:restriction>
```
|       Faceta      |               Descripción               |
|:-----------------:|:---------------------------------------:|
| xs:length         | Longitud Fija                           |
| xs:minLength      | Longitud mínima                         |
| xs:maxLength      | Longitud Máxima                         |
| xs:totalDigits    | Total dígitos de un número.             |
| xs:fractionDigits | Total dígitos decimales de un número.   |
| xs:minExclusive   | Indica el valor mínimo que puede tomar. |
| xs:maxExclusive   | Indica el valor máximo que puede tomar. |

|      Faceta     |                  Descripción                  |
|:---------------:|:---------------------------------------------:|
| xs:minInclusive | Indica el valor debe ser mayor o igual        |
| xs:maxInclusive | Indica el valor debe ser menor o igual        |
| xs:enumeration  | Lista de valores posibles(string)             |
| xs:whiteSpace   | Determina cómo tratar los espacios en blanco. |
| xs:pattern      | Fija un patrón de caracteres permitidos.      |

### Tipos de Datos básicos

|     Tipo    |                         Descripción                         |
|:-----------:|:-----------------------------------------------------------:|
| xs:string   | cadena de caracteres.                                       |
| xs:integer  | Número enteros.                                             |
| xs:decima   | Número decimales; usando "." como separador.                |
| xs:boolean  | Booleano. "true" para verdadero y "false" para lo contrario |
| xs:date     | Fecha con formato AAAA-MM-DD                                |
| xs:time     | hora con formato hh:mm:ss                                   |
| xs:duration | duración de tiempo en formato "PnYNMbDTnHnMNS".             |

### Comentarios 
Se pueden establecer comentarios dentro de XMLSchema para ayudar a enterderlo.
<xs:element name="mensaje">
<xs:annotation>
    <xs:appInfo>Información de mensaje</xs:appInfo>
    <xs:documentation xml:lang="es">
        mensaje a enviar    
    </xs:documentation>
</xs:annotation>
Donde:
* appInfo: información del elemento o atributo.
* documentation: documentación en detalle del elemento o atributo.