La idea de este notebook es entrenar y testear una red neuronal que tenga celdas LSTM a partir de vectores de 8 elementos.

Cada elemento de ese vector representa un tiempo en una secuencia. El elemento 0 representa el T0, el elemento 1 representa 
el tiempo 1, el ultimo elemento representa el tiempo 7.

Cada elemento de ese vector representa un PIXEL (inventado aleatoriamente) y es OTRO vector compuesto por tres elementos, que llamaré CANALES. 
las imágenes satelitales con las que trabajamos tienen 6 canales, pero aqui decidi trabajar con 1 por simplicidad, la idea 
es complicar las cosas luego en otro Notebook. 

Estos pixels entonces estan compuestos por un canal. Cada canal es un numero entero entre 0 y 255. La idea es generar esos números
a partir de funciones senoidales que tengan algun parámetro aleatorio como el corrimiento frecuencial y elevacion del seno. 

Un humano puede saber con exactitud cualquier TIEMPO conociendo la funcion completa con la que se generan los datos. Es decir, puedo
ir a la calculadora, escribir por ejemplo sin(2*T + a) + B con T = 7 y ya se que para el tiempo 7 el valor de ese canal del pixel valdra
lo que me diga la calculadora.

La idea de la red neuronal con celdas LSTM es poder mostrarle los primeros 7 elementos de un vector (T0, T1, T2 y T3) y que la red
me PREDIGA qué va a ocurrir en T7.

Para entrenarla, la idea es generar un número grande de estos vectores de 8 elemenos, por ejemplo 10000. Y entrenar la red con los mismos.
En principio la red tiene 7 entradas secuenciales (que corresponden a T0 T1 T2, T3, T4, T5, T6 y T7) y una sola salida. Cada una de las entradas y salidas
es un PIXEL, es decir un vector de 1 elemento (que es un numero natural de entre 0 y 255).

Con este notebook se puede poner a prueba la robustez de una red LSTM ante una situacion como esta. En futuros Notebooks, se puede probar testear esto
con mas de 1 canal y con datasets mas variados.