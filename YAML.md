# YAML
## Características de YAML 
* Facil legibilidad.
* Tiene una estructura basada en sangría, los datos se definen mediante la cantidad de espacios utilizadas en la sangria.
* Tipos de datos simples, YAML admite cadenas, números, booleanos, fechas...
* Permite comentarios en el documento para añadir notas.
* No es un lenguaje de marcado.
* Es facilmente porteable.
### Ejemplo de YAML
``` YAML
definitions:
    person:
        properties:
            id:
                typer: string
                description: Identificador unico de la persona
            firstname:
                type: string
                description: Nombre
            lastName:
                type: string
                description: Apellidos
            age: 
                type: number
                format: Int32
                minimum: 0
            gender:
                type: string
                enum:
                    - Male
                    - Female
```
