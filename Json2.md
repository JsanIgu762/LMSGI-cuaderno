# ¿Qué es Json?
Durante el cuso ya hemos visto lo que es el lenguaje de marcas JSON, Sin embarga también se puede utilizar fuera de su uso como lenguaje de marcas como tal, la comunidad ha extendido su uso en infinidad de casos.
## Sintaxis 
JSON, tiene una sintaxis basada en etiquetas clave: valor, separadas comas y componiendo diferentes objetos dentro de las etiquetas {  }.

Es decir, que se comienza siempre con { Seguido de uno o varios elementos separados por ,.

Cada elemento, se define como un par clave-valor, separado por : la primera es la clave que va entre comillas " " y la segunda parte es el valor.

Ejemplo:
```JSON
"nombre":"Juanmi"
```
Cada elemento, puede tener 1 valor simple, una lista o un objeto.

* Un valor simple, es un objeto con un válor unico.
* Una lista, es uno o varios objetos dentro de las etiquetas [ ].
* Un objeto, es uno o varios elementos dentro de las etiquetas { }.

## Tipos de datos
Un valor simple, tiene asociado un tipo, que puede ser:
 * Numeros: Indica un numero que puede ser entero o decimal.
 * Cadenas: Una cadena de caracteres encerrada entre " ".
 * Booleanos: Sólo pueden tener el valor true o false.
 * null: Indica un valor nulo o vácio.
Ejemplos de tipos de datos:
 * Numérico: ```"age":30```
 * Cadena:```"name":"John"```
 * Booleano: ```"sale":true```
 * null: ```"middlename":null```
## Objetos Compuestos
Un objeto en JSON, es un conjunto de subelementos que componen en sí un elemento.
Por así decirlo, son elementos compuestos.

Se definen dentro de las etiqueras {  }.

```JSON
{"firstName":"Juan", "lastName":"Connor"}
```

## Listas 
Una lista, o array es un conjunto de elementos que tienen una posición u índice. 
Se define dentro de los elementos [] y cada elemento está separado por comas.

```JSON
"employees":[
    {"firstName":"Reed", "lastName":"Richard"},
    {"firstName":"Scott", "lastName":"Summer"},
    {"firstName":"Peter", "lastName":"Parker"}
]
```

### Ejemplo JSON
```JSON
{
    "Localizaciónes turisticas": [
        {
            "Nombre": "Alcazaba",
            "Descripción": "Monumento historico de Almería",
            "Latitud": 36.841286,
            "Longitud": -2.4723476,
            "Palabra clave":["Pescata","Alcazaba","Monumento"]
        },
        {
            "Nombre":"Pescaderia",
            "Descripción":"Barrio de gente",
            "Latitud": 36.21212,
            "Longitud": -1.23232,
            "Palabra clave":["Pescaderia","Barrio","Almería"]

        }
    ]
}
```