# ¿Qué es Pyhton?
Python es un lenguaje de programación que permite realizar aplicaciones web, el desarrollo de software, la ciencia de datos y el machine learning. 
Los desarrolladores utilizan Python lo utilizan porque es eficiente y fácil de aprender.
## Variables
Las variables son contenedores para almacenar valores de datos.

Python como tal no tienen nigun comando para crear variables por lo que se crea en el momento en que se le asigna un valor por primera vez.
Las variables no necesitan ser declaradas con ningún tipo en particular, e incluso pueden cambiar de tipo después de haber sido establecidas

**EJEMPLO**
```Python
x = 5
y = "John"
print(x)
print(y)
```
## Tipos de datos
En python los tipos de datos estan integrados de forma predeterminado, alguno de ellos son:

* Tipo de texto: ```str```.
* Tipos numéricos: ```int```,```float```,```complex```.
* Tipos de secuencia: ```list```,```tuple```,```range```.
* Tipo de mapeo: ```dict```.
* Tipos de conjuntos: ```set```,```frozenset```.
* Tipo booleano: ```bool```.
* Tipos binarios: ```bytes```,```bytearray```,```memoryview```.
* Ningun tipo: ```NoneType```.
## Estructura de control
Normalmente es necesario  poder decidir la acción a realizar o repetir una serie de acciones por lo que se utilizan *instrucciones de control*.
Hay dos tipos:
* Instrucciones de control condicional.
* Instrucciones de control repetitivas.
### Instrucciones de Control Condicional
Las instruccions de condicionales son 3:
* **if** --> Comprueba una condicion y realiza una serie de acciones.
* **if-else** --> Comprueba una condición y realiza una serie de acciones u otras en caso de no cumplirse.
* **if-elif-else** --> Comprueba una serie de condiciones y reliza las acciones que contemplen dichas condiciones.

**Ejemplo de condicionales:**
```Python
#Ejemplo If
if a > 1:
    a=a+1
#Ejemplo If-else
if a > 1:
    a=a+1
else:
    a=a-1
#Ejemplo If-elif-else
if a == 1:
    a=a+1
elif a==1:
    a=a+2
else:
    a=a-1
```

### Instrucciones de Control Repetitivo
Instrucciones que permiten repetir acciones a partir de una o varias condiciones.

Existen 2 instrucciones de control repetivas o *bucles*:
* **Mientras** --> El bucle Mientras (**while**),permite ejecutar repetidamente unas instrucciones mientras ocurra una condición.
* **For** --> El bucle for, permite repetir una serie de acciones a partir de un contador o mientras se recorre una lista.

**Ejemplo de Bucles:**
```Python
#Ejemplo Mientras

while a>1:
    a=a-1
#Ejemplo for

for i in range(1,10):
    a=a+i
```

## Listas 
Las listas se utilizan para almacenar varios elementos en una sola variable.

En Python podemos crear una lista vacia.
```python
Lista = []
```
O con datos..
```python
Lista = [2, 3, 4, 5]
```
Para acceder a un dato de la lista usaremos un idice comenzando por 0.
```python
Lista [0]
1
Lista[2]
4
```
Para recorrer una lista podemos usar el bucle for.
```python
for n in lista:
    print(n)
1
2
3
4
5
```
operadores con listas.
```Python
Lista[:2]
[1,2,3]

Lista[1:3]
[2,3]

Lista2 = [7,8]

Lista+Lista2

[1,2,3,4,5,6,7,8]
```

## Tuplas
Las tuplas se comportan de igualmanera que las listas, excepto que estas son inmutables, es decir que no se pueden modificar.
```Python
Tupla = (1,2,3,4)

Tupla[0]
1
Tupla[:2]
(1,2)
Tupla[1:3]
(2,3)
```