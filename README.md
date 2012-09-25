
Visitas Virtuales HTML5
=======================


El objetivo de la aplicación es poder encadenar fotografias, permitiendo hacer recorridos virtuales por espacios existentes, o maquetas de flujo, a partir de imagenes fijas

Modelo de datos
---------------

Con la finalidad de poder realizar el grafo de navegacion, los datos se modelan en un archivo json con una estructura de esta forma:

 * Objeto Escena
```json
    {   
    "id" : "<hash_imagen>"
    , "file" : "url de la imagen"
    , "paths" : [ <array_de_objetos_path> ]
    , "title" : "Titulo corto de la imagen"
    , "description" : "Descripcion de la Escena"
    }
```

 * Objeto Path
```json
    {
        "points": [ <array de objetos point> ]
       , "color": "<color rgb>"
       , "destination":"<Escena.id>"    
    }
```

 * Objeto Point 
```json
    {
        "x":"coordenada x relativa al canvas"
        , "y":"coordenada y relativa al canvas"
    }
```

Editor
------
El editor permite cargar fotografias, dibujar los trazados, seleccionar el color de relleno, y completar el titulo y la descripción.

Visualizador
------------
Permite realizar el recorrido desde el navegador.



