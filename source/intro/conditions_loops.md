# Condiciones y bucles

Para dominar con éxito el material sobre cifrado, es necesario conocer los conceptos básicos del trabajo con condiciones y bucles. Las condiciones y los bucles son los principales mecanismos que permiten a los programas informáticos tomar decisiones y repetir determinadas acciones. Gracias a las condiciones, un programa puede reaccionar de forma diferente según los datos que recibe, mientras que los bucles permiten repetir los mismos pasos varias veces de manera eficiente. Estos conceptos son de vital importancia en el cifrado, ya que los algoritmos de protección de datos se basan en una serie de reglas, comprobaciones y procedimientos repetitivos que garantizan la seguridad de la información.


## Condiciones

En la mayoría de los lenguajes de programación modernos, las instrucciones condicionales se utilizan para tomar decisiones y controlar el flujo del programa. Las estructuras más habituales son:

* if
* if-else
* switch-case

Aunque la sintaxis varía de un lenguaje a otro, la lógica básica es la misma.

### Instrucción `if`

La instrucción `if` ejecuta un bloque de código únicamente si se cumple la condición indicada (es decir, si es verdadera).

```text
if condition then
    statement(s)
```

Por ejemplo, en C, C++, C# y Java, si queremos comprobar si x es mayor que 0, la instrucción condicional se puede escribir de la siguiente manera:

```csharp
int x = 5;
if (x > 0) {
    // ...
}
```

### Instrucción `if-else`

La instrucción `if-else` ejecuta un bloque de código si se cumple la condición y otro bloque si no se cumple.

```text
if condition then
    statement(s)
else
    statement(s)
```

Por ejemplo, en C, C++, C# y Java, si queremos comprobar si x es mayor que 0 o no, la instrucción condicional se puede escribir así:

```csharp
int x = 5;
if (x > 0) {
    // ...
} else {
    // ...
}
```

### Instrucción `switch-case`

La instrucción `switch-case` resulta útil cuando una misma variable se compara con varios valores posibles. Esta estructura puede ser más clara que utilizar varias instrucciones  `if-else`.

```text
switch expression do
    case value1:
        statement(s)
    case value2:
        statement(s)
    ...
    default:
        statement(s)
```

Por ejemplo, en C, C++, C# y Java, si queremos determinar el nombre de un día de la semana a partir de su número, la instrucción condicional se puede escribir así:

```csharp
int day = 3;
string name = "";
switch (day) {
    case 1:
        name = "Monday";
        break;
    case 2:
        name = "Tuesday";
        break;
    case 3:
        name = "Wednesday";
        break;
    // ...
    default:
        name = "";
        break;
}
```

### Anidamiento de condiciones

Las instrucciones condicionales pueden colocarse unas dentro de otras. Esto se conoce como **anidamiento**. Las condiciones anidadas son útiles cuando una decisión depende del resultado de una decisión anterior. Por ejemplo, primero podemos comprobar si un usuario ha iniciado sesión y, después, dentro de ese bloque, comprobar si tiene permiso para realizar una determinada acción.


## Bucles

En la mayoría de los lenguajes de programación modernos, los bucles suelen implementarse mediante alguna de las siguientes estructuras:

* `for`,
* `while` (o `while-do`),
* `do-while` (o `repeat-until`),
* `foreach` (o `for-each`).

Aunque la sintaxis varía de un lenguaje a otro, la lógica básica es la misma.

### Bucle `for`

La instrucción `for` se utiliza cuando el número de repeticiones es limitado y se conoce de antemano.

```text
for variable ← start to end do
    statement(s)
```

Por ejemplo, en C, C++, C# y Java, un bucle for para recorrer los números del 0 al 9 se puede escribir así:

```csharp
for (int i = 0; i <= 9; i++) {
    // ...
}
```

### Bucle `while`

La instrucción `while` (o `while-do`) se utiliza cuando no se conoce de antemano el número de repeticiones. La condición se comprueba antes de cada iteración, por lo que este bucle se denomina **bucle con condición previa**.

```text
while condition do
    statement(s)
```

Por ejemplo, en C, C++, C# y Java, un bucle while para recorrer los números del 0 al 9 se puede escribir así:

```csharp
int i = 0;
while (i <= 9) {
    // ...
    i++;
}
```

### Bucle `do-while`

La instrucción `do-while` (o `repeat-until`) también permite realizar un número desconocido de repeticiones, pero la condición se comprueba después de cada iteración. Se trata de un **bucle con condición posterior**, que siempre se ejecuta al menos una vez.

```text
repeat
    statement(s)
until condition
```

Por ejemplo, en C, C++, C# y Java, un bucle do-while para recorrer los números del 0 al 9 se puede escribir así:

```csharp
int i = 0;
do {
    // ...
    i++;
} while (i <= 9);
```

### Bucle `foreach`

La instrucción `foreach` (o `for-each`) se utiliza para recorrer todos los elementos de una colección o de un array. Este bucle simplifica la iteración cuando no necesitamos conocer el índice de cada elemento.

```text
for-each element in collection do
    statement(s)
```

Por ejemplo, un bucle for-each para recorrer un array llamado nums se puede escribir en C++ de la siguiente manera:

```cpp
int nums[] = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
for (int i : nums) {
    // ...
}
```

...o en C#:

```csharp
int[] nums = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
foreach (int i in nums) {
    // ...
}
```

...o en Java:

```java
int[] nums = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
for (int i : nums) {
    // ...
}
```

### Anidamiento de bucles

Los bucles también pueden anidarse, es decir, un bucle puede encontrarse dentro de otro. Esto ocurre con frecuencia cuando se trabaja con datos multidimensionales, como al recorrer las filas y columnas de una matriz o al iterar sobre una cuadrícula en un videojuego. Además, los bucles y las condiciones se pueden combinar libremente. Por ejemplo, un bucle puede contener una instrucción if para procesar únicamente determinados elementos, o una instrucción if puede contener un bucle para repetir ciertas acciones cuando se cumple la condición. Esta posibilidad de combinar y anidar bucles y condiciones permite crear algoritmos complejos manteniendo una lógica clara.


¡Necesitarás distintos tipos de bucles para los diferentes métodos de cifrado que aprenderás en las próximas páginas!
