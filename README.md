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
---

2. **Como crear una partida**

   *Ejecuta el comando correspondiente en el bot

   ```bash
  /neww_mind
  
  ```
    *Y se va a generar un id unico como por ejemplo

  ```bash
  game_1774552318_6vq9

  ```
---

3. **Como invitar jugadores**

   *Comparte el id unico de la partida que se te genero con los otros jugadores

   *⚠️ Restricción:
   *Solo pueden unirse usuarios que pertenezcan al /team actual.



5. **🧠 Unirse a la Partida**

    * Cada jugador debe:
    * Abrir el chat privado (DM) con el bot
    * Enviar el comando que anteriormente se le genero

     ```bash
      game_1774552318_6vq9

      ```
  ---
5. **Ver el estado de la partida**

    *Con el comando /game

     ```bash
      /game
  ```

 *Permite ver los jugadores registrados en la partida actual

  
    *El juego se organiza por niveles, cada uno representado por una Ronda
    *En cada nivel, el sistema reparte cartas desde el Mazo a cada Jugador
    *Cada jugador almacena sus cartas en su ManoJugador (ordenadas automáticamente)
    *Sin comunicarse, los jugadores deben jugar cartas en orden ascendente



6. **Iniciar la partida**

 *El anfitrion ejecuta el comando de inicio:
 
 /start_mind game_1774552318_6vq9
     
  
7. **Turno de juego:**
   
    +Un jugador usa jugarCarta()
    *La carta se coloca en la PilaMesa
    *La Ronda valida si la jugada es correcta:
    *✔️ Si es mayor que la anterior → continúa la ronda
    *❌ Si no → se considera error
    *❌ Errores y Penalizaciones
    *Si una carta rompe el orden:
    *Se pierde un vida
    


9. **⭐ Uso de Shurikens**
    *Un jugador puede proponer usar un shuriken
    *Si todos aceptan:
    *usarShuriken() activa el efecto
    *Cada jugador descarta su carta más baja 



11. **🔁 Progreso del Juego**
    *Cuando todos los jugadores juegan sus cartas correctamente:
    *Se completa la Ronda
    *Se avanza al siguiente nivel (nivelActual++)
    *Se reparten nuevas cartas


11. **🏆 Final del Juego**
    *Si completan todos los niveles → ¡Victoria! 🎉
    *Si las vidas llegan a 0 → Fin del juego



13. **💾 Guardado y Carga**
    *Las partidas se almacenan 
    *se guarda el estado completo:
    *jugadores
    *mazo
    *ronda actual
    *vidas, shurikens y nivel
   


## ✨ Características

🧠 **Juego Cooperativo** — Todos ganan o pierden juntos
🤫 **Sin Comunicación** — Basado en intuición
📊 **Control por Niveles** — Aumenta la dificultad progresivamente
💾 **Sistema de Guardado** — Persistencia completa del estado
⚙️ **Arquitectura Modular** — Basada en clases como Juego, Ronda y Jugador



## 🔁 Ejemplo de Flujo de Juego
  1. Se inicia una partida con el comando 
  2. El sistema prepara el nivel
  3. Cada jugador recibe cartas del Mazo
  4. Se inicia una Ronda
  5. Los jugadores juegan cartas en orden:
  6. Si aciertan → continúan
  7. Si fallan → pierden vidas
  8. Pueden usar shurikens estratégicamente
  9. Se completa la ronda y se avanza de nivel
  10. El juego termina al ganar o perder todas las vidas


