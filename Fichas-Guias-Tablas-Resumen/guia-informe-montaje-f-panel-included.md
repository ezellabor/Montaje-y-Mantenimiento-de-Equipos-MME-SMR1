![Módulo](https://img.shields.io/badge/Módulo-Montaje_y_Mantenimiento_de_Equipos-brown?style=for-the-badge)
![Grupo](https://img.shields.io/badge/Grupo-SMR1-blue?style=for-the-badge)
![Profesor](https://img.shields.io/badge/Profesor-Ezequiel_Llarena_Borges-blue?style=for-the-badge)  

# Guía de montaje e informe técnico

## 1. Instalación de CPU y pasta térmica
* **Procedimiento** Levanta la palanca de retención del zócalo. Localiza el triángulo dorado en una esquina del procesador y hazlo coincidir con la marca del zócalo de la placa base.
    
    ![CPU installation](../img/palanca-cpu.png)
  
* **Principio ZIF:** La CPU debe encajar sin ejercer ninguna presión (Zero Insertion Force). Si no entra suavemente, la orientación es incorrecta.
* **Pasta térmica:** Aplica una gota del tamaño de un grano de arroz exactamente en el centro del procesador.  
    ```NOTA: La pasta sirve para eliminar el aire entre el procesador y el disipador. Un exceso de pasta actuará como aislante térmico y provocará  sobrecalentamiento.```  

---

## 2. Conexión del panel frontal (F-Panel)
Consulta el diagrama de pines (JFP1) en el manual de tu placa base para realizar las conexiones correctamente.

![Frontpaneldiagram](../img/panel.png)
    
* **Power SW y Reset SW:** Son interruptores de contacto; no tienen polaridad, por lo que la orientación de los dos cables no afecta al funcionamiento.
* **HDD LED y Power LED:** **Tienen polaridad**. El cable de color (rojo, verde o azul) es el **Positivo (+)** y el cable blanco o negro es el **Negativo (-)**. Si se invierten, el LED no encenderá.
    
    ![Front panel diagram](../img/conectores-f-panel-color.jpeg)  

* **USB y Audio:** Poseen una muesca de seguridad (pin bloqueado). Si el conector no entra, comprueba que no haya pines doblados en la placa.

---

## 3. Configuración inicial de la BIOS (UEFI)
Al arrancar el equipo por primera vez, pulsa `Supr` o `F2` para acceder a la configuración:

1.  **System Time / Date:** Configurar fecha y hora actuales (Control de fecha).
2.  **SATA Mode:** Verificar que esté en **AHCI** para optimizar el SSD.
3.  **Boot Priority:** Establecer la unidad USB como la primera opción de arranque.
4.  **XMP / DOCP:** Activar el perfil para que la RAM trabaje a su frecuencia nominal.
5.  **H/W Monitor:** Monitorizar que la temperatura de la CPU sea estable (30°C - 50°C).
   <!-- ![BIOS Monitor](https://www.msi.com/blog/storage/images/monitor.png)-->

---

## 4. Informe de montaje y control de calidad

**Técnico:** ________________________________________  
**Fecha de montaje:** `20 / 02 / 2026`  
**Equipo ID:** ________

| Paso | Tarea eralizada | Estado (OK) | Observaciones e incidencias |
| :--- | :--- | :---: | :--- |
| 1 | CPU y disipador instalados correctamente | [  ] | |
| 2 | RAM instalada en slots correctos (Dual Channel) | [  ] | |
| 3 | I/O Shield colocado en la caja | [  ] | |
| 4 | Placa base fijada al chasis (con separadores) | [  ] | |
| 5 | Fuente de alimentación instalada y apagada | [  ] | |
| 6 | Almacenamiento (SSD/HDD) instalado y conectado | [  ] | |
| 7 | Cables alimentación (24p ATX y CPU) conectados | [  ] | |
| 8 | Cables panel frontal (Power, LEDs, USB) conectados | [  ] | |
| 9 | Tarjeta gráfica y alimentación PCIe instaladas | [  ] | |
| 10 | Gestión de cables finalizada con bridas | [  ] | |
| **TEST** | **El equipo enciende y muestra BIOS correctamente** | **[  ]** | **Temp. CPU: _______** |

### Observaciones finales
*Indicar anomalías detectadas, dificultades en el montaje o sugerencias de mejora.*
____________________________________________________________________________________________________
____________________________________________________________________________________________________

---
