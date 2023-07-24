# Generación de página web con GitLab y Pelican

A continuación se indica **cómo generar una página web del repositorio** servida por GitLab. Para ello se cuenta con el mínimo de pasos a realizar mediante el uso de Pelican.

En el archivo [`pelicanconf.py`](pelicanconf.py) se hallan las configuraciones generales de la página (_título del proyecto, autor/grupo, bibliografía, , links de interés, etc_). El grupo que elija éste camino de deberá cambiar esas configuraciones según como le corresponda.


En la carpeta [_/content_](./content/) se encuentran las páginas, imágenes y archivo de bibliografía. Las páginas son escritas en lenguaje _**markdown**_ (el mismo que las celdas de texto en _jupyter notebooks_), donde cada archivo corresponde a una sección. En el ejemplo de la sección de [_**Introducción**_](./content/pages/introduction.md) se puede ver el títlo, categoría (**page**) y posición de dicha sección (**ordinal**) en la página. En el mismo hay ejemplos de mostrar figuras (ubicadas en directorio [`images`](./content/images/)) y referencias (especificadas en [`biblio.bib`](./content/biblio.bib)). También puede ser útil una herramienta para generar tablas como [esta](https://www.tablesgenerator.com/markdown_tables).


En general, los pasos para generar la página son los siguientes:

1. Modificar los archivos _.md_ mencionados anteriormente, que corresponden a las secciones de la página. Con el **IDE de GitLab** (_**Web IDE**_, a la izquierda de _**Clone**_ en el repositorio) se puede visualizar un preview del markdown usando _Ctrl+Shift+V_ dentro del archivo. Notar que con ésta preview no se verán las referencias a figuras ni a bibliografía.

2. Realizar un commit y push para actualizar los cambios en el repositorio. Los cambios hecho se pueden ver en el IDE dentro de Source Control (_Ctrl+Shift+G_). Por defecto (a menos que se vea encesario) usar la branch _main_:
__No, use the current branch "main"__.

3. Una vez hecho el commit y push, se inicia el proceso de creado de página. Se puede ver su estado en **CI/CD --> Pipelines** (puede demorar un minuto aproximadamente). En caso de que el proceso falle, comuncarse con el cuerpo docente responsable del uso de las páginas.

4. Una vez exitoso el proceso, se puede revisar la página en el enlace ubicado en **Settings --> Pages --> Access pages**