![Electrónica Gambino](https://electronicagambino.com/wp-content/uploads/elementor/thumbs/cropped-Electronica-Gambino-e1684335474114-q6losum0uq8caxhait9doqxx83gv53yq2d8g8oiv7o.png)

# ELECTRÓNICA GAMBINO

### Ingeniería Electrónica • Sistemas Embebidos • IoT • Diseño de Hardware • PCB

# SMART DENTAL UNIT PLATFORM

## Repositorio Oficial de Desarrollo

![Diseñado](https://img.shields.io/badge/Diseñado%20en-Argentina-skyblue?style=for-the-badge)
![Ubicación](https://img.shields.io/badge/Tucumán-Argentina-blue?style=for-the-badge)
![CEO](https://img.shields.io/badge/CEO-Fernando%20Gambino-black?style=for-the-badge)
![Estado](https://img.shields.io/badge/Estado-En%20Desarrollo-orange?style=for-the-badge)
![Fase](https://img.shields.io/badge/Fase-0%20Ingeniería-yellow?style=for-the-badge)
![Hardware](https://img.shields.io/badge/ESP32-Control%20Multimodal-green?style=for-the-badge)

---

# Proyecto

## Diseño e Implementación de una Plataforma Electrónica Basada en ESP32 para el Control Multimodal de una Unidad Odontológica mediante Tecnologías IoT, Sistemas Embebidos y Reconocimiento de Voz Offline

Este repositorio constituye la fuente oficial de ingeniería del proyecto desarrollado por **Electrónica Gambino**, orientado al diseño de una plataforma electrónica capaz de centralizar el control de una unidad odontológica moderna mediante una única tarjeta basada en ESP32.

El proyecto integra:

- Control de actuadores lineales del sillón y respaldo.
- Control de electroválvulas.
- Control de lámpara odontológica.
- Control de negatoscopio.
- Control de fotocurado.
- Control del sistema de ultrasonido.
- Pedal multifunción.
- Reconocimiento de voz offline.
- Arquitectura preparada para IoT.

---

# Arquitectura General

```mermaid
flowchart TD
AC[Transformador 200W] --> PS[Fuente 24V / 5V / 3.3V]
PS --> ESP[ESP32]
ESP --> H1[Driver H-Bridge]
H1 --> M1[Motor Sillón]
H1 --> M2[Motor Respaldo]
ESP --> MOS[MOSFET Drivers]
MOS --> EV[Electroválvulas]
MOS --> NEG[Negatoscopio]
MOS --> FOTO[Fotocurado]
ESP --> TRIAC[Optotriac]
TRIAC --> LAMP[Lámpara]
TRIAC --> US[Ultrasonido]
VOICE[Módulo Voz Offline] -->|UART| ESP
PEDAL[Pedal] --> ESP
WIFI[WiFi/Bluetooth] --> ESP
