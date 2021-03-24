# El Lenguaje de Marcas de Hipertexto (HTML)
El [Lenguaje de Marcas de Hipertexto o HTML](https://html.spec.whatwg.org/) (siglas en inglés de *Hypertext Markup Language*) es el lenguaje de marcas estándar para documentos diseñados para desplegarse en un navegador web.  El término "hipertexto" hace referencia a los enlaces que conectan páginas web entre sí, ya sea dentro de un mismo sitio web o entre diferentes sitios web (ej. [este es un enlace al primer sitio web](http://info.cern.ch/)). El HTML fue creado en 1990 por Tim Berners-Lee. Junto con [Hojas de Estilo en Cascada o CSS](https://www.w3.org/TR/CSS/#css) (siglas en inglés de *Cascading Style Sheets*) y [JavaScript](https://es.wikipedia.org/wiki/JavaScript) conforma el grupo de las tres tecnologías principales de la Web.

El HTML especifica la estructura y la semántica de una página web mediante marcas (también llamadas etiquetas) o *tags*. Un navegador web recibe documentos HTML desde un servidor web (o desde almacenamiento local) y despliega sus componentes (textos, imágenes, hiperenlaces, etc.) de acuerdo con las especificaciones contenidas en los *tags.* Se recomienda que los documentos HTML no contengan componentes de presentación ni de interactivdad y que estos sean implementados mediante CSS y JavaScript.

EL HTML es un estándar del [World Wide Web Consortium (W3C)](https://www.w3.org/), un consorcio internacional creado por Tim Berners-Lee en 1994 que genera recomendaciones y estándares que aseguran el crecimiento de la WWW a largo plazo. La versión más reciente del estándar es [HTML5](https://www.w3.org/TR/2017/REC-html52-20171214/) y se caracteriza por incluir soporte para los tipos más recientes de multimedios y reducir la necesidad de plataformas propietarias (ej. Adobe Flash) para su incorporación en páginas web que pueden desplegarse en diferentes tipos de dispositivos y tamaños de pantallas (computadoras, tabletas, teléfonos, pantallas gigantes, etc.).

El siguiente es un ejemplo de un documento HTML, el cual contiene, entre otras, etiquetas que especifican el lenguaje, el título y el cuerpo del documento, además de comentarios (que no son desplegados por el navegador web).
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo de documento HTML</title>     
</head>
<body>
    <!-- Comentario -->
    Contenido de documento HTML.
</body>
</html>
```

## Conceptos básicos
### Elementos
Un documento HTML está compuesto por **elementos** HTML, como el que muestra en la figura 1.

<p>
  <figure>
    <img src="img/elementohtml.png" alt="Elemento HTML">
    <figcaption>
      <small>
        <strong>Figura 1.</strong> Componentes de un elemento HTML. Fuente: <a href="https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/HTML_basics">MDN Web Docs</a>.
      </small>
    </figcaption>
  </figure>  
<p>
  
Los componentes de un elemento HTML son:

1. <strong>La etiqueta de apertura</strong>: consiste del nombre del elemento (en este caso ```p```, correspondiente a un párrafo), encerrado por paréntesis angulares (< >) de apertura y cierre. Establece el inicio del elemento —en este caso, dónde es el comienzo del párrafo—.
2. <strong>El contenido</strong>: este es el contenido del elemento, que en este caso es solamente texto. También pueden usarse imágenes, hipervínculos, direcciones web u otros elementos HTML.
3. <strong>La etiqueta de cierre</strong>: es similar que la etiqueta de apertura, pero incluye una barra de cierre (/) antes del nombre de la etiqueta. Establece el final del elemento —en este caso, en dónde termina el párrafo—.

### Atributos
Los elementos HTML pueden tener **atributos**, como el que se muestra en la figura 2.

<p>
  <figure>
    <img src="img/atributohtml.png" alt="Atributo HTML">
    <figcaption>
      <small>
        <strong>Figura 2.</strong> Ejemplo de atributo en un elemento HTML. Fuente: <a href="https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/HTML_basics">MDN Web Docs</a>.
      </small>
    </figcaption>
  </figure>  
<p>
  
Los atributos proporcionan información adicional acerca del elemento, la cual no se despliega en su contenido. Los atributos se especifican en la etiqueta de apertura mediante la sintaxis ```nombre_atributo=valor```. En la figura 2, ```class``` es el nombre del atributo y ```editor-note``` su valor (```class``` es un atributo que permite asociar al elemento con una clase o grupo de elementos, lo que puede ser útil para asignarles de manera conjunta estilos y otras propiedades). Si un elemento tiene varios atributos, deben separarse con (al menos) un espacio en blanco. Si el valor del atributo contiene espacios, debe encerrarse entre comillas dobles ("") o simples (''). Se considera una buena práctica entrecomillar los valores de atributos aunque no contengan espacios, para mejorar la legibilidad.

Cada elemento tiene una lista de atributos que puede usar. Existen [atributos globales](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes), que pueden usarse en todos los elementos.

### Elementos anidados y elementos vacíos
Un elemento HTML puede contener otros elementos. A estos elementos se les llama **elementos anidados**. Por ejemplo:
```html
<p>Mi gato es muy <strong>gruñón</strong></p>
```

El elemento anterior también puede escribirse así:
```html
<p>
    Mi gato es muy <strong>gruñón</strong>
</p>
```

La tabulación es opcional, pero ayuda a mejorar la legibilidad. En ambos casos, el resultado es:
<p>Mi gato es muy <strong>gruñón</strong></p>

Algunos elementos no tienen contenido, solamente atributos. Estos elementos se denominan **elementos vacíos**. Por ejemplo:

```html
<img src="img/atributohtml.png" alt="Atributo HTML">
```

Como puede observarse, el elemento ```img```, el cual se usa para incluir una imagen, no tiene una etiqueta de cierre y, por lo tanto, no puede especificar contenido.

### Comentarios
Las etiquetas ```<!--``` y ```-->``` marcan el inicio y el final de cadenas de caracteres que no son interpretadas como código HTML por los navegadores web y, por lo tanto, no se despliegan. Estos "comentarios" pueden ser utilizados para explicar la lógica del documento HTML o realizar cualquier tipo de anotación. Como en el caso de los comentarios de los lenguajes de programación, se recomienda utilizar comentarios en HTML para facilitar la comprensión del código.

```html
<!-- Esto es un comentario -->
<p>Esto es un párrafo.</p>
```

## Principales elementos
A continuación, se describen y se ejemplifican algunos de los principales elementos de HTML.

### DOCTYPE
[```DOCTYPE```](https://developer.mozilla.org/es/docs/Glossary/Doctype) (tipo de documento) es una etiqueta que le informa al navegador web cual es la versión HTML de un documento. No es una etiqueta ni un elemento HTML. Más bien es una declaración que le permite al navegador saber como interpretar los elementos HTML que hay en el resto del documento. Se coloca al inicio del documento.

La siguiente etiqueta ```DOCTYPE``` especifica que el documento usa HTML5.
```html
<!DOCTYPE html>
```

### html
El elemento [```html```](https://developer.mozilla.org/es/docs/Web/HTML/Element/html) es el elemento raíz de un documento y contiene el resto de los elementos.

El siguiente elemento ```html``` especifica el lenguaje del documento a través del atributo globlal [```lang```](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/lang).
```html
<html lang="es">
    <head>
    </head>
    <body>
    </body>
</html>
```

### head
El elemento [```head```](https://developer.mozilla.org/es/docs/Web/HTML/Element/head) contiene los metadatos del documento y otros elementos como su título y referencias a *scripts* y hojas de estilo (CSS).

```html
<head>
    <meta charset="UTF-8">
    <title>Título del documento</title>
    
    <link rel="stylesheet" href="css/estilos.css">
    <script src="js/scripts.js"></script>        
</head>
```

### meta
El elemento [```meta```](https://developer.mozilla.org/es/docs/Web/HTML/Element/meta) especifica metadatos del documento tales como su autor, descripción, palabras clave y juego de caracteres, entre otros.

```html
<meta charset="UTF-8">
<meta name="author" content="Manuel Vargas">
<meta name="description" content="Curso introductorio de programación">
<meta name="keywords" content="Python, programación">
```

### title
El elemento [```title```](https://developer.mozilla.org/es/docs/Web/HTML/Element/title) especifica el título del documento, el cual se muestra en la parte superior de la ventana (o pestaña del navegador). Es un elemento obligatorio de todo documento HTML válido y debe estar ubicado dentro del elemento ```head```.

```html
<title>Curso de programación en Python</title>
```

### link
[```link```](https://developer.mozilla.org/es/docs/Web/HTML/Element/link) especifica la relación entre el documento actual y un recurso externo, como una hoja de estilos.

Enlace a la hoja de estilos de la biblioteca geoespacial [Leaflet](https://leafletjs.com/):
```html
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A==" crossorigin=""/>
```

### script
El elemento [```script```](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script) se utiliza para incluir código de algún lenguaje de programación, típicamente JavaScript, aunque también usarse con otros lenguajes y sintaxis (ej. [JSON](https://www.json.org/json-en.html)).

Enlace al código JavaScript de la biblioteca geoespacial [Leaflet](https://leafletjs.com/):
```html
<script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js" integrity="sha512XQoYMqMTK8LvdxXYG3nZ448hOEQiglfqkJs1NOQV44cWnUrBc8PkAOcXy20w0vlaXaVUearIOBhiXZ5V3ynxwA==" crossorigin=""></script>
```

### body
[```body```](https://developer.mozilla.org/es/docs/Web/HTML/Element/body) especifica el contenido principal del documento (texto, multimedia, hipervínculos, etc.).

```html
<body>
    <a href="https://www.python.org/">Python</a> es un lenguaje de programación creado por Guido van Rossum.
</body>
```

### h1-h6
Los elementos [```h1-h6```](https://developer.mozilla.org/es/docs/Web/HTML/Element/Heading_Elements) (```h1, h2, h3, h4, h5, h6```) definen encabezados (*headings*) de seis niveles. ```h1``` es el encabezado de mayor nivel (con letras más grandes) y ```h6``` el de menor nivel.

```html
<h1>El lenguaje Python</h1>
<h2>Tipos de datos<h2>
<h3>Numéricos</h3>
<h3>Textuales</h3>
<h2>Control de flujo<h2>
<h3>Condicionales</h3>
<h3>Ciclos</h3>
```

### p
El elemento [```p```](https://developer.mozilla.org/es/docs/Web/HTML/Element/p) define un párrafo (i.e. texto o elementos HTML delimitados por líneas en blanco al principio y al final). La etiqueta de cierre es opcional. Una etiqueta ```<p>``` sola genera una línea en blanco.

```html
<p>Python es un lenguaje de programación de propósito general ...</p>
<p>Fue creado en 1989 por Guido van Rossum...</p>
```

### br
El elemento [```br```](https://developer.mozilla.org/es/docs/Web/HTML/Element/br) (*line break*) genera un salto de línea (o "retorno de carro") en el documento. No debe usarse para incrementar el espacio entre los parrafos. Para eso se recomienda utilizar el elemento ```p``` u hojas de estilo.

```html
Mozilla Foundation<br>
1981 Landings Drive<br>
Building K<br>
Mountain View, CA 94043-0801<br>
USA
```

### strong
El elemento [```strong```](https://developer.mozilla.org/es/docs/Web/HTML/Element/strong) se utiliza para denotar la importancia de una parte del texto. Los navegadores acostumbran usar letra en negrita para implementar este elemento. Sin embargo, no debe utilizarse para simplemente escribir un texto en negrita. Para eso, se recomienda emplear la propiedad [```font-weight```](https://developer.mozilla.org/es/docs/Web/CSS/font-weight) de CSS.

```html
<p>"... the most important rule, the rule you can never forget, no matter how much he cries, no matter how much he begs: <strong>never feed him after midnight</strong>."</p>
```

Los elementos semánticos (i.e que pretenden transmitir un significado) como ```strong``` y ```em``` facilitan la comprensión de textos por parte de personas y también programas. Por ejemplo, los [lectores de pantalla](https://es.wikipedia.org/wiki/Lector_de_pantalla) pueden utilizar estos elementos para pronunciar las palabras con mayor fuerza o volumen.

### em
[```em```](https://developer.mozilla.org/es/docs/Web/HTML/Element/em) marca un fragmento de texto al que se se da un énfasis particular. Puede utilizarse de forma anidada, con cada nivel de anidamiento indicando un mayor grado de énfasis. Los navegadores acostumbran usar letra en itálica para implementar este elemento. Sin embargo, no debe utilizarse para simplemente escribir un texto en itálica. Para eso, se recomienda emplear la propiedad [```font-style```](https://developer.mozilla.org/es/docs/Web/CSS/font-style) de CSS.

```html
<p>Tenemos que <em>hacer</em> algo al respecto.</p>
```

Los elementos semánticos (i.e que pretenden transmitir un significado) como ```strong``` y ```em``` facilitan la comprensión de textos por parte de personas y también programas. Por ejemplo, los [lectores de pantalla](https://es.wikipedia.org/wiki/Lector_de_pantalla) pueden utilizar estos elementos para pronunciar las palabras con mayor fuerza o volumen.

### a
El elemento [```a```](https://developer.mozilla.org/es/docs/Web/HTML/Element/a) (*anchor* o ancla) crea un hipervínculo a otro documento HTML, a un archivo, a una dirección de email o a cualquier otro tipo de URL [(*Uniform Resource Locator* o localizador de recursos uniforme)](https://es.wikipedia.org/wiki/Localizador_de_recursos_uniforme). El atributo ```href``` especifica el URL. El contenido del elemento especifica el texto que se le muestra al usuario en el enlace.

```html
<a href="https://www.python.org/">El lenguaje de programación Python</a>
```

### img
El elemento [```img```](https://developer.mozilla.org/es/docs/Web/HTML/Element/img) (*anchor* o ancla) inserta una imagen en un documento. Solo usa la etiqueta de apertura. El atributo src especifica el URL de la imagen y el atributo alt una descripción textual de la imagen. El atributo ```src``` especifica el URL de la imagen y el atributo ```alt``` una descripción textual de la imagen.

```html
<img src="img/python-logo.png" alt="Logo de Python">
```

## Recursos adicionales
- [HTML: Lenguaje de marcas de hipertexto | MDN](https://developer.mozilla.org/es/docs/Web/HTML)
- [HTML Tutorial | W3Schools](https://www.w3schools.com/html/)
- [The W3C Markup Validation Service](https://validator.w3.org/)
