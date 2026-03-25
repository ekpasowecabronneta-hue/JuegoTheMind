# 🚀 Instalación

1️⃣ Clona o descarga este repositorio

git clone https://github.com/Santiagox01/JuegoColoretteCPP


2️⃣ Compila el juego

make


Nota: Asegúrate de que tu compilador soporte C++11 o superior.

🕹️ Uso

Ejecuta el programa compilado

make run


o directamente:

./TheMind

🎮 Menú Principal

🎮 Nueva Partida → Inicia una nueva sesión cooperativa (2 a 4 jugadores)
💾 Cargar Partida → Reanuda una partida guardada
🗂️ Administrar Partidas → Lista y elimina partidas guardadas
🚪 Salir → Cierra el juego

🧠 Nueva Partida
Elige el número de jugadores (de 2 a 4)
Ingresa un nombre para la partida (sin espacios)
Se inicializan las vidas ❤️, shurikens ⭐ y el nivel actual
Presiona Enter para comenzar
🎮 Durante la Partida
El juego se organiza por niveles, cada uno representado por una Ronda
En cada nivel, el sistema reparte cartas desde el Mazo a cada Jugador
Cada jugador almacena sus cartas en su ManoJugador (ordenadas automáticamente)
Sin comunicarse, los jugadores deben jugar cartas en orden ascendente
🔄 Turno de juego:
Un jugador usa jugarCarta()
La carta se coloca en la PilaMesa
La Ronda valida si la jugada es correcta:
✔️ Si es mayor que la anterior → continúa la ronda
❌ Si no → se considera error
❌ Errores y Penalizaciones
Si una carta rompe el orden:
Se ejecuta esErrorDeSecuencia()
Se aplica aplicarPenalizacion()
El juego reduce vidas con reducirVida()
⭐ Uso de Shurikens
Un jugador puede proponer usar un shuriken
Si todos aceptan:
usarShuriken() activa el efecto
Cada jugador descarta su carta más baja (extraerMinima())
🔁 Progreso del Juego
Cuando todos los jugadores juegan sus cartas correctamente:
Se completa la Ronda
Se avanza al siguiente nivel (nivelActual++)
Se reparten nuevas cartas
🏆 Final del Juego
Si completan todos los niveles → ¡Victoria! 🎉
Si las vidas llegan a 0 → Fin del juego
💾 Guardado y Carga
Las partidas se almacenan en la carpeta saves/
Se guarda el estado completo:
jugadores
mazo
ronda actual
vidas, shurikens y nivel
✨ Características

🧠 Juego Cooperativo — Todos ganan o pierden juntos
🤫 Sin Comunicación — Basado en intuición
📊 Control por Niveles — Aumenta la dificultad progresivamente
💾 Sistema de Guardado — Persistencia completa del estado
⚙️ Arquitectura Modular — Basada en clases como Juego, Ronda y Jugador

🔁 Ejemplo de Flujo de Juego
Se inicia una partida con iniciarPartida()
El sistema prepara el nivel con prepararNivel()
Cada jugador recibe cartas del Mazo
Se inicia una Ronda
Los jugadores juegan cartas en orden:
Si aciertan → continúan
Si fallan → pierden vidas
Pueden usar shurikens estratégicamente
Se completa la ronda y se avanza de nivel
El juego termina al ganar o perder todas las vidas
