<div align="center">
  <h1>🧟‍♂️ Zombie Survival 3D: Gas Station</h1>
  <p><i>Un trepidante FPS de supervivencia zombie basado en la web, construido en un solo archivo HTML.</i></p>
  
  ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
  ![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=threedotjs&logoColor=white)
  ![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
  ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
</div>

<br>

## 🎮 Sobre el Juego

**Zombie Survival 3D** es un shooter en primera persona (FPS) donde debes sobrevivir el mayor tiempo posible a oleadas infinitas de zombies en una gasolinera abandonada. El juego destaca por su arquitectura única: **todo el código (HTML, CSS, JS, lógicas, texturas y modelos) está contenido en un único archivo `index.html`**, logrando un alto rendimiento sin necesidad de descargar assets externos pesados.

---

## ✨ Características Principales

*   🔫 **Armamento Dinámico:**
    *   `[1] Glock`: Precisa y confiable, fuego semiautomático.
    *   `[2] Escopeta`: Daño masivo de área para corta distancia (dispersión de 5 perdigones).
    *   `[3] SMG`: Subfusil automático de alta cadencia (Se desbloquea al alcanzar 8,000 puntos).
*   🧟 **Enemigos Procedurales:**
    *   🟢 **Walker:** Zombie estándar, rápido pero frágil (100 PTS).
    *   🟠 **Bruiser:** Zombie resistente y corpulento (200 PTS).
    *   🔴 **Mutante (Jefe):** Gigante y letal, aparece en rondas altas (500 PTS).
*   📈 **Dificultad Escalable:** Conforme aumenta tu puntuación, los zombies generan más rápido y se mueven a mayor velocidad.
*   ⚡ **Alto Rendimiento:** Utiliza *Object Pooling* para el manejo de memoria de balas y partículas de sangre, garantizando 60 FPS estables.

---

## ⌨️ Controles

| Tecla / Acción | Descripción |
| :--- | :--- |
| `W` `A` `S` `D` | Mover al jugador |
| `Mouse` | Apuntar y mirar |
| `Click Izquierdo` | Disparar armas |
| `1`, `2`, `3` | Cambiar de arma (Glock, Escopeta, SMG) |

---

## 🛠️ Cómo Funciona (Arquitectura Técnica)

Este juego fue construido utilizando **Three.js** para el renderizado 3D y **Tailwind CSS** para la interfaz gráfica (HUD). Algunas de sus características técnicas más interesantes son:

1.  **Texturas Procedurales Canvas:** Para mantener el juego en un solo archivo, los rostros y la ropa rasgada de los zombies se dibujan matemáticamente utilizando la API de Canvas 2D en tiempo real al cargar el juego.
2.  **Motor de Colisiones AABB Vectorial:** El juego no utiliza un motor de físicas pesado (como Cannon.js o Ammo.js). En su lugar, usa un sistema personalizado de colisiones 2D de Cajas Delimitadoras Alineadas a los Ejes (AABB). Esto permite que el jugador y los zombies "se deslicen" suavemente por las paredes sin quedarse atascados.
3.  **Object Pooling (Piscina de Objetos):** Para evitar fugas de memoria (Memory Leaks) y tirones de rendimiento (Stutters) por el Recolector de Basura (Garbage Collector), las partículas de sangre y las balas se reciclan en memoria en lugar de crearse y destruirse constantemente.

---

## 🚀 Instalación y Uso

Dado que el juego completo vive en un solo archivo, no requiere servidor local ni instalación de dependencias (Node.js/NPM).

1. Clona o descarga este repositorio.
2. Haz doble clic en el archivo `index.html` para abrirlo en cualquier navegador web moderno (Chrome, Edge, Firefox, Brave).
3. ¡Haz clic en "Deploy Now" y empieza a jugar!

---

## 🚧 Cosas por Mejorar (Roadmap)

Este proyecto es una base excelente, pero siempre hay espacio para crecer. ¡Las contribuciones son bienvenidas!

- [ ] **Efectos de Sonido (SFX):** Añadir sonidos de disparos, recargas, gruñidos de zombies y música de fondo usando la Web Audio API.
- [ ] **Sistema de Rondas:** Cambiar el modelo de oleada infinita por un sistema de rondas estructurado (estilo Call of Duty Zombies).
- [ ] **Power-Ups (Drops):** Hacer que los zombies suelten objetos como "Insta-Kill", "Munición Máxima" o "Curación".
- [ ] **Iluminación Dinámica Avanzada:** Transición de día a noche mientras sobrevives.
- [ ] **Soporte Móvil:** Añadir un joystick virtual (on-screen touch controls) para poder jugar en dispositivos móviles.

---

## 📝 Licencia

Este proyecto es de código abierto. Siéntete libre de clonarlo, modificarlo y crear tus propias versiones. ¡No olvides dar los créditos!
