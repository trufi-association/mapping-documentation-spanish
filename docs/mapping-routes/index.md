# Mapear rutas de transporte informal

Este tutorial muestra cómo agregar rutas de transporte informal a OpenStreetMap. Para poder hacerlo debes primero tener [JOSM instalado](../installing-josm-on-linux/index.md) así como la [herramienta custom mapping tool](../installing-mapping-tool/index.md) (si requerido por tu comunidad). Para subir los cambios a OSM, necesitas tener JOSM [sincronizado](../oauth-josm/index.md) con tu cuenta de OpenStreetMap.

## Preparar un espacio de trabajo

1. Abre JOSM (en este tutorial se asume que ya lo tienes instalado). ![](josm-logo.png)

2. Una ventana debe abrirse, como sigue ![](josm-startpage.png)

3. Debes cargar primero los datos que recibiste de tu comunidad. Haz clic en _File_ en la barra superior: ![](josm-topbar.png)

4. Luego das clic en _Open_ desde el menú: ![](josm-file-menu.png)

5. Una caja de diálogo se abre, selecciona el archivo de tu comunidad. Ve a la ubicación donde guardaste el `*.geojson`, haz clic en este archivo y abrelo _Open_:![](josm-opendialog.png)

6. Espera que el proceso de carga haya terminado. Cuando terminó, la interfaz cambia, puedes ahora ver el editor: ![](josm-editor-overview.png)

7. Antes de comenzar el mapeo, necesitas preparar el editor y cargarle los datos de OSM. Carguemos primero los datos de OSM. Haz clic de nuevo en _File_ en la barra superior: ![](josm-topbar.png)

8. Y luego en _Download data..._: ![](josm-file-menu-downloaddata.png)

9. Empezamos a amar las ventanas emergentes. En ésta, probablemente no necesites ajustar el cuadro y límites que ves en el mapa porque JOSM hizo esto para tí ya que se adecuó al `*.geojson` que cargaste: ![](josm-downloaddialog.png)

10. Haz clic en _Download as new layer_. Si aparece que el área seleccionada es demasiado grande, cambia su tamaño volviendo a ese cuadro de diálogo, haz clic y arrastra el mouse sobre una parte más pequeña del área previamente seleccionada. Suelta el mouse para crear nuevos límites. Repite hasta que el sistema acepte el área seleccionada :)

11. Esto se ve más aceptable: ![](josm-editor-osmdataloaded.png)

12. Pero aún no estamos satisfechos, ¿verdad? Para tenerlo aún mejor, debemos agregar los mosaicos de OSM. Ve a _Imagery_ en la barra superior y luego seleccia _OpenStreetMap Carto (Standard)_. Magnifico, ¿no?

13. Echemos un vistazo rápido a la sección _Layers_ en el sitio superior derecho del editor.
    
    ![](josm-editor-layers.png)
    
    Por cierto, puedes cambiar el tamaño de las ventanas haciendo clic en los límites respectivos y arrastrándolos a la posición que desees.

15. El nombre del bloque se ve ahora así: ![](josm-editor-layers-aftertogpx.png)

16. Haz clic en el bloque de nuevo y selecciona
    
    - _Customize Colour_ primero,
    
    - Luego _Download from OSM along this track_
    
    - Y finalmente _Precache imagery tiles along this track_.

17. Haz clic de nuevo en le bloque y selecciona _Customize track drawing_, una nueva ventana emergente aparece: ![](josm-layers-customizedrawing.png)

18. En el campo de texto pegado a _Drawing width of GPX lines_, escribe la medida deseada de ancho en pixeles. Te recomiendo `5`. Y haz clic en _Okay_.

19. Oprime ALT+SHIFT+F1 para detener automaticamente la descarga de datos mientras te mueves en el mapa. En paralelo, haz clic en _File_ en la barra superior y luego _Download OSM data continuously_. Es una palanca. Luego, navega dentro del mapa hasta el final de la línea. Para navegar en el mapa, debes mantener presionada la tecla derecha del mouse mientras mueve el mouse. Usa la rueda del mouse para acercar o alejar el zoom. **La línea tiene dos extremidades: _inicio_ y _final_. Selecciona la que tiene la flecha que abre, y no la flecha que cierra.**
    
    - Final <-- Inicio
    
    - ![](josm-editor-arrowrule.png)

## Preparar los datos de OSM a lo largo de la ruta que queremos agregar

Antes de comenzar, necesitamos trabajar un poco los datos de OSM. En la última imagen puedes ver la línea de color rojo oscuro y la azul. La primera línea es la ruta del autobús y la segunda es la calle en OSM donde circula el autobús. Esta parte del tutorial muestra cómo convertir la primera línea en datos útiles.

Presiona ALT+SHIFT+F1 para parar/iniciar la descarga automática de datos mientras te mueves en el mapa. En paralelo haz clic en *File* en la barra superior y luego *Download OSM data continuously*. Es una palanca. Cuando te muevas en el mapa en un área donde no hay datos disponibles, enciende la palanca _Download OSM data continuously_. Si usas mucho la función de zoom, entonces mejor apaga esta palanca _Download OSM data continuously_.

1. Selecciona la línea que no es la roja más oscura, pero la que está alineada a ella: ![](josm-editor-selectedstreet.png)

2. No vemos que toda la línea se ponga roja. Lo que nosotros vemos como una sola línea (la azul), son dos diferentes para la computadora, porque la línea se ha dividido en el punto donde _Calle Campinas_ cruza la línea que seleccionamos.

3. Queremos crear una ruta, por lo que damos clic en el icono de línea en la barra de símbolos justo debajo de la barra de herramientas: ![](josm-symbolbar-busroute.png)

4. Una ventana emergente se abre, que te solicita los datos que recibiste de tu comunidad. Escribe los datos en los campos correspondientes y haz clic en _Okay_. Se abre una nueva ventana que da una descripción general: ![](josm-createrelation-overview.png)

5. En el sitio de la derecha, verás una lista de todos los objetos (calles) que has seleccionado en el editor JOSM. En el sitio de la izquierda, verás una lista de todos los objetos (calles) ya agregados a la relación. **¡No cierres ese diálogo, aún lo necesitamos!**

6. Selecciona otras calles a lo largo de la línea rojo oscuro, ve al diálogo de nuevo y haz clic en el bloque resaltado en rojo, donde seleccionas la última fila de tus cuatro filas, para agregar la selección a la lista de rutas en el sitio derecho.![](josm-createrelation-addafterlastmember.png) Puedes seleccionar varias calles a la vez manteniendo presionada la tecla de mayúsculas.

7. Repeat step _6_ after you have the following situation: ![](josm-editor-splitwaysneeded.png)

8. _Newton, we've got a problem!_ What do we next is spliting the way. So we click on the map to deselect our selection. Be sure to add all streets except the street in question to the route like in step _6_.

9. Select the street (way) in question. Zoom to the point where you need the split: ![](josm-editor-splitwaysneeded2.png)Zoomed in (cuted view):![](josm-editor-splitwaysneeded3.png)

10. Select the street (here in blue).

11. Hold down the key you use to write an upper letter at the beginning of a new sentence. Select the square (JOSM highlights it yellow) while holding down the key.![](josm-editor-splitwaysneeded4.png)

12. In the topbar click on _Tools_ and then on _Split way_. Alternatively press key _P_. A dialog prompts you to decide which way segment should preserve history. Just ignore it and click _Okay_. Deselect everything by clicking on a free space on the map.

13. Continue with step _6_ until the end of the darkred line.

14. When you reached the end of the darkred line, it means you are almost done. Now we need to validate your work. For that we go to the dialog you should leave open the whole time while mapping.

15. You should consult someone with validation if you're unfamilar with it. It's a critical part. Take a look on the different options the dialog offers you.
    
    - Select an entry from the list on the left site. Right click on it and click _Zoom to_ to zoom to that object on the map. Use this method to repair objects having the following symbol or similiar:![](josm-createvalidation-routelist-error.png)
    
    - Use the feature _Zoom to_ and the map to find missing ways (streets). and hover on the buttons of the highlighted red area next to the _selection_ table to get what they do with the selection.![](josm-createselection-validate.png)
    
    - Black is your friend :) Everything black in the validation line means that the data is okay.![](josm-createrelation-validate2.png)
    
    - The first and last entry show always a red symbol in the validation line because one end is not connected to another way (street). This is logical. A bus route usually ends somewhere.

16. In the route list dialog click _Okay_ to create that route. Do it when you think you're finish.

17. Click on the _Upload icon_ in the symbolbar right under the topbar: ![](josm-symbolbar-upload.png)

18. Ignore the dialogue _Suspicious data found_ when it popups or fix the issues. Inform your community about that and tell them what you've edited.

19. A new popup appears: ![](josm-uploaddialog.png)

20. Fil in the information requested and then click _Upload Changes_ to finish upload process.
