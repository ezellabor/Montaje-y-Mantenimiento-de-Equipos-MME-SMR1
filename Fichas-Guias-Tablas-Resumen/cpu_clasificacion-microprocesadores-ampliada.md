# Microprocesadores  

### Clasificación según:  
- Tipo (arquitectura y propósito)
- Número de transistores
- Frecuencia del reloj
- Temperatura y disipación térmica
- Fabricante
- Tecnología (nanómetros)
- TDP
- Compatibilidad con Chipset
- Compatibilidad con socket (PCB)  

  ---

## 1️⃣ Arquitectura y propósito

| Tipo                                       | Descripción                                                                       | Usos habituales                                 |
| ------------------------------------------ | --------------------------------------------------------------------------------- | ----------------------------------------------- |
| **CISC (x86 / x64)**                       | Conjunto de instrucciones complejo, gran compatibilidad con software tradicional. | PC, portátiles, estaciones, servidores.         |
| **RISC (ARM)**                             | Instrucciones simples y alta eficiencia energética.                               | Móviles, tablets, IoT, servidores ARM modernos. |
| **SoC (System on Chip)**                   | CPU + GPU + controladores + comunicaciones en un mismo chip.                      | Smartphones, consolas, sistemas embebidos.      |
| **APU**                                    | CPU con GPU integrada en la misma pastilla de silicio.                            | Equipos domésticos/media y portátiles.          |
| **Microcontroladores (MCU)**               | Procesador con memoria y periféricos integrados para control dedicado.            | Electrónica, automatización e IoT.              |
| **Procesadores de alto rendimiento (HPC)** | Multinúcleo de muy alta potencia para cálculo intensivo.                          | Servidores y supercomputación.                  |


---

## 2️⃣ Cantidad de transistores

| Época | Nº de transistores               | Ejemplo                  |
| ----- | -------------------------------- | ------------------------ |
| 1970s | Miles                            | Intel 4004               |
| 1980s | Cientos de miles                 | 8086, Motorola 68000     |
| 1990s | Millones                         | Pentium, AMD K6          |
| 2000s | Decenas–centenas de millones     | Core Duo, Athlon 64      |
| 2010s | Miles de millones                | Intel i7, Ryzen          |
| 2020s | **Decenas de miles de millones** | AMD Ryzen 7000, Apple M3 |

- Miles → millones → miles de millones → decenas de miles de millones
- A mayor densidad: mayor capacidad de cálculo y eficiencia.

---

## 3️⃣ Frecuencia de reloj

- Indica los ciclos por segundo que ejecuta la CPU.
- Se mide en MHz o GHz.
- Frecuencias bajas (1.0 – 2.5 GHz) → dispositivos móviles y eficiencia energética.
- Frecuencias medias (2.5 – 4.0 GHz) → equipos de uso general.
- Frecuencias altas (4.0 – 6.5 GHz e incluso +) → gaming y alto rendimiento.
  
⚠ Dos procesadores con igual frecuencia pueden rendir de forma diferente según la arquitectura interna e **IPC** (Instructions Per Cycle).

- MHz / GHz
- Baja: 1.0–2.5 GHz
- Media: 2.5–4.0 GHz
- Alta: 4.0–6.5 GHz

⚠ La frecuencia por sí sola no define el rendimiento.

---

## 4️⃣ Temperatura operativa / disipación térmica

| Categoría  | Temperatura permitida | Características                         |
| ---------- | --------------------- | --------------------------------------- |
| Baja       | 30–60 °C              | Dispositivos móviles / embebidos        |
| Moderada   | 60–85 °C              | PC de oficina / portátiles              |
| Alta       | 85–100+ °C            | Gaming, estaciones, servidores          |
| Industrial | -40 – 125 °C          | Sistemas embebidos en entornos extremos |

---

## 5️⃣ Consumo de energía (TDP)  

| Rango TDP              | Aplicación típica          |
| ---------------------- | -------------------------- |
| Bajo: l5 – 25 W        | Móviles / ultrabooks / ARM |
| Medio: 35 – 65 W       | Sobremesa general          |
| Alto:  95 – 150+ W     | Gaming / estaciones        |
| Muy alto: 200 – 400+ W | Servidores / HPC           |  


---


## 6️⃣ Fabricante

| Fabricante             | Mercado principal                    | Arquitectura      |
| ---------------------- | ------------------------------------ | ----------------- |
| **Intel**              | PC, portátiles, servidores           | x86 / x64         |
| **AMD**                | PC, gaming, servidores               | x86 / x64         |
| **ARM Ltd.**           | Licencia de arquitectura móvil y SoC | ARM               |
| **Apple**              | Mac y dispositivos móviles           | ARM (serie M / A) |
| **Qualcomm**           | Smartphones                          | ARM (Snapdragon)  |
| **IBM**                | Servidores críticos                  | POWER             |
| **RISC-V fabricantes** | Variado                              | RISC-V            |


---


## 7️⃣ Tecnología de fabricación (nodos en nm)

| Año aproximado | Nodos comunes                        |
| -------------- | ------------------------------------ |
| 2000–2010      | 90 nm → 65 nm → 45 nm                |
| 2010–2020      | 32 nm → 22 nm → 14 nm → 10 nm → 7 nm |
| 2020–2025      | **5 nm → 4 nm → 3 nm → 2 nm**        |

>- Nodos más pequeños:  + transistores – energía – temperatura

---

## 8️⃣ Compatibilidad con Chipset

| Marca | Generación CPU | Chipsets compatibles       |
| ----- | -------------- | -------------------------- |
| AMD   | Ryzen AM4      | A320 / B450 / X470 / X570… |
| AMD   | Ryzen AM5      | A620 / B650 / X670…        |
| Intel | 12ª–14ª Gen    | B660 / Z690 / B760 / Z790  |  

---

## 9️⃣ Compatibilidad con placabase (socket)

| Fabricante           | Socket reciente     | Ejemplo de CPU           |
| -------------------- | ------------------- | ------------------------ |
| Intel                | **LGA1700**         | Core 12ª–14ª Gen         |
| AMD                  | **AM5**             | Ryzen 7000               |
| AMD                  | **AM4**             | Ryzen 1000–5000          |
| Workstation/Servidor | SP5, sTR5, LGA4677… | EPYC, Threadripper, Xeon |

---

> **Compatibilidad** implica:  
>- Mismo socket físico
>- Chipset soporte
>- Versión BIOS/UEFI válida
>- Perfil de energía adecuado  

⚠ Una CPU puede no funcionar con un chipset aun si el socket coincide — depende de soporte del fabricante y BIOS/UEFI.  

#  

## Resumen

- Tipo → Transistores → Frecuencia    
- Temperatura → Energía (TDP) → Fabricante 
- Tecnología (nm) → Chipset → Socket  

>Para elegir un procesador se deben considerar **todos** estos criterios en conjunto.
