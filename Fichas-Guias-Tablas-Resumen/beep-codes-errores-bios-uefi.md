![Módulo](https://img.shields.io/badge/Módulo-Montaje-y-Mantenimiento-de-Equipos-orange?style=for-the-badge)
![Grupo](https://img.shields.io/badge/Grupo-SMR1-blue?style=for-the-badge)
![Profesor](https://img.shields.io/badge/Profesor-Ezequiel_Llarena_Borges-blue?style=for-the-badge)
<div align="center">   
 
# Señales Acústicas (Beep Codes) de Errores BIOS/UEFI

> **Descripción:** Tabla de referencia completa de los códigos de sonido (beeps) emitidos durante el POST (Power-On Self-Test) para diagnóstico de errores de hardware.  
> **Aplicación:** Diagnóstico de fallos cuando no hay salida de video.  

---

## Índice

1. [BIOS AMI (American Megatrends)](#bios-ami-american-megatrends)
2. [BIOS Award/Phoenix](#bios-awardphoenix)
3. [BIOS Phoenix](#bios-phoenix)
4. [BIOS IBM](#bios-ibm)
5. [BIOS Dell](#bios-dell)
6. [BIOS HP/Compaq](#bios-hpcompaq)
7. [BIOS Lenovo](#bios-lenovo)
8. [Códigos Especiales](#códigos-especiales)

---

## BIOS AMI (American Megatrends)

| Beeps | Descripción | Componente Afectado | Solución Recomendada |
|-------|-------------|---------------------|----------------------|
| **1 beep corto** | Refresh Timer Error | DRAM/Placa base | Verificar/Reemplazar RAM |
| **2 beeps cortos** | Parity Error | RAM | Error de paridad en memoria. Reemplazar RAM |
| **3 beeps cortos** | Base 64K RAM Failure | RAM | Fallo en primeros 64KB de RAM. Reemplazar RAM |
| **4 beeps cortos** | System Timer Failure | Placa base | Fallo en temporizador del sistema. Reemplazar placa |
| **5 beeps cortos** | Processor Failure | CPU | Fallo de procesador. Verificar/Reemplazar CPU |
| **6 beeps cortos** | Keyboard Controller Gate A20 Error | Teclado/Placa base | Controlador de teclado. Verificar teclado/placa |
| **7 beeps cortos** | Virtual Mode Exception Error | CPU/Placa base | Error en modo virtual CPU. Reemplazar CPU/placa |
| **8 beeps cortos** | Display Memory Read/Write Error | Tarjeta gráfica | Fallo en memoria de video. Reemplazar GPU |
| **9 beeps cortos** | BIOS ROM Checksum Error | BIOS | BIOS corrupta. Reflashear/Reemplazar chip BIOS |
| **10 beeps cortos** | CMOS Shutdown Register Read/Write Error | CMOS/Placa base | Error en registro CMOS. Reemplazar placa base |
| **11 beeps cortos** | Cache Memory Bad | Caché CPU | Error en caché L1/L2. Reemplazar CPU |
| **1 beep largo + 2 cortos** | Video Error | Tarjeta gráfica | Fallo en inicialización de video. Verificar GPU |
| **1 beep largo + 3 cortos** | Video Error | Tarjeta gráfica | Error en detección de video. Verificar GPU/RAM |
| **1 beep largo + 8 cortos** | Display Test Error | Tarjeta gráfica | Fallo en test de pantalla. Reemplazar GPU |
| **Beeps continuos** | Memory/Video Problem | RAM/GPU | Problema crítico de memoria o video. Verificar ambos |

---

## BIOS Award/Phoenix

| Beeps | Descripción | Componente Afectado | Solución Recomendada |
|-------|-------------|---------------------|----------------------|
| **1 beep largo + 2 cortos** | Video Card Not Found/Video RAM Error | Tarjeta gráfica | GPU no detectada o error en VRAM. Verificar GPU |
| **1 beep largo + 3 cortos** | Video Card Not Found/Video RAM Error | Tarjeta gráfica | Similar al anterior. Reemplazar/Reasentar GPU |
| **Beeps continuos largos** | Memory Problem | RAM | Problema de memoria. Verificar/Reemplazar RAM |
| **Beeps continuos cortos** | Power/Thermal Problem | PSU/Temperatura | Problema de energía o sobrecalentamiento. Verificar PSU/ventilación |
| **Sin beeps** | No Power/Dead System | PSU/Placa base | Sistema no arranca. Verificar fuente de alimentación |

---

## BIOS Phoenix

| Beeps (Patrón) | Descripción | Componente Afectado | Solución Recomendada |
|----------------|-------------|---------------------|----------------------|
| **1-1-1-3** | CPU/Motherboard Error | CPU/Placa base | Error de CPU o placa. Verificar CPU |
| **1-1-2-1** | CPU/Motherboard Error | CPU/Placa base | Similar al anterior. Reemplazar CPU/placa |
| **1-1-2-3** | Motherboard Error | Placa base | Error de placa base. Reemplazar placa |
| **1-1-3-1** | Memory Refresh Error | RAM | Error en refresco de memoria. Reemplazar RAM |
| **1-1-3-2** | Parity Error | RAM | Error de paridad. Verificar/Reemplazar RAM |
| **1-1-3-3** | Base 64K RAM Failure | RAM | Fallo en RAM base. Reemplazar RAM |
| **1-1-4-1** | Address Line Failure | RAM/Placa base | Fallo en líneas de dirección. Verificar RAM/placa |
| **1-1-4-2** | Parity Error | RAM | Error de paridad en RAM. Reemplazar RAM |
| **1-1-4-3** | Timer Tick Interrupt Error | Placa base | Error en interrupción de timer. Reemplazar placa |
| **1-2-1-1** | PIC Error | Placa base | Error en controlador de interrupciones. Reemplazar placa |
| **1-2-1-2** | PIC Error | Placa base | Similar al anterior. Reemplazar placa |
| **1-2-1-3** | PIC Error | Placa base | Similar al anterior. Reemplazar placa |
| **1-2-2-1** | DMA Error | Placa base | Error en controlador DMA. Reemplazar placa |
| **1-2-2-2** | DMA Error | Placa base | Similar al anterior. Reemplazar placa |
| **1-2-2-3** | DMA Error | Placa base | Similar al anterior. Reemplazar placa |

---  

# 🔊 Tabla Genérica de Beep Codes BIOS/UEFI

> **Descripción:** Referencia rápida de códigos de sonido (beeps) del POST para diagnóstico de hardware. Válida para las BIOS/UEFI más comunes: AMI, Award, Phoenix, Dell, HP.  
> **Uso:** Diagnóstico cuando no hay salida de vídeo.  
> **Nota:** Los patrones pueden variar ligeramente según fabricante y versión.

---

## Tabla Genérica de Beep Codes

| Patrón de Beeps | Significado Genérico | Componente Probable | Acción Recomendada |
|-----------------|---------------------|---------------------|-------------------|
| **1 beep corto** | ✅ POST correcto | Ninguno (sistema OK) | Normal. El sistema arrancó correctamente. |
| **2 beeps cortos** | ⚠️ Error de configuración/CMOS | CMOS/BIOS Settings | Resetear CMOS (quitar pila o usar jumper). |
| **3 beeps cortos** | ❌ Error crítico de RAM | Memoria RAM | Reasentar/limpiar contactos RAM. Probar con otro módulo. |
| **4 beeps cortos** | ❌ Error de temporizador/placa | Placa base | Fallo en chipset o timer. Posible reemplazo de placa. |
| **5 beeps cortos** | ❌ Error de CPU | Procesador | Verificar CPU: ¿bien asentada? ¿thermal paste? ¿sobrecalentamiento? |
| **6 beeps cortos** | ❌ Error teclado/controlador | Teclado/Placa base | Desconectar teclado y probar. Verificar puerto PS/2/USB. |
| **7 beeps cortos** | ❌ Error de CPU o placa | CPU/Placa base | Fallo en modo protegido/virtual. Revisar CPU y placa. |
| **8 beeps cortos** | ❌ Error de vídeo/VRAM | Tarjeta gráfica | Reasentar GPU. Probar con gráfica integrada si hay. |
| **9 beeps cortos** | ❌ Error de checksum BIOS | BIOS/Chip SPI | BIOS corrupta. Intentar reflashear o reemplazar chip. |
| **10 beeps cortos** | ❌ Error CMOS/RTC | Placa base (CMOS) | Fallo en registro CMOS. Reemplazar placa o chip RTC. |
| **11 beeps cortos** | ❌ Error de caché CPU | Caché L1/L2 | CPU defectuosa. Reemplazar procesador. |
| **1 beep largo + 2 cortos** | ❌ Error de vídeo (común) | Tarjeta gráfica | **Muy frecuente en AMI/Award**. Verificar GPU, cables, monitor. |
| **1 beep largo + 3 cortos** | ❌ Error de vídeo/VRAM | Tarjeta gráfica | Similar al anterior. Probar otra GPU o ranura PCIe. |
| **1 beep largo + 8 cortos** | ❌ Error de test de vídeo | Tarjeta gráfica/Pantalla | Fallo en inicialización de pantalla. Verificar conexión. |
| **Beeps continuos (largos)** | ❌ Error de RAM o energía | RAM / Fuente de alimentación | Reasentar RAM. Verificar PSU y conexiones de energía. |
| **Beeps continuos (cortos)** | ❌ Problema de energía/sobrecalentamiento | PSU / Ventilación | Verificar fuente, temperaturas, ventiladores. |
| **Sin beeps + sin vídeo** | ❌ Sin energía o placa muerta | PSU / Placa base / CPU | Verificar PSU con tester. Probar placa con mínimo hardware. |
| **Beeps intermitentes irregulares** | ⚠️ Error no catalogado | Varios | Consultar manual específico de la placa/base. |

---

## IMPORTANTE

### ✅ 1 Beep Corto = Éxito
- En **casi todas las BIOS**, un solo beep corto indica que el POST se completó correctamente.
- Si hay vídeo y sistema operativo, ignora cualquier otro beep posterior.

### ⚠️ Variaciones por Fabricante
| Fabricante | Nota Específica |
|------------|----------------|
| **AMI** | Usa patrones de 1-11 beeps cortos + combinaciones largas/cortas. Muy detallada. |
| **Award** | Similar a AMI, pero con menos códigos. 1 largo + 2/3 cortos = vídeo. |
| **Phoenix** | Usa patrones de grupos (ej: 1-2-3 = beep, pausa, 2 beeps, pausa, 3 beeps). Anotar secuencia exacta. |
| **Dell/HP/Lenovo** | A veces usan patrones propios o combinan beeps con luces LED. Consultar manual del equipo. |

### Pasos de diagnóstico rápido
1. **Escucha y cuenta** los beeps con atención.
2. **Anota el patrón**: ¿cortos/largos? ¿cuántos? ¿hay pausas?
3. **Consulta esta tabla** para identificar el componente probable.
4. **Prueba lo más simple primero**: reasentar RAM, GPU, cables.
5. **Minimal Boot**: desconecta todo menos CPU, 1 RAM, GPU (si no hay integrada).
6. **Reset CMOS**: quita la pila 5 minutos o usa el jumper CLR_CMOS.
7. **Si persiste**, consulta el manual exacto de tu placa base o equipo.

---

## Patrones Phoenix (Formato especial)

Phoenix BIOS usa secuencias agrupadas. Ejemplo: `1-2-3` = 1 beep, pausa, 2 beeps, pausa, 3 beeps.

| Patrón Phoenix | Significado más probable |
|----------------|--------------------------|
| **1-1-1-x** | Error de CPU o placa base |
| **1-1-2-x** | Error de CPU o placa base |
| **1-1-3-x** | Error de RAM / paridad |
| **1-2-x-x** | Error de placa base (DMA/PIC) |
| **1-3-x-x** | Error de RAM (refresco/test) |
| **2-x-x-x** | Error de RAM (test extendido) |
| **3-x-x-x** | Error de RAM (más crítico) |
| **4-x-x-x** | Error de RAM o placa base |

> **Consejo:** Para Phoenix, anota la secuencia completa y busca en el manual específico. Muchos códigos Phoenix apuntan a RAM.

---

## Equipos de Marca (Dell, HP, Lenovo)

Estos fabricantes a veces personalizan los beep codes. Patrones comunes:

| Equipo | Patrón Común | Significado Típico |
|--------|-------------|-------------------|
| **Dell** | 1-2 (corto-largo) | Error de RAM |
| **Dell** | 1-3-1-1 | Error de RAM |
| **Dell** | 2-1 | Error de placa base |
| **HP** | 1 largo + 2 cortos | Error de vídeo |
| **HP** | Beeps continuos | Error de RAM |
| **Lenovo** | 1 beep + pausa + 2 beeps | Error de vídeo |
| **Lenovo** | 3 beeps + pausa + 3 beeps | Error de RAM |

> **Recomendación:** Para equipos de marca, busca en Google: `"beep codes" + [modelo exacto del equipo]`.

---

## Cuando no hay beeps (silencio total)

Si al encender **no hay ningún beep ni ventiladores girando**:

1. ✅ Verifica que el cable de alimentación esté conectado y la PSU encendida (interruptor trasero).
2. ✅ Prueba con otro cable de alimentación o toma de corriente.
3. ✅ Verifica el botón de encendido del chasis (puede estar roto).
4. ✅ Prueba a encender la placa haciendo puente en los pines `PWR_SW` con un destornillador.
5. ✅ Si sigue sin respuesta, prueba con otra fuente de alimentación conocida como buena.
6. ✅ Si la PSU funciona pero no hay beeps, la placa base o CPU podrían estar dañadas.

---

## MUY IMPORTANTE !!

- Los beep codes pueden variar. Consulta siempre el manual oficial de tu placa si es crítico.

---

> **Licencia:** Uso libre para fines educativos y técnicos.  
> **Última revisión:** 2024  
> **Fuentes:** Manuales AMI, Award, Phoenix, Dell, HP, Lenovo + experiencia técnica en soporte hardware.
