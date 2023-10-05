# XML
## Características de XML
Las características principales de XML son:
* Permite crear etiquetas (creando en sí lengujaes de marcas).
* Permite utilizar esquemas (usando espacios de nombres), para poder validar la estructura del mismo, usando los llamados DtD
* En un documento XML, estructura y diseño estan separados.
* Se almacena en formato Texto (no binario).
* Permite ser utilizado desde HTMI v4.0.
* Permite intercambiar información entre sistemas de información.
* Permite guardar información en distintas codificaciones.
### Ejemplo de XML 
``` XML
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<root>
    <client dni="77997725H">
        <name>pepe</name>
        <lastname>Pérez</lastname>  
    </client>
    <products>
        <product startdate="05-10-2023" finaldate="09-10-2023">
            <name>Producto 1</name>
        </product>
        <procuct startdate="25-12-2023" finaldate="22-01-2024">
            <name>producto 2</name>
        </product>
    </products>
</root>
```