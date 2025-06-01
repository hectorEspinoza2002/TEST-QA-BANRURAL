# Estrategia de Testeo - Juego "Adivina tu número"

## Objetivo
Verificar que el juego cumpla con la lógica establecida: permitir al usuario adivinar un número aleatorio entre 1 y 100 en un máximo de 5 intentos, indicando si el número es más alto o más bajo.

## Tipos de pruebas realizadas

### 1. Pruebas funcionales
- Se verifico que el juego genere un número aleatorio entre 1 y 100.
- Se verifico que el botón "Ingresar el número" compare correctamente la entrada del usuario.
- Se muestran mensajes correctos según el resultado: victoria, derrota, mayor/menor.
- Se deshabilito la entrada luego de 5 intentos o al adivinar el número.
- Se muestrar el botón de reinicio y que reinicie correctamente el juego.

### 2. Pruebas de validación de entrada
- Verificar comportamiento con entrada vacía.
- Verificar comportamiento con texto no numérico.
- Verificar números fuera del rango (negativos, mayores de 100).

### 3. Pruebas de usabilidad
- Se enfoca automáticamente el campo de entrada tras cada intento.
- Los mensajes son claros, visibles y contrastan bien con el fondo.
- El botón de reinicio aparece solo cuando el juego termina.

## Herramientas usadas
- Navegador web (Chrome)
- Consola del navegador para verificar valores generados y errores de JavaScript

## Resultados
Todas las pruebas fueron satisfactorias. La aplicación es funcional, clara para el usuario y cumple con la lógica de negocio planteada.

## Recomendaciones futuras
- Añadir validación visual para entradas inválidas.
- Limitar a solo números positivos entre 1 y 100.
- Mejorar estilos visuales y accesibilidad.


## Correcciones realizadas:

- Se generaba un número entre 0 y 10 en lugar de 1 a 100.

- Había confusión en la lógica: el mensaje de "perdiste" aparecía al adivinar el número y el de "ganaste" al fallar todos los intentos.

- Faltaba el . en el selector de lowOrHi (document.querySelector('lowOrHi') correccion => document.querySelector('.lowOrHi')).

- addeventListener estaba mal escrito. Es addEventListener.

- Comparabas un string con un número (userGuess === randomNumber). Debes convertir userGuess a número.

La lógica de victoria y derrota estaba invertida.

En randomNumber = Math.floor(Math.random()) + 1, el número generado siempre sería 1.