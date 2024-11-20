Curso HTML
=========
<a name="indice"></a>
# Contenido
- [Entorno de trabajo](#0)
- [Estructura de un HTML](#1)
- [Contenido de un HTML](#2)
- [Etiquetas](#3)
- [Enlaces](#4)
- [Tablas](#5)
- [Imágenes](#6)
- [Estilos (CSS)](#7)
- [Librería de estilos (CSS)](#8)
- [Contenedores](#9)
- [Colores](#10)
- [Formularios](#11)
- [JavaScript](#12)


<a name="0"></a>
# Entorno de trabajo
Para aprender HTML sólo se necesita un editor de texto. Sirve cualquiera (hasta el block de notas). El problema es que te resultará complicado distinguir lo que estas escribiendo, por lo que te recomiendo utilizar un editor de código. 

Para este curso te recomiendo utilizar [**Visual Studio Code**](https://code.visualstudio.com/): Es gratuito, multilenguaje, con resaltado de sintaxis y muy potente.

También vas a necesitar un servidor web para que tus páginas esten en algo parecido a **http://misitio/mipagina.html**
Existen muchos servidores web, siendo **Apache** el más conocido, pero para el objeto de este curso te recomendamos una solución mucho más sencilla. Se trata de utilizar una extensión de Visual Studio Code para montar un servidor web.

Las instrucciones son las siguientes:

Ver este enlace
[https://www.hostinet.com/formacion/diseno-web/3-editores-html-visuales-wysiwyg-y-gratuitos/](https://www.hostinet.com/formacion/diseno-web/3-editores-html-visuales-wysiwyg-y-gratuitos/)

Para activar un servidor web, con Visual Code:
- instalar extensión "**Live Server**"
- Ahora sólo tienes que abrir una carpeta en la aplicación y crear o abrir un archivo HTML.
- En la parte inferior de la pantalla, verás una opción que dice **Go Live** y si haces click ahí, se abrirá un navegador y mostrará la previsualización del archivo.

Respecto a editores online de html mira estos ejemplos


- De WYSIWYG a HTML    [https://html-online.com/](https://html-online.com/)
- De HTML a WYSIWYG   [https://www.w3schools.com/html/tryit.asp?filename=tryhtml_default](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_default)


[Volver al índice](#indice)
<a name="1"></a>
# Estructura de un HTML

Una página web tiene que tener los siguiente elementos

- html: Es la palabra clave para que el navegador sepa que es una página escrita en lenguaje HTML

Dentro del HTML encontrarás:

- head: 
- body

## Head
Dentro del HEAD podrás indicar parámetros opcionales, pero interesante de añadir

- TITLE: Título de la página web que verás en el encabezado del navegador
- Codificación del texto: Sirve para que reconozca aspectos como acentos, eñes, etc. Si no te la quieres jugar utiliza la codificación universal UTF8 ```<meta charset="UTF-8">```
- STYLE: Sirve para dar formato a los elementos del BODY.  Están escritos en un lenguaje que se llama CSS
- SCRIPT: Hace referencia a código, o nombre de ficheros, escritos en lenguaje JavaScript (JS)

##Body
Aquí es donde se encuentra el contenido que veremos en el navegador. Es lo que tienes que preocuparte en escribir.

### Plantilla
En resumén, aquí tienes un página web lista para que la utilices como base para añadir más contenido

```html
<HTML>
	<HEAD>
		<TITLE> Título de la página </TITLE>
		<meta charset="UTF-8">
	</HEAD>
	<BODY>
		[Aquí van las etiquetas que visualizan la página]
	</BODY>
</HTML>
```


[Volver al índice](#indice)

<a name="2"></a>
# Contenido de un HTML
Por ahora sólo tiene que preocuparnos escribir dentro del tag **BODY** .

### Comentarios
Te recomiendo que escribas comentarios dentro del código. Ta ayudará a poner tus notas y recordar para que sirven.

Los comentarios nunca saldrán en el navegador, que los ignorará.

Un comentario, a diferencia del resto de TAGS no empieza y termina igual.

```html
<!-- Hola, soy un comentario -->
```

###  Editor online:
Como hasta ahora no conoces el lenguaje HTML te recomiendo que utilices un editor online para escribir el contenido del BODY. Para ello utilizarás un editor WYSIWYG, y sólo tendrás que copiar el código HTML generado y pegarlo dentro de la etiqueta BODY.

El editor de texto es el siguiente:

[editor HTML WYSIWYG](./editor.html)


### Texto completo:
```html
<HTML>

<HEAD>
	<TITLE> Mi segunda página en el Web </TITLE>
	<meta charset="UTF-8">
</HEAD>

<BODY>
	<!--COMENTARIO: Empieza el BODY-->
	<H1>
		<CENTER> Segunda Página </CENTER>
	</H1>
	<HR>
	<P>Esta es mi segunda página, aunque todavía es muy sencilla. Como el lenguaje HTML
		no es difícil, pronto estaré en condiciones de hacer cosas más interesantes.</P>
	<P> Aquí va un segundo párrafo, ¿ qué les parece ?</P>
	<!--COMENTARIO: Termina el BODY-->
</BODY>

</HTML>
```

### Tareas
Crea un HTML llamado **ej2.html**  con la plantilla de esta página y rellena el BODY con lo que has creado con el editor online.

[Volver al índice](#indice)

<a name="3"></a>
# Etiquetas

Las etiquetas es el corazón del lenguaje HTML. Todo son etiquetas.

Por regla general todas las etiquetas tiene la misma sintaxis: 

- empiezan por un ** <nombre tag>**
- terminan por un ** </nombre tag>** . Fíjate que hemos añadido **/**
- emmedio de los tags estará el contenido del tag.

*** Ejemplo:

Por ejemplo, la etiqueta o tag para crear un párrafo se llama **p**, por tanto un párrafo se utilizará de esta  manera
```html
<p>Hola esto es un párrafo</p>
```
Hay algunas excepciones en algunos tags que no tienen contenido, y por tanto sólo se escriben una vez. Aquí tienes algunas excepciones:

- Retorno de carro: Se escribirá
```html
<br>
```
- Línea: Se escribirá
```html
<hr>
```

### Etiquetas más comunes

**** Centrar texto: 
<center>Este texto aparecerá centrado en la página</center>
```
**** Títulos
En función del tamaño del título podemos utilizar varias opciones, desdes el más grande, el **H1** hasta el má pequeño, el **H5**
```html
	<h1>título en H1</h1>
	<h2>título en H2</h2>
	<h3>título en H3</h3>
	<h4>título en H4</h4>
	<h5>título en H5</h5>
```

*** Párrafo
Ya lo hemos visto. Aquí tienes más ejemplos:

```html
	<p>Esto es un párrafo</p>
	<p>Esto es otro párrafo</p>
	<P> Aquí va un tercer párrafo, ¿ qué les parece ?</P>
	<p>
		<center>esto es un parrafo centrado. Fíjate como las etiquetas se pueden anidar unas dentro de otra</center>
	</p>
```

*** Formas del texto: negrita, cursiva, subrayado

- Escribir algo en negrita. Utiliza **b**, o **strong**
```html
	<b>Este texto aparecerá en negrita</b>
```
- Escribir algo en cursiva. Utiliza **i**
```html
	<i>Este texto aparecerá en cursiva</i>
```
- Escribir algo subrayado. Utiliza **u**
```html
	<u>Este texto aparecerá subrayado</u>
```
- Combinación.
```html
	<b><i><u>Este texto aparecerá de las tres maneras</u></i></b>
```




### Listas

Hay 2 tipos de listas, ordenadas (con números como 1,2,3, etc) y sin ordenar

- Listas ordenadas. Empiezan y acaban con **ol** y cada elemento tendrá un **li**. Veamos un ejemplo:
```html
<ol>
    <li>Soy el primero</li>
    <li>Soy el segundo</li>
    <li>Soy el tercero</li>
</ol>
```
- listas sin orden: Empiezan y acaban por **ul** y cada elemento tendrá un **li**

```html
<ul>
    <li>Ford</li>
    <li>Renault</li>
    <li>Citroen</li>
</ul>
```

### Caracteres especiales

Si tienes especificado en el HEAD que vas a utilizar la codificación de caracteres UTF-8 no tienes que :
preocuparte. De lo contrarío deberás de saber que algunos caracteres utilizan otra notificación para que el navegador lo entienda. Se trata del caso de los acentos, eñe, diáresis, y otros caracteres específicos del español.

**** Te pongo unos ejemplos

- La **á** podrás escribir por ejemplo **`irá`**, o también `&aacute;`, que en el ejemplo será **ir&aacute;**

Te pongo algunos caracteres más :

```html
á es &aacute;
é es &eacute;
í es &iacute;
ó es &oacute;
ú es &uacute;
ñ es &ntilde;
ç es &ccedil;
Un espacio en blanco se escribe &nbsp;
```
NOTA: Estos caracteres están en minúscula. En mayúscula será diferente.

Puedes ver más ejemplos en este [enlace](http://www.webusable.com/CharsExtendedTable.htm)


### Texto completo

```html
<HTML>

<HEAD>
	<TITLE> Etiquetas </TITLE>
	<meta charset="UTF-8">
</HEAD>

<BODY>
	<!-- esto es un comentario, y nunca verás el resultado en la página. Sirve para ayudar a entender el código -->
	<H1>
		<CENTER> Etiquetas HTML </CENTER>
	</H1>
	<!-- esto es una línea -->
	<HR>
	<!-- diferentes tipos de títulos, desde el más grande H1 al más pequeño -->
	<h1>título en H1</h1>
	<h2>título en H2</h2>
	<h3>título en H3</h3>
	<h4>título en H4</h4>
	<h5>título en H5</h5>
	<!-- ahora vamos a ver los párrafos -->
	<p>Esto es un párrafo</p>
	<p>Esto es otro párrafo</p>
	<P> Aquí va un tercer párrafo, ¿ qué les parece ?</P>
	<p>
		<center>esto es un parrafo centrado</center>
	</p>
	<!-- párrafo con más etiquetas: BR, B y I -->
	<P>
		En este párrafo vamos a añadir algunas cosas más como un retorno de carro BR </br>
		Otra línea más con BR <br>
		<b>Esta línea la vamos a poner en negrita usando B, que viene de Bold</b> <br>
		<i>Esta otra línea la vamos a poner en cursiva usando I, que viene de Italic</i> <br>
	</P>
	<p>Vamos a mezclarlo todo en un sólo párrafo con br b e i: <br> Escribo esta palabra en <b>negrita</b> y la
		siguiente en <i>cursiva</i>.
		¿Qué te parece?</p>

	<p>En el siguiente párrafo vamos a aprender a hacer listas, que contienen <b>ul</b> y <b>li</b></p>
	<p>
		Esto es una lista <br>
	<ul>
		<li>primer elemento de la lista</li>
		<li>segundo</li>
		<li>tercero</li>
	</ul>
	</p>
	<p>En el lenguaje HTML no se consideran los retornos de carro y los espacios.
		Por ejemplo, la lista anterior la vamos a poner en una sólo línea. Ocupa menos espacio, pero es más dificil de
		interpretar</p>
	<p>
	<ul>
		<li>primero</li>
		<li>segundo</li>
		<li>tercero</li>
	</ul>
	</p>


</BODY>
</HTML>
```
[Volver al índice](#indice)

<a name="4"></a>
# Enlaces
Si por algo se lle llama al HTML un lenguaje de hipertextos es porque está lleno de hiperenlaces.

### Sintaxis
Un hiperenlace empieza y acaba con **A** y tiene varios parámetros. Veamos los más importantes:

- **href**: Es la fuente o destino del enlace. Será una URL o una ruta relativa a otra página del mismo website
- **target**: indica la forma en que se abrirá el enlace. Si no se indica el target el enlace se cargará en la propia página, si por ejemplo utilizamos un **target="_blank"** el enlace (src) se abrirá en otra pestaña del navegador.

### Ejemplo
```html
<a href="https://www.ua.es">Enlace a la web de la UA y cargarla aquí mismo</a>
<a href="https://www.ua.es" target="_blank">Enlace a la web de la UA en una nueva pestaña</a>
<a href="#marcador1">Ir al marcador 1</a>
```

### Marca (o ancla)
Para que un enlace se dirija a un marcador interno, es decir, a una zona de la propia página web, algo así como ir a un capítulo de un libro, es necesario indicar en la zona donde queremos que se enlace un ** marcador**.

El marcador tiene la sintaxis siguiente:
```html
<a name="marcador1"></a>
```
Para referirnos a ese marcador se utiliza el tag **a name** con esta sintáxis:
```html
<a name="#marcador1">Ir al marcador 1</a>
```

### Ejemplo marcador interno
Aquí tienes 2 enlaces a 2 marcadores internos
```html
<ul>
    <li>Ir al: <a href="#capitulo1">capitulo 1</a></li>
    <li>Ir al: <a href="#capitulo2">capitulo 2</a></li>
</ul>

<a name="capitulo1"></a>
<h3>Capítulo 1</h3>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>


<a name="capitulo2"></a>
<h3>Capítulo 2</h3>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>
```


### Ejemplo completo


```html
<HTML>

<HEAD>
	<TITLE> Enlaces </TITLE>
	<meta charset="UTF-8">
</HEAD>

<BODY>
	<!-- marca de inicio -->
	<A name="inicio">
		<!-- esto es un comentario, y nunca verás el resultado en la página. Sirve para ayudar a entender el código -->
		<H1>
			<CENTER> Enlaces </CENTER>
		</H1>
		<HR>
		<p>Tipos de enlace</p>
		<p>
			<ul>
				<li><b>Externos</b>: Formato &lt;A HREF="XXX"&gt; YYY &lt;/A&gt; <br>
					Ejemplo: Visita la web de la <A HREF="https://www.ua.es"> Universidad de Alicante </A><br>
					Descargar <a href="Curso de HTML.pdf">manual HTML</a> de la Univ. Valencia.
				</li>
				<li><b>Enlaces dentro de la misma página</b>: Se necesita un marcador (name)<br>
					Su estructura es, entonces:
					<b>&lt;A HREF="#MARCA"&gt; YYY &lt;/A&gt; </b><br>
					Y en el sitio exacto a donde queremos saltar, debemos poner la siguiente etiqueta. No olvides poner
					"#":
					<b>&lt;A NAME="MARCA"&gt; &lt;/A&gt; </b><br>
					Ejemplo: <br>
					Ir la <a href="#marca1">marca1</a> con el texto Loren ipsum. <br>
					Ir la <a href="#marca2">marca2</a> con el texto Loren ipsum con formato. <br>
				</li>
				<li>Enlaces dentro de las páginas web del mismo portal. Por ejemplo este manual<br>
					<p>
					<ul>
						<li><a href="pagina1.html">Estructura de un HTML</a></li>
						<li><a href="pagina2.html">Contenido</a></li>
						<li><a href="pagina3.html">Etiquetas</a></li>
						<li><a href="pagina4.html">Imágenes</a></li>
						<li><a href="pagina5.html">Enlaces</a></li>
						<li><a href="pagina6.html">Tablas</a></li>
					</ul>



					<p>Enlaces internos:</p>
					<ul>
						<li>Ir al: <a href="#capitulo1">capitulo 1</a></li>
						<li>Ir al: <a href="#capitulo2">capitulo 2</a></li>
					</ul>


					<a name="capitulo1"></a>
					<h3>Capítulo 1</h3>
					<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
						labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
						laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
						voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
						non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor
						sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
						labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
						laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
						voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
						non proident, sunt in culpa qui officia deserunt mollit anim id est laborum
						.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
						labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
						laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
						voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
						non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>


					<a name="capitulo2"></a>
					<h3>Capítulo 2</h3>
					<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
						labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
						laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
						voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
						non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor
						sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
						labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
						laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
						voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
						non proident, sunt in culpa qui officia deserunt mollit anim id est laborum
						.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
						labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
						laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
						voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
						non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>


		</p>
		</li>
		</ul>

		</p>


</BODY>

</HTML>

```
[Volver al índice](#indice)
<a name="6"></a>
# Tablas
Para crear una tabla utiliza el tag **TABLE**

Cada file tendrá un **TR**, excepto la primera, que contiene el nombre de las columnas, que tiene un **TH**

Dentro de cada fila (td) deberás de incluir un **TD**


### Parámetros:
Una tabla tiene multititud de parámetros para definir el borde, grosor, fondo, padding, espacio, etc.

En este [enlace a w3schools.com](https://www.w3schools.com/html/html_tables.asp) verás como usarlos

### Ejemplo
Veamos un ejemplo de una tabla con 3 columnas y 4 filas, donde la primera será la cabecera de las columnas
```html
   <TABLE>
		<TH>
			<TH>Columna 1</TH>
			<TH>Columna 2</TH>
			<TH>Columna 3</TH>
		</TH>
		<TR>
			<TD>fila1-celda1</TD>
			<TD>fila1-celda2</TD>
			<TD>fila1-celda3</TD>
		</TR>
		<TR>
			<TD>fila2-celda1</TD>
			<TD>fila2-celda2</TD>
			<TD>fila2-celda3</TD>
		</TR>
		<TR>
			<TD>fila3-celda1</TD>
			<TD>fila3-celda2</TD>
			<TD>fila3-celda3</TD>
		</TR>
	</TABLE>
```



<a name="7"></a>
# Imágenes
Una web sin imágenes es algo raro, así que debes de saber como utilizarlo

Una imagen utiliza el tag **IMG** paro no termina con **IMG**. Debes de tener en cuenta que el tag IMG tiene varias propiedades para usar la imagen, como indicar el origen de la imagen o fichero gráfico empleado, el tamaño, etc.

### Parámetros de imágen

- **src**: indica el origen de la imagen, que estará entrecomillado (simple o doble). Este parámetro, obviamente, es el único que es obligatorio. La ruta a la imagen puede ser **una URL **(ej: "http://sitioweb/fichero.jpg" o **relativa**, es decir, que está dentro de nuestro servidor local. Por ejemplo "carpeta/fichero.jpg"
- **width**: indica al ancho. Lo puedes indicar en **píxeles**, o en **porcentaje** (%)
- **height**: altura. Igual que el anterior.
- Hay varios parámetros más, pero estos son los más utilizados

> TIP: Si te has dado cuenta los mapas en la web se presentan como imágenes con un 100% de ancho y largo para ocupar toda la pantalla del navegador.

```html
<HTML>
	<HEAD>
		<TITLE> Imágenes </TITLE>
		<meta charset="UTF-8">
	</HEAD>
	<BODY>
		<!-- esto es un comentario, y nunca verás el resultado en la página. Sirve para ayudar a entender el código -->
		<H1> <CENTER> Imágenes </CENTER> </H1>

		<HR>
		<!-- una imagen utiliza la etiqueta IMG y tiene como argumento obligatorio el SRC o source, que es la ruta al archivo-->
		<p>Esto es una imagen. Fijate que en SRC añadimos la ruta a la carpeta donde está la imagen y usando "/"</p>
		<p>
			<IMG SRC="img/test-image-500x500.jpg">
		</p>
		<p>La siguiente imagen es muy grande (1280*768) y ocuparía toda la página, por eso utilizamos la opción WIDTH o HEIGHT para redimensionar.
		Ejemplo con width=200</p>
		<p>
			<IMG SRC="img/test.png" width="200">
		</p>
		<p>Lo mismo pero ahora utilizo HEIGHT</p>
		<p>
			<IMG SRC="img/test.png" height="200">
		</p>
		<p>Varios ejemplos de tamaño:<br>
		<IMG SRC="img/test.png" width="50">50 píxeles<br>
		<IMG SRC="img/test.png" width="100">100 píxeles<br>
		<IMG SRC="img/test.png" width="150">150 píxeles<br>
		</p>
		<p>También se puede utilizar el tamaño en % en vez de píxeles:<br>
		<IMG SRC="img/test.png" width="5%">5 %<br>
		<IMG SRC="img/test.png" width="10%">10 %<br>
		<IMG SRC="img/test.png" width="15%">15 %<br>
		</p>
		<p>Diferencias de fichero</p>
		<p>
			<ul><b>JPG</b>: Admite millones de colores. Ocupa muy poco tamaño, pero la compresión es a base de perder información, aunque sea imperceptible al ojo humano. Tampoco admite transparencia</ul>
			<ul><b>PNG</b>: Admite millones de colores. Ocupa muy poco más de tamaño, pero no tiene pérdida de información. Admite transparencias</ul>
			<ul><b>GIF</b>: Admite 256 colores. Ocupa muy poco y admite transparencia. Se utilizan también como animaciones. Es un formato propietario</ul>
		</p>		

		<p>
			<ul><b>JPG</b>: <img src="img/pantone.jpg"> </ul>
			<ul><b>PNG</b>: <img src="img/pantone.png"> </ul>
			<ul><b>GIF</b>: <img src="img/giphy.gif"></ul>
		</p>
		
		<p>El SRC puede ser una ruta a una URL (http://...../fichero imagen)</p>
			<ul><b>JPG</b>: <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Amanecer_en_la_playa.jpg/1024px-Amanecer_en_la_playa.jpg"> </ul>
			<ul><b>PNG</b>: <img src="https://upload.wikimedia.org/wikipedia/commons/2/24/Mapa_Ficha_de_pueblo_antiguo_colores.png"> </ul>
			<ul><b>GIF</b>: <img src="https://media.tenor.com/VVOA7SCKgmkAAAAC/test.gif"></ul>		
	</BODY>
</HTML>

```

[Volver al índice](#indice)
<a name="7">
# Estilos CSS

###Objetivo

Estilizar el contenido con colores, efectos, fuentes, etc.
Estas propiedades se escriben en un lenguaje que se llama CSS (estilos de cascada), y no dejan de ser propiedades para modificar la visualización de las etiquetas en el navegador

#### Ejemplo de CSS
```css
body {  background-color: grey;}

h1 {  
  color: blue;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}
```

Lo que se está indicando con el ejemplo indicado es que lo siguiente:

- la página web tendrá un fondo gris
-  el título H1 será  de color de fondo azul y justificado al centro
-  el párrafo usará la fuente verdana y un tamaño de 20 píxeles

### Manual
Aquí tienes un [enlace](https://lenguajecss.com/css/introduccion/que-es-css/) a un manual sobre CSS

### Tipos de estilo


|   Nombre       |Mediante                       |Descripción                  |
|----------------|-------------------------------|-----------------------------|
|Archivo CSS externo|Etiqueta: `<link rel="stylesheet" src="archivo.css">`     |El código se escribe en un archivo .css a parte. Recomendado.           |
|Bloque de estilos          |Etiqueta `<style>contenido</style>`            |El código se escribe en una etiqueta <style> en el documento HTML.            |
|Estilos en línea           |Atributo HTML: `style="..."`|El código se escribe en un atributo HTML style en una etiqueta.|

#### Estilo especificado en la propia etiqueta

Hay que añadir el parámetro **style** dentro de cualquier tag, como por ejemlo un párrafo (p).

```html
<p>Párrafo normal, sin estilo. El siguiente si que tiene estilo</p>
<p style="color:red;">Soy rojo</p>
<p style="color:blue;">Soy azul</p>
<p style="font-size:50px;">Soy muy grande</p>
<p style="color:blue;font-size:25px;">Combino estilos. Soy azul y mediano</p>
```

#### Tipo estilos en el HEAD
Lo que hemos indicado en el ejemplo anterior lo podemos poner dentro del tag HEAD, utilizando el tag **STYLE***

Veamos un ejemplo


```html
<!DOCTYPE html>
<html>

<head>
<!-- aquí coloco el style para fondo, h1 y párrafo -->
    <style>
        body {
            background-color: grey;
        }

        h1 {
            color: white;
            text-align: center;
        }

        p {
            font-family: verdana;
            font-size: 20px;
        }
    </style>
</head>

<body>
<!-- aquí se aplica el style -->
    <h1>Mi primer ejemplo CSS</h1>
    <p>Esto es un párrafo.</p>

</body>

</html>
```
#### Tipo enlace a un fichero
Lo único que hay que hacer es crear un fichero que tenga la extensión **.css**  con el contenido del estilo, pero sin el tag **style**

Veamos un ejemplo creando un fichero llamado **miestilo.css** con las mismas características vistas antes
```css
body {background-color: grey;}
h1 {
    color: white;
    text-align: center;
}
p {
    font-family: verdana;
    font-size: 20px;
}
```

En el HEAD debes de añadir la siguiente referencia a la ubicación del archivo **.css** que incluye el estilo.

```html
<link rel="stylesheet" href="/ruta_al_fichero/miestilo.css">
```
### Nombre para los estilos por identificador
Hasta ahora hemos aplicado estilos a los tags, de esta forma todos los tags de la misma categoría, por ejemplo párrafos, tendrán el mismo formato indicado en el estilo.

Sí queremos tener 2 estilos diferentes para los párrafos no podemos hacerlo. Para solventar este problema hay 2 opciones. 

- Utilizar un identificador como nombre (**id**) del tag
- utilizar un nombre de class (**class**) de estilo

##### Para los que tienen identificador
 El estilo tendrá un nombre cuando va precedido de un **#nombre_del id**

Por ejemplo vamos a crear 2 estilos diferentes para párrafos (o el tag que queramos), llamados para1 y para2

```html
#para1 {
  text-align: center;
  color: red;
}
#para2 {
  text-align: center;
  color: blue;
  font-weight: bold;
}
#para3 {  
  color: grey;
  font-weight: bold;
}
```

Para aplicarlos dentro del BODY podemos utilizarlo con el parámetro **id=nombre_del_identificador**. Veamos un ejemplo:

```html
<p id="para1"> Este parrafo estará centrado y será de color rojo </p>
<p id="para2"> Este otro parrafo estará también centrado y será de color azul </p>
<ul id="para3">
    <li>A esta lista le vamos a </li>
    <li>aplicar el estilo para1</li>
</ul>
```
> NOTA: No puede haber 2 tags que tengan el mismo identificador. Por ejemplo, esto es un error:

```html
<p id="para1"> Este parrafo estará centrado y será de color rojo </p>
<p id="para1"> Este otro parrafo estará también centrado y será de color azul </p>

```

### Nombre para los estilos por clase (class)

Se utiliza cuando queremos adjudicar un nombre para cada estilo, y aplicarlo siempre que queramos

Por ejemplo vamos a crear 3 estilos con nombres diferentes. Cada nombre va precedido de un punto (**.**)

```html
.estilo1 {
  text-align: center;
  color: red;
}
.estilo2 {
  text-align: center;
  color: blue;
  font-weight: bold;
}
.estilo3 {  
  color: grey;
  font-weight: bold;
}
```

La forma de aplicarlo es utilizando el parámetro **class="nombre_del_estilo_sin_punto"
```html
<p class="estilo1"> Este parrafo estará centrado y será de color rojo </p>
<p class="estilo2"> Este otro parrafo estará también centrado y será de color azul </p>
<p class="estilo1"> De nuevo reutilizo este  parrafo con el estilo llamado <b>estilo1</b> </p>
<ul class="estilo3">
    <li>A esta lista le vamos a </li>
    <li>aplicar el estilo para1</li>
</ul>
```
> NOTA: Como has podido comprobar hay 2 párrafos con la misma clase **para**1

### Ejemplo completo
```html
<HTML>

<HEAD>
	<TITLE> Estilos </TITLE>
	<meta charset="UTF-8">
	<link rel="stylesheet" href="css/mi_estilo.css" />
</HEAD>

<style>
	p.resaltado1 {
		background: yellow;
	}

	p.resaltado2 {
		background: red;
		color: white;
	}
</style>

<BODY>
	<!-- marca de inicio -->
	<A name="inicio">
		<!-- esto es un comentario, y nunca verás el resultado en la página. Sirve para ayudar a entender el código -->


		<H1>
			<CENTER> Estilos CSS </CENTER>
		</H1>
		<HR>
		<h2>Objetivo</h2>
		<p>Estilizar el contenido con colores, efectos, fuentes, etc.</p>
		<h2>Enlace web</h2>
		<p><a href="https://lenguajecss.com/css/introduccion/que-es-css/">Manual CSS</a></p>

		<table border>
			<thead>
				<tr>
					<th>Nombre</th>
					<th>Mediante...</th>
					<th>Descripción</th>
				</tr>
			</thead>
			<tbody>
				<tr>
					<td><strong>Archivo CSS externo</strong></td>
					<td>Etiqueta <code>&lt;link rel="stylesheet"&gt;</code></td>
					<td>El código se escribe en un archivo <code>.css</code> a parte. <strong>Recomendado</strong>.</td>
				</tr>
				<tr>
					<td><strong>Bloque de estilos</strong></td>
					<td>Etiqueta <code>&lt;style&gt;</code></td>
					<td>El código se escribe en una etiqueta <code>&lt;style&gt;</code> en el documento HTML.</td>
				</tr>
				<tr>
					<td><strong>Estilos en línea</strong></td>
					<td>Atributo HTML <code>style="..."</code></td>
					<td>El código se escribe en un atributo HTML <code>style</code> en una etiqueta.</td>
				</tr>
			</tbody>
		</table>



		<h2>Ejemplo 1</h2>
		<p>Si te fijas el color de fondo es azul claro, los H1 están en blanco y centrado, y los H2 son azules,
			y los párrafos están en verdana y tamaño 20px. Todos estos parámetros están escritos en el fichero
			<b>css/mi_estilo.css</b>
		</p>

		<h2>Ejemplo 2</h2>
		<p>Fíjate que también hemos añadido en el HEAD una etiqueta <b>style</b> que contiene un estilo para párrafos,
			pero que tienen un nombre. Se le llaman clases y sirve para diferenciar diferentes formas de dar estilo a
			una etiqueta. En este caso
			verás 2 párrafos con diferentes estilos, y en la etiqueta se añade la class</p>
		<pre>&lt;p class="resaltado1"&gt;Este párrafo utiiza el estilo p.resaltado1&lt;/p&gt;</pre>
		<p class="resaltado1">Este párrafo utiiza el estilo p.resaltado1</p>
		<p class="resaltado2">Este párrafo utiiza el estilo p.resaltado2</p>


		<h2>Ejemplo 3</h2>
		<p>El estilo también se puede añadir a cada etiqueta utilizando style, pero es poco frecuente. Veamos un ejemplo
		</p>
		<pre>&lt;p style="color:green;background:orange;"&gt;Ejemplo de estilo en la propia etiqueta&lt;/p&gt;</pre>
		<p style="color:green;background:orange;">Ejemplo de estilo en la propia etiqueta</p>

</BODY>

</HTML>
```

[Volver al índice](#indice)
<a name="8">
# Librería de estilos

Hay muchas librería de estilos que son utilizados hasta la saciedad en la gran mayoría de los portales webs. La ventaja es que ya están optimizados para usarse con facilidad, mostrando resultados rápidos con un mínimo esfuerzo.

Entre las más utilizadas se encuentran:

- [w3.css](https://www.w3schools.com/w3css/defaulT.asp):CSS propuesto por el W3C (World Wide Web Consortium). Mi preferido
- [Bootstrap](https://getbootstrap.com/): Seguramente será el más utilizado. Es el usado en UA Cloud en la Universidad de Alicante. Además de CSS incluye utilidades en Javascript

### W3.CSS
Vamos a ver un ejemplo utilizando la librería w3.css.

Lo primero que hay que hacer es referirse a la URL del fichero w3.css  en el HEAD:
```html
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
```

### Dar estilo en el BODY

Fíjate como con muy poco esfuerzo vamos a crear una página web con mucho estilo
```html
<div class="w3-container w3-teal">
  <h1>My Car</h1>
</div>

<img src="https://www.w3schools.com/w3css/img_car.jpg" alt="Car" style="width:100%">

<div class="w3-container">
  <p>Este es un coche deportivo clásico.</p>
</div>

<div class="w3-container w3-teal">
  <p>Créditos: <i>w3.css</i></p>
</div>
```

### Ejemplo comopleto

```html
<!DOCTYPE html>
<html>
<title>Ejemplo de uso del estilo W3.CSS</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">

<body>
    <div class="w3-container w3-teal">
        <h1>My Car</h1>
    </div>

    <img src="https://www.w3schools.com/w3css/img_car.jpg" alt="Car" style="width:100%">

    <div class="w3-container">
        <p>Este es un coche deportivo clásico.</p>
    </div>

    <div class="w3-container w3-teal">
        <p>Créditos: <i>w3.css</i></p>
    </div>
</body>

</html>
```


### Práctica:
Visita la web de w3.css y utiliza alguno de los ejemplos indicados, como por ejemplo paneles (panel), tarjetas (cards), etc.

<a name="9">
# Contenedores (DIV)

### Definición
En HTML, la etiqueta   `<div>`  es un contenedor genérico de bloque para otros elementos. Se puede posicionar donde uno quiera usando style. Un contenedor puede tener también un nombre. Un ejemplo de un div es un formulario con botones, cajas de texto, etc.

Ejemplo:
```html
		<div>
		  <h2>Madrid</h2>
		  <p>Madrid es la capital de ESpaña</p>
		  <p>Tiene 4 millones de habitantes</p>
		</div>
```
Verás que el resultado es igual que si no hubiese un **div**

### Contenedor con nombre y estilo
El div casi siempre tiene un identificador (**id**), y los programadores le asignan un estilo a ese div

Vamos a crear 2 contenedores, cada uno tendrá asignado un nombre


```html
		<div id="nombre_div_1" class="miClassDiv1">		  
		  <p>Contenido del div 1. Fíjate en el estilo llamado <b>miClassDiv1</b></p>
		</div>
		<br>
		<div id="nombre_div_2" class="miClassDiv2">		  
		  <p>Contenido del div 2. Fíjate en el estilo llamado <b>miClassDiv2</b></p>
		</div>
```

También vamos a crear un **style** en el HEAD para que se formateen los divs con los estilos
```html
<style>
		#nombre_div_1 {
			font-family: 'Avenir Next LT Pro';
			font-weight: bold;
			border: 5px outset #00A4BD;
			color: #2D3E50;
			background-color: #EAF0F6;
			text-align: center;
		}
		#nombre_div_1 {
			font-family: Arial, Helvetica, sans-serif;
			font-weight: bold;
			border: 10px outset chocolate;
			color: blueviolet;
			background-color: antiquewhite;
			text-align: center;
		}
</style>
```html

El resultado será que cada contenedor se formateará con los estilos definidos en **#nombre_div_1** y **#nombre_div_2**

### Ejemplo completo

```html
<!DOCTYPE html>
<html lang="es-ES">
	<HEAD>
		<meta charset="UTF-8">
		<TITLE> Contenedores y colores </TITLE>
	</HEAD>
	
	<style>
		.miClassDiv1 {
			font-family: 'Avenir Next LT Pro';
			font-weight: bold;
			border: 5px outset #00A4BD;
			color: #2D3E50;
			background-color: #EAF0F6;
			text-align: center;
		}
		.miClassDiv2 {
			font-family: Arial, Helvetica, sans-serif;
			font-weight: bold;
			border: 10px outset chocolate;
			color: blueviolet;
			background-color: antiquewhite;
			text-align: center;
		}
		.miMapa {
			font-family: Arial, Helvetica, sans-serif;
			font-weight: bold;
			border: 10px outset chocolate;
			color: blueviolet;
			background-color: antiquewhite;
			text-align: center;
		}		
		#mapDiv { 
			width: 800px; height: 500px; 
			background-color: antiquewhite;
		}
	</style>
	


	<BODY>
	<h2>Contenedores</h2>
	<p>En HTML, la etiqueta <b>&lt;div&gt;</b> es un contenedor genérico de bloque para otros elementos. 
	Se puede posicionar donde uno quiera usando style. Un contenedor puede tener también un nombre</p>
	<p>Ejemplo:</p>
	<pre>
		&lt;div&gt;
		  &lt;h2&gt;Madrid&lt;/h2&gt;
		  &lt;p&gt;Madrid es la capital de ESpaña&lt;/p&gt;
		  &lt;p&gt;Tiene 4 millones de habitantes&lt;/p&gt;
		&lt;/div&gt;
	</pre>
	<p>Resultado:</p>
		<div>
		  <h2>Madrid</h2>
		  <p>Madrid es la capital de ESpaña</p>
		  <p>Tiene 4 millones de habitantes</p>
		</div>	
	
	<p>Div con nombres y estilos</p>
	<pre>
		&lt;div id="nombre_div_1" class="miClassDiv1"&gt;		  
		  &lt;p&gt;Contenido del div 1. Fíjate en el estilo llamado &lt;b&gt;miClassDiv1&lt;/b&gt;&lt;/p&gt;
		&lt;/div&gt;
		&lt;br&gt;
		&lt;div id="nombre_div_2" class="miClassDiv2"&gt;		  
		  &lt;p&gt;Contenido del div 2. Fíjate en el estilo llamado &lt;b&gt;miClassDiv2&lt;/b&gt;&lt;/p&gt;
		&lt;/div&gt;
	</pre>
	<p>Resultado</p>
		<div id="nombre_div_1" class="miClassDiv1">		  
		  <p>Contenido del div 1. Fíjate en el estilo llamado <b>miClassDiv1</b></p>
		</div>
		<br>
		<div id="nombre_div_2" class="miClassDiv2">		  
		  <p>Contenido del div 2. Fíjate en el estilo llamado <b>miClassDiv2</b></p>
		</div>
		
	<p>Y ahora un div con un nombre espacial</p>
	
	<p>Ejemplo</p>
	<pre>&lt;div id="mapDiv"&gt;Hola, soy un div llamado <b>divMapa</b> donde en un futuro habrá un mapa&lt;/div&gt;</pre>
	<p>Resultado</p>
	<div id="mapDiv">Hola, soy un div donde en un futuro habrá un mapa. Fíjate en el style</div>

	</BODY>
</HTML>
```

[Volver al índice](#indice)
<a name="10">
# Colores

Los colores se pueden formar de varias formas.

En este ejemplo vamos a representar el mismo color de 3 formas diferentes:

| Forma          |Ejemplo                        |Resultado                    |
|----------------|-------------------------------|-----------------------------|
|RGB             |`	rgb(255, 99, 71)`           | <span style="background-color:rgb(255,99,71)">resultado</span>          |
|Nombre color    |`tomato`                       |<span style="background-color:tomato">resultado</span>            |
|Notación HTML   |`#ff6347`                      |<span style="background-color:#ff6347">resultado</span>|

### Algunos nombres de colores


| Nombre del color | Color de fondo       |
|------------------|----------------------|
| Red              | $${\color{red}Red}$$ |
| Green            | $${\color{green}Green▆}$$  |
| Blue             | $${\color{blue}Green}$$ |
| Yellow           | $${\color{yelow}yelow}$$ |
| Cyan             | $${\color{cyan}cyan}$$ |
| Magenta          | $${\color{magenta}magenta}$$ |
| Black            | $${\color{black}black}$$ |
| White            | $${\color{white}white}$$ |
| Gray             | $${\color{gray}gray}$$ |
| Orange           | $${\color{orange}orange}$$ |
| Pink             | $${\color{pink}pink}$$ |
| Purple           | $${\color{purple}purple}$$ |
| Brown            |$${\color{brown}brown}$$ |





### Ejemplo
Aquí tienes un HTML con una tabla con los nombres de los colores y su representación
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Colores HTML</title>
    <style>
        table {
            width: 50%;
            border-collapse: collapse;
            margin: 20px auto;
            font-family: Arial, sans-serif;
        }
        th, td {
            border: 1px solid #ccc;
            padding: 10px;
            text-align: center;
        }
        th {
            background-color: #f4f4f4;
        }
    </style>
</head>
<body>
    <table>
        <thead>
            <tr>
                <th>Nombre del Color</th>
                <th>Color</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Red</td>
                <td style="background-color: red;"></td>
            </tr>
            <tr>
                <td>Green</td>
                <td style="background-color: green;"></td>
            </tr>
            <tr>
                <td>Blue</td>
                <td style="background-color: blue;"></td>
            </tr>
            <tr>
                <td>Yellow</td>
                <td style="background-color: yellow;"></td>
            </tr>
            <tr>
                <td>Orange</td>
                <td style="background-color: orange;"></td>
            </tr>
            <tr>
                <td>Purple</td>
                <td style="background-color: purple;"></td>
            </tr>
            <tr>
                <td>Pink</td>
                <td style="background-color: pink;"></td>
            </tr>
            <tr>
                <td>Brown</td>
                <td style="background-color: brown;"></td>
            </tr>
            <tr>
                <td>Gray</td>
                <td style="background-color: gray;"></td>
            </tr>
            <tr>
                <td>Black</td>
                <td style="background-color: black;"></td>
            </tr>
            <tr>
                <td>White</td>
                <td style="background-color: white; border: 1px solid #ccc;"></td>
            </tr>
        </tbody>
    </table>
</body>
</html>

```

[Volver al índice](#indice)
<a name="11"></a>
# Formularios

### Definición

Los formularios HTML son elementos de las páginas web que nos sirven para recuperar información del usuario y enviarla al servidor para que pueda ser procesada.

En este [enlace](https://www.manualweb.net/html/formularios-html/) aprenderás más


Un formulario debemos de entenderlo como un contenedor de objetos de formulario. La sintaxis para definir un formulario será mediante el elemento **form**:
```html
<form>...</form>
```

### Tipo de objetos de formulario


Dentro de los campos que podemos incluir en formularios HTML encontramos los siguientes:

- Campos de texto, de contraseña, de fichero, etc.
- Checkbox
- Radios
- Áreas de texto
- Combos de selección
- Botones (por supuesto)

#### Cajas de texto

Caja de texto normal
```html
<input type="text" name="username" size="15" />
```

Caja de texto para contraseña
```html
<input type="password" name="password" size="15" />
```

#### Área de texto
Se utiliza para escribir mucho texto en varias líneas
```html
<textarea cols="40" name="comments" rows="6">Commentarios...</textarea>
```
#### Fichero
```html
<input type="file" name="fichero" size="35" />
```html

#### Checkbox
Son cajas de selección. Se pueden elegir varios

```html
<input type="checkbox" name="checkboxes[]" value="cb1" /> Rojo
<input type="checkbox" name="checkboxes[]" value="cb2" /> Azul
<input type="checkbox" name="checkboxes[]" value="cb3" checked="checked" /> Morado
<input type="checkbox" name="checkboxes[]" value="cb4" /> Naranja
```

> Fíjate que el tercero ya está **seleccionado (checked)**

#### Botones tipo radio 
Es igual que el anterior, pero sólo permite seleccionar uno

```html
<input type="radio" name="radioval" value="rd1" />tarde</input>
<input type="radio" name="radioval" value="rd2" checked="checked" />mañana</input>
<input type="radio" name="radioval" value="rd3" />noche</input>

#### Caja con múltiples valores 

Utiliza el tag **select** . Te permite elegir en una caja uno o varios valores. Cada elemento tiene un tag **option**
```html
<select multiple="multiple" name="multipleselect[]"	size="4">
   <option value="ms1">Lectura</option>
   <option value="ms2">Deportes al aire libre</option>
   <option value="ms3">Redes sociales</option>
   <option value="ms4">TV online</option>
   <option value="ms5">Pasear</option>
</select>
```
Si tiene activado la opción  **multiple="multiple"** te permite seleccionar varios

#### Combo desplegable

También es un campo de tipo **select** pero de una sóla línea y la opción de expandirse
Se utiliza para indicar una selección entre múltiples elementos. 

Cada elemento se denomina **option**, y tiene 2 parámetros, el nombre y el valor (**value**) que se le pasa al formulario cuando el usuario selecciona un elemento del desplegable.


##### Ejemplo con provincias

```html
<select name="ciudad">
  <option value="00" >OTROS</option>
  <option value="02"  selected="selected">Albacete</option>
  <option value="03" >Alicante/Alacant</option>
  <option value="04" >Almería</option>
</select>
```

> TIP: Fíjate que está selecconada la opción nº 02 con la palabra **selected**

#### Botones
Los formularios deben de tener asociado algún evento, como cancelar o enviar los datos a algún sitio

Los botones tienen asociado el tag **button**

Veamos algunos ejemplos
```html
<button name="rechazar" type="button">Cancelar</button>
<button name="aceptar"  type="button">Aceptar</button>	
<button name="test"     type="button" onClick="alert('hola alumno')">Test JS</button>
```

> TIP: Fíjate en el último de los botones. Tiene asociada una acción cuando el usuario hace click. Esto lo entenderás mejor cuando veas la parte de **Javascript**

### Práctica
Crea un html con un formulario para realizar la matrícula de un alumno con estos campos:

- nombre
- apellidos
- contraseña
- estudios, con 3 opciones tipo radio: 1. Geografía, 2. Historia, 3. Filología
- provincia: desplegable con todas las provincias de España
- código postal
- intereses: 3 checkbox: lectura, informática, juegos


### Ejemplo completo

```html
<!DOCTYPE html>
<html lang="es-ES">

<HEAD>
    <meta charset="UTF-8">
    <TITLE> Formularios </TITLE>
</HEAD>

<BODY>
    <H1>
        <CENTER> Formularios </CENTER>
    </H1>
    <HR>
    <h2>¿Qué es un formulario?</h2>
    <p>Los formularios HTML son elementos de las páginas web que nos sirven para recuperar información del usuario y
        enviarla al servidor para que pueda ser procesada.</p>
    <p>En este <a href="https://www.manualweb.net/html/formularios-html/">enlace</a> aprenderás más</p>
    <p>La sintaxis para definir un formulario será mediante el elemento form:</p>
    <pre>&lt;form&gt;...&lt;/form&gt;</pre>

    <h2>Campos de formularios</h2>
    <p>Dentro de los campos que podemos incluir en formularios HTML encontramos los siguientes:</p>
    <ul>
        <li>Campos de texto, de contraseña, de fichero, etc.</li>
        <li>Checkbox</li>
        <li>Radios</li>
        <li> Áreas de texto</li>
        <li>Combos de selección</li>
        <li>Botones (por supuesto)</li>
    </ul>

    <h2>Ejemplo</h2>
    <div id="miFormulario">
        <form name="HTMLFormElements" action="the_form_processor.php" method="post" id="HTMLFormElements">
            <p>Campo <b>input text</b>: Usuario</p>
            <p>
                Nombre usuario:<br>
                <input type="text" name="username" size="15" />
            </p>
            <p>Campo <b>input password</b>:Constraseña</p>
            <p>
                Contraseña:<br>
                <input type="password" name="password" size="15" />
            </p>
            <p>Campo <b>textarea</b>: Comentario</p>
            <p>
                <textarea cols="40" name="comments" rows="6">Commentarios...</textarea>
            </p>
            <p>Campo <b>input file</b>: Fichero</p>
            <p>
                Selecciona un fichero <br>
                <input type="file" name="fichero" size="35" />
                <input type="hidden" name="campoOculto" value="valor campo oculto" />
            </p>
            <p>Campo <b>Checkbox</b>: Selecciona los colores frios</p>
            <p>
                <input type="checkbox" name="checkboxes[]" value="cb1" /> Rojo
                <input type="checkbox" name="checkboxes[]" value="cb2" /> Azul
                <input type="checkbox" name="checkboxes[]" value="cb3" checked="checked" /> Morado
                <input type="checkbox" name="checkboxes[]" value="cb4" /> Naranja
            </p>
            <p>Campo <b>Radio</b>: Selecciona el momento del día en que te encuentras ahora</p>
            <p>
                <input type="radio" name="radioval" value="rd1" />tarde
                <input type="radio" name="radioval" value="rd2" checked="checked" />mañana
                <input type="radio" name="radioval" value="rd3" />noche
            </p>
            <p>Campo Múltiples valores (<b>select multiple</b>). Selecciona tus hobbies favoritos</p>
            <p>
                <select multiple="multiple" name="multipleselect[]" size="4">
                    <option value="ms1">Lectura</option>
                    <option value="ms2">Deportes al aire libre</option>
                    <option value="ms3">Redes sociales</option>
                    <option value="ms4">TV online</option>
                    <option value="ms5">Pasear</option>
                </select>
            </p>
            <p>Combo desplegable (<b>Select</b>): Donde vives</p>
            <p>
                <select name="ciudad">
                    <option value="00">OTROS</option>
                    <option value="02" selected="selected">Albacete</option>
                    <option value="03">Alicante/Alacant</option>
                    <option value="04">Almería</option>
                    <option value="01">Araba/Álava</option>
                    <option value="33">Asturias</option>
                    <option value="05">Ávila</option>
                    <option value="06">Badajoz</option>
                    <option value="07">Balears, Illes</option>
                    <option value="08">Barcelona</option>
                    <option value="48">Bizkaia</option>
                    <option value="09">Burgos</option>
                    <option value="10">Cáceres</option>
                    <option value="11">Cádiz</option>
                    <option value="39">Cantabria</option>
                    <option value="12">Castellón/Castelló</option>
                    <option value="13">Ciudad Real</option>
                    <option value="14">Córdoba</option>
                    <option value="15">Coruña, A</option>
                    <option value="16">Cuenca</option>
                    <option value="20">Gipuzkoa</option>
                    <option value="17">Girona</option>
                    <option value="18">Granada</option>
                    <option value="19">Guadalajara</option>
                    <option value="21">Huelva</option>
                    <option value="22">Huesca</option>
                    <option value="23">Jaén</option>
                    <option value="24">León</option>
                    <option value="25">Lleida</option>
                    <option value="27">Lugo</option>
                    <option value="28">Madrid</option>
                    <option value="29">Málaga</option>
                    <option value="30">Murcia</option>
                    <option value="31">Navarra</option>
                    <option value="32">Ourense</option>
                    <option value="34">Palencia</option>
                    <option value="35">Palmas, Las</option>
                    <option value="36">Pontevedra</option>
                    <option value="26">Rioja, La</option>
                    <option value="37">Salamanca</option>
                    <option value="38">Santa Cruz de Tenerife</option>
                    <option value="40">Segovia</option>
                    <option value="41">Sevilla</option>
                    <option value="42">Soria</option>
                    <option value="43">Tarragona</option>
                    <option value="44">Teruel</option>
                    <option value="45">Toledo</option>
                    <option value="46">Valencia/València</option>
                    <option value="47">Valladolid</option>
                    <option value="49">Zamora</option>
                    <option value="50">Zaragoza</option>
                    <option value="51">Ceuta</option>
                    <option value="52">Melilla</option>
                </select>
            </p>
            <p>Botones <b>button</b></p>
            <p>
                <button name="rechazar" type="button">Cancelar</button>
                <button name="aceptar" type="button">Aceptar</button>
                <button name="test" type="button" onClick="alert('hola alumno')">Test JS</button>
            </p>
        </form>

    </div>

</BODY>

</HTML>
```

[Volver al índice](#indice)
<a name="12"></a>
# JavaScript
Sí con el CSS la web se enriquece visualmente, la interacción viene de la mano de Javascript. Si quieres darle **magia** a tu web debes de conocer este lenguaje. 

Como todos los lenguajes de programación tiene su complicación, pero nuestro objetivo es conocer los principios básicos.

# Definición
Tal como se indica en casi todas partes **JavaScript** es 

> JavaScript es un lenguaje de programación o de secuencias de comandos que te permite implementar funciones complejas en páginas web, cada vez que una página web hace algo más que sentarse allí y mostrar información estática para que la veas, muestra oportunas actualizaciones de contenido, mapas interactivos, animación de Gráficos 2D/3D, desplazamiento de máquinas reproductoras de vídeo, etc., puedes apostar que probablemente JavaScript está involucrado. Es la tercera capa del pastel de las tecnologías web estándar, junto con el HTML y CSS.

[Fuente](https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps/What_is_JavaScript)

Es importante que entiendas que Javascript se ejecuta dentro del navegador, y por tanto forma parte del cliente. Esto verás que no es del todo es cierto, y más desde que apareció **NODE.JS**, capaz de ejercer funciones de servidor.

### HTML5
Seguramente habrás oido este acrónimo, y hace refenencia a la unión de tres elementos: HTML + CSS + JAVASCRIPT

Es importante que entiendas que estos 3 elementos están muy unidos entre sí.

Otra cosa importante que necesitas saber es que Javascript suele ejecutarse cuando se desencadena un evento, que puede ser cualquier cosa: evento al abrirse la página web, evento al hacer click en un botón, evento al pasar el ratón por algo, o incluso en un dispositivo móvil sería un evento al arrastrar el dedo sobre algún objeto.


### Código

El código Javascript, y a partir de ahora me referiré como **JS** lo podemos incluir donde queramos, utizando el tag **SCRIPT**

Al igual que en el CSS tenemos 3 formas diferentes de llamar a un código JS:

1. Referenciar a un archivo **.js** que incluya el código en Javascript
2. Incluir entre el tag `<SCRIPT>`  la funcionalidad deseada
3. Asociarla a un elemeno indicando el evento

# JS asociado a un elemento

Vamos por el final. Imaginemos que queremos lanzar un evento asociado al click de un botón. Tenemos que incluir la funcionalidad asociada al mismo utilizando el evento especificado. En este caso el evento es **onClick**, es decir, cuando hacemos click en un botón
```html
<button onclick="alert('Hola amigo');">Haz clic aquí</button> 
```
El código JS es muy sencillo. Sólo consta de una línea
```js
alert('Hola amigo');
```

Al oprimir saldrá una alerta con un mensaje. 

> TIP: Cada línea de JS debe de terminar en un ";"

Crea una página web e incluye esta línea. Comprueba el resultado

## JS en el elemento, y con el tag SCRIPT

Vamos a crear un botón con una única llamada a una función que estará escrita en un tag SCRIPT, que se ejecutará cuando hagamos un clic

En el botón añado este evento:

```html
<button onclick="saluda();">Haz clic aquí</button> 
```
También voy a crear un contenedor vacio con un identificador  para que escriba lo que yo quiera cuando se lance el evento
```html
<div id="miContenedor"></div> 
```

Ahora vemos a incluir un código JS dentro del tag SCRIPT que defina la función **saluda()**
```js
<script>
function saluda() {
  document.getElementById("miContenedor").innerHTML = "Hola mundo. Estoy aquí creando mi primera función JS";
}
</script>
```
Además, para que sea HTML5 vamos a asociar un estilo al div **miContenedor**

Este HTML completo sería así
```html
<!DOCTYPE html>
<html>
<style>
#miContenedor { 
  font-family: Arial, Helvetica, sans-serif;
  font-weight: bold;
  border: 10px outset chocolate;
  color: blueviolet;
  background-color: antiquewhite;
  text-align: center;
}
</style>
<body>
<h1>HTML DOM eventos</h1>
<h2>Evento click</h2>

<p>Ejemplo básico para escribir texto en un contenedor vacío llamado miContenedor</p>
<p>El evento se lanza al hacer click en el botón</p>

<button onclick="saluda();">Haz clic aquí</button> 

<p id="miContenedor"></p>

<script>
function saluda() {
  document.getElementById("miContenedor").innerHTML = "Hola mundo. Estoy aquí creando mi primera función JS";
}
</script>

</body>
</html>
```

## JS en un fichero
Sí queremos que todo el HTML quede más limpio podemos incluir referencia al archivo JS y al CSS. Ahora vamos a crear 2 botones, y 2 funciones, una para saludar, y otra para despedirse.

a) Contenido del archivo **misFunciones.js**
```js
function saluda() {
  document.getElementById("miContenedor").innerHTML = "Hola mundo. Estoy aquí creando mi primera función JS";
}
function despedida() {
  document.getElementById("miContenedor").innerHTML = "Adios amigo. Ha sido un placer tenerte cerca";
}
```

b) Contenido del fichero **miestilo.css**
```css
#miContenedor { 
  font-family: Arial, Helvetica, sans-serif;
  font-weight: bold;
  border: 10px outset chocolate;
  color: blueviolet;
  background-color: antiquewhite;
  text-align: center;
}
```
c) Contenido del HTML


```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="miestilo.css">
  <script type="Javascript" src="misFunciones.js"></script>
</head>
<body>
  <h1>HTML DOM eventos</h1>
  <h2>Evento click</h2>

  <p>Ejemplo básico para escribir texto en un contenedor vacío llamado miContenedor</p>
  <p>El evento se lanza al hacer click en el botón</p>

  <button onclick="saluda();">Saluda</button> 
  <button onclick="despedida();">Despedida</button> 
  <p id="miContenedor"></p>

</body>
</html>
```

### Ejemplo completo

```html
<!DOCTYPE html>
<html lang="es-ES">

<HEAD>
	<meta charset="UTF-8">
	<TITLE> Javascript </TITLE>
</HEAD>
<script>
	function ocultame() {
		document.getElementById("miTexto").style.display = 'none';
	}
	function cambiaColor() {
		document.getElementById("miTexto").style.backgroundColor = "red";
	}

	function cambiaColorDiv(colorSel) {
		var colorSel = document.getElementById("colorSel").value;
		document.getElementById("miTexto").style.backgroundColor = colorSel;
	}
	function suma() {
		var num1 = Number(document.getElementById("valor1").value);
		var num2 = Number(document.getElementById("valor2").value);
		var sum = num1 + num2;
		document.getElementById("resultado").value = sum;
		//alert(sum.toString());
	}

	function operacion() {
		var num1 = Number(document.getElementById("valor1").value);
		var num2 = Number(document.getElementById("valor2").value);
		var sum = num1 + num2;
		document.getElementById("resultado").value = sum;
		//alert(sum.toString());
	}

	function variasOperaciones() {
		var num1 = Number(document.getElementById("valor1").value);
		var num2 = Number(document.getElementById("valor2").value);
		var getSelectedValue = document.querySelector('input[name="operacion"]:checked');
		if (getSelectedValue.value == "sumar") { document.getElementById("resultado").value = num1 + num2; }
		else if (getSelectedValue.value == "restar") { document.getElementById("resultado").value = num1 - num2; }
		else if (getSelectedValue.value == "multiplicar") { document.getElementById("resultado").value = num1 * num2; }
		else if (getSelectedValue.value == "dividir") { document.getElementById("resultado").value = num1 / num2; }
		else if (getSelectedValue.value == "potencia") { document.getElementById("resultado").value = Math.pow(num1, num2); }
		else { alert("falta algo") }
		//alert(getSelectedValue.value);
	}





	// Función para obtener el valor de una cookie por nombre
	function getCookie(name) {
		const cookies = document.cookie.split(';');
		for (let i = 0; i < cookies.length; i++) {
			const cookie = cookies[i].trim();
			if (cookie.startsWith(name + '=')) {
				return cookie.substring(name.length + 1);
			}
		}
		return null;
	}



	function crearGalleta() {
		// almacenar valores en la cookie
		// obtener color
		var hoy = new Date();
		var navegador = navigator.userAgent;
		var color = document.getElementById("color").value;
		// crear galleta
		//document.cookie = "color" + "=" + color + ";" + "navegador" + "=" + navegador + ";" + "fecha" + "=" + hoy + ";" ;
		document.cookie = "color=" + color;
		document.cookie = "navegador=" + navegador;
		document.cookie = "fecha=" + hoy;
		console.log(document.cookie);
		alert("Acabo de crear la galleta con los valores del color, tu navegador y la fecha.\n Si quieres verlo activa la consola (CTTL+Shitf+i)");

	}
	function verGalleta() {
		// ver valores en la cookie
		let x = document.cookie;
		alert("Esto es lo que se sobre ti:\n" + "tu color es " + getCookie("color") +
			"\ntu navegador es " + getCookie("navegador") +
			"\nhoy es " + getCookie("fecha"));
	} 
</script>




<BODY>


	<H1>
		<CENTER> Javascript. Empieza la magia </CENTER>
	</H1>
	<HR>
	<h2>¿Qué es Javascript?</h2>
	<p>Un lenguaje de programación para manipular el HTML y el CSS, y hacer lo que quieras</p>
	<p>Es importante que sepas que todo el código javascript se ejecuta en el cliente, osea, el navegador.</p>
	<p>En esta página web el código Javascript está incluido dentro de la página html entre los tags <B>SCRIPT</B></p>
	<pre>
			&lt;script&gt;
			console.log('Hola');
			&lt;/script&gt;
		</pre>
	<h2>Ejemplos</h2>
	<div id="miTexto">
		<h3>Este texto que pertenece al div miTexto se ocultará con Javascript cuando hagas click (evento onClick) en el
			botón de abajo.
			Entonces llamará a la función <b>ocultame</b></h3>
	</div>
	<button onclick="cambiaColor()">Cambia el color del div</button>
	<button onclick="ocultame()">Oculta el div miTexto</button>
	<hr>
	<button onclick="cambiaColorDiv(color)">Función con parámetros. Cambia el color del div</button>
	<select id="colorSel">
		<option>Selecciona un color</option>
		<option value="AliceBlue">AliceBlue</option>
		<option value="AntiqueWhite">AntiqueWhite</option>
		<option value="Aqua">Aqua</option>
		<option value="Aquamarine">Aquamarine</option>
		<option value="Azure">Azure</option>
		<option value="Beige">Beige</option>
		<option value="Bisque">Bisque</option>
		<option value="Black">Black</option>
		<option value="BlanchedAlmond">BlanchedAlmond</option>
		<option value="Blue">Blue</option>
		<option value="BlueViolet">BlueViolet</option>
		<option value="Brown">Brown</option>
		<option value="BurlyWood">BurlyWood</option>
		<option value="CadetBlue">CadetBlue</option>
		<option value="Chartreuse">Chartreuse</option>
		<option value="Chocolate">Chocolate</option>
		<option value="Coral">Coral</option>
		<option value="CornflowerBlue">CornflowerBlue</option>
		<option value="Cornsilk">Cornsilk</option>
		<option value="Crimson">Crimson</option>
		<option value="Cyan">Cyan</option>
		<option value="DarkBlue">DarkBlue</option>
		<option value="DarkCyan">DarkCyan</option>
		<option value="DarkGoldenRod">DarkGoldenRod</option>
		<option value="DarkGray">DarkGray</option>
		<option value="DarkGreen">DarkGreen</option>
		<option value="DarkKhaki">DarkKhaki</option>
		<option value="DarkMagenta">DarkMagenta</option>
		<option value="DarkOliveGreen">DarkOliveGreen</option>
		<option value="DarkOrange">DarkOrange</option>
		<option value="DarkOrchid">DarkOrchid</option>
		<option value="DarkRed">DarkRed</option>
		<option value="DarkSalmon">DarkSalmon</option>
		<option value="DarkSeaGreen">DarkSeaGreen</option>
		<option value="DarkSlateBlue">DarkSlateBlue</option>
		<option value="DarkSlateGray">DarkSlateGray</option>
		<option value="DarkTurquoise">DarkTurquoise</option>
		<option value="DarkViolet">DarkViolet</option>
		<option value="DeepPink">DeepPink</option>
		<option value="DeepSkyBlue">DeepSkyBlue</option>
		<option value="DimGray">DimGray</option>
		<option value="DodgerBlue">DodgerBlue</option>
		<option value="FireBrick">FireBrick</option>
		<option value="FloralWhite">FloralWhite</option>
		<option value="ForestGreen">ForestGreen</option>
		<option value="Fuchsia">Fuchsia</option>
		<option value="Gainsboro">Gainsboro</option>
		<option value="GhostWhite">GhostWhite</option>
		<option value="Gold">Gold</option>
		<option value="GoldenRod">GoldenRod</option>
		<option value="Gray">Gray</option>
		<option value="Green">Green</option>
		<option value="GreenYellow">GreenYellow</option>
		<option value="HoneyDew">HoneyDew</option>
		<option value="HotPink">HotPink</option>
		<option value="IndianRed">IndianRed</option>
		<option value="Indigo">Indigo</option>
		<option value="Ivory">Ivory</option>
		<option value="Khaki">Khaki</option>
		<option value="Lavender">Lavender</option>
		<option value="LavenderBlush">LavenderBlush</option>
		<option value="LawnGreen">LawnGreen</option>
		<option value="LemonChiffon">LemonChiffon</option>
		<option value="LightBlue">LightBlue</option>
		<option value="LightCoral">LightCoral</option>
		<option value="LightCyan">LightCyan</option>
		<option value="LightGoldenRodYellow">LightGoldenRodYellow</option>
		<option value="LightGray">LightGray</option>
		<option value="LightGreen">LightGreen</option>
		<option value="LightPink">LightPink</option>
		<option value="LightSalmon">LightSalmon</option>
		<option value="LightSeaGreen">LightSeaGreen</option>
		<option value="LightSkyBlue">LightSkyBlue</option>
		<option value="LightSlateGray">LightSlateGray</option>
		<option value="LightSteelBlue">LightSteelBlue</option>
		<option value="LightYellow">LightYellow</option>
		<option value="Lime">Lime</option>
		<option value="LimeGreen">LimeGreen</option>
		<option value="Linen">Linen</option>
		<option value="Magenta">Magenta</option>
		<option value="Maroon">Maroon</option>
		<option value="MediumAquaMarine">MediumAquaMarine</option>
		<option value="MediumBlue">MediumBlue</option>
		<option value="MediumOrchid">MediumOrchid</option>
		<option value="MediumPurple">MediumPurple</option>
		<option value="MediumSeaGreen">MediumSeaGreen</option>
		<option value="MediumSlateBlue">MediumSlateBlue</option>
		<option value="MediumSpringGreen">MediumSpringGreen</option>
		<option value="MediumTurquoise">MediumTurquoise</option>
		<option value="MediumVioletRed">MediumVioletRed</option>
		<option value="MidnightBlue">MidnightBlue</option>
		<option value="MintCream">MintCream</option>
		<option value="MistyRose">MistyRose</option>
		<option value="Moccasin">Moccasin</option>
		<option value="NavajoWhite">NavajoWhite</option>
		<option value="Navy">Navy</option>
		<option value="OldLace">OldLace</option>
		<option value="Olive">Olive</option>
		<option value="OliveDrab">OliveDrab</option>
		<option value="Orange">Orange</option>
		<option value="OrangeRed">OrangeRed</option>
		<option value="Orchid">Orchid</option>
		<option value="PaleGoldenRod">PaleGoldenRod</option>
		<option value="PaleGreen">PaleGreen</option>
		<option value="PaleTurquoise">PaleTurquoise</option>
		<option value="PaleVioletRed">PaleVioletRed</option>
		<option value="PapayaWhip">PapayaWhip</option>
		<option value="PeachPuff">PeachPuff</option>
		<option value="Peru">Peru</option>
		<option value="Pink">Pink</option>
		<option value="Plum">Plum</option>
		<option value="PowderBlue">PowderBlue</option>
		<option value="Purple">Purple</option>
		<option value="RebeccaPurple">RebeccaPurple</option>
		<option value="Red">Red</option>
		<option value="RosyBrown">RosyBrown</option>
		<option value="RoyalBlue">RoyalBlue</option>
		<option value="SaddleBrown">SaddleBrown</option>
		<option value="Salmon">Salmon</option>
		<option value="SandyBrown">SandyBrown</option>
		<option value="SeaGreen">SeaGreen</option>
		<option value="SeaShell">SeaShell</option>
		<option value="Sienna">Sienna</option>
		<option value="Silver">Silver</option>
		<option value="SkyBlue">SkyBlue</option>
		<option value="SlateBlue">SlateBlue</option>
		<option value="SlateGray">SlateGray</option>
		<option value="Snow">Snow</option>
		<option value="SpringGreen">SpringGreen</option>
		<option value="SteelBlue">SteelBlue</option>
		<option value="Tan">Tan</option>
		<option value="Teal">Teal</option>
		<option value="Thistle">Thistle</option>
		<option value="Tomato">Tomato</option>
		<option value="Turquoise">Turquoise</option>
		<option value="Violet">Violet</option>
		<option value="Wheat">Wheat</option>
		<option value="White">White</option>
		<option value="WhiteSmoke">WhiteSmoke</option>
		<option value="Yellow">Yellow</option>
		<option value="YellowGreen">YellowGreen</option>
	</select>
	<hr>
	<p><br></p>
	<div id="calculadora">
		Numero 1: <input type="text" id="valor1"><br>
		Numero 2: <input type="text" id="valor2"><br>
		Resultado: <input type="text" id="resultado"><br>
		<button onclick="suma()">Suma los 2 valores</button>
		<hr>
		<p> Escribe 2 números y selecciona una operación: </p>
		<input type="radio" name="operacion" value="sumar">Sumar<br>
		<input type="radio" name="operacion" value="restar">Restar<br>
		<input type="radio" name="operacion" value="multiplicar">Multiplicar<br>
		<input type="radio" name="operacion" value="dividir">Dividir<br>
		<input type="radio" name="operacion" value="potencia">Potencia<br>
		<button type="button" onclick="variasOperaciones()"> Realizar operación </button>
		<hr>
		<p>Uso de cookies</p>
		<p>NOTA: Sólo funciona en un servidor web (http://...), no en local (c:/...)</p>
		<select id="color">
			<option value="Select Color">Selecciona un color</option>
			<option value="yellow">Yellow</option>
			<option value="green">Green</option>
			<option value="red">Red</option>
		</select>
		<button type="button" onclick="crearGalleta()">Crear galleta</button>
		<button type="button" onclick="verGalleta()">Comer (ver) galleta</button>
	</div>

</BODY>
</HTML>
```

[Volver al índice](#indice)

