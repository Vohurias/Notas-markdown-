## Grep
Sirve para buscar en base al nombre 
Estructura:
``` bash 
grep [opciones] "Palabra a buscar" [ruta/archivo o nombrearchivo]
```
EJEMPLO 
``` bash
grep "hola" prueba.txt
```
### R o r
Sirve para buscar la palabra en todos los archivos que hay en la ruta 
``` bash
grep -R "hola" ~/documentos
```
### i
Sirve para ignorar mayúsculas y minúsculas 
``` bash
grep -i "HoLa" ~/documentos
```
### n
Avisa en el número de linea que encontró la palabra en el archivo .mz