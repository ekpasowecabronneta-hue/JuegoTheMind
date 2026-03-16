# Juego The Mind
Una adaptación del **The Mind**, desarrollada en **C++** para consola, donde los jugadores deben colaborar para colocar cartas numeradas en orden ascendente sin comunicarse entre sí.  

Incluye **sistema de gestión de niveles, vidas y estrellas, control del mazo y las cartas jugadas**, y un **menú interactivo con reglas integradas** para facilitar la experiencia del jugador

Ideal para practicar **programación estructurada y orientada a objetos en C++**, diseño de **lógica de juegos y manejo de estructuras de datos**.

---

## 🚀 Instalación

### 1️⃣ Clona o descarga este repositorio

```bash
git clone https://github.com/Santiagox01/JuegoColoretteCPP
````

### 2️⃣ Compila el juego

```bash
make 
```

> **Nota:** Asegúrate de que tu compilador soporte **C++11** o superior.

---

## 🕹️ Uso

1. **Ejecuta el programa compilado**

   ```bash
   make run
   ```

   o directamente:

   ```bash
   ./Colorette
   ```

2. **Menú Principal:**

   * 🎮 **Nueva Partida** → Inicia una nueva sesión local (3 a 5 jugadores humanos)
   * 💾 **Cargar Partida** → Reanuda una partida guardada
   * 🗂️ **Administrar Partidas** → Lista y elimina partidas guardadas
   * 🚪 **Salir** → Cierra el juego

3. **Nueva Partida:**

   * Elige el número de jugadores (de 3 a 5)
   * Ingresa un nombre para la partida (sin espacios)
   * Se mostrarán las **reglas completas** del juego
   * Presiona **Enter** para comenzar

4. **Durante la Partida:**

   * Cada jugador puede **robar una carta** del mazo y colocarla en una fila
   * O bien, **tomar una fila completa** de cartas disponibles
   * Cuando todos los jugadores han tomado una fila, inicia una nueva ronda
   * La carta **“Última Ronda”** marca el final del juego

5. **Puntuación Final:**

   * Cada jugador elige **3 colores positivos**, los demás se cuentan como negativos
   * Las cartas **+2** suman puntos extra
   * El sistema aplica la tabla oficial de puntuación automáticamente

6. **Guardado y Carga:**

   * Las partidas se almacenan en la carpeta `saves/`
   * Puedes cargarlas o eliminarlas desde el menú principal

---

## ✨ Características

🃏 **Modo Local Multijugador** — Hasta 5 jugadores humanos en una sola consola
💾 **Sistema de Guardado Completo** — Guarda y reanuda partidas fácilmente
📚 **Reglas Integradas** — Explicación detallada antes de comenzar
🧠 **Estrategia Pura** — Elige bien tus colores positivos y negativos
🗂️ **Gestor de Partidas** — Lista, carga o elimina tus partidas guardadas

---

## 🧩 Arquitectura del Proyecto

### 🔹 Clases Principales

#### 🟨 `Juego`

* **Responsabilidad:** Controla la lógica general de las partidas.
* **Métodos principales:**

  * `inicializarMazo(int jugadores)`
  * `barajar()`
  * `crearJugadores(int jugadores)`
  * `repartirCartasIniciales()`
  * `ejecutarJuegoConGuardado(string nombrePartida)`
  * `cargarPartida(string ruta)`

#### 🟩 `SaveManager`

* **Responsabilidad:** Gestiona el guardado y la eliminación de partidas.
* **Métodos principales:**

  * `listarPartidas()`
  * `eliminarPartida(string nombre)`
  * `guardarPartida(string nombre, Estado estado)`

#### 🟦 `Jugador`

* **Responsabilidad:** Representar a un jugador humano.
* **Atributos:**

  * `nombre`, `cartas`
* **Métodos:**

  * `tomarFila()`
  * `elegirColorPositivo()`

#### 🟥 `Carta`

* **Responsabilidad:** Representa una carta individual.
* **Atributos:**

  * `color`, `valor`
* **Ejemplo:** cartas de color o carta especial “+2” o “Última Ronda”.

#### 🟪 `Mazo`

* **Responsabilidad:** Gestiona todas las cartas del juego.
* **Métodos principales:**

  * `barajar()`
  * `robarCarta()`

#### 🟫 `FilaDeJuego`

* **Responsabilidad:** Representar las filas de cartas en la mesa.
* **Métodos principales:**

  * `agregarCarta(Carta c)`
  * `estaCompleta()`

---

## 📂 Estructuras de Datos

### `EstadoPartida`

Estructura que almacena el progreso completo del juego:

* `mazo`: Cartas restantes
* `jugadores`: Lista de jugadores y sus cartas
* `filas`: Estado actual de las filas
* `rondaActual`: Número de ronda
* `ultimaRonda`: Indica si es la ronda final

---

## 🔁 Ejemplo de Flujo de Juego

1. Se eligen 3-5 jugadores y se asigna un nombre de partida
2. Se prepara el mazo según las reglas del número de jugadores
3. Cada jugador en su turno elige entre **robar** o **tomar una fila**
4. Se repite hasta que todos hayan tomado una fila
5. Al llegar la **Última Ronda**, se calcula la puntuación
6. Se guardan los resultados automáticamente

---

## 🤝 Contribuciones

Si deseas mejorar el proyecto, contáctanos:

* [@Santiagox01](https://github.com/Santiagox01)
* [@YForondaa](https://github.com/YForondaa)
* [@jaiderehaco-eng](https://github.com/jaiderehaco-eng)

---

## 👨‍💻 Desarrollado por

**Estudiantes del ITM:**

* Santiago Jaramillo Valencia
* Yenifer Foronda Hernandez
* Jayder Alejandro Arias Arango

---

🎨 **¡Disfruta de Colorette y demuestra tu mejor estrategia de colores!**
