### 📌 Análisis del Problema
Tic-Tac-Toe es un juego de dos jugadores que alternan turnos para colocar sus marcas ("X" o "O") en una cuadrícula de 3x3. El objetivo es lograr tres en línea (horizontal, vertical o diagonal) antes que el oponente.

#### 📋 Reglas del Juego

Se juega en un tablero de 3x3.
Dos jugadores alternan turnos: Jugador 1 ("X") y Jugador 2 ("O").
Un jugador gana si coloca tres de sus marcas en línea (horizontal, vertical o diagonal).
El juego termina en empate si el tablero se llena sin un ganador.
No se permite colocar una marca en una casilla ya ocupada.

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

### 📌 Implementación en Código (Python)
