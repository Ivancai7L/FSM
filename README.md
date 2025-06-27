# Football Simulation Manager (FSM)

**Fecha:** 25/04/2025

## 👥 Integrantes del grupo

- Quintanilla Lucas Nahuel  
- Langlois Ivan  
- Zelaya Lautaro  

---

## 📝 Documento de Diseño de Juego

### 1. Introducción

**Objetivo:**  
Desarrollar un videojuego de simulación táctica de fútbol en 2D para PC, utilizando Java y el framework LibGDX. El juego, titulado *Football Simulation Manager*, permitirá a los jugadores asumir el rol de director técnico, gestionar equipos, definir tácticas y competir en torneos. El enfoque principal será la gestión táctica y la toma de decisiones, no el control directo de los jugadores.

**Tipo de Vista:**  
Vista top-down (desde arriba), similar a *Online Soccer Manager* o *Football Manager Touch*, con énfasis en simulación de partidos y gestión de plantillas.

---

### 2. Alcance del Proyecto

**Alcance mínimo (versión básica funcional):**
- Modo local sin conexión.
- Gestión de un equipo en una liga ficticia pequeña (4–8 equipos).
- Elección de formaciones, alineaciones y tácticas básicas.
- Simulación de partidos contra IA simple (con lógica probabilística).
- Interfaz básica: menú, gestión de equipo, pantalla de simulación de partidos.
- Guardado/carga de progreso mediante JSON.

**Alcance deseable (versión avanzada):**
- Multijugador en línea con torneos diarios y emparejamiento.
- IA avanzada para bots.
- Comentarios dinámicos más complejos y variados.
- Fichajes, sistema económico y cantera juvenil.
- Estadísticas históricas y rankings globales.
- Personalización de escudos, nombres de equipos, etc.

---

### 3. Descripción de la Propuesta

**Frameworks y librerías:**
- LibGDX: Motor principal del juego.
- Gson: Serialización/deserialización de objetos.
- java.util, java.io, java.time: Manejo de estructuras, persistencia y fechas.
- JUnit: Pruebas unitarias.

**Estructura del juego – Pantallas:**
- Menú Principal  
- Gestión de Equipo  
- Simulación de Partido  
- Estadísticas y resultados

**Mecánicas de Juego:**
- Formaciones: 4-4-2, 4-3-3, 3-5-2, entre otras.
- Tácticas: Presión alta/baja, posesión, contraataque, etc.
- Atributos de los jugadores: Ataque, defensa, resistencia, moral y forma física.
- Eventos: Goles, tarjetas, sustituciones, lesiones.

---

### 4. Detalle de Simulación

- Algoritmo de simulación pondera atributos de jugadores, alineación y táctica.
- La moral afecta el rendimiento en el campo.
- El cansancio acumulado penaliza a jugadores usados sin rotación.
- Los estilos tácticos influyen en la probabilidad de eventos (ej: presión alta → más recuperaciones pero mayor cansancio).
- Cambios tácticos posibles al entretiempo.

---

### 5. Interfaz de Usuario (HUD)

- **Menú Principal:** Nueva partida, cargar, ajustes.
- **Gestión de Equipo:** Plantilla, táctica, estadísticas individuales y colectivas.
- **Simulación:** Panel de comentarios, marcador, barra de tiempo, cambios tácticos.
- **Controles:** Mouse (clic, arrastrar y soltar).

---

### 6. Persistencia de Datos

**Formato:** Archivos JSON.

**Acciones:**
- Guardado automático tras cada partido o cambio de configuración.
- Carga de datos al iniciar partida o aplicación.

---

### 7. Funcionalidad de Red (Alcance Deseable)

- Torneos en línea emparejados automáticamente.
- Servidor central para resultados y rankings.
- IA para equipos faltantes.
- Comunicación mediante sockets o REST API.

---

### 8. Aportes y Originalidad

*Football Simulation Manager* buscará destacarse en:

- **Accesibilidad:** Simulador táctico ligero y multiplataforma para PCs modestas.
- **Enfoque en decisiones:** Minimiza el azar visual y destaca decisiones tácticas.
- **Torneos diarios:** Motivación para partidas cortas pero frecuentes.
- **Diseño modular:** Facilita agregar funcionalidades como economía, fichajes, etc.

---

### 9. Pruebas y Validación

- **Pruebas unitarias:** Algoritmo de simulación, manejo de datos, IA.
- **Pruebas de integración:** Flujo completo entre pantallas y persistencia.
- **Pruebas de red (fase avanzada):** Partidas sincronizadas entre jugadores.

