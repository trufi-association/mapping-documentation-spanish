# Barra superior: _Herramientas_ en JOSM

!!! note ""
	Yoviajo ([OSM Bolivia](https://wiki.openstreetmap.org/wiki/Bolivia)) tradujo la página al español. El trabajo original en inglés es desarrollado por Sören Reinecke ([Trufi Association](https://trufi-association.org))

Puedes haber visto![](josm-topbar-tools.png)

y te preguntas de qué se trata. Aquí te daré una vista general rápida.

## Preparando para que la utilidad sea útil

1. Necesitamos una vía una posición con la cual realizar acciones. La selección se volverá roja como![](josm-editor-selectway.png)

    Manteniendo presionada la tecla SHIFT y haciendo clic en otras vías podrás seleccionar más de una vía. Esto es necesario para que algunas funciones sean útiles.

2. Hacemos clic en _Herramientas_ en la barra superior: ![](josm-topbar-tools.png)

3. Entonces tenemos las siguientes opciones dependiendo de nuestra selección:
   
   - **Particionar vía**: Usado para crear dos vías a partir de una vía. Esto es útil cuando agregas una ruta a OSM y una vía es más larga que la ruta que sigue. Usualmente querrás partir en la posición donde la línea roja oscura toma su propio camino. (vea el gráfico arriba). Vea también mi [tutorial dedicado ](../split-ways/split-ways.md).
   - **Combinar vía**: Usado para crear una vía a partir de dos vías. Es lo opuesto de la funcionalida _Particionar vía_. Para que esta funcionalidad sea efectiva necesitarás dos vías seleccionadas manteniendo presionada la tecla SHIFT y seleccionándolas.
     - No Seleccionado: ![](josm-editor-twoways.png)
     - Seleccionado: ![](josm-editor-twowaysselected.png)
   - **Reservar dirección**: Used to reserve the direction of one or more ways. This just changes the technical direction how the data was entered (beginning to draw the way from left to right or backwards). Mappers use this tool just to make technical data more clean. This feature does not affect the interpretation of the data, it doesn't affect tags. **You likely don't need it.**
   - **Simplificar vía**: Used to remove unncessary nodes from a way. Technically a bunch of nodes connected to each other in a specified order represent a way. This is another option to make OSM data more beautiful, it does not affect the tags from the way itself. Nodes on a way usually don't have tags (are empty).
   - **Alinear nodos en un círculo**: Esta función hace lo que dice. Esta es otra funcionalidad que raramente necesitarás.
   - **Alinear nodos en una línea**: Útil si tienes un montón de nodos como diferentes puntos en un sistema de coordendas en matemáticas (e.g. representación de datos como una _nube_.) en un umbral especificado e.g. dentro de un rango de 0.5cm y quieres crear una línea a partir de este nodo, entonces esta función es para ti.
   - **Distribuir Nodos**: PorHacer: encuentra que hace y crea una explicación fácil de entender.
   - **Ortogonalizar Forma**: PorHacer: encuentra que hace y crea una explicación fácil de entender.
   - **Seguir línea**: Para que esto sea efectivo necesitas dos vías seleccionadas. Una vía puede compartir nodos con otra línea. Esta función continua dibujando esa línea.
   - **Agregar nodo**: Una vía es una representación de nodos conectados entre ellos en un orden lineal ordenado. Esta función agrega un nodo a la vía seleccionada y te pide ingresar sus coordenadas.
   - **Mover nodo**: Selecciona sólo un nodo para que esta función sea efectiva. Te pide ingresar sus nuevas coordenadas.
   - **Crear círculo**: Similar a la función _Alinear nodos en un círculo_ pero trabaja con sólo tres nodos.
   - **Fusionar nodos**: Para que esto sea efectivo necesitas sólo seleccionar los nodos de manera de fusionarlos juntos: Fusionando sus etiquetas.
   - **Unir nodo a la vía** Arregla el casamiento del nodo y vía seleccionados.
   - **Mover nodo sobre la vía**: Mueve e incluye el nodo seleccionado a la vía más cercana.
   - **Desconectar nodo de la vía**: Arregla la separación de un nodo o vía seleccionados.
   - **Despegar vías**: Duplica nodos compartidos por más de una vía.
   - **Unir áreas sobrepuestas**: Une un área (vía cerrada) que se sobrepone con otra área en esa área.
   - **Crear multipolígono**: Crea un multipolígono a partir de la selección de vías y nodos. Un multipolígono permite la exclusión de algo dentro de él y es útil en casos donde algo está en un área de una vía cerrada pero que tiene sus propios límites para hacer que sea más ingresar.
   - **Actualizar multipolígono**: Similar a la función previa pero actualiza el área con la vías y nodos seleccionados.
