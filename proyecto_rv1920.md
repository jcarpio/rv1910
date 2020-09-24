# Proyecto de Realidad Virtual
# Curso 2019-2020
### Versión del documento: 1.0.2

# Repositorios de proyectos realizados
### https://github.com/Joseram0n/ARBOL-SIMULATOR
### https://github.com/Riickyr91/L-Systems-OpenGL
### https://github.com/pablopcr/ArbolRV
### https://github.com/IdlCM4/RV_Root-like-structure
### https://github.com/n4rgel/RV-Angel-Aznar--Arbol-processing
### https://github.com/Narovik/LSystems
### https://github.com/FranBeltranM/Proyecto_LSystem
### https://github.com/steevenja9/RealidadVirtual
###

# Introducción

**Importante: este documento puede sufrir modificaciones durante el transcurso del cuatrimestre. Por favor, consulte la última versión del mismo en este repositorio** https://github.com/jcarpio/rv1920

El objetivo de este proyecto será crear un programa que utilice OpenGL para la creación y manipulación de un objeto en 3D. El objeto se creará a través de código y commandos de OpenGL no estando permitido la importación del objeto como una nube de puntos generado por otros medios (Blender, Unity, etc.). Como herramienta de desarrollo se permitirá el uso de C++ y Visual Studio (versiones 2017 o 2019) y/o la aplicación Processing [6].  Se creará un objeto 3D que represente la raiz de un árbol en 3D o bien un árbol en 3D con o sin raiz. Para la construcción del objeto puede seguir las indicaciones del artículo “Generation and visualization of root-like structures in a three-dimensional space”, Louise Y. Spek, 1997, así como las indicaciones que encontrará en L-system o Lindenmayer system [5].

En [1] se hace referencia a los cuadernos de **Leonardo da Vinci** dónde se describe su regla del diámetro al cuadrado para la ramificación de las ramas de un árbol. Esta regla también se puede aplicar a las raíces de los árboles. La aplicación repetida de esta regla en un programa recursivo produce los diámetros de las ramas. El programa calcula la orientación de las ramas en un espacio tridimensional. La visualización muestra que, a partir de una estructura simétrica relativamente simple es posible generar estructuras más complejas y asimétricas en forma de raíz modificando solo algunos parámetros. La introducción de la aleatoriedad en los valores de los parámetros produce estructuras que difieren considerablemente en su arquitectura. El artículo añade también una fuerza adicional para influir en la orientación de nuevas ramas en el espacio y aumentar la flexibilidad de la formación de la estructura.

En [5] se describen los resultados de investigación del biólogo y botánico teórico húngaro Aristid Lindenmayer de la Universidad de Utrecht (1925-1989) que permiten modelar el crecimiento de las plantas, pudiendo además modelar la morfología de muchos organismos.

Para la realización del proyecto se constituirán **equipos de 2 a 4 personas**.

## Requisitos para superar las prácticas de Realidad Virtual en el curso 2019-2020:

0. Realizar una aplicación que, utilizando OpenGL, cree un modelo en 3D siguiendo las indicaciones descritas anteriormente. Para la realización de este apartado puede utizar C++ y Visual Studio o bien Processing. Si realiza las dos versiones se considerará tarea opcional que puntuará como elemento extra.
1.	La aplicación debe disponer de algún método que permita variar los parámetos del algoritmo. Las opciones para este punto pueden ser  menús, entradas de formulario o bien la modificación de variables globales o locales dentro del programa. La opción que más puntuación dará sera el uso de menús o entradas de formulario, siendo la opción de modificación de variables la que dará una calificación más baja en este apartado.
2.	El algoritmo implementado para la construcción del objeto 3D podrá ser recursivo o iterativo. En este apartado se valorará más la calidad del resultado que la elección de un método u otro.
3.	Se valorará positivamente la aplicación de texturas al objeto creado de forma que simulen un árbol real. Punturá más alto aquel modelo que resulte más realista.
4.	Implementar movimientos de cámara que permitan visualizar las diferentes partes del objeto. Estos movimientos deben permiter la correcta visualización del objeto en 3D creado. Tendrá una puntuación más alta aquel proyecto que permita visualizar el objeto creado con más detalle.
5.	Implementar un juego en primera persona que consista en capturar objetos que están situados en las diferentes partes del árbol. El personaje irá saltando de una rama a otra de las raíces y de las ramas sobre la superficie. Cada objeto tendrá una puntuación diferente y ganará aquel jugador que consiga obtener más puntos a través de la captura de objetos y mediante el desplazamiento por las diferentes partes del árbol.

Para superar la práctica en los **equipos de dos personas** será necesario realizar al menos los **puntos 0, 1, 2 y 4**, valorándose la calidad de los resultados obtenidos. Con una ejecución correcta de estos apartados se obtendrá la calificación de 7 puntos en la práctica. Si alguno de los objetivos no es alcanzado en su totalidad y se realiza de forma imprecisa o con errores entre las diferentes partes del objeto, la puntuación se verá reducida. 

Para los **equipos de tres personas** será necesario realizar los **puntos 0, 1, 2, 3 y 4** para superar la práctica, obteniendo un **máximo de 7 puntos** si todos los objetivos están completados correctamente. 

En el caso de los **equipos de 4 personas** será necesario realizar al menos los **puntos 0, 1, 2 , 3, 4 y 5** para superar la práctica obteniendo un **máximo de 9 puntos** si todos los objetivos están completados correctamente.

Para conseguir los puntos restantes hasta **alcanzar los 9 puntos** los equipos podrán realizar alguna de las características no obligatorias para su grupo. Un punto por cada característica adicional realizada correctamente.

Adicionalmente se pueden **obtener puntos extra colaborando** con componentes de otros equipos en la realización del apartado 5. El profesor valorará el resultado obtenido en la realización del juego, otorgando a todos los participantes los mismos puntos adicionales hasta un máximo de 3 puntos extra. Esto obliga a los equipos de 4 personas a colaborar con componentes de otros equipos en la realización de alguna característica del juego y a aquellos componentes que deseen alcanzar la puntuación de 10 a colaborar para realizar algunas de las funcionalidades del juego.

Para la versión de OpenGL con Visual Studio, en la generación del objeto en 3D sólo está permitido utilizar los elementos que se muestran en las prácticas realizadas por el Profesor Francisco Moreno Velo. El objetivo del proyecto es aprender el uso de las directivas de OpenGL. Por lo tanto, debemos realizas las diferentes operaciones en el modo en que se muestran en las prácticas anteriormente citadas. Para cuestiones accesorias como manejo de ratón, u otros elementos adicionales si podrán utilizarse librerías adicionales.

Para la ejecución de los proyectos se utilizará el estándar GIT y deberá al menos conocer los comandos básicos y sus argumentos en línea de comando (_clone, add, commit, push y pull_). Mi recomendación es utilizar los accesos al repositorio a través de línea de comando sin utilizar herramientas gráficas para la gestión.

Uno de los modos de evaluar la participacion de los diferentes componentes del equipo en el proyecto será a través de los _commits_ registrados en los repositorios de los diferentes proyectos. Es **muy importante que los avances queden registrados en el repositorio** con las tareas asignadas a cada componente del equipo. Si estas tareas no quedan debidamente registradas, el **profesor podrá examinar a los componentes de un equipo** a traves de consultas sobre las diferentes partes realizadas en el proyecto, con el fin de evaluar su participación efectiva en el mismo.

Con el fin de gestionar de una forma más adecuada las diferentes tareas a realizar, se crearán Issues por cada tarea pendiente y se finalizarán añadiendo la palabra _fixes #<num_issue>_ dentro del comentario del comando _commit_.

Como material de apoyo se recomienda seguir las indicaciones de las sesiones de prácticas elaboradas por el profesor Francisco Moreno Velo [2]. Adicionalmente puede consultar el libro [3] "OpenGL 4 Shading Language Cookbook" de David Wolff, así como sus ejercios en el repositorio de GitHub [4].
 
## Referencias
[1] “Generation and visualization of root-like structures in a three-dimensional space”, Louise Y. Spek, 1997

[2] Material de las prácticas de laboratorio del profesor Francisco Moreno Velo.
       http://www.uhu.es/francisco.moreno/gii_rv/

[3] OpenGL 4 Shading Language Cookbook, David Wolff, 2011

[4] Example code from the OpenGL 4 Shading Language Cookbook, 3rd Edition.
       https://github.com/PacktPublishing/OpenGL-4-Shading-Language-Cookbook-Third-Edition
       
[5]  L-system or Lindenmayer system
     https://en.wikipedia.org/wiki/L-system
     
[6] Processing
    https://processing.org/
