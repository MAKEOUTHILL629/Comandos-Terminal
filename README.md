COMANDOS EN LA TERMINAL
=========
La raiz es / de todo nuestro directorio de carpetas

_En el promt nombreUsuario@nombrePc_
&nbsp;
*Importante que algunos comandos necesitan que se especifique algo, por temas de dejarlo implicito utilizare el [archivo, ruta, etc]*

*Los archivos oculto se muestra con un punto antes
.carpetaOculta*
### Comandos basicos a usar en la terminal

| Comando | Descripcion |
| ------- | ----------- |
| `ls` | Listar todos los directorios en la carpeta en la que nos encontramos|
| `cd [ruta]` | _Change Directory_, cambiar el directorio a uno en especifico |
| `clear` o `cls` | Limpia la informacion en la terminal |
| `pwd` | _Print Working Directory_, nos muestra la ruta en donde estamos |
| `file [archivo]` | el comando nos describe que archivo es el que estamos trabajando | 
| `mkdir [nombre_nuevo_directorio]` | Nos crea un directorio o carpeta, podemos crear multiples directorios al tiempo |
| `touch [nombre_nuevo_archivo]` | Nos ayuda a crear un archivo, se pueden crear varios archivos al tiempo |
| `cp [archivo_a_copiar] [nombre_copia_archivo]` | Nos ayuda a copiar un archivo | 
| `mv [archivo_a_mover] [ruta_destino]` | Nos ayuda a mover archivos entre directorios |
| `mv [archivo_a_renombrar] [nuevo_nombre]` | Es un truco para renombrar archivos o carpetas |
| `rm [archivo_a_borrar]` | Para borrar archivos o carpetas |
| `tree` | Muestra todos mis archivos en manera de arbol, y la profundizacion de cada carpeta |
| `type [comando]` | El type del comando, es decir nos retorna que tipo de comando es |
| `alias [nombre_alias]="comando"` | Nos permite renombrar los comandos para ejecutarlos de manera mas rapida y sencilla, los alias son temporales |
| `help [comando]` | Es una utilidad para saber mas sobre el comando |
| `man [comando]` | El manual del comando que se utilizara |
| `info [comando]` | Mas informacion del comando |
| `whatis [comando]` | Breve descripcion del comando |
| `ln -s [ruta] [nombre]` | Crea un link simbolico a una ruta establecida |
| `echo $0` | Para saber que shell se esta usando |

## Comandos basicos con sus respectivas variantes
| Comando | Descripcion | 
| ------- | ----------- |
| `ls -l` | Muestra todos los archivos y directorios en forma de lista |
| `ls -la` | Muestra todos los archivos incluidos los ocultos |
| `ls -ls` | Muestra en orden todos los directorios y documentos por espacio en disco |
| `ls -lr` | Muestra los archivos organizados de manera desendente |
| `tree -L [cantidad]` | Muestra el arbol especificando la cantidad de niveles que se quieren observar |
| `rm -i [nombre_archivo_borrar]` | De manera interactiva, es decir toca confirmar para que se borre un archivo o carpeta Y/N |
| `rm -r [nombre_directorio_borrar] ` | Elimina de manera recursiva, por ejemplo cuando la carpeta tiene archivos adentro |

## Comandos para manipular el contenido de archivos
| Comando | Descripcion |
| ------- | ----------- |
| `head [archivo]` | Muestra las primera 10 lineas del archivo, el archivo tiene que ser de texto |
| `head [archivo] -n [cantidad]` | Muestras las n primeras lineas de un archivo |
| `tail [archivo]` | Muestras las 10 ultimas lineas del archivo, se puede utilizar el modificador -n |
| `less [archivo_de_texto]` | Explorar un archivo de texto, provee una interfaz para explorar el archivo |
| `xdg-open [archivo_texto]` | Nos abre nuestro editor de texto predeterminado para editar el texto |


## WildCards
| Comando | Descripcion |
| ------- | ----------- |
| `ls *.txt` | Mostrar los archivos que terminen en .txt | 
| `ls datos*` | Mostrar todos los archivos que contengan en el nombre datos, sin impotar los que valla despues | 
| `ls datos?` | Mostrar todos los archivos que en su nombre contenga la palabra datos y una letra de mas |
| `ls [[:upper:]]*` | Mostrar todos los directorios que o archivos que en su nombre la primera letra comienze con una mayuscula |
| `ls [[:lowe:]]*` | Mostrar todos los directorios que o archivos que en su nombre la primera letra comienze con una minuscula |
| `ls [ad]*` | Mostrar todos los archivos que en su nombre comience con la letra a o d |

## Redireccionamientos
La terminal maneja tres formas en manipular la informacion.
stdin = 0, entrada en la terminal
stdout = 1, salida normal
stderr = 2, salida de error

La tabla se entiende con que la l del comando es |, un _Pipe Operator_.

| Comando | Ejemplo | Descripcion |
| ------- | ------- | ----------- |
| `>` | `ls Descargas > archivo.txt` | Guarda el resultado en un archivo de texto |
| `>>` | `ls Descargas >> archivo_concatenado.txt` | Guarda el resultado en un archivo de texto, pero esta vez concatena lo que este en el archivo de texto |
| `2>` | `ls carpeta_no_existe 2> archivo.txt` | Guarda el resultado en un archivo de texto, pero esta vez guarda el error del terminal, como es stdout 1, stderr 2 y stdin 0 |
|`2>&1`| `ls asdasd > outputerror.txt 2>&1` | Guarda el resultado sin importar si es de error o un estandar output |
| `l` | `ls -lh ./ l less` | El operador pipe nos ayuda a redirigir el stdout de un comando a otro de manera stdin |
| `l tee [archivo_a_crear]` | `ls -lh l tee output.txt l less` | Nos ayuda a crear un archivo con la salida de anterior comando, se puede decir que tee es > |
| `;` | `ls -lh; mkdir nueva_carpeta; cal` | El operador ; nos ayudara a ejecutar comandos de manera sincrona es decir uno tras de otro |
| `&` | `ls & date & cal` | Ejecuta los comandos de manera asincrona es decir por cada comando crea un proceso en diferentes hilos, se ejecuta simultaneamente |
| `&&` | `mkdir test && cd test` | Para ejecutar comandos si y solamente si, se ejecutan de manera correcta |
| `ll` | `cd asdasd ll touch archivo.txt ll echo "Archivo creado"` | Para ejecutar comandos sin importar si no se cumplen |


## Tipos de Permisos

# Tipos de archivos
- `- => Archivo normal
- d => Directorio o carpeta
- l => Link simbolico
- b => Bloque de archivos, guarda infomacion

# Permisos
- w => write, escritura
- r => Read, lectura
- x => Executable, ejecutable

# Tipo de modo
| Dueño | Grupo | World |
| ----- | ----- | ----- |
|  rwx  |  rwx  |  rwx  |
|  111  |  101  |  000  |
|   7   |   5   |   1   |

# Simbolico

| Simbolo | Significado |
| ------- | ----------- |
| u | Solo usuario |
| g | Solo grupo |
| o | Solo otros |
| a | Todos |

| Comando | Ejemplo | Descripcion |
| ------- | ------- | ----------- |
| `chmod [permisos] [archivo]` | `chmod 755 mitexto.txt` | El comando me permite cambiar y asignar permisos de carpetas o archivos |
| `chmod [simbolo][+-][permisos] [archivo]` | `chmod u-r mitexto.txt` | Me permite quitarle o agregar permisos a un tipo de usuario en especifico |
| `whoami` | `whoami` | Me permite conocer desde que usuario estoy en la terminal |
| `id` | `id` | Informacion sobre el usuario, permisos, grupos, id etc | 
| `su [usuario]` | `su root` | Realizo un cambio al usuario root, importante colocar la clave del root | 
| `passwd` | `passwd` | Cambiar la clave de mi usuario |

## Comandos de busqueda
| Comando | Ejemplo | Descripcion |
| ------- | ------- | ----------- |
| `which [comando]` | `which code` | Busca el binario en el path, donde se encuentra el comando en la shell | 
| `find [ruta_desde_donde_comienza] -name [nombre]` | `find ./ -name *.txt` | Busca un archivo desde donde se le especifique la ruta, comienza a buscar |
| `find [ruta_desde_donde_empieza] -type [d/f] -name [nombre]` | `find ./ -type d -name Documents ` | Busca un archivo o carpeta desde una ruta en especifica |  
| `find [ruta_desde_donde_comienza] -size [tamanio_archivo]` | `find ./ -size 20m` | Busca los archivos con un tamanio mayor | 
| `grep [expresion_regular] [archivo]`  | `grep Towers excel.cvs` | Encuentra todas las coincidencias en un archivo, las coincidencias con la expresion regular |
| `grep [expresion_regular] -i [archivo]` | `grep -i The movies.csv` | Realiza la busqueda ignorando las mayusculas o minusculas el keySensive |
| `grep -c [expresion_regular] [archivo]` | `grep -c the movies.txt` | Realiza el conteo de las coincidencias en el archivo |
| `grep -v [expresion_regular] [archivo]` | `grep -v towers movies.txt` | Realiza la busqueda de las palabras que no coincidan con la expresion regular |
| `wc [archivo] -l -c -w` | `wc movies.csv` | Realiza el conteo de las lineas, letras o caracteres, numero de bits y el nombre del archivo |


## Utilizades de Red
| Comando | Ejemplo | Descripcion |
| ------- | ------- | ----------- |
| `ping [pagina_web]` | `ping www.google.com` | Se usa para recibir paquetes de una pagina |
| `curl [pagina_web]`| `curl www.google.com` | Se usa para traer el html de una pagina web |
| `wget [pagina_web]`| `wget www.googgle.com` | Guarda el archivo o la respuesta del servidor |  
| `traceroute [pagina_web]` | `traceroute www.google.com` | Traza el camino que recorre normalmente para conectarme al servidor o pagina web |
| `netstat -i`| `netstat -i` | Muestra todos los dispositivos de red |
| `ifconfig` | `ifconfig` | Muestra la informacion de mi conexion de red |

## Comprimiendo Archivos
| Comando | Ejemplo | Descripcion |
| ------- | ------- | ----------- |
| `tar -cvf [archivo_despues_de_comprimir.tar] [archivo_comprimir]`| `tar -cvf ToCompress.tar ToCompress` | Me permite comprimir un archivo a .tar, c es comprimir, v es verbose para que se vea lo que hace el comando, f de file |
| `tar -cvzf [archivo_despues_de_comprimir.tar.gz] [archivo_comprimir]` | `tar -cvzf ToCompress.tar.gz ToCompress` | Comprime un archivo a .gz que es un algoritmo eficiente, para decirle que es gz, se le agrega la z |
| `tar -xzvf [archivo_comprimido.tar.gz]` | `tar -xzvf ToCompress.tar.gz` | Descomprime el archivo tar.gz, x es de descomprimir | 
| `zip -r [archivo_despues_comprimir.zip] [archivo_a_comprimir]` | ` zip -r toCompressInZip.zip ToCompress` | Comprime un archivo a .zip |
| `unzip [archivo_comprimido.zip]`| `unzip toCompressInZip.zip` | Descomprime mi archivo .zip | 

## Manejo de procesos
| Comando | Ejemplo | Descripcion |
| ------- | ------- | ----------- |
| `ps` | `ps` | Observar los procesos que estan corriendo de fondo |
| `kill [PID_proceso]` | `kill 123465` | Mata a un proceso | 
| `top` | `top` | Mostrar toda la informacion de todos los procesos |

## VIM
| Comando | Descripcion |
| ------- | ----------- |
| `vim` | Abre el editor de texto vim |
| `vim nuevo_archivo` | me crear un archivo y me abre el editor de vim |
| `:q` | Para salir de vim |


