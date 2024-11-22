Para entender bien esta metodología hay que quedarse con 3 conceptos: bloque, elemento y modificador.

Bloque: Este es el contenedor central de todos nuestros elementos y modificadores. Los bloques son los que nos ayudan a separar las secciones de nuestro sitio. ¿Cuales son algunos contenedores?, bueno, tu ya los conoces: <header> <main> <section> <article> <footer> o incluso los <div>. Teniendo esto en cuenta, así es como nombramos los bloques con BEM:

<!--HTML:--> 
<section>
	<article class="news"></article> -> Bloque
</section>

<!--CSS:--> 
.news-> Bloque
Elemento: Lo que son los flex-items para el flex-container, son los elementos para el bloque. Un elemento en la metodología BEM es algo que contiene dentro un bloque. Algunos dirán que se nombra con dos guiones normales o dos guiones bajos, pero en realidad es como gustes, lo importante es aplicar la metodología Block-Element-Modifier.

<!--HTML:--> 
<section>
	<article class="news"> -> Bloque
		<h1 class="news__title"></h1> -> Elemento
		<p class="news__description"></p> -> Elemento
	</article>
</section >

<!--CSS:--> 
.news-> Bloque
.new__title -> Elemento
.news__description -> Elemento
Modificador: Un elemento puede repetirse, pero no es el caso de los modificadores. Porque tal como su nombre lo dice es algo modificado, diferente. Tomando el ejemplo anterior, ahora queremos que el titulo sea en mayúscula y que un párrafo azul y el otro normal.

<!--HTML:--> 
<section>
	<article class="news"> -> Bloque
		<h1 class="news__title--uppercase"></h1> -> Modificador
		<p class="news__description"></p>
		<p class="news__description--blue"></p> -> Modificador
	</article>
</section >

<!--CSS:--> 
.news-> Bloque
.new__title--uppercase {text-transform: uppercase;} -> Elemento modificado (modificador)
.news__description {} -> Elemento
.news__description--blue {color: blue;} ->  Elemento modificado (modificador)
Y nada más, esa es la metodología BEM. :D

Tome el ejemplo de aquí Puedes consultar la documentación en getbem .com

> Documentación

https://blog.ida.cl/desarrollo/metodologia-bem-desarrollo-front-end/