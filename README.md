# Hola mundo

[![Engine: GDevelop 5.6.287](https://img.shields.io/badge/GDevelop-5.6.287-blue.svg)](https://gdevelop.io/)
[![Platform: Windows Desktop / Web](https://img.shields.io/badge/Platform-Windows%20%7C%20HTML5-lightgrey.svg)]()
[![Status: In Development](https://img.shields.io/badge/Status-In%20Progress-yellow.svg)]()

Prototipo de videojuego de plataformas en 2D desarrollado como proyecto de evaluación académica. El videojuego implementa mecánicas de interacción con el entorno, comportamientos de Inteligencia Artificial para 3 clases de NPCs, sonorización ambiental, arquitectura de datos desacoplada y transiciones cinemáticas entre niveles mediante el motor GDevelop.

---

## 1. Ficha del Proyecto y Concepto Lúdico

* **Género:** Plataformas 2D / Fantasía y Aventura.
* **Resolución Nativa:** 1280 × 720 px (16:9 HD).
* **Extensión de Mundo:** 10 pantallas horizontales continuas (~12.800 px en el eje X).
* **Público Objetivo:** Jugadores mayores de 10 años que buscan desafíos de precisión y progresión narrativa.
* **Sinopsis:** Eldrin, caballero protector de Aethelgard, debe atravesar el Bosque de las Sombras y descender a las Ruinas de Obsidiana para recolectar las Runas Primordiales y restablecer la paz en el reino.

---


## 2. Estructura del Repositorio

```text
hola-mundo-juego/
├── .gitignore
├── README.md
├── game.json                  # Archivo principal de configuración y lógica de GDevelop
└── assets/
    ├── audio/                 # BGM incidental y efectos SFX
    ├── images/                # Spritesheets y texturas de entorno
    └── video/                 # Cinemática de transición inter-nivel
```

---

## 3. Requisitos y Ejecución del Proyecto

### Requisitos Previos
* **GDevelop Desktop:** Versión `5.6.287` para Windows.

### Instrucciones de Ejecución
1. Clona este repositorio localmente:
   ```bash
   git clone [https://github.com/](https://github.com/)<tu-usuario>/hola-mundo-juego.git
   ```
2. Abre **GDevelop**.
3. Selecciona **"Open a project"** y carga el archivo `Hola mundo.json`.
4. Abre la escena `Nivel1_Bosque` y presiona el botón **Preview**.

---

## 4. Mapeo de Controles

| Tecla / Acción | Función en Juego |
| :--- | :--- |
| `Flecha Izquierda` / `A` | Desplazamiento hacia la izquierda (con volteo de sprite horizontal). |
| `Flecha Derecha` / `D` | Desplazamiento hacia la derecha. |
| `Flecha Arriba` / `Espacio` | Salto. |
| `E` | Interactuar con el Sabio Místico. |

---

## 5. A solucionar

1. Personaje de mueve de forma errática al estar en el suelo.