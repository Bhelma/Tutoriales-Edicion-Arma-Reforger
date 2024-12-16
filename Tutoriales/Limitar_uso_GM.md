# Limitar el uso del Game Master


Todo editor sabe que realizar una misión lleva tiempo y que todo el trabajo de ella, aunque se quede perfecta, se puede venir abajo si un Game Master decide esa noche o partida, añadir mas objetos o AIs a la mision para darle mas complejidad a la misma, sin saber que la mision ya esta equilibrada. Esto puede llevar a cargar el servidor, ya que el GM desconoce si hay AIs por salir y sobre todo que los jugadores acaben con un mal sabor de boca por haber sido avasallados por la AI.

Por esto, en la actualizacion del juego V1.2.1.169, Bohemia integro la posibilidad de inhabilitar los recursos para el GM y solo dejarlo para mopmentos en los cuales se requiera para corregir un bug o la caida del servidor de un jugador, asi que paso a explicar que realizar para limitar los recursos en tus misiones que no quieras que el GM interfiera. Comentar antes de nada, que se va a poder limitar al completo o parcialmente, segun se desee, los recursos que va a tener disponible el Game Master.


## Pasos

### Paso 1
Teniendo el editor del scenario framework abierto, no dirijimos al explorador de recursos habilitado en la parte central y abajo del editor.
Es donde localizamos los diferentes elementos que queremos añadir a nuestra mision.

En su buscador, buscamos el prefab EditorManager.et

### Paso 2
Con el puntero del raton encima del archivo buscado, pinchamos con el boton derecho del raton para que se despligue las diferentes opciones que se permiten hacer con el prefab seleccionado.
Y seleccionamos "Sobreescribir" "Override", para que sobre escriba en tu mision el archivo original y coja los nuevos parametros que deseas modificar, si miramos abajo de ese desplegable, la opcion de "open prefab" esta oscurecida, esto es por que Bohemia no permite el modificado de los archivos originales. esto tiene logica, para mantener los archivos originales siempre fieles, ya que si hubiese un error en esos archivos, quedaria corrupto el juego.

Si hicieramos "Duplicar" en vez de "Sobreescribir" solo conseguiramos que funcionase la priemra vez que cargasemos la mision, en este caso en el editor, para sucesivas ocasiones, cogeria los datos del archivo original y no de la copia.

Una seleccionado "Sobreescribir", saldra una pequeña ventana para asignarle un nombre al nuevo archivo, esto es importante, **mantener el mismo nombre que el original**, asi automaticamente siempre cogera este archivo como lectura.

### Paso 3
Una vez guardado, se nos generara el archivo dentro de nuestra carpeta de la mision, con la misma ruta que el archivo original, esta ruta no modificarla.
Poniendo el cursor del raton de nuevo encima del nuevo archivo creado, pinchamos con el boton derecho del raton y ahora si, pinchamos sobre la opcion "open prefab".

Se nos abrira el archivo, donde se podra configurar cualquier detalle del Game Master.
Nosotros nos vamos a fijar en el complemento "SCR_BudgetEditorComponent" del listado de la derecha, vease la siguiente imagen.

![Imagen GM Limitado](https://i.imgur.com/PnzhJbF.png)

### Paso 4
Basandonos en la imagen anterior, podemos ver que en la marca roja de abajo, estan los "presupuestos" de cada apartado disponible que tiene el GM cuando entra en una mision, me refiero a vehiculos, grupos, sistemas, componentes, etc...

Dejando en valor 0, cualquiera de las opciones que no deseemos que tenga el GM acceso, automaticamente cada vez que el GM entre en su panel, le saldran oscurecidas esos apartados.

En la imagen anterior que tienen a 0 todos los valores, automaticamente el GM no tiene acceso a ningun recurso.

### Paso 5
Una vez tengamos modificados los valores que deseemos, ya podemos darle a guardar.


## Aclaraciones
Hay que tener en cuenta que esto llimita y sin posibilidad de volver de otra forma al GM de todos los recursos marcados a 0, es decir, desde la mision no se puede volver este valor al valor original, asi que para devolver este valor al original implica tener que abrir de nuevo la mision, modificarlo y volver a subir la mision al workshop.
Tambien es util, por si no deseas que te añadan minas en mitad de la mision, o mas AIs o blindados cuando tu como creador no lo quieres asi.


