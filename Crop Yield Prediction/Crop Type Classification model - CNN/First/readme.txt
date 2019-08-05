En la carpeta E:\Imágenes Satelitales\2017\226_86\1 se identificó una imagen satelital de buena calidad (tiene pocas nubes).
Sus coordenadas son 226 - 86 y agarra perfectamente la transecta de coronel pringles ubicada en el archivo T28_Pringles.

Los objetivos son los siguientes:

1. En un notebook de Jupyter lograr superponer la imágen satelital con la transecta y graficarla (aquí se tendrá que usar
solo un canal de los 7 disponibles o quizás dos o tres). Esto servirá para avanzar mejor con el objetivo 2, tener mejor feedback, etc.

2. Pararse en cada punto de la transecta y recortar un pedasito de la imágen satelital (digamos una seccion de 15 x 15 pixeles)
Generando así un conjunto de datos, cada uno de ellos con las siguientes dimensiones: 15 x 15 x 7. (el 7 es porque la imagen tiene 7 canales)
Cada uno de esos datos estará etiquetado en una clase determinada que dependerá del tipo de suelo. Digamos que algunas de esas imágenes recortadas
serán campo natural, otras barbecho, otras maiz, etc.

3. A partir de ese conjunto de datos, entrenar una red CNN programada con keras que permita clasificar imágenes en categorías de campo
(campo natural, barbecho, maíz, etc). Cabe destacar que dada la poca cantidad de puntos, por ahora, quizás lo mejor sea armar solo 2 
categorías: campo natural y OTROS, por ejemplo.






Cabe destacar que el recorte del paso 2 seguramente sea bien simple y no implique una identificación compleja. Esto implicará que algunas
imágenes contendran pedazos de ruta que podrían afectar al entrenamiento de la red, porque al fin y al cabo es ruido. Pero bueno, es un comienzo.
Si el dataset en el futuro es suficientemente grande, entonces la red aprenderá "que las rutas no son información relevante", supongo.

En la imágen "objetivo 1 - idea" se ve lo que prentendo lograr con el objetivo 1, solo que en vez de hacerlo en QGIS como está en la imágen, 
yo lo quiero hacer en jupyter notebook.