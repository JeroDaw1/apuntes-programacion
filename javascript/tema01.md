# Importaciones en JavaScript

En JavaScript moderno (ES6+), podemos importar módulos para usar funciones, objetos o variables de otros archivos.

```javascript
// Importación de módulos
import { nombreModulo } from './modulo.js' // Importar algo específico

import * as modulo from './modulo.js' // Importar todo el módulo

// Importación de la exportación por defecto
import modulo from './modulo.js' // Importa la exportación por defecto
```

# Comentarios

Los comentarios son esenciales para hacer el código más entendible.

```javascript
// Este es un comentario de una sola línea

/*
Este es un comentario de múltiples líneas
que puede extenderse por varias líneas
*/
```

# Impresión por consola

Se usa console.log() para imprimir mensajes o valores en la consola.

```javascript
console.log('Hola, Mundo!') // Imprime un mensaje en la consola
console.log(5 + 3) // Imprime el resultado de una operación
```

# Declaración de Variables y Constantes

En JavaScript, se usan `var`, `let` y `const` para declarar variables. Aquí están sus diferencias:

- `var`: Declaración de variables con un alcance global o de función. Su uso es más antiguo y menos recomendable.
- `let`: Declaración de variables con alcance de bloque (más moderno y recomendado).
- `const`: Declaración de constantes (variables que no cambian).

```javascript
var x = 10 // Puede ser redeclarada
let y = 20 // No puede ser redeclarada en el mismo bloque
const z = 30 // No puede ser redeclarada ni reasignada

// Diferencia entre var y let
if (true) {
  var a = 1 // 'a' tiene un alcance global o de función
  let b = 2 // 'b' solo existe dentro de este bloque
}
console.log(a) // 1
console.log(b) // Error: b is not defined
```

# Tipos Primitivos

En JavaScript, los tipos primitivos incluyen:

- Number: 42, 3.14
- String: "Hola"
- Boolean: true o false
- Null: null
- Undefined: undefined
- Symbol: Tipo único y mutable
- BigInt: Para números grandes

```javascript
let edad = 25 // Number
let nombre = 'Juan' // String
let esEstudiante = true // Boolean
let x = null // Null
let y // Undefined
```

# Comparaciones Lógicas

Las comparaciones lógicas se utilizan para evaluar condiciones.
Operadores:

- ==: Compara valores, pero no tipos (coerción de tipos).
- ===: Compara valores y tipos.
- !=: Diferente valor (con coerción de tipos).
- !==: Diferente valor y tipo.

```javascript
console.log(5 == '5') // true (coerción de tipo)
console.log(5 === '5') // false (sin coerción de tipo)
```

# Asignaciones Operacionales

Permiten realizar operaciones y asignarlas en una sola expresión.

```javascript
let x = 10
x += 5 // x = x + 5 => 15
x -= 2 // x = x - 2 => 13
x *= 3 // x = x * 3 => 39
x /= 3 // x = x / 3 => 13
```

# Operadores Aritméticos

Son los operadores básicos para trabajar con números.

```javascript
let a = 10
let b = 5
console.log(a + b) // Suma
console.log(a - b) // Resta
console.log(a * b) // Multiplicación
console.log(a / b) // División
console.log(a % b) // Módulo (resto de la división)
console.log(a ** b) // Exponenciación
```

# Operadores Lógicos

Estos operadores sirven para comparar expresiones booleanas.

```javascript
let a = true
let b = false
console.log(a && b) // AND
console.log(a || b) // OR
console.log(!a) // NOT
```

# Condiciones (if, else, else if)

Se usan para tomar decisiones en función de una condición.

```javascript
let edad = 18
if (edad >= 18) {
  console.log('Es mayor de edad')
} else {
  console.log('Es menor de edad')
}
```

# Condiciones Anidadas

Puedes tener condiciones dentro de otras.

```javascript
let edad = 20
let ciudad = 'Madrid'

if (edad >= 18) {
  if (ciudad === 'Madrid') {
    console.log('Mayor de edad y en Madrid')
  }
} else {
  console.log('Menor de edad')
}
```

# Valores Truthy y Falsy

En JavaScript, los valores pueden evaluarse como true o false en un contexto lógico.
Falsy:

- `false`
- `0`
- `""` (cadena vacía)
- `null`
- `undefined`
- `NaN`

Truthy:

Cualquier valor que no sea uno de los anteriores es considerado "truthy", como los números distintos de cero, objetos, y arrays.

# Bucle while

El bucle `while` ejecuta un bloque de código mientras la condición sea verdadera.

```javascript
let i = 0
while (i < 5) {
  console.log(i)
  i++
}
```

# Bucle do while

Este bucle garantiza que el código se ejecute al menos una vez, ya que la condición se evalúa después de ejecutar el bloque.

```javascript
let i = 0
do {
  console.log(i)
  i++
} while (i < 5)
```

# Bucle for

El bucle `for` es útil cuando se sabe cuántas veces se debe ejecutar el código.

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i)
}
```

# Longitud de Elementos

Para obtener la longitud de una cadena, arreglo u otro objeto iterable, se usa `.length`.

```javascript
let arreglo = [1, 2, 3, 4]
console.log(arreglo.length) // 4

let texto = 'Hola Mundo'
console.log(texto.length) // 10
```

# Funciones

Una función es un bloque de código que puede ser llamado para ejecutar una tarea específica.

```javascript
function saludar(nombre) {
  console.log('Hola, ' + nombre)
}
saludar('Juan') // Llama a la función
```

# Función Flecha (Arrow Function)

Las funciones flecha son una forma más concisa de escribir funciones.

```javascript
const saludar = nombre => {
  console.log('Hola, ' + nombre)
}
saludar('Ana')
```

# Excepciones con Bloques try-catch-finally

Las excepciones permiten manejar errores sin interrumpir el flujo del programa.

```javascript
try {
  let x = 10 / 0 // Esto podría causar un error
  console.log(x)
} catch (error) {
  console.log('Ocurrió un error:', error)
} finally {
  console.log('Este bloque siempre se ejecuta.')
}
```
