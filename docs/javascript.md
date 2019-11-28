# JavaScript Relámpago :zap:

## ¿Qué es JavaScript? :alien:

JavaScript es un lenguaje de programación desarrollado para que sus programas sean ejecutados directamente en el navegador web. Por este motivo, este lenguaje se integra muy bien al lenguaje de marcado de documentos web [HTML](https://github.com/srsergiorodriguez/relampagos/blob/master/docs/html.md) y al formato de estilo [CSS](https://github.com/srsergiorodriguez/relampagos/blob/master/docs/css.md). Para información más detallada sobre el lenguaje [clic aquí](https://developer.mozilla.org/es/docs/Web/JavaScript).

## ¿Cómo funciona? :sunglasses:

### Añadir código a un documento HTML

Primero hay que añadir el código a un documento HTML para que pueda ser ejecutado. Eso se puede hacer de dos formas. La primera, poniendo el código de JavaScript dentro de etiquetas 'script':

```
<html>
  <head>
     <!–– Aquí van los metadatos ––>
     <script>
      <!–– Aquí va el código de JavaScript ––>
     </script>
  </head>
  <body>
    <!–– Aquí van los elementos visibles del documento ––>
  </body>
<html>
```

La segunda, poniendo el camino o enlace al código en el atributo 'src' de una etiqueta 'script':

`<script src="p5.min.js"></script>`

:exclamation: Los archivos de JavaScript tienen la extensión .js

:speak_no_evil: Este relámpago no incluye una explicación exhaustiva de los principios de la programación computacional, solo funciona como una hoja de recuerdo o *cheatsheet* para mantener fresca la memoria.

### Referencia relámpago de la sintaxis de JavaScript :zap:

#### Variables y tipos de datos

En Javascript se pueden **declarar** variables usando tres palabras clave diferentes: **'var'**, **'let'** y **'const'**. Tanto 'var' como 'let' sirven para crear variables que se pueden reasignar (aunque 'var' ha caído en desuso y ya no se recomienda usarla, pero no sobra saber que existe). Por otro lado, 'const' sirve para crear variables constantes, o sea, variables que no pueden variar, paradójicamente.
Para **asignar** valores a una variable se usa un igual '=' seguido por el valor. Se puede declarar y asignar al mismo tiempo.


```
let x; // declara la variable x
x = 10; // asigna el valor 10 a la variable x

const y = 3; // declara la constante y con el valor 3

let z = 30; // declara y asigna la variable z con el valor 30
z = 31; // reasigna a z el valor 31
```

:exclamation: Nota dos cosas:
* Al terminar la línea de declaración o asignación hay un punto y coma ';'.
* Para hacer comentarios se usa un *slash* doble '//'.

Los tipos de datos que se pueden declarar en Javascript son:

let num = 15; // números... tanto enteros como
let numf = 0.00001; // de punto flotante (decimales)
let str = "Hola" // strings o cadenas de caracteres
let boo = true // booleanos (true o false)
let nulo = null // nulos
let ind = undefined // indefinidios

##### Estructuras de datos

Se pueden crear, además, **arrays** (o listas ordenadas) y **objetos** (o estructuras de datos con clave-valor).

Para crear una array se declara su nombre y luego, entre llaves cuadradas '[]', se listan sus elementos separados por comas ','. Para leer alguno de los elementos o asignar un nuevo valor se pone el índice del elemento entre llaves cuadradas después del nombre de la array. 

```
// una array de números
let arr = [5, 10, 40, 3, 6];

let num0 == arr[0]; // el primer elemento de la array (el 5)
```

:exclamation: Los índices de las arrays empiezan por 0

Para crear una array se declara su nombre y luego, entre corchetes '{}', se describen sus elementos usando una clave seguida de dos puntos ':' y el valor. Cada par clave-valor se separa con comas ','. Para leer alguno de los elementos o asignar un nuevo valor se pone el nombre del objeto seguido de un punto '.' y luego la clave del elemento. También se puede poner la llave entre comillas '""' y luego entre llaves cuadradas después del nombre del objeto.

```
let gato = {
  nombre: "Kibo",
  edad: 3,
  negro: true
}

let nom = gato.nombre;
gato["ojos"] = "amarillos";
```

:exclamation: Los objetos sirven para describir estructuras de datos complejas y son la base del formato de intercambio JSON (JavaScript Object Notation)

#### Operaciones

En JavaScript se pueden hacer las operaciones típicas de cualquier lenguaje de programación

##### Aritméticas

Sumar, restar, multiplicar, dividir, módulo y otras...

```
let suma = 1 + 2;
let rest = 10 - 5;
let mult = 3 * 6;
let div = 9 / 3;
let modulo = 5 % 2;
```

:exclamation: también se pueden sumar strings, lo que da como resultado una concatenación de caracteres

`let str = "Hola " + "mundo"`



##### Asignación

Algunas versiones abreviadas de reasignación

```
let a = 5;
a += 2; // suma 2 al valor que ya tenía a
a++; // suma 1 al valor que ya tenía a
a -=1 // resta 1 al valor que ya tenía a
a *=2 // multiplica a por 2
a /= 5 // divide a en 5
```


##### Lógicas

Devuelven valores booleanos

```
let y = true && true; // operación 'Y' lógico
let o = false || true; // operación 'O' lógico
let no = !true; // negación
```

##### Comparadores

Devuelven valores booleanos

```
let a = 2 < 1; // menor que
let b = 3 > 4; // mayor que
let c = 2 == 5; // igual a
let d = 2 != 5; // diferente a
let e = 3 >= 8 // mayor o igual
let f = 5 <= 9 // menor o igual

let s = "gato" == "perro"; // igual a (con strings)
let p = "gato" != "perro"; // diferente a (con strings)

```

#### Condicionales

Para hacer condicionales se usan las palabras clave 'if', 'else if' y 'else'. If establece la primera condición, 'else if' las condiciones siguientes, y 'else' engloba el resto de posibilidades si no se cumple ninguna de las condiciones anteriores.
Las condiciones deben ponerse entre paréntesis '()' y el código que se ejecutará si se cumple la función debe ponerse entre corchetes '{}'.

```
let clima = "frío";

if (clima == "frío") {
  // haz algo
else if (clima == "cálido") {
  // haz otra cosa
} else {
  // haz otra cosa
}
```

#### Loops (o ciclos)

##### while-loop

Se cumple mientras la condición sea cierta. Se usa la palabra clave 'while' seguida de unos paréntesis que encierran la condición '()' y unos corchetes que encierran el código que se repetirá '{}'

```
let contador = 0;

while (contador < 10) {
  // haz algo diez veces
  contador++; // va sumando uno al contador
}
```

##### for-loop

Se cumple mientras la condición sea cierta. Pero tiene una sintaxis particular:
Primero se usa la palabra clave 'for', luego, entre paréntesis, se pone lo siguiente separado por puntos y comas ';': una declaración que sirve como contador del loop, una condición que debe ser cierta para que se repita el loop, una acción (normalmente sobre el contador).


```
for (let i = 0; i < 10; i++) {
  // haz algo diez veces
}
```

:exclamation: nota que este for-loop hace lo mismo que el while-loop anterior, pero tiene una sintaxis más comprimida

#### Funciones

Se crean usando la palabra clave 'function', luego se pone un nombre a la función, entre paréntesis '()' se ponen sus argumentos (o parámetros) y entre corchetes '{}' se pone el código que se ejecuta cuando se llama la functión. Si se quiere devolver algún valor se usa la palabra clave 'return'

```
function duplicar(num) {
  let duplicado = num * 2;
  return duplicado
}
```

Para llamar una función se usa el nombre seguido de unos paréntesis que contienen los argumentos:

`let nuevonum = duplicar(2);`

:exclamation: Cuando una función no tiene argumentos se dejan los paréntesis vacíos.

##### Sintaxis de flechita

La sintaxis de flechita es una versión reducida que sirve para crear funciones anónimas (funciones que solo se usarán una vez y que no requieren un nombre). Hay varias versiones de la sintaxis de flechita, cada una más reducida que la anterior. Sin embargo, siguen un formato común: argumentos o paréntesis vacíos seguidos de una flecha '=>' (signo igual y mayor que) seguidos por lo que debe retornar la función.

```
// formato flechita convencional
(x) => {
  return y

// formato sin argumentos
() => {
  return y
}

// formato que omite los paréntesis del argumento (cuando es solo uno)

x => {
  return y
}

// formato ultracomprimido (omite paréntesis, corchetes y palabra clave return)
x => y
```

#### Clases (por añadir)

...


#### Funciones útiles y comunes

Algunas funciones por defecto del legnuaje que se usan muy a menudo


```
console.log(valor) // imprime algún valor o string en la consola
console.table(array) // muestra una array anidada como una tabla en la consola

array.push(valor) // añade un elemento al final de una array
array.pop() // devuelve y saca de la array el último valor

Math.random() // devuelve un número al azar entre 0 y 1

Math.sin(valor) // devuelve el seno de algún valor (en radianes)
Math.cos(valor) // devuelve el cos de algún valor (en radianes)
Math.tan(valor) // devuelve el tangente de algún valor (en radianes)

array.map(x=>{return x*y}) // devuelve una array luego de haber aplicado la misma función a todos los elementos de la array original

```
