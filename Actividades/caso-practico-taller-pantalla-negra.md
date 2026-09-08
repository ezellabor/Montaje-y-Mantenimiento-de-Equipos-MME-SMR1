# 🛠️ Caso Práctico de Taller: "El misterio de la pantalla en negro"
**Módulo:** Montaje y Mantenimiento de Equipos (SMR)  
**Actividad:** Juego de rol de texto (Troubleshooting de Hardware)

---

### 📋 Orden de Trabajo #1042
* **Equipo:** Torre clónica estándar (PC de escritorio).
* **Sintoma reportado:** "El ordenador enciende (los ventiladores giran y los LEDs de la torre se iluminan), pero no da ninguna señal de vídeo en la pantalla."
* **Tu rol:** Técnico/a informático de soporte de nivel 1.

---

## 🔹 Escena 1: Recepción y comprobación inicial

El ordenador está sobre tu mesa de trabajo. Conectas el cable de alimentación, el cable de vídeo (HDMI) a la pantalla del taller y enciendes el equipo. 

Los ventiladores empiezan a girar y la luz del botón de encendido se ilumina, pero el monitor se queda en negro y muestra el mensaje: **"Sin señal"**.

**¿Cuál es tu primer paso técnico?**

* [ ] **Opción A:** Abrir la caja inmediatamente, quitar la pila de la placa base (*Clear CMOS*) y cambiar los módulos de memoria RAM.
* [x] **Opción B:** Verificar conexiones externas: comprobar el cable HDMI, probar otro monitor del taller y revisar a qué puerto específico de la torre está conectado el cable.
* [ ] **Opción C:** Apagar el equipo, extraer la tarjeta gráfica dedicada y tirarla a la basura porque claramente está averiada.

---

## 🔹 Escena 2: Inspección física y diagnóstico de placa

> *(Si elegiste la Opción B)*  
> Te das cuenta de un detalle clave: el cable HDMI estaba conectado a la salida de la **placa base**, pero el equipo tiene una **tarjeta gráfica dedicada** instalada. Conectas el cable a la GPU... ¡pero sigue sin dar vídeo! Cambias el cable y el monitor, pero la pantalla continúa en negro. 

Es hora de inspeccionar el interior. Apagas la fuente de alimentación, desconectas la toma de corriente, te colocas la **pulsera antiestática** y retiras el panel lateral.

Al encender de nuevo el PC con la tapa abierta, observas que el ventilador de la GPU gira, pero el altavoz interno (*speaker*) emite un código de **1 pitido largo y 2 pitidos cortos** (o el LED de diagnóstico *EZ Debug* se queda fijo en la luz de **DRAM**).

**¿Cómo procedes a aislar la avería?**

* [x] **Opción A:** Desconectar los módulos de memoria RAM, limpiar sus contactos dorados con una goma de borrar suave o alcohol isopropílico, y probar a arrancar insertando solo un módulo en el zócalo (*slot*) principal.
* [ ] **Opción B:** Sustituir la fuente de alimentación por una de 1000W porque le falta potencia.
* [ ] **Opción C:** Formatear el disco duro utilizando otro equipo del taller.

---

## 🔹 Escena 3: Verificación y control de calidad

> *(Si elegiste la Opción A)*  
> Retiras los dos módulos de RAM. Limpias los contactos dorados, insertas un solo módulo en el slot recomendado por el manual (A2) y vuelves a encender.

Esta vez el *speaker* no pita, los LEDs de diagnóstico avanzan correctamente... **¡y aparece el logotipo de la BIOS en la pantalla!** Has recuperado la señal de vídeo. 

Sin embargo, antes de dar el trabajo por finalizado y avisar al cliente, debes certificar la reparación.

**¿Cómo concluyes la intervención en el taller?**

* [ ] **Opción A:** Cerrar la tapa, entregar el equipo inmediatamente y cobrar la sustitución de un módulo de RAM.
* [x] **Opción B:** Probar el segundo módulo de RAM por separado para comprobar si está defectuoso o si era un mal contacto. Posteriormente, ejecutar un test de memoria (*MemTest86*) y una prueba de estrés para verificar la estabilidad global del sistema.
* [ ] **Opción C:** Dejar el equipo encendido en la BIOS durante 5 minutos y dar el visto bueno.

---

## 📑 Solucionario y Rúbrica de Evaluación

| Criterio | Ruta Correcta | Explicación Técnica |
| :--- | :---: | :--- |
| **Fase 1: Capa Física / Periféricos** | **Opción B** | **Regra de oro:** *De lo más simple a lo más complejo*. Conectar el monitor a la gráfica integrada teniendo una dedicada es un error común del usuario. Siempre se comprueban cables y conexiones antes de abrir el chasis. |
| **Fase 2: Hardware Interno** | **Opción A** | Los códigos POST (pitidos o LEDs de diagnóstico) guiaron la avería hacia la **RAM**. Limpiar los contactos elimina sulfatación o suciedad, y probar un solo módulo permite aislar si el fallo está en un módulo o en un socket. |
| **Fase 3: Quality Assurance (QA)** | **Opción B** | Un técnico profesional no se limita a "ver imagen". Debe verificar si el componente retirado estaba dañado o solo mal asentado, y certificar mediante software de diagnóstico (*MemTest86*) que el PC no fallará bajo carga. |

### 📊 Puntuación final del alumno
* **3/3 Respuestas correctas:** 🏆 *Técnico Senior* – Diagnóstico impecable, metódico y eficiente.
* **2/3 Respuestas correctas:** 🛠️ *Técnico Junior* – Buen camino, pero falta pulir metodología o pruebas de estrés.
* **0-1/3 Respuestas correctas:** ⚠️ *Técnico en Prácticas* – Recuerda aplicar la metodología de descarte en orden de complejidad.