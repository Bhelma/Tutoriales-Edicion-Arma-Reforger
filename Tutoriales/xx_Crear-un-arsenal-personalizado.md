# Crear un Arsenal Personalizado

Explicare de forma facil como generar un arsenal personalizado para vuestras misiones.
Imaginaos que en el arsenal de vuestra faccion en la cual vais a basar la mision, necesitais meter las armas de otra faccion. Voy a poner un ejemplo practico.

Actualmente en las cajas de arsenal de la faccion US, solo estan disponibles las armas vanilla del juego, la cual si vais a crear una mision en una epoca distinta, mas moderna por ejemplo, debeis de meter otra caja de arsenal mas a la mision de la faccion deseada y editarla como entidad para que salgan todos los objetos de esa faccion, esto es engorroso ya que primero llenaras la zona de spawn con muchos arsenales sin saber cual tiene que arma y aparte no sabras a ciencia cierta si se han cargado todas ellas hasta que realmente esten en partida los jugadores y se tendran que habiliar mediante GM, algo que como editor quiero evitar.
Ponemos el ejemplo de querer meter las armas del RHS dentro del arsenal US para asi disponer de todas las armas de esas dos facciones en un unico arsenal colocado en la mision.

Este ejemplo practico sera un caso que sera de uso seguro para muchos editores.

### Paso 1
Para realizar estos pasos no hace falta estar en el mundo de la mision,pero lo recomiendo para asegurarte que cada arma que añades esta realmente en el arsenal.

Sobre la herarquia de la izquierda, donde estan los mods en la parte de arriba nos dirigiremos al de ***ArmaReforger***, pinchamos en la flecha azul y se nos desglosara todas sus subcarpetas.
Ahora abrimos ***Config*** y seguido de ***EntityCatalog***.

Una vez que tengamos abierta esta ultima carpeta ***EntityCatalog*** en la ventana de abajo a la izquierda, tendremos las facciones que tiene el juego vanilla, Seleccionamos la faccion, de este ejemplo, US y abrimos de nuevo la carpeta. Cuando pinchemos do veces con el raton como si estuviesemos en windows, se nos abrira todos los entitycatalogs que tiene la faccion.

Nos vamos a fijar en el archivo llamado ***InventoryItems_EntityCatalog.conf***, como se puede ver en la siguiente imagen.

![Imagen Paso1](https://i.imgur.com/0mTqk8G.jpeg)

Ahora poniendo el raton encima de dicho archivo, pinchamos con el boton derecho del raton y del desplegable seleccionamos __overwrite__ o __sobreescribir_, seleccionamos nuestro mod en caso de que lo pregunte y ya tenemos una copia del archivo _InventoryItems_EntityCatalog.conf_ en nuestro mundo y del cual la mision leera por encima del vanilla, asi que todo lo que hagamos con ese archivo sera lo que la mision lea.
___Muy Importante___ a de seleccionase ___overwrite___ y no ___duplicate___ ya que aunque puede parecer lo mismo no lo es. En otros tutoriales explicare la diferencia, pero para este debeis de saber que si seleccionais _duplicate_ cuando se reinicie tan solo una vez la mision, ya no leera ese archivo la mision, sino el archivo original.

### Paso 2

Habiendo creado el nuevo archivo en tu mundo, ahora debemos de localizarlo y abrirlo, asi que nos dirigimos a la siguiente ruta, como henos realizado anteriormente con la carpeta de _ArmaReforger_, pero en este caso para tu mision.
___nombredetumision/Config/EntityCatalog/Facciondeseada___
Y nos aparecera el nuevo archivo en la parte de abajo, como se puede ver en la siguiente imagen.

![Imagen Paso 2](https://i.imgur.com/8sOtRx4.jpeg)

Pinchamos dos veces con el boton izquierdo del raton sobre el nombre del archivo, y en el centro del editor se nos abrira su contenido, como podemos observar en la iiguiente imagen.

![Imagen Paso 3](https://i.imgur.com/kWG2fYZ.jpeg)

### Paso 3

Como podemos ver en la imagen anterior, al lado del nombre de cada multilista tenemos unos numeros entre parentesis,eso implica la cantidad de items que hay añadidos en ese apartado, por ejemplo, en la imagen anterior en la multi lista __Weapons__ hay 76 armas introducidas. Si se da el caso, como en la imagen, de que hay una multi lista con vario numeros, como __Ammunition__ que pone (127 to 130) indica que hay tres elementos añadidos, pero que estan deshabilitados, Esto seguramente ocurre, o por que el creador del mod la tiene desactivada para una proxima actualizacion o por que esta duplicado el nombre del item.
Hay que familiarizarse con el nombre de cada multilist, ya que aunque los siguientes pasos son sencillos de hacer, son muy repetitivos.

### Paso 4

Con tu archivo abierto, ahora nos dirigimos a la izquierda a la herarquia de carpetas y vamos al mod que queremos integrar. Siguiendo la siguiente estructura, abrimos los archivos entitycatalog que queramos introducir en nuestro arsenal.
___nombredelmod/Config/EntityCatalog/Faccion/InventoryItems_EntityCatalog.conf___

Segun el mod, nos apareceran mas o menos multilist, y dependiendo del mod nos apareceran _Weapons_ o _Clothing_.

Con este archivo abierto, nos ponemos con el raton encima de la multilist y con el boton derecho del raton seleccionmos __Copy__, nos vamos a nuestro archivo abierto, nos ponemos encima de la misma multilit que hemos copiado, pinchamos con el boton derecho del raton y seleccionamos __Paste__, nos espemos unos segundos y vemos como el numero de la multilist aumenta, eso significa que ya se han copiado los items de la faccion del mod a nuestro arsenal.
#### Cosas a tener en cuenta
__1.__ Muy importante que los multilist que se copien sean del mismo nombre, ya que si es diferente, aunque se copien, no se veran en el arsenal una vez en la mision, ya que el juego categoriza para mostrar los items por las multilist creadas y en ese orden.
__2.__ Si el numero no aumenta cuando copies, significa que ya existen, asi que deberas verificar que se han copiado. Para saber esto tendras que abrir el multilist que quieres copiar y ver los nombres de los items, dirigirte a tu archivo, y verificar en el multilist qe dichos items estan correctamente copiados.

### Paso 5

Siguiendo el paso anterior, copiar todos los multilist de los mods ue necesites que aparezcan en tu arsenal.

Toma nota, que si copias muchos items en una mismo arsenal, cuando estes enel juego y varias personas intenten entrar a los arsenales, esto puede producir lag en el servidor, al tener que cargar todos los item, y segun el tipo de ordenador del jugador puede llegar a quedarse congelado por que su PC es bastante justito.
Asi que tenlo en cuenta cuando vayas a meter todos los mods del workshop.
