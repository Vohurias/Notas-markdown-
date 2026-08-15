# Inicio python 
## básico 
### Comentario 
Usamos  `#` para comentar una linea
``` python
# este es un comentario
```
>**Nota**
> todo codigo dentro no se ejecuta 

### Mostrar o imprimir por pantalla 
Usamos la palabra reservada `print()` para mostrar el resultado.
* Estructura 
```python
print(lo que queremos mostrar)
```
* Ejemplo
```python
print("Hola")
# hola

```
>Nota 
>podemos mostrar que un solo texto , esto se demostrar mas adelante 
### Pedir un dato
Usamos la palabra reservada `input()` para pedir que se ingrese un dato
```python
Input("Ingresa algo ")
# ingresa algo
```
> Nota
> al ejecutarlo esto no va a mostrar `Ingresa algo` y un espacio para que ingreses lo que tu quieras y al aceptar mostara lo que ingresaste. EJEMPLO, supongamos que valos a ingresar `hola` después de ejecutar.
``` python
Input("Ingresa algo: ")
#Ingresa algo: hola
#'hola'
```
>
### Variables
Las variables contienen un nombre , el valor que va atener ya se numérico,  decimal, etc. Esta es la estructura que deben de tener 
``` python
NombreDeLaVariable = Valor; 
```
#### Tipos de Variables 

##### Cadena de caracteres (Texto)
``` python 
texto1 = 'hola'
print(texto1)
#hola
texto2 = "hola"
print(texto2)
#hola 
```
> tipo de datos 
> str
##### Enteros (Numeros)
``` python 
Numero = 1;
print(Numero)
#1
```
> tipo de datos 
> int
##### Boleanos(True , False)
``` python 
Booleano1 = True;
print(Booleano1)
# True
Booleano2 = False;
print(Booleano2)
# False
```
> tipo de datos 
> bool
##### Decimal (flotante )
``` python 
Decimal = 1.2;
print(Decimal)
#1.2
```
> tipo de datos 
> float


### Operaciones matemáticas 
Se pueden realizar operaciones matemáticas básicas en python 
#### Suma
``` python 
Print(2+1)
# 3
```
#### Resta
``` python 
print(2-1)
# 3
```
#### Multiplicación 
``` python 
print(2*1)
# 3
```
#### División 
``` python 
print(2/1)
# 2
```
##### Division -Resultado con datos flotantes
``` python
print(5/6)
#0.8333333333
```
##### Division - Resultado valores enteros 
```python
print(5/6)
#0
```
###### División- Resultado resto
``` python
print(5%6)
#5
```

> Nota
> Al utilizar las operaciones matematicas nos puede funcionar como calculadora , pero debemos de colocar `()` para que se pueda ejecutar alguna operación antes, dependiendo de lo que quieres lograr 

#### Potencia 
``` python 
Print(3**2)
# 9
```

> Nota
> Podemos usar y colocar las operaciones dentro de variables de esta forma `n = 5+6` Esto nos permite usar operaciones salamcenando nuestra operación en una variable 







# Librería 
## Generar qr 
### Instalacion de libreria 

``` bash
pip install qrcode
```

### Codigo general 
``` python 
import qrcode
img = qrcode.make("hello word")
img.save("hello.png")
img.show()
```








