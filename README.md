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

Por temas de markdow, la l es |

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

#Tipos de archivos
- => Archivo normal
d => Directorio o carpeta
l => Link simbolico
b => Bloque de archivos, guarda infomacion

#Permisos
w => write, escritura
r => Read, lectura
x => Executable, ejecutable

# Tipo de modo
| Dueño | Grupo | World |
| ----- | ----- | ----- |
|  wrx  |  wrx  |  wrx  |
|  111  |  101  |  000  |
