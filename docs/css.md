# CSS Relámpago :zap:

## ¿Qué es CSS? :alien:

CSS, *Cascading Style Sheets*, u Hojas de Estilo en Cascada es un lenguaje de diseño con el que se describen y ajustan las formas en las que se presenta un documento marcado. Podemos pensar que CSS permite hacer la maquetación o diagramación de un documento, porque sirve para definir de qué manera se verán sus secciones, sus bordes, sus colores, sus tamaños, sus interacciones, etc. En este relámpago nos fijaremos solamente en el uso de CSS para editar la presentación de documentos en HTML, que, justamente, es su uso más extendido. Para una referencia mucho más exhaustiva de CSS, [clic aquí](https://developer.mozilla.org/es/docs/Web/CSS).

## ¿Cómo funciona? :sunglasses:

### Añadir CSS a un documento HTML

Primero que todo, hay tres maneras de añadir estilo sobre los elementos de un documento HTML. La primera, aunque la menos recomendada, es asignar algún tipo de propiedad de estilo directamente en los atributos del elemento HTML.

`<p style="color: red">Esto es un párrafo rojo</p>`

:exclamation: ¿Lo de atributos de un elemento suena extraño? ¡Entonces remóntate al [relámpago sobre HTML](https://github.com/srsergiorodriguez/relampagos/blob/master/docs/html.md)!

Otra opción consiste en usar la etiqueta 'style' dentro de un documento HTML. Todo lo que se ponga dentro de la etiqueta se usará para dar estilo al documento.

```
<html>
  <head>
     <!–– Aquí van los metadatos ––>
     <style>
      <!–– Aquí va el CSS ––>
     </style>
  </head>
  <body>
    <!–– Aquí van los elementos visibles del documento ––>
  </body>
<html>
```

Por último, se puede crear un archivo independiente, con la extensión .css, que debe estar referenciado en el head del documento HTML, así:

`<link href="camino/a/hojadeestilos.css" rel="stylesheet" />`

Esta es la opción más sensata cuando se están aplicando muchos cambios en el estilo, o cuando se quieren trasladar esos cambios a otros documentos.

### Los selectores y el bloque de reglas

CSS utiliza **"reglas"** que se aplican sobre **"selectores"** para ajustar el estilo del documento. 

Los selectores referencian elementos del DOM sobre los que se aplicará cierto estilo y pueden ser de varios tipos: pueden ser un tipo de elemento general del DOM, pueden ser un conjunto de elementos del documento que tienen como atributo la misma clase (atributo 'class'), o puede ser un elemento del documento que tiene una identificación particular (atributo 'id'). 

Para referenciar un elemento del DOM simplemente se usa su nombre, para referenciar una clase se usa el nombre de la clase antecedido por un punto '.', y para referenciar una identificación se usa el nombre de la id antecedido por un numeral '#'. Luego se abren y cierran corchetes. Dentro de esos corchetes se pondrá el bloque de reglas.

```
/* esto selecciona todos los h1 */

h1 {
  /* aquí va el estilo de esos h1 */
}

/* esto selecciona todos elementos con la clase 'especial' */

.especial {
  /* aquí va el estilo */
}

/* esto selecciona el elemento con la identificación 'unico' */

#unico {
  /* aquí va el estilo */
}
```

:exclamation: Nota que para hacer comentarios en CSS se debe encerrar el texto entre  '/\*' y '\*/'

### Las propiedades de estilo

Dentro de los corchetes que van después de cada selector se pone el bloque de reglas para ese selector particular. Ese bloque es un conjunto de **"propiedades"** de estilo que describen cómo se verá el elemento o cómo se organizará en relación con la estructura del documento o de los otros elementos.
Las propiedades se describen usando el **nombre** de la propiedad, seguido por **dos puntos** ':', seguido por un **valor** y cerrado por un punto y coma ';':

```
selector {
  propiedad: valor;
}
```

:speak_no_evil: Hacer un recuento de todas las propiedades que pueden modificar el estilo de un documento tomaría mucho más tiempo y espacio que el que tenemos en este relámpago. CSS es todo un sistema de diseño, así que se requiere práctica y estudio para dominarlo. Sin embargo, aquí mencionaremos algunas propiedades básicas que se usan a menudo.

:pray: Ante la duda, busca en una referencia más completa cómo se usa alguna de las propiedades (por ejemplo, [esta](https://www.w3schools.com/css/css_intro.asp)). O busca en google la pregunta de estilo específica que tengas: cosas como "cómo cambio el color del borde de un título en css" siempre tienen respuesta en internet.

### :zap: Referencia relámpago de propiedades CSS

#### Propiedades de caja
Todos los elementos de un documento están encerrados en cajas, aunque no siempre sean visibles. Esta organización es la que permite que CSS funcione como un sistema de diagramación web. Aquí hay algunas propiedades que modifican las cualidades de las cajas que encierran a los elementos:

```
div {
  display: inline; /* modifica el tipo de caja */
  bakground-color: red; /* modifica el color de fondo de la caja */
  border: solid 1px; /* modifica el calibre y el color del borde de la caja */
  margin: 5px; /* modifica las márgenes exteriores de la caja */
  padding: 5px; /* modifica las márgenes interiores de la caja */
  width: 500px; /* modifica el ancho de la caja */
  height: 500px; /* modifica el alto de la caja */
}
```

:exclamation: el selector 'div' en este caso es solo un ejemplo, recuerda que estas reglas se pueden aplicar sobre otros tipos de elementos en el DOM, sobre clases o sobre elementos particulares con identificación.

#### Propiedades de texto
Aquí unos ejemplos de propiedades comunes que modifican un texto

```
.instrucciones {
  bakground-color: blue; /* modifica el color del texto */
  font-family: arial; /* modifica la fuente tipográfica */
  font-size: 10px; /* modifica el tamaño de la fuente */
  text-transform: capitalize; /* modifica las mayúsculas/minúsculas */
  font-weight: bold; /* modifica el calibre del texto */
  text-align: center; /* modifica la alineación del texto */
}
```
:exclamation: de nuevo, el selector de la clase 'instrucciones' es solo un ejemplo.

#### Pseudoclases
En CSS, las pseudoclases se refieren a estados especiales de algunos elementos cuando se interactúa con ellos. Por ejemplo, pasar el cursor sobre un texto, presionar un botón o ver un enlace ya visitado. Para modificar una pseudoclase, se usa un selector convencional, luego unos dos puntos ':', el nombre de la pseudoclase y, finalmente, el bloque de reglas. Por ejemplo:

```
/* esta pseudoclase modifica el color de los botones cuando se pasa el cursor por encima*/

button:hover {
  bakground-color: green;
}
```
