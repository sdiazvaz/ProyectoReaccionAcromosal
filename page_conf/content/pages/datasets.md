Title: Datasets
Date: 2023-07-03
Category: Page
Ordinal: 003

## Generalidades 

La base de datos disponible consta de un conjunto de archivos .tif, en donde cada uno de ellos presenta dos vieos, uno correspondiente al canal flúo y otro el canal membrana. 

El archivo .tif presenta 482 frames, 241 correspondientes a cada canal, en una resolución de 1024x1024. Los frames se encuentran intercalados, es decir, el frame 1 del archivo corresponde al frame 1 del canal flúo, mientras que el frame 2 del archivo corresponde al frame 1 del canal membrana. 


## Ejemplo

En los videos {#ej_video}  y {#ej_video_m} se puede apreciar un ejemplo de los canales fluo y membrana respectivamente, obtenidos de procesar un único archivo .tif. 

Como se puede apreciar, las cabezas de los espermatozoides se encuentran fijas, es decir, no se pueden mover, mientras que los espermatozoides pueden girar. 

Ademas, el canal fluo se observa más claramente la cabeza del espermatozoide, mientras que el canal membrana se observa de forma más uniforme la intensidad en la cabeza y cola. Es por esto que el primero nos permite ajustar y trackear elipses correspondientes a cada espermatozoide, mientras que el segundo se utiliza unicamente para la detección de la reacción

<video width="640" height="640" controls>
  <source src="../images/canal_fluo.mp4" type="video/mp4">
    <figcaption>
    ej_video :: Ejemplo de canal flúo.
    </figcaption>
</video>

<video width="640" height="640" controls>
  <source src="../images/canal_membrana.mp4" type="video/mp4">
    <figcaption>
    ej_video_m :: Ejemplo de canal membrana.
    </figcaption>
</video>