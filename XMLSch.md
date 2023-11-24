# ¿Que es XMLSchema?
Es una serie de reglas para definir la estructura y las restricciones de un documento XML, atraves de un fichero XSD (XML Schema Definition).
## ¿Cuales son sus funcionalidades?
* Permite determinar qué elementos y atributos admiten un XML.
* Permite determinar los tipo de datos que contiene tanto elementos como atributos.
* Permite asignar valores por defecto.
* Permite determinar cardinalidades más precisas, orden de los elementos u opcionalidad.
* XMLSchema esta escrito en XML a diferencia de DTD.

### **Ejemplo de XMLSchema**

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
Enlazar