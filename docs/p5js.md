# p5.js Relámpago :zap:

## ¿Qué es p5.js? :alien:
p5.js es una librería de JavaScript, creada por Lauren McCarthy y apoyada por la [Processing Foundation](https://processingfoundation.org/). p5.js fue desarrollada específicamente para facilitarle a artistas, diseñadores y humanistas digitales la expresión creativa usando código de programación. Por eso, p5.js contiene un buen número de funciones que permiten manipular texto, crear imágenes, hacer animaciones, crear aplicaciones interactivas, visualizar datos, crear sonido, etc. Para leer la referencia oficial de p5.js, [clic aquí](https://p5js.org/es/reference/).

:speak_no_evil: Este relámpago no incluye una explicación exhaustiva de todos las funciones de p5, solo funciona como una hoja de recuerdo o *cheatsheet* para mantener fresca la memoria.

:exclamation: Para entender mejor lo que se resume aquí, es importante tener claro cómo funciona [HTML](https://github.com/srsergiorodriguez/relampagos/blob/master/docs/html.md) y [JavaScript](https://github.com/srsergiorodriguez/relampagos/blob/master/docs/javascript.md). Ante la duda, revisa los relámpagos al respecto.

## ¿Cómo funciona? :sunglasses:
Para usar p5 se debe crear una referencia al archivo que contiene la librería en el documento .html principal:

`<script src="p5.min.js"></script>`

:exclamation: el (archivo)[https://p5js.org/download/] con la librería puede incluirse dentro de los archivos de la aplicación, o puede provenir de un servicio de distribución como este [CDN](https://cdn.jsdelivr.net/npm/p5).

:exclamation: una forma fácil y rápida de escribir código con p5 es usar su [editor web](https://editor.p5js.org/), una interfaz interactiva que permite usar la librería desde el explorador.

### Las funciones Setup y Draw
El código de p5 se puede usar dentro de dos funciones preestablecidas que vienen con la librería: **setup** y **draw**.
**Setup** se ejecuta una sola vez, **draw** se ejecuta múltiples veces en ciclo. Así, **setup** sirve para crear las configuraciones iniciales del programa, mientras que **draw** sirve para hacer modificaciones constantes a variables o para hacer animaciones.

```
function setup() {
  // Aquí va el código de p5.js que se ejecutará una sola vez
}

function draw() {
  // Aquí va el código de p5.js que se en ciclo
}

// no es necesario llamar setup() o draw()
```

:exclamation: Las funciones **setup** y **draw** se llaman automáticamente. Así que solo es necesario escribir código dentro de ellas para que p5.js las ejecute.

### El canvas
El **canvas** (o lienzo) es el lugar donde se pueden disponer las imágenes y formas, y, en general, toda la manipulación visual, que permite p5.js.
Para crear un canvas debes llamar la función **createCanvas** y poner, como argumentos, el ancho y el alto que tendrá el canvas. Esta función debe llamarse dentro de la función **setup**.

`createCanvas(500,400);`

### Colores
Por defecto, el color del fondo del canvas, de las formas primitivas que se crean en p5, y del texto, se define a partir de parámetros [RGB](https://es.wikipedia.org/wiki/RGB) (rojo, verde y azul). Aunque es posible [cambiar el modelo de color](https://p5js.org/es/reference/#/p5/colorMode) por otros tipos como HEX, HSL, o HSB.
Los valores que se ponen en los parámetros de las funciones que modifican el color tienen un rango de 0-255, porque cada canal de color se codifica en 8 bits.

```
background(255, 0, 0); // cambia el color de fondo del canvas a rojo
fill(0, 255, 0); // cambia el relleno de las formas a verde
stroke(0, 0, 255); // cambia el color de la línea de borde a azul
noFill(); // quita el color de relleno de las formas
noStroke(); // quita el color de línea
```

### Formas
p5 permite crear varios tipos de formas primitivas. Están listadas a continuación junto sus parámetros más comunes.

```
point(x1, y1); // dibuja un punto

line(x1, y1, x2, y2); // dibuja una línea

ellipse(x, y, ancho, alto); // dibuja una elipse (si solo se pasa el argumento 'ancho' y no el 'alto' la función crea un círculo)

rect(x, y, ancho, alto); // dibuja un rectángulo

square(x, y, tamaño, borde_redondo) // dibuja un cuadrado

triangle(x1, y1, x2, y2, x3, y3); // dibuja un triángulo

quad(x1, y1, x2, y2, x3, y3, x4, y4); // dibuja un polígono de cuatro lados
```

:exclamation: Es importante tener presente que las cada función usa puntos de referencia diferentes para dibujar las formas. Por ejemplo, las elipses y los círculos se dibujan con respecto al centro, mientras que los rectángulos se dibujan con respecto a la esquina superior derecha. Para cambiar el punto de referencia se debe usar la función `elipseMode()` o `rectMode()`.

Para crear formas más complexas se debe usar las funciones de curvas de bezier y vértices. Para entender este tipo de formas, recomiendo [este libro](https://programmingdesignsystems.com/shape/custom-shapes/index.html#custom-shapes-pANLh0l) como referencia.

```
bezier(x1, y1, x2, y2, x3, y3, x4, y4) // dibuja formas de bezier cúbicas
curve(x1, y1, x2, y2, x3, y3, x4, y4) // dibuja formas de bezier cuadráticas

beginShape(); // indica a p5 que vas a crear una forma a partir de vértices
vertex(x, y); // indica un vértice
vertex(x2, y2); // ... indica todos los demás vértices que sean necesarios
endShape(); // termina la figura
```

### Texto
Para crear texto en el canvas, se usa la función **text**:

`text(string, x, y)`

Es posible modificar el texto usando otras funciones como:

```
textAlign(ALINEACIÓN); // Cambia la alineación (LEFT, CENTER, RIGHT)
textSize(número); // Cambia el tamaño del texto
textFont(fuente); // Cambia la fuente
```

### Referencia relámpago de las funciones más comunes :zap:
`random(valor)` -> Devuelve un número decimal entre 0 y el valor del argumento

`max(array)` y `min(array)` -> Devuelve el valor máximo o mínimo de una array, respectivamente

`map(valor, min1, max1, min2, max2)` -> Permite mapear valores de un dominio a otro de forma lineal

`sin(valor)`, `cos(valor)` y `tan(valor)` -> Las funciones Seno, Coseno y Tangente, respectivamente

`PI`-> Un valor aproximado de Pi

`int(valor)` -> convierte un valor a un número entero

`saveCanvas()` -> Guarda el canvas como una imagen. La extensión del archivo puede ser .jpg o .png

`loadJSON(url_o_archivo, callback)` -> Carga un archivo JSON desde una URL o un archivo

`loadStrings(url_o_archivo, callback)` -> Carga un archivo de texto desde una URL o un archivo

`mouseX` y `mouseY` -> Devuelven la posición X y Y del mouse, respectivamente

`loadImage(url_o_archivo, callback)` y `image(imagen, x, y)` -> Carga una imagen en el sketch, muestra la imagen en el canvas, respectivamente. **loadImage** Se suele usar dentro de la función optional `preload()`

### Maniulación del DOM
p5 permite crear y manipular elementos del [DOM](https://es.wikipedia.org/wiki/Document_Object_Model) de tu documento html a través del código. Estas son algunas de las funciones básicas al respecto:

`select(selector)` -> Devuelve un elemento del DOM usando selectores CSS (el nombre del elemento, el nombre de una clase antecedido por un `.`, el nombre de una identificación antecedido por un `#`)

`selectAll(selector)` -> Devuelve una array con elementos del DOM usando selectores CSS

`createElement(elemento)` -> Crea un elemento del DOM del tipo especificado.

También es posible crear algunos elementos particulares con funciones especializadas. Aquí hay algunos de los máscomunes

```
createDiv(html); // crea un divisor
createP(texto); // crea un párrafo
createA(href, html, target) // crea un enlace
createButton(etiqueta); // crea un botón
createInput(valor); // crea una entrada de texto
createSlider(min, max, valor_inicial, salto); // crea un slider
```

Los elementos del DOM creados o seleccionados con p5 cuentan con varias funciones. Supongamos que creamos un elemento: `elemento = createP("elemento")`. Ahora, con él se pueden hacer cosas como estas:

`elemento.id(string)`-> Si tiene un argumento, se le asigna una nueva identificación al elemento. Si no tiene argumento, devuelve la id actual.

`elemento.class(string)`-> Si tiene un argumento, se le asigna una nueva clase al elemento. Si no tiene argumento, devuelve las clases actuales.

`elemento.mousePressed(función)` -> Ejecuta la función cuando el elemento es presionado con el mouse. Hay otras funciones similares: `mouseClicked()`, `mouseReleased()`, `mouseOver()`, `mouseMoved()`, `mouseOver()`, `mouseOut()`, `doubleClicked()`

`elemento.child(selector_o_variable_hijo)` y `elemento.parent(selector_o_variable_padre)` -> Asigna otro elemento como hijo o como padre, respectivamente

`elemento.html(valor)` -> Cambia el atributo html del elemento

`elemento.style(clave, valor)` -> Cambia el estilo CSS del elemento

`elemento.attribute(clave, valor)` -> Añade o modifica un atributo del elemento

`elemento.value(valor)`-> Asigna, si hay argumento, o devuelve, si no lo hay, el valor del elemento.

`elemento.remove()` -> Remueve el elemento del documento