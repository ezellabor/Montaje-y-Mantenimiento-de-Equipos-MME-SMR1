## Clasificación de Microprocesadores

| **Criterio de clasificación**                     | **Descripción / Qué distingue**                                   | **Ejemplos / Consideraciones**                                                                                    |
| ------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Según el tipo**                                 | Tipo de arquitectura y propósito del procesador.                  | *CISC* (x86), *RISC* (ARM), *SoC*, *APU*, *CPU*, *Microcontroladores*.                                            |
| (1) Cantidad de **transistores**                | Influye en capacidad de cálculo, eficiencia y miniaturización.    | Evolución histórica: miles → millones → **miles de millones (billions)**.                                         |
| (2) **Frecuencia** de reloj                     | Número de ciclos por segundo para procesar instrucciones.         | Se mide en **GHz**. Un mayor valor no siempre implica mejor rendimiento si la arquitectura es diferente.          |
| (3) **Temperatura** operativa                   | Rango térmico que puede soportar sin perder rendimiento o fallar. | Procesadores móviles y embebidos → bajas temperaturas; estaciones y gaming → requieren sistemas de refrigeración. |
| 4. Consumo de **energía (TDP)**                | Cantidad de energía/ calor que disipa a máxima carga.             | Bajo TDP (5–25 W) móviles; Medio (45–65 W) equipos estándar; Alto (95–150 W) gama entusiasta/servidores.          |
| 5. **Fabricante**                    | Marca y ecosistema tecnológico asociado.                          | **Intel, AMD, ARM, Apple (M-Series), Qualcomm, IBM Power, RISC-V**.                                               |
| 6. Tecnología de fabricación **(nanómetros)**  | Tamaño del transistor → eficiencia y rendimiento.                 | 90 nm → 65 nm → 14 nm → 7 nm → **5 nm / 3 nm / 2 nm (nodos actuales)**.                                           |
| 7. Compatibilidad con **chipset**              | Debe estar diseñado para trabajar con un determinado chipset.     | Ej.: AMD **Ryzen → chipsets AM4 / AM5** — Intel **Core → B760 / Z790, etc.**                                      |
| 8. Compatibilidad con **motherboard (socket)** | Determinado por el tipo de **zócalo físico** y **BIOS/UEFI**.     | Ej.: Intel **LGA1700**, AMD **AM5**, servidores **SP5**, etc.                                                     |

---

## Conceptos clave  

- Un mismo número de GHz no implica el mismo rendimiento — depende de la arquitectura y tecnología.  
- Los nanómetros no son tamaño físico exacto del transistor, sino el “nodo” del proceso litográfico.  
- TDP no es consumo real, sino energía térmica que debe ser disipada.
- Siempre debe haber coincidencia entre CPU ↔ chipset ↔ socket ↔ BIOS/UEFI para ser compatible.

---

Fabricante → Tecnología de fabricación (nm) → Tipo / Arquitectura  
                 ↓  
   Transistores → Frecuencia → Energía/TDP → Temperatura  
                 ↓  
Compatibilidad con chipset → Compatibilidad con motherboard/socket  

