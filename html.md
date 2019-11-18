# HTML Relámpago

## ¿Qué es HTML?

HTML es un lenguaje de marcado con el que se describen, categorizan y especifican las partes que componen una página web.

## ¿Cómo funciona?

HTML utiliza etiquetas para describir cada parte de la página web. Esas etiquetas sirven tanto para definir la presentación del documento como para definir sus cualidades semánticas.
Como HTML es una derivación del lenguaje de marcado SGML, Las etiquetas se crean usando corchetes angulares ('<' y '>') que contienen el nombre del tipo de elemento. Algo como esto:

`<etiqueta>Contenido</etiqueta>`

Hay que notar que la etiqueta de cierre tiene un '/' antes del nombre de la etiqueta.

Adicionalmente, dentro de las etiquetas se puede definir información con respecto al elemento al especificar sus "atributos". Los atributos se escriben dentro de la etiqueta de apertura y tienen el formato de pares nombre valor, separados por un igual "=". Algo así:

`<etiqueta nombreDeAtributo="valorDelAtributo">Contenido</etiqueta>`

### El DOM

El DOM o *Document Object Model* es un estándar que define la estructura que puede tener un documento marcado en HTML, sus tipos de elementos, etiquetas y atributos.

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

Nota dos cosas: 
* Es una buena práctica usar indentaciones para que el documento sea fácil de leer y para que sean evidentes las jerarquías. Así, tanto el 'head' como el 'body' están indentados un nivel para mostrar que se encuentran dentro de la etiqueta 'html'.
* Para hacer comentarios dentro de html se usa una etiqueta como esta: <!–– aquí va el comentario ––>

### Referencia relámpago de etiquetas

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

#### Encabezados o títulos
Existen 6 etiquetas de encabezados con tamaños y jerarquías diferentes:

```
<p>Título 1</p>
```

#### Encabezados o títulos
Existen 6 etiquetas de encabezados con tamaños y jerarquías diferentes:

```
<span>Título 1</span>
```

#### Encabezados o títulos
Existen 6 etiquetas de encabezados con tamaños y jerarquías diferentes:

```
<button>Título 1</button>
```
