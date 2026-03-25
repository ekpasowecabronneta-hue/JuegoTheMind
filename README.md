# 🚀 Juego The Mind

Una adaptación del juego cooperativo de cartas **The Mind**, desarrollada en **C++** y con una jugabilidad por medio de un grupo de telegram.
Colabora con tus amigos localmente y pongan a prueba su sincronización mental jugando cartas en orden… ¡sin comunicarse!

Incluye sistema de guardado y carga de partidas, administrador de partidas guardadas, y un completo menú interactivo con reglas integradas.

Ideal para practicar programación estructurada y orientada a objetos en C++ y manejo de archivos.

---

## 🕹️ Uso

1. **Abre el siguiente link de telegram**

  ```bash
  https://t.me/mind_crupier_bot 
  ```


2. **Menú Principal**

    * 🎮 **Nueva Partida** → Inicia una nueva sesión cooperativa (2 a 4 jugadores)
    * 💾 **Cargar Partida** → Reanuda una partida guardada
    * 🗂️ **Administrar Partidas** → Lista y elimina partidas guardadas
    * 🚪 **Salir** → Cierra el juego

3. **🧠 Nueva Partida**

    * Elige el número de jugadores (de 2 a 4)
    * Ingresa un nombre para la partida (sin espacios)
    * Se inicializan las vidas ❤️, shurikens ⭐ y el nivel actual
    * Presiona Enter para comenzar

4. **Durante la Partida**
  
    *El juego se organiza por niveles, cada uno representado por una Ronda
    *En cada nivel, el sistema reparte cartas desde el Mazo a cada Jugador
    *Cada jugador almacena sus cartas en su ManoJugador (ordenadas automáticamente)
    *Sin comunicarse, los jugadores deben jugar cartas en orden ascendente

5. **Turno de juego:**
   
    +Un jugador usa jugarCarta()
    *La carta se coloca en la PilaMesa
    *La Ronda valida si la jugada es correcta:
    *✔️ Si es mayor que la anterior → continúa la ronda
    *❌ Si no → se considera error
    *❌ Errores y Penalizaciones
    *Si una carta rompe el orden:
    *Se ejecuta esErrorDeSecuencia()
    *Se aplica aplicarPenalizacion()
    *El juego reduce vidas con reducirVida()

6. **⭐ Uso de Shurikens**
    *Un jugador puede proponer usar un shuriken
    *Si todos aceptan:
    *usarShuriken() activa el efecto
    *Cada jugador descarta su carta más baja (extraerMinima())

7. **🔁 Progreso del Juego**
    *Cuando todos los jugadores juegan sus cartas correctamente:
    *Se completa la Ronda
    *Se avanza al siguiente nivel (nivelActual++)
    *Se reparten nuevas cartas

8. **🏆 Final del Juego**
    *Si completan todos los niveles → ¡Victoria! 🎉
    *Si las vidas llegan a 0 → Fin del juego

9. **💾 Guardado y Carga**
    *Las partidas se almacenan en la carpeta saves/
    *se guarda el estado completo:
    *jugadores
    *mazo
    *ronda actual
    *vidas, shurikens y nivel
   
---

## ✨ Características

🧠 **Juego Cooperativo** — Todos ganan o pierden juntos
🤫 **Sin Comunicación** — Basado en intuición
📊 **Control por Niveles** — Aumenta la dificultad progresivamente
💾 **Sistema de Guardado** — Persistencia completa del estado
⚙️ **Arquitectura Modular** — Basada en clases como Juego, Ronda y Jugador

---

## 🔁 Ejemplo de Flujo de Juego
  1. Se inicia una partida con el comando *********
  2. El sistema prepara el nivel **********
  3. Cada jugador recibe cartas del Mazo
  4. Se inicia una Ronda
  5. Los jugadores juegan cartas en orden:
  6. Si aciertan → continúan
  7. Si fallan → pierden vidas
  8. Pueden usar shurikens estratégicamente
  9. Se completa la ronda y se avanza de nivel
  10. El juego termina al ganar o perder todas las vidas

---
