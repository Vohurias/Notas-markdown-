# Nota GIT - GitHub

## Configuracion inical(Requerido)

Para empezar hay que hacer un configuracion global para identificarte

~~~ bash
  #Configurar tu nombre
  git config --global user.name "Nombre"
  #Configura tu correo
  git config --global user.email "TuCorreo@identicable.com"
~~~

## Iniciar el repositorio en Git

~~~ bash
  git init
~~~

> Nota
>>  En caso de que tengas problemas para hacer init 'detected dubious ownership in repository' usa este codigo:

~~~bash
  #Ruta especifica
  git config --global --add safe.directory /ruta/del/directorio/
  # todo
  git config --global --add safe.directory '*'
~~~

## Agregar cambios

~~~ bash
git add .
~~~

## Guardar cambios

~~~ bash
git commit -m "Mensaje"
~~~

## Creacion de repositorio en GitHub

### Manual

Ve a la pagina de github y abre tu sesion y ve a la parte superior donde dice 'new' o 'new repository', ponle un nombre y no marques las casillas 'README' o 'gitignore'. Para terminar presiona donde dice 'Create repository'.

### Comandos

## Acceder mediante https

En esta parte te pedira el toekn siempre que subar un archivo , sin importar que sea el mismo usuario, consejo usarolo en maquinas que no son las peronales

### Token(PAT)

1. Haz click donde esta tu foto y entra a settings , despues busca en la barra lateral izquierdo donde dice 'Developer settings' luego ve a 'Personal access' y luego a la seccion de 'tokens(classic)'.

2. Haz click en 'Generate new token' y preciona 'Generate new token (classic)' ingresas tus datos de seguridad si te lo piden. Ponle un nombre en 'Note' y marca la casilla 'repo' para tener acceso a los repositorios tanto publicos como prvados y para terminar 'Generate token', copia el codigo que inicia con 'ghp_...' y guardalo bien.

## Acceder mediante ssh

Sirve para que se ingrese una clave de manera automatica sin la necesidad de un token como https. Consejo usarlo en una computadora personal

### Generar llave SSH

~~~bash
# Genera una clave con el algoritmo ed25519
ssh-keygen -t ed25519 -C "tu_email@ejemplo.com"
~~~

> Nota
>> Primero te pedira la ruta donde quieres guardarlo, selecciona cual quieres o puedes dejarla en blanco presioando enter. Despues te pedira una contraseña opcional, puedes dejarla en blanco con doble enter

Despues de generar la clave para verlo hacemos

~~~ bash
cat ~/.ssh/id_ed25519.pub
~~~

luego copialo

### Agregar clave a github

1. Haz click donde esta tu foto y entra a settings , despues busca en la barra lateral izquierdo donde dice 'SSH and GPG keys' luego presiona 'New SSH key'.
2. En title coloca el nombre para identificarlo y en key coloca el codigo que se genero en la terminal
3. Probamos la conexion con:

~~~ bash
ssh -T git@github.com
~~~

> Nota
>> tiene que salir 'Hi TU_USUARIO! You've successfully authenticated, but GitHub does not provide shell access.' , pero si sale Si te sale un aviso preguntando Are you sure you want to continue connecting (yes/no/fingerprint)?, escribe yes y presiona Enter.

### Asegurar que la rama principal se llame main

~~~ bash
  git branch -M main 
~~~

### Conectar con tu repositorio

~~~ bash
  git remore add origin https://github.com/Turespositorio.git
~~~

> Nota 1
>> En esta parte si no te acepta el https, si colocaste uno erronia o no te carga con el link 'https' o colocaste el link 'ssh' usamos el siguiente codigo para sobreescribirlo,

~~~ bash
git remote set-url origin https://github.com/Turespositorio.git
~~~~

### Subir archivos

~~~ bash
  git push -u origin main
~~~

> Nota
>> Al ejecutarlo este te pedira el nombre , colocas el tuyo y al presionar enter , te pedira la clave y ahi pegas el token

----- 
# Despues de configurar 
## Comandos
### Ramas
Son zonas donde podemos hacer cambios, pruebas y mejoras sin afectar la el avance que hicimos hasta el momento
#### Ver ramas existentes.
~~~ bash
  git branch
~~~
    
##### Variantes
* Ver ramas tanto en locales como subidas a github
~~~ bash 
  git branch -a
~~~

#### Creacion de ramas
~~~ bash 
  git branch Nombre_de_la_rama
~~~
##### Variantes.
* Crear ramas y moverse a ellas
~~~ bash
  git switch -c Nombre_de_la_rama
~~~

#### Cambiar entre ramas 
~~~ bash 
  git switch Nombre_de_la_rama
~~~

#### Renombrar ramas
~~~ bash 
  #Renombra la rama actual
  git branch -m nuevo-nombre
  #Renombra rama que no es la actual(En la que no estas)
  git branch -m Nombre_de_la_rama nuevo-nombre
~~~

#### Juntar ramas 
Permite juntar la rama actual con la rama que seleccionemos, esto permite traer los cambios de otra rama a la rama actua.
~~~ bash 
  git merge Nombre_de_la_rama
  #Formzar la union de dos rmas 
  git merge Nombre_de_la_rama --allow-unrelated-histories
~~~

> [!Warning]
> Antes de hacer algo con una rama debes de hacer un commint sino perderas archivos y datos

#### Borrar ramas
~~~ bash 
#Se borra solo si se guardaron los cambios
git branch -d Nombre_de_la_rama
# Fuerza para borrar la rama 
git branch -D Nombre_de_la_rama
#Borra rama de github
git push origin --delete Nombre_de_la_rama
~~~

### Revisar todos los 'Commits'
~~~ bash 
  git log
~~~

  * Vista simplificada
    ~~~ bash 
     git log --oneline
    ~~~

Para ir al commit solo lectura usamos:
~~~ bash 
  git checkout codigo_del_commit
~~~

Para regresar al commit actual usamos 
~~~ bash 
  git checkout Nombre_de_la_rama
~~~

Para volver al pasado de manera permanente dejando lo actual como un commit sin guardar
~~~ bash 
  git reset codigo_del_commit
  #Para regresar a atras y borrar todo lo actual
  git reset --hard codigo_del_commit
~~~

Para crear una nueva rama con el commit seleccionado
~~~ bash
git checkout -b Nombre_de_la_rama_con_el_commit codigo_del_commit
~~~


