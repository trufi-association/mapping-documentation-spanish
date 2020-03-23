# Barra superior: _Herramientas_ en JOSM

!!! note ""
	Yoviajo (OSM Bolivia) tradujo la página al español. El trabajo original en inglés es desarrollado por Sören Reinecke ([Trufi Association](https://trufi-association.org))

Puedes haber visto![](josm-topbar-tools.png)

y te preguntas de qué se trata. Aquí te daré una vista general rápida.

## Preparando para que la utilidad sea útil

1. Necesitamos una vía una posición con la cual realizar acciones. La selección se volverá roja como![](josm-editor-selectway.png)

    Manteniendo presionada la tecla SHIFT y haciendo clic en otras vías podrás seleccionar más de una vía. Esto es necesario para que algunas funciones sean útiles.

2. Hacemos clic en _Herramientas_ en la barra superior: ![](josm-topbar-tools.png)

3. Entonces tenemos las siguientes opciones dependiendo de nuestra selección:
   
   - **Particionar vía**: Used to make two ways out of one way. This is useful when you add a route to OSM and a way is longer than the route follows it. Usually you want to split at the position where the darkred line goes its own way. (see picture above). See also my [dedicated tutorial](../split-ways/split-ways.md).
   - **Combinar vía**: Used to make one way out of two ways. The opposite to the _Split way_ feature. For this feature to be effective you need two ways selected by holding down the SHIFT key and selecting them.
     - No Seleccionado: ![](josm-editor-twoways.png)
     - Seleccionado: ![](josm-editor-twowaysselected.png)
   - **Reservar dirección**: Used to reserve the direction of one or more ways. This just changes the technical direction how the data was entered (beginning to draw the way from left to right or backwards). Mappers use this tool just to make technical data more clean. This feature does not affect the interpretation of the data, it doesn't affect tags. **You likely don't need it.**
   - **Simplificar vía**: Used to remove unncessary nodes from a way. Technically a bunch of nodes connected to each other in a specified order represent a way. This is another option to make OSM data more beautiful, it does not affect the tags from the way itself. Nodes on a way usually don't have tags (are empty).
   - **Alinear nodos en un círculo**: This function does what it says. This is another feature you rarely need.
   - **Alinear nodos en una línea**: Useful if you have a bunch of nodes like different points in a coordinate system in maths (e.g. data representation as a _cloud_.) in a specified treshold e.g. within range of 0.5cm and you want to create a line out of this node then this function is for you.
   - **Distribuir Nodos**: ToDo: find out what it does and create an easy to understand explanation.
   - **Ortogonalizar Forma**: ToDo: find out what it does and create an easy to understand explanation.
   - **Seguir línea**: For this to be effective you need two selected ways. A way can share nodes with another line. This function continues drawing that line.
   - **Agregar nodo**: A way is a representation of nodes connected to each other in a sorted linear order. This function adds a node to the selected way and prompts you for entering its coordinates.
   - **Mover nodo**: Select just one node for this function to be effective. It prompts you entering its new coordinates.
   - **Crear círculo**: Similar to function _Align nodes in a circle_ but it works with just three nodes.
   - **Fusionar nodos**: For this to be effective you need to just select nodes in order to merge them together: Merging their tags.
   - **Unir nodo a la vía** Arrange a selected node's and a selected way's marriage.
   - **Mover nodo sobre la vía**: Moves and includes the selected node to the nearest way.
   - **Desconectar nodo de la vía**: Arrange a selected node's and a selected way's seperation.
   - **Despegar vías**: Duplicate nodes shared by more than one way.
   - **Unir áreas sobrepuestas**: Join an area (closed way) which overlaps with another area into that area.
   - **Crear multipolígono**: Create a multiploygon out of the selection of ways and nodes. A multipolygon allows the exclusion of something inside of it and is useful in cases where something is in the area of a closed way but which has its own boundaries for making entering something more difficult.
   - **Actualizar multipolígono**: Similiar to the previous function but updates the area with the selected ways and nodes.
