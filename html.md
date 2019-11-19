# HTML Relámpago :zap:

## ¿Qué es HTML? :alien:

HTML o *Hypertext Markup Language* es un lenguaje de marcado con el que se describen, categorizan y especifican las partes que componen una página web. Para una referencia mucho más exhaustiva de HTML, [clic aquí](https://developer.mozilla.org/es/docs/Web/HTML).

## ¿Cómo funciona? :sunglasses:

HTML utiliza **etiquetas** para describir cada parte de la página web. Esas etiquetas sirven tanto para definir la presentación del documento como para definir sus cualidades semánticas.
Como HTML es una derivación del lenguaje de marcado SGML, las etiquetas se crean usando corchetes angulares ('<' y '>') que contienen el nombre del tipo de elemento. Algo como esto:

`<etiqueta>Contenido</etiqueta>`

:exclamation: Fíjate que la etiqueta de cierre tiene un '/' antes del nombre de la etiqueta.

Adicionalmente, dentro de las etiquetas se puede definir información con respecto al elemento al especificar sus "atributos". Los atributos se escriben dentro de la etiqueta de apertura. Se escribe primero el atributo y luego el valor, separados por un igual "=". Algo así:

`<etiqueta nombreDeAtributo="valorDelAtributo">Contenido</etiqueta>`

### El DOM

El DOM o [*Document Object Model*](https://es.wikipedia.org/wiki/Document_Object_Model) es un estándar que define la estructura que puede tener un documento marcado en HTML, sus tipos de elementos, etiquetas y atributos.

### La estructura general

En términos generales, se define un documento HTML con la etiqueta 'html' y adentro de la etiqueta se ponen las etiquetas 'head' y 'body'. La etiqueta 'head' define los metadatos del documento, es decir, la información relevante del documento que no debe ser presentada al usuario, mientras que la etiqueta 'body' define los elementos del documento que deben ser visibles para el usuario.
```
<html>
  <head>
    <!–– Aquí van los metadatos ––>
  </head>
  <body>
    <!–– Aquí van los elementos visibles del documento ––>
  </body>
<html>
```
:exclamation: Nota dos cosas: 
* Es una buena práctica usar indentaciones (o espacios al comienzo de la línea) para que el documento sea fácil de leer y para que sean evidentes las jerarquías. Así, tanto el 'head' como el 'body' están indentados para mostrar que se encuentran dentro de la etiqueta 'html'.
* Para hacer comentarios dentro de html se usa una etiqueta como esta: <!–– aquí va el comentario ––>

### :zap: Referencia relámpago de etiquetas del cuerpo del documento
Aquí unos ejemplos de etiquetas comunes en HTML para el cuerpo del documento

#### Encabezados o títulos
Existen 6 etiquetas de encabezados con tamaños y jerarquías diferentes:

```
<h1>Título 1</h1>
<h2>Título 2</h2>
<h3>Título 3</h3>
<h4>Título 4</h4>
<h5>Título 5</h5>
<h6>Título 6</h6>
```

#### Párrafos

`<p>Esto es un párrafo</p>`

Se puede usar la etiqueta 'br' para definir nuevas líneas:

`<p>Línea 1<br>Línea 2</p>`

#### Enlaces

Se debe poner el atributo 'href' que referencia el enlace al que queremos direccionar:

`<a href="https://www.elenlacealquequierollevar.com">Texto del enlace</a>`

#### Imágenes

Se debe poner el atributo 'source' que direcciona al enlace o camino de la imagen, y también el atributo 'alt' que contiene un texto alternativo cuando la imagen no se puede presentar. No se usa etiqueta de cierre:

`<img src="/enlace/a/la/imagen.png" alt="Texto alternativo">`

#### Listas
Pueden ser ordenadas o desordenadas. Para las desordenadas se usa la etiqueta 'ul' y para las ordenadas la etiqueta 'ol'. Cada elemento de la lista se marca con 'li'.

Desordenada:

```
<ul>
  <li>Elemento desordenado 1</li>
  <li>Elemento desordenado 2</li>
  <li>Elemento desordenado 3</li>
</ul>
```

Ordenada:

```
<ol>
  <li>Elemento ordenado 1</li>
  <li>Elemento ordenado 2</li>
  <li>Elemento ordenado 3</li>
</ol>
```

En el documento final se ven así:

<ul>
  <li>Elemento desordenado 1</li>
  <li>Elemento desordenado 2</li>
  <li>Elemento desordenado 3</li>
</ul>

<ol>
  <li>Elemento ordenado 1</li>
  <li>Elemento ordenado 2</li>
  <li>Elemento ordenado 3</li>
</ol>

#### Bloques o divisores
Se usan para contener partes del Documento que están marcadas con otras etiquetas:

`<div></div>`

Por ejemplo:

```
<div>
  <h1>Encabezado</h1>
  <p>Párrafo</p>
</div>
```
#### Botones

`<button>Texto del botón</button>`

#### Área para escribir texto

`<textarea>Escribe aquí...</textarea>`

#### Selecciones

Se usa la etiqueta 'select'. Para cada opción se usa la etiqueta 'option' y se define el valor de la opción con el atributo 'value':

```
<select>
    <option value="op1">Opción 1</option>
    <option value="op2">Opción 2</option>
    <option value="op3">Opción 3</option>
</select>
```

#### Tablas
Se definen con la etiqueta 'table'. Para definir filas se usa 'tr', para definir celdas 'td' y para definir celdas de cabecera 'th':

```
<table>
  <tr>
    <th>Titular 1</th>
    <th>Titular 2</th>
    <th>Titular 3</th>
  </tr>
  <tr>
    <td>Dato 11</td>
    <td>Dato 12</td>
    <td>Dato 13</td>
  </tr>
  <tr>
    <td>Dato 21</td>
    <td>Dato 22</td>
    <td>Dato 23</td>
  </tr>
</table>
```
Se ve así:

<table>
  <tr>
    <th>Titular 1</th>
    <th>Titular 2</th>
    <th>Titular 3</th>
  </tr>
  <tr>
    <td>Dato 11</td>
    <td>Dato 12</td>
    <td>Dato 13</td>
  </tr>
  <tr>
    <td>Dato 21</td>
    <td>Dato 22</td>
    <td>Dato 23</td>
  </tr>
</table>

### :zap: Referencia relámpago de Atributos
Aquí unos ejemplos de atributos comunes en HTML

#### Clases
Permite asignar una clase a un elemento a través del atributo 'class'. Esto se usa para luego poder acceder a un grupo específico de elementos.

`<p class="cuento">Este párrafo pertenece a la clase cuento</p>`
`<p class="cuento">Este párrafo también</p>`

#### Identificación
Permite asignar una identificación a un elemento a través del atributo 'id'. Esto se usa para luego poder acceder elemento específico.

`<p id="introduccion">Este párrafo es la introducción del documento</p>`

#### Estilo
Permite definir características del estilo del documento a través del atributo 'style'.

`<div style="background: red;">Esto es un bloque rojo</div>`

### :zap: Referencia relámpago de metadatos HTML
Aquí unos ejemplos de etiquetas comunes en HTML para los metadatos del documento

#### Título de la página
Se muestra en la parte superior o en la pestaña del explorador:

`<title>Título de la página</title>`

#### Enlace externo
Se usa para referenciar un enlace externo, comúnmente una hoja de estilo escrita en CSS. Se usa el atributo 'href' para definir el enlace.

`<link href="/enlace/a/hoja/de/estilo.css" rel="stylesheet">`

#### Enlace a código
Se usa para referenciar un enlace externo, comúnmente un código de programación escrito en JavaScript. Se usa el atributo 'src' para la ruta del archivo.

`<script src="/ruta/a/codigo.js"></script>`


#### Estilo CSS
Se usa para definir características del estilo de presentación del documento en formato CSS.

```
<style type="text/css">
  /* Aquí va la descripción del estilo  */ 
</style>
```

