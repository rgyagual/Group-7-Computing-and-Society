# EcoSense Bin: Gestión Inteligente de Residuos Urbanos

> **Materia:** Computación y Sociedad  
> **Grupo:** 7 | **Paralelo:** 2  
> **Integrantes:**  
> - Coronel Varas Oscar Jeanpiere  
> - Leon Rodriguez Arturo Daniel  
> - Palaguachi Jalca Jordan Raul  
> - Yagual Pincay Ronny Gabriel  

---

## 📌 Contexto y Problemática

En Ecuador, la gestión de residuos sólidos enfrenta un déficit crítico[cite: 26]:
* A nivel nacional se recolectan **14.193,5 toneladas diarias**, de las cuales el **77,1% se recoge sin ninguna separación en la fuente** y solo el 27,1% de los municipios cuenta con programas de reciclaje[cite: 26, 27].
* En el cantón **Guayaquil**, la generación per cápita alcanza **1,41 kg/hab/día** (la más alta del país), produciendo entre 2.600 y 4.700 toneladas diarias[cite: 26, 27].

Esta situación colapsa rápidamente los tachos públicos en zonas de alto flujo peatonal (centros comerciales, terminales terrestres y campus universitarios), propiciando el desbordamiento de contenedores, malos olores, sobrecarga al personal de limpieza y abandono de desperdicios en el suelo[cite: 26, 27, 28].

---

## 🎯 Alineación con los ODS y Objetivos

* **ODS Principal:** ODS 12 — *Producción y consumo responsables*[cite: 26].
* **Meta Específica:** Meta 12.5 — *De aquí a 2030, reducir considerablemente la generación de desechos mediante actividades de prevención, reducción, reciclado y reutilización*[cite: 26].

### Objetivo General
Proponer una solución tecnológica para la gestión de residuos sólidos dirigida a los usuarios de zonas de alta concurrencia en la ciudad de Guayaquil, mediante el diseño de un prototipo de contenedor inteligente que prevenga la acumulación de basura[cite: 30].

---

## 💡 Propuesta de Solución: EcoSense Bin

**EcoSense Bin** es una estación de reciclaje inteligente y automatizada para espacios públicos concurrentes que integra tres subsistemas mecatrónicos y de sensado IoT[cite: 30]:

1. **Clasificación Asistida Automatizada:**  
   Módulo de admisión con sensores inductivos/capacitivos y visión artificial ligera que identifica el residuo (plástico/latas vs. desechos generales) y lo redirige al compartimento correspondiente mediante compuertas motorizadas por servomotores[cite: 30].

2. **Monitoreo de Nivel de Capacidad en Tiempo Real:**  
   Sensores ultrasónicos e infrarrojos superiores que calculan el volumen ocupado y disparan alertas preventivas telemáticas (al 85% y 95% de capacidad) dirigidas al personal de aseo[cite: 30].

3. **Detección Perimetral y Alerta Disuasoria:**  
   Sensor de proximidad perimetral orientado al suelo (radio de 1 a 1,5 metros) conectado a un sintetizador de voz y LEDs que emite una advertencia cordial al detectar que un usuario abandona basura alrededor del tacho[cite: 30, 32].

---

## 🛠️ Arquitectura Tecnológica (IoT)

* **Sensado y Actuación:** Sensores ultrasónicos HC-SR04, sensores capacitivos/inductivos, servomotores de alto torque, actuadores lumínicos RGB y módulo de reproducción de audio[cite: 31].
* **Control y Procesamiento Local:** Microcontroladores IoT (ESP32 / Raspberry Pi Pico W) para el control en tiempo real[cite: 31].
* **Conectividad y Red:** Protocolos ligeros MQTT / HTTP REST sobre Wi-Fi o LoRaWAN conectados a tableros de monitoreo y alertas automáticas (Telegram Webhook / Web App)[cite: 31].

---

## 👥 Público Objetivo

* **Usuarios transeúntes y consumidores (18 a 55 años):** Estudiantes, trabajadores y visitantes de espacios comerciales y universitarios de Guayaquil[cite: 28, 31].
* **Personal operativo de aseo y mantenimiento:** Conserjes y cuadrillas de limpieza que requieren trazabilidad y alertas oportunas para optimizar sus rutas de recolección[cite: 29, 31].

---

## 🚫 Alcance del Sistema

* **Lo que hace:** Clasificación automática preliminar, monitoreo continuo de nivel y disuasión perimetral de basura arrojada al piso[cite: 32].
* **Lo que NO hace:** No compacta ni tritura desechos, no gestiona residuos químicos/hospitalarios ni realiza transporte autónomo de contenedores[cite: 32].
