---
title: "Tic Tac Toe with javascript + HTML basic usacase"
meta_title: "Tic Tac Toe with javascript + HTML basic usacase"
description: "Tic-Tac-Toe es un juego de dos jugadores que alternan turnos para colocar sus marcas ('X' o 'O') en una cuadrícula de 3x3. El objetivo es lograr tres en línea (horizontal, vertical o diagonal) antes que el oponente."
date: 2022-03-19T05:00:00Z
image: "/images/tic-tac-toe.png"
categories: ["Juegos", "Javscript", "HTML"]
author: "LBYTE"
tags: ["javascript", "html"]
draft: false
---


### 📌 Análisis del Problema
Tic-Tac-Toe es un juego de dos jugadores que alternan turnos para colocar sus marcas ("X" o "O") en una cuadrícula de 3x3. El objetivo es lograr tres en línea (horizontal, vertical o diagonal) antes que el oponente.

#### 📋 Reglas del Juego

1. Se juega en un tablero de 3x3.
2. Dos jugadores alternan turnos: Jugador 1 ("X") y Jugador 2 ("O").
3. Un jugador gana si coloca tres de sus marcas en línea (horizontal, vertical o diagonal).
4. El juego termina en empate si el tablero se llena sin un ganador.
5. No se permite colocar una marca en una casilla ya ocupada.

### 📌 Algoritmo para Implementar el Juego

#### 1️⃣ Inicialización

1. Crear una matriz de 3x3 vacía para representar el tablero.
2. Definir los símbolos de los jugadores ("X" y "O").
3. Establecer una variable para rastrear el turno actual.


#### 2️⃣ Bucle Principal del Juego

1. Mostrar el tablero al usuario.
2. Pedir al jugador actual que ingrese la fila y la columna donde quiere jugar.
    * Verificar que la casilla esté vacía antes de permitir la jugada.
3. Colocar la marca del jugador en la posición elegida.
4. Comprobar si el jugador ha ganado con esta jugada.
    * Si ganó, mostrar el tablero y terminar el juego.
5. Si no hay ganador y el tablero está lleno, declarar empate.
6. Alternar el turno al otro jugador.
7. Repetir hasta que haya un ganador o empate.

#### 3️⃣ Comprobación de Ganador

Un jugador gana si:

1. Alguna fila contiene las mismas tres marcas.
2. Alguna columna contiene las mismas tres marcas.
3. Una de las diagonales contiene las mismas tres marcas.

#### 4️⃣ Fin del Juego
1. Si hay un ganador, anunciarlo y finalizar el programa.
2. Si hay empate, mostrar un mensaje y finalizar.

### 📌 Implementación en Código (Javascript)

1. Crear una matriz de 3x3 vacía para representar el tablero.

    * crear un folder desde el navegador de archivos o usando la terminal 

        ```
        mkdir NOMBRE_DEL_FOLDER
        ```
    * navegar al tu proyecto y crear un archivo html
        ```
        touch index.html
        ```
    
        ```html
        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Tic-Tac-Toe</title>
        </head>
        <body>
            <h1>Tic-Tac-Toe</h1>
            <div class="board" id="board"></div>
            <p id="status"></p>
            <button>Reiniciar</button>
        </body>
        </html>

        ```

    * creamos el archivo de javascript
    ```
    touch scripts.js
    ```



### 📌 Codigo Fuente

* Para ver el codigo fuente del ejercicio visita el siguiente link

   https://github.com/rubenpazch/tic-tac-toe-with-js.git 

* Para clonar el proyecto en github

    ```
    git clone https://github.com/rubenpazch/tic-tac-toe-with-js.git
    ```