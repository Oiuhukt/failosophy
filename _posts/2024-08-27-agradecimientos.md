---
layout: post
title: "Agradezco a \LaTeX"
subtitle: ·
date: 2024-07-08
author: oiuhukt
---

<!-- LTeX: language=es -->

Estudié filosofía y soy parte de la comunidad dedicada a hacer investigación --para eso me pagan-- y necesito producir documentos para mostrar mi trabajo.
Como producir documentos es una parte importante del trabajo, creo que es necesario conocer las herramientas que nos lo permiten.

## La tesis

He estado últimamente pensando en muchas cosas.
En particular he pensado largo y tendido sobre el tema de mi tesis de doctorado.
Si bien he trabajado principalmente en el tema, también he pensado en la _tesis_: el producto impreso que se entrega a las manos de los lectores.
Ese documento tiene una medida de papel particular, como carta, oficio o A4; 
el contenido del documento descansa dentro de ciertos márgenes con medida particular; 
y el contenido está estructurado por encabezados, subsecciones, títulos, notas al pies, etc. 

De todas estas características físicas, me interesa hablar de este último conjunto de características, digamos la _estructura del contenido_ [EC].
La EC es una parte esencial del formato, pero también es una guía para estructurar el contenido de la tesis: hay que decidir qué secciones y subsecciones son necesarias para escribir un capítulo y decidir qué notas a pie incorporar.

Es gracias a un par de herramientas que he podido concentrarme más en el contenido y la estructura del contenido y no en el formato de dicha estructura;
formato ejemplificado por nuestros longevos compañeros: tamaño de letra, espaciado, sangría, espacio entre líneas, __negritas__, _itálicas_, etc;
y ha sido gracias a buenas herramientas que he podido producir el documento. 
Claro que la herramienta principal es la que de hecho nos permite redactar.

## _suite_ de ofimática

En este trabajo es indispensable manejar una _suite de ofimática_ --como Microsoft Office{% sidenote '0' 'En mi caso particular uso (Libre Office)[https://es.libreoffice.org/], que es una alternativa de código libre a Microsoft Office' %} o similares.--
Es la suite de ofimática la que tiene algún programa para redactar documentos.

La herramienta por excelencia para este trabajo es el _procesador de textos_{% sidenote '1' 'Otra de las herramientas útiles en la investigación es la _hoja de cálculo_, en la que podemos procesar grandes cantidades de datos y obtener sus propiedades estadístícas.' %}.
Es en el procesador de textos en el que vemos el _formato_ y el _contenido_ del documento.
Podemos agregar contenido sin formato, escribir cualquier cadena de carácteres que queramos; 
luego guardar el documento con algún nombre recordable para editarlo en el futuro.

Con el procesador de textos{% sidenote '2' 'Voy a hablar mayormente de procesadores de textos porque estudié filosofía. No es necesario hacer estadística (que no estaría nada mal). Pero quiero hablar de una herramienta de procesado de datos en otra entrada' %} podemos no sólo agregar contenido a un documento sino también darle estructura y declarar el _formato_ del documento.

Writer es la herramienta que suelo utilizar para esto --parte de la _suite_ de LibreOffice-- en la interfaz del programa hay botones para cambiar si una cadena de caracteres es un encabezado, una sección, un párrafo, una nota a pie, etc.
Esta estructura sirve para darle forma completa a nuestro documento.

En mi caso sirve para escribir ensayos, presentaciones, entradas de blog, planes de clase, etc.
Pero Writer no es la herramienta que utilizo para estos propósitos.
Para mi trabajo diario utilizo (Neovim)[https://neovim.io/] como editor.
Que hace exactamente lo mismo que Word: edita texto.
No quiero hablar de _Neovim_ aquí porque es un programa del que quiero dar más detalles, pero quiero sí debo decir que uso este procesador de textos porque me permite editar diferentes formatos como `.tex,` `.bib,` `.md,` `.html` y `.css`.
Pero para esta entrada, sólo me interesan los dos últimos formatos: `.tex` y `.bib.`

## El sistema de composición de textos \LaTeX

Hay que ser cautelosos cuando hablamos de qué demonios es \LaTeX.
El encabezado anterior afirma que \LaTeX es un sistema de composición de textos;
y es esta descripción la que voy a usar.
He escuchado a algunas personas decir que "programan en $\LaTex$" y esto es ligeramente incorrecto.

Hay en ciencias computacionales --prometo que este rodeo tiene un objetivo-- una taxonomía de los lenguajes de programación,{% sidenote '3' 'Hay un debate acerca de si esta taxonomía es adecuada o no. Pero esto es un debate académico del cuál obviamente no me voy a ocupar aquí.' %} que divide a los lenguajes de programación en los paradigmas:{% sidenote '4' 'Kuhn llegó aquí también' %} _imperativo_ y _declarativo_.

Los lenguajes _imperativos_ son lenguajes en los que se le dice al compilador qué hacer durante cierta línea de código.
Como una máquina a  la que hay que alimentar constantemente para obtener un resultado particular.
Los lenguajes de programación _declarativos_ usan código para decirle a la máquina cómo hacer las cosas.
Más cómo una receta para obtener un resultado, sin tener que obligar al compilador a cambiar de estado.

La definición de lo que es un lenguaje de programación declarativo está construida sobre lo que es un lenguaje de programación imperativo, {% sidenote '5' 'Otro debate académico que voy a evitar.' %} por lo que no puedo ofrecer mucho más detalle.
Pero un ejemplo claro de lenguaje declarativo es Haskell --que es puramente funcional.--

El rodeo anterior tiene como objetivo apaciguar las preocupaciones de los nuevos  usuarios que están por utilizar esta herramienta.
\LaTeX fue creado con el objetivo de hacer \TeX más sencillo de utilizar, porque \TeX sí es un lenguaje de programación, explícitamente "$\ldots$ \LaTeX was described as '\TeX' for the masses'." {% sidenote '6' ' "The \LaTeX Legacy, escrito por Chris Rowley" ' %}
No se programa en \LaTeX, pero se escribe en este lenguaje.

Para fines de este escrito, \LaTeX es un sistema de composición del documento y no es un lenguaje de programación{% sidenote '6' 'Por supuesto que comparte características con un lenguaje de programación imperativo y $\TeX$ es turing completo y discutir esto nos saca de tema' %}.
Decir esto es importante porque suele ser una preocupación común, porque hace parecer a \LaTeX más complicado de lo que es.

Otra cosa que debo decir es que $\LaTeX$ sí comparte ciertas características con los lenguajes de programación: el documento  necesita un _compilador_ y hay que aprender una _sintaxis;_ 
aprender esta sintaxis tiene una curva.
Microsoft Word no tiene esta curva, porque es más familiar a todas nosotras, en corto: si estás dedicando más tiempo a aprender la sintaxis y dar formato al documento en lugar de escribir, entonces no vale la pena.
Simplemente usa Word o similares.

Dicho lo anterior, debo decir también que son las características que \LaTeX comparte con un lenguaje de programación lo que lo hace una gran herramienta para editar trabajos académicos{% sidenote '7' 'Quiero hablar --en el futuro cercano-- de por qué deberíamos usar \LaTeX si lo que buscamos es un acceso libre a la investigación.' %}.

En primer lugar, como \LaTeX es un formato de archivo y no un editor como Word, puedo editar el código de con cualquier programa de edición de texto --incluyendo Word.--
Esto tiene la ventaja de la customización porque nos deja elegir diferentes editores.
Peronalmente he usado (TeXStudio)[https://www.texstudio.org/], (TeXWorks)[https://tug.org/texworks/] y (TeXMaker)[https://www.xm1math.net/texmaker/].
Los tres son buenos editores para comenzar a crear un documento.

\LaTeX tiene una sintaxis con la que le decimos qué hacer con una cadena de caracteres
Esto es algo que \Latex comparte con los lenguajes imperativos, pero para el caso en cuestión: para crear un documento no hace falta entrar en detalles.
Lo importante es que al igual que con Word y sus botones para cambiar una cadena a __negritas__, en \LaTeX declaramos `\estovaennegritas{negritas}`; el comando real es `\textbf{negritas}`.


## Creando un documento

Para este caso particular, diremos que un documento de \LaTeX tiene tres partes: el preámbulo del documento, el contenido del documento y la bibliografía.
La bibliografía está separada del contenido porque crear una base de datos bibliográfica contenida en un archivo `.bib` es un proceso diferente. 
Entonces concentrémonos en las dos primeras

En el preámbulo del documento, señalamos el tipo de documento que vamos a redactar. 
Las opciones que más uso son `article` y `book`.
La diferencia radica en las variables que podemos modificar, el tipoi de documento `book` define un comando para dar formato a encabezados como capítulo, la etiqueta `\chapter{*}` y que podemos definir qué tanto margen izquierdo y derecho queremos dejar para la encuadernación;
el tipo `article` no tiene estas características --aunque se pueden agregar.--

En el preámbulo también definimos los paquetes que queremos usar para nuestro documento, que nos permiten usar otros comandos.
El preámbulo se ve así 

```
\documentclass[letterpaper,12pt]{article}
\usepackage{paper}
\usepackage[spanish]{babel}
\usepackage[T1]{fontenc}    % 
\usepackage{url}
```

Donde `letterpaper, 12pt` dicen que el documento tiene el tamaño de una hoja carta con letra de tamaño 12.
Los paquetes que uso para el documento son `babel`, `fontenc` y `url`.
Por ahora no prestemos atención a `paper`, entonces el primer paquete `babel`, es un paquete para usar diferentes lenguajes en el documento.
En este caso usar el español y que las reglas para romper las sílabas de una palabra sean las del español; 
`fontenc` es el paquete que nos permite escribir "á" y no  "\'a".
Esto se debe a que la versión original, \TeX no tiene estos caracteres, sólo tiene 7 bits y el acento y la letra son dos caracteres diferentes, mientras que T1 usa 8 bits y tiene "á" como un caracter, no la composición de dos caracteres.
El último paquete `url` hace que los enlaces tengan el formato adecuado.





## Queda fuera

Pero Latex no es un _lenguaje de programación._
No es un lenguaje de programación funcional
porque no usamos funciones sino que es más parecido 

Pero es importante esta relación entre el proyecto Latex y el lenguaje de etiquetas html.
html fue creado originalmente para mostrar documentos en una pantalla que sólo podía renderizar caracteres. 
Pero como el internet se creó para compartir la investigación más rápido entre grupos geográficamente distantes. 
Surge la necesidad de dar estructura al documento: título, información de los autores, secciones, subsecciones, notas a pie, etc.
El lenguaje de html se creo para solucionar este problema. 



## Apuntes para lo siguiente

As is also the case with HTML, the relationships
between these tags define a fairly simple document
model that is not sufficiently rich, so that it can-
not express (or not correctly express) many real-life
documents; this is often due to the fact that certain
elements appear in such documents with nesting re-
lationships that are not permitted by the inclusion
rules defined in ISO 32005 [5].

In these discussions it’s worth remembering that LaTeX is not actually an executable typesetting program, it is a large collection of sophisticated macros (commands) written in a lower-level language called TeX. Sitting between your carefully crafted LaTeX document and the final typeset PDF is a piece of software called a TeX engine whose job is to “execute” the collection of LaTeX commands (i.e., macros) used to write and construct your document—converting them into the typeset representation of your document saved as a PDF file. De la documentación de Overleaf



In the modern world of small devices, IoT and connected systems, where interchange and reuse of data is critical, it is reasonable to question the continued relevance of PDF’s core value proposition. In particular, search engines, machine learning and artificial intelligence systems focus on accessing information contained in documents over visual representation. In other cases, document producers wish to deliver data in a form that is suitable for automated processing while using a PDF file as a record for trust purposes. End users want electronic documents that adapt smoothly to viewing on diverse small devices.

By describing the algorithm that produces conforming HTML from a tagged PDF, this document shows how well-tagged PDF documents, containing both traditional fixed-layout content and the semantic structures leveraged by modern devices and software, can be reliably and consistently reused as HTML to support better user experiences and renew PDF’s value proposition.

HTML was chosen as a derivation target because HTML is consumed on all platforms and supported by all major vendors. With small modifications, developers can use this document to export content from well-tagged PDF to any format. de la pdf association https://pdfa.org/resource/deriving-html-from-pdf/

At the TUG 2020 online conference the LATEX Project
Team announced the start of a multi-year project
to enhance LATEX so that it will fully and naturally
support the creation of structured document formats,
in particular the “tagged PDF” format as required
by accessibility standards such as PDF/UA. de https://www.latex-project.org/publications/2024-FMi-UFi-TUB-tb139mitt-deims24.pdf

For over 30 years now, the LATEX system has been
used, widely and successfully, for document produc-
tion in the STEM world and also in other places
where high-quality output is required; but until re-
cently its focus was solely on page-oriented output
for print (on paper) or as paged output using the
PDF format. Therefore, the structural information
about the document that was present in the LATEX
source did not get incorporated into the PDF output.
Rather, this information was discarded as soon as
possible during the processing; this was necessary so
as to conserve the limited computer resources (mem-
ory and storage) that were typically available at that
time (when the core of the LATEX processing model
was first designed).
As long as the intention is only to print a docu-
ment on a physical medium, then this is all that is
required. However, for quite a while now other uses
of documents have been increasing in importance so
that nowadays many documents are never printed,
or printed only as a secondary consideration





## Pensar si quuiero escribir sobre los documentos de análisis de datos.




He pensado que es lo que quiero lograr con este documento 


Hace un par de semanas tuve que dejar el lugar en el que vivía. 
Ahora mismo, al escribir esto, estoy en casa de mis padres en Pabellón de Arteaga {% sidenote '0' 'El primer distrito de riego del país.' %}. }
Antes de esto, vivía en Tlalnepantla. 

La mudanza interestatal es muy costosa y tuve que repartir mis cosas en las casas de dos amigos que viven cerca de ese municipio, ahora mis pertenencias están divididas. 
Otros de mis bienes materiales los tuve que abandonar en la casa que deshabité: mi silla y mi

