# Documentación

## Entender las relaciones en OSM

Las relaciones utilizan objetos existentes de la base de datos de OpenStreetMap para crear nuevos datos al conectar estos objetos. En OSM, existen diferentes tipos de relaciones, ver por ejemplo la [Relation 9373675](https://www.openstreetmap.org/relation/9373675), es una relación de bus con una calle: `type=route`.

---

![](streets.png)

Vemos aquí un grupo de calles y sus nombres. Las calles están representadas por uno o más caminos (ways). No podemos saber cuál línea de bus pasa por qué calle, por ejemplo, no sabemos si la ruta _Bus 101_ usa la _Avenida República_ o la _Avenida Oquendo_. Es donde las relaciones son útiles. Las relaciones permiten conectar calles con una ruta en este caso de transporte, para saber exactamente cual bus pasa por cual calle.

![](busroute.png)

La línea naranja muestra la ruta _Bus 101_. Lo que hay que hacer ahora es agregar esta información a OSM.

![](connected-streets.png)

Aquí vemos una pequeña parte de la relación del bus. Todo lo que es parte de la relación se muestra en rojo: significa que todas las calles en rojo son partes de la relación, quedando conectada la calle *Avenida República* con la *Avenida Oquenda*. Así que una relación es básicamente un conjunto de nodos y caminos en un orden específico, que describe un objeto de alto nivel (por ejemplo una ruta de bus) al solo combinar datos existentes.

![](relation-street-list.png)

JOSM puede mostrar los elementos (calles) de una relación no solo de manera gráfica pero también tabular. La tabla muestra una lista ordenada de arriba hacia abajo, de los caminos (ways) que son parte de una relación.



**En resúmen:** Las relaciones en OSM son objetos de alto nivel que construyen algo nuevo (como una ruta de bus) sobre datos de OpenStreetMap pre-existentes (por ejemplo calles (caminos mapeados)). Así que las relaciones pueden usarse para agregar rutas de bus u objetos mucho más elaborados, y hacer uso de infraestructuras ya agregadas.
