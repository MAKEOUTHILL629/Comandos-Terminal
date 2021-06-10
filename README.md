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


