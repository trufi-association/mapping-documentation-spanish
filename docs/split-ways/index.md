# Documentación

!!! note ""
	Pionen ([OSM Latam](https://wiki.openstreetmap.org/wiki/ES:OSM_Latam)) tradujo la página al español. El trabajo original en inglés es desarrollado por Sören Reinecke ([Trufi Association](https://trufi-association.org))

## Dividir una vía en dos o más

Dividir vías (partir una vía en dos o más) puede ser necesario cuando se intenta agregar una relación que sigue una vía parcialmente y no hasta el final. Agregar una vía a una relación, sin dividirla, podría traer efectos secundarios no deseados. También es necesario dividir una vía cuando las etiquetas no son consistentes a lo largo de la vía (Del punto A al punto B las etiquetas podrían variar de aquellas del punto C al punto D).

![](josm-editor-splitwaysneeded.png)

La rojo oscura es nuestra ruta que queremos agregar a OSM como una relación. La de color rojo es la calle (vía) que ya tenemos en la base de datos de OSM. Vemos que en algún punto no coinciden. La vía (calle) en OSM no termina donde nuestra ruta comienza a seguir su propio recorrido. Eso significa que primero debemos dividir la calle en OSM en el punto que nuestra ruta sigue su propio camino.

## Dividir vías

Suponiendo que ya abriste JOSM y que te dirigiste a la vía que deseas dividir.

1. Haz clic sobre la vía que quieres dividir. Debería cambiar a color rojo: ![](josm-editor-splitwaysneeded.png)

2. Ahora mantén presionada la tecla _SHIFT_ (la que está sobre la tecla _Ctrl_) y selecciona un nodo de la vía resaltada donde quieres dividir la vía en dos. Por lo general, se requiere dividir la vía en el punto donde la línea rojo oscuro sigue su propio camino (posición: círculo azul).

   ![](josm-editor-splitwaysneeded2.png)

   ![](josm-editor-splitwaysneeded4.png)

       Después de seleccionarlo, debería cambiar a rojo.

4. En la barra superior haz clic en *Tools* y luego en *Split way*. Alternativamente puedes presionar la tecla *P*.![](josm-topbar-tools.png)

5. Un cuadro de diálogo te solicitará que indiques qué segmento debe conservar el historial. Simplemente ignóralo y presiona *Okay*. Deselecciona todo haciendo clic en un espacio libre sobre el mapa.
