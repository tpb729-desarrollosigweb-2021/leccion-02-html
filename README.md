# HTML
El [Lenguaje de Marcas de Hipertexto o HTML](https://html.spec.whatwg.org/) (siglas en inglés de *Hypertext Markup Language*) es el lenguaje de marcas estándar para documentos diseñados para desplegarse en un navegador web.  El término "hipertexto" hace referencia a los enlaces que conectan páginas web entre sí, ya sea dentro de un mismo sitio web o entre diferentes sitios web (ej. [enlace al primer sitio web](http://info.cern.ch/)). El HTML fue creado en 1990 por Tim Berners-Lee. Junto con [Hojas de Estilo en Cascada o CSS](https://www.w3.org/TR/CSS/#css) (siglas en inglés de *Cascading Style Sheets*) y [JavaScript](https://es.wikipedia.org/wiki/JavaScript) conforma el grupo de las tres tecnologías principales de la Web.

El HTML especifica la estructura y la semántica de una página web mediante marcas (también llamadas etiquetas) o *tags*. Un navegador web recibe documentos HTML desde un servidor web (o desde almacenamiento local) y despliega sus componentes (textos, imágenes, hiperenlaces, etc.) de acuerdo con las especificaciones contenidas en los *tags.* Se recomienda que los documentos HTML no contengan componentes de presentación ni de interactivdad y que estos sean implementados mediante CSS y JavaScript.

EL HTML es un estándar del [World Wide Web Consortium (W3C)](https://www.w3.org/), un consorcio internacional creado por Tim Berners-Lee en 1994 que genera recomendaciones y estándares que aseguran el crecimiento de la WWW a largo plazo. La versión más reciente del estándar es [HTML5](https://www.w3.org/TR/2017/REC-html52-20171214/) y se caracteriza por incluir soporte para los tipos más recientes de multimedios y reducir la necesidad de plataformas propietarias (ej. Adobe Flash) para su incorporación en páginas web que pueden desplegarse en diferentes tipos de dispositivos y tamaños de pantallas (computadoras, tabletas, teléfonos, pantallas gigantes, etc.).

## Conceptos básicos
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

1. <strong>La etiqueta de apertura</strong>: consiste del nombre del elemento (en este caso, <strong>p</strong>, correspondiente a un párrafo), encerrado por paréntesis angulares (< >) de apertura y cierre. Establece el inicio del elemento —en este caso, dónde es el comienzo del párrafo—.
2. <strong>El contenido</strong>: este es el contenido del elemento, que en este caso es solamente texto. También pueden usarse imágenes, hipervínculos, direcciones web u otros elementos HTML.
3. <strong>La etiqueta de cierre</strong>: es similar que la etiqueta de apertura, pero incluye una barra de cierre (/) antes del nombre de la etiqueta. Establece el final del elemento —en este caso, en dónde termina el párrafo—.

Los elementos HTML pueden tener **atributos**, como el que se muestra en la figura 2.

<p>
  <figure>
    <img src="img/atributohtml.png" alt="Elemento HTML">
    <figcaption>
      <small>
        <strong>Figura 2.</strong> Ejemplo de atributo en un elemento HTML. Fuente: <a href="https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/HTML_basics">MDN Web Docs</a>.
      </small>
    </figcaption>
  </figure>  
<p>
  
Los atributos proporcionan información adicional acerca del elemento, la cual no se despliega en su contenido. Los atributos se especifican en la etiqueta de apertura mediante la sintaxis ```nombre_atributo=valor```. En la figura 2, ```class``` es el nombre del atributo y ```editor-note``` su valor (```class``` es un atributo que permite asociar al elemento con una clase o grupo de elementos, lo que puede ser útil para asignarles de manera conjunta estilos y otras propiedades). Si un elemento tiene varios atributos, deben separarse con (al menos) un espacio en blanco. Si el valor del atributo contiene espacios, debe encerrarse entre comillas (""). Se considera una buena práctica entrecomillar los valores de atributos aunque no contengan espacios, para mejorar la legibilidad.

Un elemento HTML puede contener otros elementos. Por ejemplo:
```html
<p>Mi gato es muy <strong>gruñón</strong></p>
```

Para mejorar su legibilidad, el elemento anterior también puede escribirse así:
```html
<p>
    Mi gato es muy <strong>gruñón</strong>
</p>
```

En ambos casos, el resultado es:
<p>Mi gato es muy <strong>gruñón</strong></p>

