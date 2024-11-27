# 1. Importaciones

En Python, puedes importar módulos o librerías que contienen funciones y variables ya predefinidas. Existen diferentes formas de importación:

```python
# Importar todo el módulo
import math

# Importar solo una función específica del módulo
from math import sqrt

# Darle un alias a un módulo
import math as m
```

# 2. Comentarios

Los comentarios se utilizan para añadir notas explicativas al código, y son ignorados durante la ejecución. Se escriben de la siguiente manera:

```python
# Este es un comentario de una sola línea

"""
Este es un comentario
multilínea
"""
```

# 3. Imprimir por consola

La función print() se utiliza para mostrar información en la consola.

```python
print("Hola, Mundo!")  # Imprime un mensaje
x = 5
print(x)  # Imprime el valor de la variable x
```

# 4. Declaración de variables

En Python, no es necesario declarar el tipo de una variable antes de usarla, solo se asigna el valor directamente:

```python
x = 10  # variable de tipo entero
nombre = "Juan"  # variable de tipo cadena de texto
```

# 5. Tipos de variables primitivos

```python
edad = 30  # int
altura = 1.75  # float
nombre = "Ana"  # str
es_mayor = True  # bool
```

# 6. Comparaciones lógicas

Las comparaciones lógicas se realizan con operadores como `==`, `!=`, `>`, `<`, `>=`, `<=`.

```python
x = 5
y = 10
print(x == y)  # False
print(x < y)   # True
print(x != y)  # True
```

# 7. Operadores lógicos con precedencia de operaciones

Los operadores lógicos más comunes son `and`, `or`, y `not`. Estos se pueden combinar con paréntesis para controlar su precedencia:

```python
x = 5
y = 10
z = 15
print(x < y and y < z)  # True
print(not (x < y))  # False
```

# 8. Operadores aritméticos con precedencia de operaciones

Los operadores aritméticos son los siguientes: `+`, `-`, `*`, `/`, `//` (división entera), `%` (módulo) y `**` (potencia).

La precedencia de operaciones sigue el orden matemático estándar, siendo primero las operaciones de multiplicación, división, etc., antes que las de suma y resta.

```python
resultado = 5 + 3 * 2  # El resultado es 11, porque * tiene mayor precedencia que +
```

9. Condiciones

```python
x = 5
if x > 0:
  print("Positivo")
elif x == 0:
  print("Cero")
else:
  print("Negativo")
```

# 10. Condiciones anidadas

```python
x = 10
y = 5
if x > 0:
  if y > 0:
    print("Ambos números son positivos")
  else:
    print("Solo x es positivo")
else:
  print("x no es positivo")
```

# 11. Valores truthy y falsy

En Python, ciertos valores se consideran "truthy" (verdaderos) o "falsy" (falsos) cuando se evalúan en un contexto booleano.

- Valores `falsy`: `False`, `None`, `0`, `""` (cadena vacía), `[]` (lista vacía), etc.
- Valores `truthy`: cualquier otro valor.

```python
if []:
    print("Verdadero")
else:
    print("Falso")  # Se imprimirá "Falso"
```

# 12. Bucle while

El bucle `while` ejecuta un bloque de código mientras una condición sea verdadera.

```python
x = 0
while x < 5:
  print(x)
  x += 1
```

# 13. Bucle for

El bucle `for` itera sobre una secuencia (como una lista, rango, etc.).

```python
for i in range(5):
  print(i)  # Imprime los números del 0 al 4
```

# 14. Longitud de elementos

Puedes obtener la longitud de una secuencia utilizando la función `len()`.

```python
cadena = "Hola"
print(len(cadena))  # Imprime 4
```

# 15. Funciones sin parámetros ni retorno

Las funciones sin parámetros ni retorno son aquellas que no reciben argumentos y no devuelven valor.

```python
def saludar():
  print("¡Hola!")

saludar()  # Llama a la función
```

# 16. Funciones con parámetros sin retorno

Las funciones con parámetros realizan operaciones con los valores que reciben, pero no devuelven ningún valor.

```python
def saludar(nombre):
  print(f"Hola, {nombre}!")

saludar("Juan")  # Llama a la función con un parámetro
```

# 17. Funciones sin parámetros con retorno

Estas funciones no reciben parámetros, pero devuelven un valor.

```python
def obtener_numero():
  return 5

print(obtener_numero())  # Imprime 5
```

# 18. Funciones con parámetros y retorno

Las funciones con parámetros reciben valores y devuelven un resultado.

```python
def suma(a, b):
  return a + b

print(suma(3, 4))  # Imprime 7
```

# 19. Excepciones

Una excepción es un evento que ocurre durante la ejecución de un programa, lo que interrumpe su flujo normal. Si no se maneja adecuadamente, el programa se detendrá. Por ejemplo, si intentas dividir un número entre cero, Python lanzará una excepción, que es un error que se puede manejar para evitar que el programa se caiga.

## Manejo de excepciones

Python usa una estructura de control especial llamada `try`, `except`, `else` y `finally` para manejar excepciones. A continuación, te explico cómo funcionan:

### 1. Bloque try

El bloque `try` es donde colocas el código que crees que puede generar una excepción. Si el código en este bloque produce una excepción, el control se pasa al bloque except.

```python
try:
  # Código que puede generar una excepción
  x = 10 / 0  # División por cero, esto generará un error
```

### 2. Bloque except

El bloque `except` captura y maneja las excepciones que ocurren en el bloque `try`. Si se lanza una excepción, el flujo de ejecución salta al bloque `except` correspondiente.

```python
try:
  x = 10 / 0  # División por cero
except ZeroDivisionError:
  print("¡Error! No se puede dividir por cero.")
```

En el ejemplo anterior, la excepción `ZeroDivisionError` es capturada, y el mensaje `"¡Error! No se puede dividir por cero."` es impreso, evitando que el programa se caiga.

### 3. Bloque else

El bloque `else` se ejecuta si no se generó ninguna excepción en el bloque `try`. Es útil para ejecutar código que debería correr solo cuando no haya errores.

```python
try:
  x = 10 / 2  # División correcta
except ZeroDivisionError:
  print("¡Error! No se puede dividir por cero.")
else:
  print("La división fue exitosa.")
```

Aquí, dado que la división no genera un error, el mensaje `"La división fue exitosa."` se imprime.

### 4. Bloque finally

El bloque `finally` se ejecuta siempre, haya o no haya ocurrido una excepción. Se usa para realizar tareas de limpieza, como cerrar archivos o liberar recursos, sin importar si hubo error o no.

```python
try:
  x = 10 / 2  # División correcta
except ZeroDivisionError:
  print("¡Error! No se puede dividir por cero.")
else:
  print("La división fue exitosa.")
finally:
  print("Este bloque se ejecuta siempre.")
```

En este caso, `"Este bloque se ejecuta siempre."` se imprime sin importar si la operación fue exitosa o si ocurrió un error.

## Manejo de diferentes tipos de excepciones

Puedes manejar diferentes tipos de excepciones usando múltiples bloques `except`. Es importante que pongas los bloques de excepciones más específicas primero, y luego las más generales.

```python
try:
  x = int(input("Introduce un número: "))
  y = 10 / x
except ZeroDivisionError:
  print("No se puede dividir por cero.")
except ValueError:
  print("Por favor, ingresa un número válido.")
except Exception as e:
  print(f"Se produjo un error inesperado: {e}")
```

- `ZeroDivisionError`: Captura errores de división por cero.
- `ValueError`: Captura errores cuando el valor ingresado no es válido (por ejemplo, ingresar una letra en vez de un número).
- `Exception`: Captura cualquier otro error que no haya sido manejado por los bloques anteriores. Esto debe ir al final, ya que `Exception` es una clase base de todas las excepciones en Python.

## Errores comunes y sus excepciones

| Excepción           | Descripción                                                                       |
| ------------------- | --------------------------------------------------------------------------------- |
| `ZeroDivisionError` | Ocurre cuando intentas dividir por cero                                           |
| `ValueError`        | Ocurre cuando un valor no es el tipo esperado                                     |
| `TypeError`         | Ocurre cuando se aplica un operador a un tipo de datos inapropiado                |
| `FileNotFoundError` | Ocurre cuando intentas abrir un archivo que no existe                             |
| `IndexError`        | Ocurre cuando intentas acceder a un índice que no existe en una lista o secuencia |
| `KeyError`          | Ocurre cuando intentas acceder a una clave que no existe en un diccionario        |
| `AttributeError`    | Ocurre cuando se intenta acceder a un atributo que no existe en un objeto         |

## Uso de raise para lanzar excepciones

También puedes utilizar `raise` para lanzar excepciones explícitamente en tu código. Esto puede ser útil cuando detectas un error lógico y quieres interrumpir el flujo de ejecución.

```python
def verificar_numero(x):
  if x < 0:
    raise ValueError("El número no puede ser negativo")
  return x

try:
  verificar_numero(-1)
except ValueError as e:
  print(f"Error: {e}")
```

En este caso, el `raise` lanza una `ValueError` si el número es negativo, y el mensaje es capturado en el bloque `except`.

## Ejemplo con todos los bloques

```python
try:
  x = int(input("Introduce un número: "))
  y = 10 / x
except ZeroDivisionError:
  print("¡Error! No se puede dividir por cero.")
except ValueError:
  print("Por favor, ingresa un número válido.")
else:
  print(f"El resultado de la división es {y}")
finally:
  print("Este bloque siempre se ejecuta.")
```

# Operaciones

## Sumatorio

El sumatorio de una secuencia de números:

```python
def sumatorio(n):
  return sum(range(1, n+1))
```

## Productorio

El productorio de una secuencia de números:

```python
def productorio(n):
  producto = 1
  for i in range(1, n+1):
    producto *= i
  return producto
```

## Factorial

El factorial de un número:

```python
def factorial(n):
  if n == 0:
    return 1
  else:
    return n * factorial(n - 1)
```

## Obtener número primo

Para verificar si un número es primo:

```python
def es_primo(n):
  if n <= 1:
    return False
  for i in range(2, n):
    if n % i == 0:
      return False
  return True
```

## Suma de factoriales

Suma de los factoriales de los primeros N números:

```python
def suma_factoriales(n):
  total = 0
  for i in range(1, n+1):
    total += factorial(i)
  return total
```

## Media de N números

Calcular la media de N números:

```python
def media(numeros):
  return sum(numeros) / len(numeros)
```

## Número capicúa

Verificar si un número es capicúa:

```python
def es_capicua(n):
  return str(n) == str(n)[::-1]
```

## Longitud de una cadena

Obtener la longitud de una cadena:

```python
cadena = "Python"
print(len(cadena))  # Imprime 6
```

## Tabla de multiplicar de N

Imprimir la tabla de multiplicar de un número:

```python
def tabla_multiplicar(n):
  for i in range(1, 11):
    print(f"{n} x {i} = {n*i}")
```

## Potencia

Calcular la potencia de un número:

```python
def potencia(base, exponente):
  return base ** exponente
```

## Raíz cuadrada

Calcular la raíz cuadrada:

```python
def raiz_cuadrada(n):
  return n ** 0.5
```

## Redondeo

Redondear un número a un número determinado de decimales:

```python
def redondear(n, decimales):
  return round(n, decimales)
```

## Imprimir número impar hasta un número dado

Imprimir todos los números impares hasta un número dado:

```python
def imprimir_impares(n):
  for i in range(1, n+1, 2):
    print(i)
```
