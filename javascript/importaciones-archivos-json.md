# Función fetch

La función `leerArchivoJugadores()` utiliza la API `fetch` para obtener el archivo players.json, luego lo convierte a formato JSON con `.json()`. Si la operación es exitosa, los datos se asignan a la variable `players`. Si ocurre algún error durante el proceso, se captura con `.catch()` y se devuelve el error.

```js
async function leerArchivoJugadores() {
  try {
    const response = await fetch('./players.json')
    if (!response.ok) {
      throw new Error('Error al cargar el archivo JSON')
    }
    const data = await response.json()
    return data // Devuelve los datos para que puedan ser utilizados
  } catch (error) {
    console.error('Error al leer archivo de jugadores:', error)
    throw error // Vuelve a lanzar el error para manejarlo fuera si es necesario
  }
}
```

# Función callback

- `leerJsonPalabras()`: Esta función es asincrónica y utiliza `await` para esperar que el archivo `words.json` se lea correctamente y lo convierta en un objeto JSON. La función luego devuelve el objeto JSON.
- `obtenerPalabras()`: Esta función obtiene las palabras del archivo JSON a través de `leerJsonPalabras()`, selecciona una palabra aleatoria del archivo y la muestra en el DOM.

```js
let palabraSecretaHtml = document.getElementById('palabra-secreta')
// Función que lee el archivo JSON de las palabras
const leerJsonPalabras = async () => {
  try {
    const response = await fetch('./words.json')
    if (!response.ok) {
      throw new Error('Error al cargar el archivo de palabras')
    }
    const wordsJson = await response.json()
    return wordsJson // Devuelve el objeto JSON completo
  } catch (error) {
    console.error('Error al leer archivo de palabras:', error)
    throw error // Lanza el error para poder manejarlo fuera si es necesario
  }
}

// Función que obtiene las palabras del archivo JSON
const obtenerPalabras = async () => {
  try {
    const jsonData = await leerJsonPalabras() // Esperamos la respuesta del archivo JSON
    const { words } = jsonData // Desestructuración para obtener las palabras. Es igual que usar `const words = jsonData.words`

    const palabraSecreta = words[Math.floor(Math.random() * words.length)].item

    palabraSecretaHtml.innerText = palabraOculta // Muestra la palabra oculta en el HTML
  } catch (error) {
    console.error('Error al obtener las palabras:', error)
  }
}
```
