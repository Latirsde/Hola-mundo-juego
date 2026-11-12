# Hola mundo — Chronicles of Aethelgard

[![Engine: GDevelop 5.6.287](https://img.shields.io/badge/GDevelop-5.6.287-blue.svg)](https://gdevelop.io/)
[![Platform: Windows Desktop / Web](https://img.shields.io/badge/Platform-Windows%20%7C%20HTML5-lightgrey.svg)]()
[![Status: Complete Prototype](https://img.shields.io/badge/Status-100%25%20Functional-brightgreen.svg)]()

Prototipo funcional de videojuego de plataformas en 2D desarrollado en **GDevelop 5.6.287** como proyecto de evaluación académica. Implementa un mundo de fantasía dividido en dos niveles de 10 pantallas cada uno, físicas de plataformas sólidas y atravesables, 3 clases de NPCs con comportamientos diferenciados, sistema de *checkpoints* persistentes, sonorización ambiental sincronizada y transición cinemática entre niveles.

---

## 1. Ficha del Proyecto y Concepto Lúdico

* **Género:** Plataformas 2D / Fantasía y Aventura.
* **Resolución Nativa:** 1280 × 720 px (16:9 HD).
* **Extensión de Mundo:** 2 niveles de 10 pantallas horizontales continuas cada uno (~12.800 px en el eje X por nivel).
* **Público Objetivo:** Jugadores mayores de 10 años que buscan desafíos de precisión y progresión narrativa.
* **Sinopsis:** Eldrin, caballero protector de Aethelgard, debe atravesar el *Bosque de las Sombras* (Nivel 1) y descender a las *Ruinas* (Nivel 2) para recolectar las Runas Primordiales y restablecer el equilibrio en el reino.

---

## 2. Características y Mecánicas Implementadas

* **Diseño del Mundo y Gráficos:**
  * Escenarios temáticos organizados en capas independientes (`Fondo`, `Base layer`, `UI`) para mantener fijo el HUD durante el desplazamiento de cámara.
  * Avatar jugable con máquina de estados de animación (`Idle`, `Run`, `Jump`, `Fall`) y volteo horizontal dinámico.
* **Interacción y Mecánicas de Juego (3 Tipos de NPCs):**
  * **NPC 1 — Golem Sombrío (Terrestre):** Patrullaje autónomo delimitado por topes invisibles. Inflige daño por contacto lateral y es eliminado al caer sobre él (generando rebote y `+50` puntos).
  * **NPC 2 — Espectro Alado (Aéreo):** Centinela volador con desplazamiento oscilatorio vertical continuo.
  * **NPC 3 — Sabio Eldar (Aliado Pacífico):** Detección por proximidad (`<= 130 px`), indicador visual flotante (`E`) y cuadro de diálogo narrativo en capa `UI` que desbloquea el portal de salida (`+100` puntos).
  * **Entorno y Supervivencia:** Plataformas sólidas, runas coleccionables (`+10` puntos), tótems de *checkpoint* mediante variables globales de coordenadas, detección de caída al vacío y gestión de vidas persistentes entre escenas.
* **Sonido y Ambientación:**
  * Música ambiental en bucle dedicada por nivel en canal independiente.
  * Temporizador dinámico (`TimerPasos` cada `0.35 s`) para sincronizar el sonido de pisadas únicamente al caminar sobre el suelo.
  * Efectos sonoros dedicados para salto, recolección de runas, activación de *checkpoints*, diálogos, derrota de enemigos y daño.
* **Estructura y Transiciones entre Niveles:**
  * Flujo completo de escenas: `Nivel1_Bosque`, `TransicionCinematica`, `Nivel2_Ruinas`, `GameOver` y `Victoria`.
  * Transición narrativa automatizada mediante video entre el Nivel 1 y el Nivel 2.

---

## 3. Estructura del Repositorio

```text
Hola-mundo-juego/
├── .gitignore
├── README.md
├── Hola mundo.json            # Archivo principal de configuración y lógica de GDevelop
└── assets/                    # Recursos multimedia (sprites, texturas, audio y cinemática)
```

---

## 4. Requisitos y Ejecución del Proyecto

### Requisitos Previos
* **GDevelop Desktop:** Versión `5.6.287` (Windows 10/11).

### Instrucciones de Ejecución
1. Clona este repositorio o descárgalo desde el botón verde **Code > Download ZIP**:
   ```bash
   git clone [https://github.com/Latirsde/Hola-mundo-juego.git](https://github.com/Latirsde/Hola-mundo-juego.git)
   ```
2. Abre **GDevelop**.
3. Selecciona **"Open a project"** y carga el archivo `Hola mundo.json`.
4. Selecciona la escena inicial (`MenuPrincipal` o `Nivel1_Bosque`) y presiona el botón **Preview** en la barra superior.

---

## 5. Mapeo de Controles

| Tecla / Acción | Función en Juego |
| :--- | :--- |
| `Flecha Izquierda` / `A` | Desplazamiento hacia la izquierda (con efecto espejo en el sprite). |
| `Flecha Derecha` / `D` | Desplazamiento hacia la derecha. |
| `Espacio` | Salto. |
| `E` | Interactuar con el Sabio Místico (en rango de proximidad). |

## 6. Adicional

Nyan Cat!
