# ¿Que es un DTD?
DTD (Document type Definition), es una serie de reglas que van a permitir validar que la estructura de un documento es válida.
Las reglas de un DTD tienen que ver con la estructura del documento, aunque cuenta con algunas limitaciones que se pueden suplir usando XML Schema.
Un DTD puede ser:
 * Interno: Que esta definido en el propio documento.
 * Externo: Que esta definido en un fichero externo.

DTD Interno:
  ```XML
  <!DOCTYPE elementoRaiz[
    resto de componentes
  ]>
  ```
DTD Externo:
  ```XML
  <!DOCTYPE nombreElemento SYSTEM "Uri">
```
Donde _URI_ es un identificador de fichero o una URL.
Dentro de un DTD, se pueden definir las siguientes reglas:
* Entidades.
* Anotaciones.
* Elementos.
* Atributos.  

## Entidades
Las entidades permiten utilizar un valor fijo cuando se utiliza esta unidad.

Las entidades pueden ser:
* Internas. Estan dentro del propio DTD.
* Externas. Se definen en un fichero externo, pueden ser:
    * Pública.
    * Privada.

**Internas**:
```XML
<!ENTITY nombreEntidad "Valor">
```
**Externas**:

_Pública_:
```XML
<!ENTITY nombreEntidad PUBLIC "id_publico" "URI">
```
_Privada_:
```XML
<!ENTITY nombreEntidad SYSTEM "URI">
```

No hay que olvidar que para usar una entidad se utiliza el caracter & seguido de su nombre y acabado en **;** .

``` &nombreEntidad;```

## Anotaciones
Una anotación es un componente que define un formato de un valor, concretamente que no se utilizaran como una entidad XML, como es el caso del valor de un atributo.

Las anotaciones pueden ser Pirvadas o Públicas.

* Anotación Privadas

```XML 
<!NOTATION nombre SYSTEM "URI">
```
* Anotación Pública
```XML
<!NOTATION nombre PUBLIC "id_publico">
<!NOTATION nombre PUBLIC "Id_publico" "URI">
```
## Elementos 
Un elemento en DTD, define la estructura de uno a varios elementos que contienen el elemento

Para definirlo usamos:

```XML
<!ELEMENT nombreElemento (contenido)>
```
El contenido puede ser:
* EMPTY: Vacío.
* ANY: Cualquier valor.
* (#PCDATA): Elemento de tipo carácter.
* (NombreElemento): Elemento Hijo.
* (NombreElemento1, NombreElemento2,...): Lista de elementos hijos

Es importante conocer que se puede indicar una cardinalidad, a la hora ver cuantas veces puede repetirse un elemento, en la siguiente tabla veremos las maneras para indicarlo:

| Notación                             | Descripción                                     | Ejemplo                            |
|--------------------------------------|-------------------------------------------------|------------------------------------|
| (Elemento)                           | Una única ocurrencia                            | ```<!ELEMENT aviso (Mensaje)>```         |
| (Elemento+)                          | Una o más repeticiones                          | ```<!ELEMENT aviso (Mensaje+)>```        |
| (Elemento*)                          | 0 o más repeticiones                            | ```<!ELEMENT aviso (Mensaje*)>```        |
| (Elemento1, Elemento2, Elemento3...) | Deben aparecer todos los elementos de la lista  | ```<!ELEMENT aviso (de,para,Mensaje)>``` |
| (Elemento1\|Elemento2...)            | Debe contener uno o otro                        | ```<!ELEMENT aviso(de\|para,Mensaje)>``` |

## Atributos
Para definir atributos en DTD usáremos la siguiente sintaxis:
```XML
<!ATTLIST nombreElemento nombreAtributo tipoAtributo "valorAtributo">
```
* Pueden comenzar por guion bajo o por un carácter, además su nombre no pueden **contener espacios**.
* Deben tener un valor, que puede ir entre comillas ya sean dobles o simples; pero se recomienda el uso de dobles.
* Pueden ser opcionales, siempre deben de estar dentro de un elemento.
* Siempre deben aparecer en la etiquera de apertura de un elemento; nunca en la de cierre.

Ejemplo de Atributos:

```XML
<books>
  <book isbn="11111111">
    <title>Desarrollo Homebrew para 16 bits</title>
    <author>V. Suarez Garcia</author>
  </book>
</books>  
```
## Ejemplo de DTD
```XML
<?XML version="1.0" encoding="utf-8" ?>
<!DOCTYPE books[
  <!ELEMENT book(title,author,year)>
  <!ATTLIST book isbn ID #REQUIRED>
  <!ELEMENT title(#PCDATA)>
  <!ELEMENT author(#PCDATA)>
  <!ELEMENT year(#PCDATA)>
]>

<books>
  <book isbn="1111111">
    <title>Desarrollo Hombrew para 16 bits</title>
    <author>V.Suarez Garcia</author>
    <year>2023</year>
  </book>

</books>
```