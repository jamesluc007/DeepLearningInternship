En la carpeta E:\Im�genes Satelitales\2017\226_86\1 se identific� una imagen satelital de buena calidad (tiene pocas nubes).
Sus coordenadas son 226 - 86 y agarra perfectamente la transecta de coronel pringles ubicada en el archivo T28_Pringles.

Los objetivos son los siguientes:

1. En un notebook de Jupyter lograr superponer la im�gen satelital con la transecta y graficarla (aqu� se tendr� que usar
solo un canal de los 7 disponibles o quiz�s dos o tres). Esto servir� para avanzar mejor con el objetivo 2, tener mejor feedback, etc.

2. Pararse en cada punto de la transecta y recortar un pedasito de la im�gen satelital (digamos una seccion de 15 x 15 pixeles)
Generando as� un conjunto de datos, cada uno de ellos con las siguientes dimensiones: 15 x 15 x 7. (el 7 es porque la imagen tiene 7 canales)
Cada uno de esos datos estar� etiquetado en una clase determinada que depender� del tipo de suelo. Digamos que algunas de esas im�genes recortadas
ser�n campo natural, otras barbecho, otras maiz, etc.

3. A partir de ese conjunto de datos, entrenar una red CNN programada con keras que permita clasificar im�genes en categor�as de campo
(campo natural, barbecho, ma�z, etc). Cabe destacar que dada la poca cantidad de puntos, por ahora, quiz�s lo mejor sea armar solo 2 
categor�as: campo natural y OTROS, por ejemplo.






Cabe destacar que el recorte del paso 2 seguramente sea bien simple y no implique una identificaci�n compleja. Esto implicar� que algunas
im�genes contendran pedazos de ruta que podr�an afectar al entrenamiento de la red, porque al fin y al cabo es ruido. Pero bueno, es un comienzo.
Si el dataset en el futuro es suficientemente grande, entonces la red aprender� "que las rutas no son informaci�n relevante", supongo.

En la im�gen "objetivo 1 - idea" se ve lo que prentendo lograr con el objetivo 1, solo que en vez de hacerlo en QGIS como est� en la im�gen, 
yo lo quiero hacer en jupyter notebook.