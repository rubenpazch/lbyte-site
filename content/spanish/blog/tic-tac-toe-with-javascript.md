---
title: Tic Tac Toe with javascript + HTML basic usacase
meta_title: Tic Tac Toe with javascript + HTML basic usacase
description: Tic-Tac-Toe es un juego de dos jugadores que alternan turnos para colocar sus marcas ('X' o 'O') en una cuadrícula de 3x3. El objetivo es lograr tres en línea (horizontal, vertical o diagonal) antes que el oponente.
date: 2022-03-19T05:00:00.000Z
image: /images/tic-tac-toe.png
categories: [Juegos, Javascript, HTML]
author: LBYTE
tags: [javascript, html]
draft: false
---


### Análisis del Problema

Tic-Tac-Toe es un juego de dos jugadores que alternan turnos para colocar sus marcas ("X" o "O") en una cuadrícula de 3x3. El objetivo es lograr tres en línea (horizontal, vertical o diagonal) antes que el oponente.

#### Reglas del Juego

* Se juega en un tablero de 3x3.
* Dos jugadores alternan turnos: Jugador 1 ("X") y Jugador 2 ("O").
* Un jugador gana si coloca tres de sus marcas en línea (horizontal, vertical o diagonal).
* El juego termina en empate si el tablero se llena sin un ganador.
* No se permite colocar una marca en una casilla ya ocupada.

### Algoritmo para Implementar el Juego

#### Inicialización

* Crear una matriz de 3x3 vacía para representar el tablero.
* Definir los símbolos de los jugadores ("X" y "O").
* Establecer una variable para rastrear el turno actual.

#### Bucle Principal del Juego

1. Mostrar el tablero al usuario.
2. Pedir al jugador actual que ingrese la fila y la columna donde quiere jugar.
   - Verificar que la casilla esté vacía antes de permitir la jugada.
3. Colocar la marca del jugador en la posición elegida.
4. Comprobar si el jugador ha ganado con esta jugada.
   - Si ganó, mostrar el tablero y terminar el juego.
5. Si no hay ganador y el tablero está lleno, declarar empate.
6. Alternar el turno al otro jugador.
7. Repetir hasta que haya un ganador o empate.

#### Comprobación de Ganador

Un jugador gana si:

* Alguna fila contiene las mismas tres marcas.
* Alguna columna contiene las mismas tres marcas.
* Una de las diagonales contiene las mismas tres marcas.

#### Fin del Juego

* Si hay un ganador, anunciarlo y finalizar el programa.
* Si hay empate, mostrar un mensaje y finalizar.

### Implementación en Código (Javascript)

#### Mostrar el tablero al usuario.

estructura del proyecto
* 📂 nombre_del_proyecto
  * 📄 index.html
  * 📄 scripts.js
  * 📄 styles.css


crear un folder desde el navegador de archivos o usando la terminal

```bash
mkdir nombre_del_proyecto
```

navegar a tu proyecto y crear un archivo html

```bash
touch index.html
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tic-Tac-Toe</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Tic-Tac-Toe</h1>
    <div class="tablero" id="tablero"></div>
    <p id="estado"></p>
    <button>Reiniciar</button>
    <script src="scripts.js"></script>
</body>
</html>
```

{{< notice "Notas" >}}
Hemos definido el titulo del juego haciendo uso de la etiqueta **h1**, luego tenemos
{{< /notice >}}


creamos el archivo de javascript

```bash
touch scripts.js
```

agregamos el codigo que nos permitira crear el tablero dinamicamente

```javascript
const tablero = document.getElementById("tablero");
const estado = document.getElementById("estado");
let celdas = [];
let jugadorActual = "X";
let juegoActivado = true;

function crearTablero() {
    tablero.innerHTML = "";
    celdas = [];
    for (let i = 0; i < 9; i++) {
        const celda = document.createElement("div");
        celda.classList.add("celda");
        celda.dataset.index = i;
        tablero.appendChild(celda);
        celdas.push(cell);
    }
    estado.textContent = `Turno de ${jugadorActual}`;
}

crearTablero();
```

{{< notice "Notas" >}}
ss
{{< /notice >}}

        
finalmente incluimos los estilos que nos permitiran dar algo de orden a nuestro a codigo

```css
.tablero {
    display: grid;
    grid-template-columns: repeat(3, 100px);
    gap: 5px;
    margin: 20px auto;
    width: max-content;
}
.celda {
    width: 100px;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2em;
    border: 2px solid black;
    cursor: pointer;
}
```

Hasta ahora tenemos el siguiente resultado

{{< notice "warning" >}}
Hasta ahora tenemos el tablero donde hemos definido una etiqueta **H1** para definir el titulo, luego tenemos la etiqueta **DIV** que envuelve todas las celdas del table, notar que hemos establecido una clase **"tablero"** para la tabla y otra clase **"celda"** para las celdas
{{< /notice >}}

{{< image src="images/tic-tac-toe-with-javascript/parte1-tic-tac-toe.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}


{{< notice "warning" >}}
Hasta ahora tenemos el tablero donde hemos definido una etiqueta **H1** para definir el titulo, luego tenemos la etiqueta **DIV** que envuelve todas las celdas del table, notar que hemos establecido una clase **"tablero"** para la tabla y otra clase **"celda"** para las celdas
{{< /notice >}}


### Codigo Fuente

-   Para ver el codigo fuente del ejercicio visita el siguiente link

     <https://github.com/rubenpazch/tic-tac-toe-with-js.git>

-   Para clonar el proyecto en github

    ```bash
    git clone https://github.com/rubenpazch/tic-tac-toe-with-js.git
    ```
