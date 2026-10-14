# Configuración y verificación de memoria RAM Dual Channel
```Guía práctica con CPU-Z```  


## 1. Introducción: configuración de la tecnología Dual Channel

Configurar la memoria RAM en **Dual Channel** (doble canal) permite al controlador de la placa base utilizar **dos buses de 64 bits funcionando de manera concurrente**, lo que duplica el ancho de banda efectivo y optimiza sustancialmente el rendimiento general del sistema.

Para realizar la configuración correctamente, se deben cumplir tres requisitos y reglas clave:

1. **Requisitos de los módulos:** Se recomienda emplear dos módulos de RAM del mismo kit o con las mismas especificaciones (misma capacidad, frecuencia, latencias y voltaje) para evitar problemas de estabilidad o bajadas automáticas de rendimiento.
2. **Instalación en las ranuras (Slots DIMM):** La mayoría de las placas base con 4 ranuras DIMM organizan sus canales en dos pares codificados por colores o serigrafiados como A1, A2, B1 y B2 (donde A representa el Canal 1 y B el Canal 2). Para instalar 2 módulos, la regla general para activar el Dual Channel es insertarlos en las ranuras **A2 y B2** (la segunda y cuarta ranura contando desde el socket del procesador).
3. **Ajuste en BIOS (XMP / EXPO):** Tras insertar los módulos en sus ranuras correspondientes, se debe acceder a la BIOS/UEFI al arrancar el equipo para activar el perfil de memoria **XMP** (en plataformas Intel) o **EXPO** (en plataformas AMD). Esto garantiza que la RAM funcione a la frecuencia y latencias publicitadas por el fabricante y no a la velocidad base por defecto.

---

## 2. Ejercicio práctico: Verificación de Dual Channel con CPU-Z

**Objetivo:** Diagnosticar y verificar desde el sistema operativo Windows si la memoria RAM está operando correctamente en modo Dual Channel y a su frecuencia efectiva nominal empleando la herramienta de software CPU-Z.

**Herramientas necesarias:** Equipo informático con Windows y el software CPU-Z instalado (utilidad gratuita de diagnóstico de hardware).

### Procedimiento paso a paso

#### Paso 1: Verificación del modo de canal
1. Inicia la aplicación **CPU-Z**.
2. Haz clic en la pestaña **Memory** (Memoria) en la barra superior.
3. Localiza la casilla **Channel #** (o *Channel*):
   - **Dual**: Confirma que la memoria está funcionando en **Dual Channel** activo.
   - *Nota para DDR5*: Puede mostrar la etiqueta **4 x 32-bit** o **2 x 32-bit** debido a los dos subcanales independientes por módulo de la arquitectura DDR5.
   - **Single**: Indica que la memoria opera en un único canal de 64 bits. En este caso, se debe apagar el equipo y corregir la posición de los módulos a las ranuras **A2 y B2**.

#### Paso 2: Comprobación de frecuencia física y velocidad efectiva
1. En la pestaña **Memory**, observa la cifra indicada en **DRAM Frequency**.
2. Aplica el principio de la tecnología **DDR** (*Double Data Rate*), que realiza dos transferencias por cada ciclo de reloj:
   $$\text{Velocidad Efectiva (MT/s)} = \text{DRAM Frequency (MHz)} \times 2$$
3. *Ejemplo práctico*: Si en **DRAM Frequency** se lee **1600 MHz**, la velocidad efectiva real es de **3200 MT/s** (DDR4-3200). Si muestra valores de ~1066 MHz a ~1200 MHz en DDR4, el perfil XMP/EXPO no está activado en BIOS.

#### Paso 3: Mapeo de ranuras e inspección del chip SPD
1. Accede a la pestaña **SPD** (*Serial Presence Detect*).
2. En el desplegable **Memory Slot Selection**, selecciona alternativamente cada ranura (*Slot #1*, *Slot #2*, *Slot #3*, *Slot #4*).
3. Identifica en qué posiciones físicas se encuentran detectados los módulos y comprueba que sus latencias, frecuencias y fabricantes sean coincidentes.

---

## 3. Ficha de registro y diagnóstico

Rellena la siguiente tabla con los datos obtenidos durante la inspección con CPU-Z:

| Parámetro a comprobar | Valor obtenido en CPU-Z | Evaluación / Diagnóstico |
| :--- | :--- | :--- |
| **Pestaña Memory → Channel #** | *(ej. Dual / Single)* | ¿El modo Dual Channel está activo? (Sí / No) |
| **Pestaña Memory → DRAM Frequency** | *(ej. 1600 MHz)* | Frecuencia de reloj física de bus |
| **Velocidad Efectiva Calculada** | *(DRAM Frequency × 2)* | ¿Coincide con la velocidad nominal? (ej. 3200 MT/s) |
| **Pestaña SPD → Slots ocupados** | *(ej. Slot #2 y Slot #4)* | ¿Los módulos están en la combinación A2 / B2? |
| **Perfil XMP / EXPO activo** | *(ej. XMP 2.0 / JEDEC)* | ¿El perfil de rendimiento está activado en BIOS? |    

## 4. Cuestionario de revisión de conceptos

### Bloque 1: Preguntas de opción múltiple 

### 1. ¿Cuál es el beneficio principal de activar la tecnología Dual Channel en una placa base?
* **A)** Duplica la frecuencia de reloj del procesador (CPU).
* **B)** Permite utilizar dos buses de datos de 64 bits de forma concurrente, duplicando el ancho de banda efectivo.
* **C)** Elimina la necesidad de realizar ciclos de refresco en los módulos de memoria DRAM.
* **D)** Aumenta la capacidad total instalada automáticamente al doble.

### 2. En una placa base de 4 ranuras DIMM (etiquetadas como A1, A2, B1 y B2), ¿en qué slots se deben instalar habitualmente 2 módulos para garantizar la activación del Dual Channel?
* **A)** En los slots A1 y A2.
* **B)** En los slots A1 y B1.
* **C)** En los slots A2 y B2 (segunda y cuarta ranura desde el procesador).
* **D)** Indiferentemente en cualquier par de ranuras contiguas.

### 3. Al inspeccionar la pestaña *Memory* de la herramienta CPU-Z en un sistema con DDR4 a 3200 MT/s en Dual Channel, ¿qué valor se observará en el apartado **DRAM Frequency**?
* **A)** 3200 MHz
* **B)** 6400 MHz
* **C)** ~1600 MHz
* **D)** ~800 MHz

### 4. ¿Qué función cumple el chip **SPD** (*Serial Presence Detect*) integrado en cada módulo de memoria RAM?
* **A)** Controlar el voltaje que entrega la fuente de alimentación a la ranura DIMM.
* **B)** Almacenar la información técnica de fábrica (frecuencias, latencias, voltajes y perfiles XMP/EXPO) para que la BIOS la lea durante el arranque.
* **C)** Ejecutar el proceso continuo de refresco de las celdas de almacenamiento DRAM.
* **D)** Conmutar automáticamente entre Single Channel y Dual Channel según la carga de trabajo.

### 5. Si la memoria RAM se encuentra funcionando a la velocidad base estándar de JEDEC en lugar de la velocidad nominal publicitada por el fabricante, ¿qué ajuste debe realizarse en la BIOS/UEFI?
* **A)** Cambiar el formato de partición del disco duro.
* **B)** Activar el perfil **XMP** (Intel) o **EXPO** (AMD).
* **C)** Desactivar la virtualización de la CPU.
* **D)** Cambiar la disposición física de los módulos a los slots A1 y B1.

### 6. ¿Por qué al instalar dos módulos de memoria **DDR5** en Dual Channel, la herramienta CPU-Z puede mostrar la casilla *Channel #* con el texto "4 x 32-bit"?
* **A)** Es un error de lectura de la aplicación CPU-Z.
* **B)** Porque la tecnología DDR5 utiliza cuatro módulos físicos obligatorios.
* **C)** Porque cada módulo físico DDR5 incorpora internamente dos subcanales independientes de 32 bits de ancho.
* **D)** Porque el sistema ha desactivado automáticamente dos canales por compatibilidad.

---

## Bloque 2: Casos prácticos y diagnóstico de averías

### Caso práctico 1
Un usuario ha comprado dos módulos de RAM DDR4 de 8 GB a 3600 MT/s. Los ha instalado en las ranuras **A1 y A2** de su placa base. Al encender el equipo y abrir CPU-Z, observa que el apartado *Channel #* indica **Single** y *DRAM Frequency* indica **1333 MHz** (~2666 MT/s efectivos).

* **Pregunta 1.1**: Explica por qué la casilla *Channel #* muestra "Single" y qué solución física se debe aplicar en la placa base.
* **Pregunta 1.2**: Explica por qué la velocidad efectiva es de 2666 MT/s en lugar de los 3600 MT/s comprados y qué configuración debe modificarse en la BIOS.

---

### Caso práctico 2
Durante una práctica en el taller de montaje, se leen los datos de la pestaña **SPD** en CPU-Z para los cuatro slots de memoria:
* **Slot #2 (A2)**: Módulo Corsair DDR4 8GB 3200 MT/s CL16 (1.35V)
* **Slot #4 (B2)**: Módulo Kingston DDR4 8GB 2666 MT/s CL19 (1.20V)

* **Pregunta 2.1**: ¿Funcionará el sistema en modo Dual Channel? ¿Qué ocurrirá con la frecuencia de trabajo y las latencias globales del equipo?

---

<!--
## Clave de respuestas

### Clave de Respuestas del Bloque 1
1. **B** — El Dual Channel utiliza dos buses de 64 bits en paralelo, duplicando el ancho de banda de la memoria.
2. **C** — La recomendación estándar en la mayoría de placas de 4 ranuras es utilizar los slots A2 y B2 (canal A y canal B alternados).
3. **C** — Debido a la tecnología DDR (*Double Data Rate*), la frecuencia física de bus en CPU-Z (*DRAM Frequency*) es exactamente la mitad de la velocidad efectiva en MT/s (3200 / 2 = 1600 MHz).
4. **B** — El chip SPD es una EEPROM no volátil que contiene la tabla de parámetros y perfiles grabados por el fabricante para la inicialización en BIOS.
5. **B** — La activación de XMP (Intel) o EXPO (AMD) en la BIOS aplica las frecuencias y voltajes con *overclocking* de fábrica probados por el fabricante.
6. **C** — La arquitectura DDR5 divide cada módulo DIMM físico de 64 bits en dos subcanales independientes de 32 bits (2 módulos × 2 subcanales = 4 x 32-bit).

### Respuestas del Bloque 2
* **Caso 1.1**: Muestra "Single" porque los módulos se instalaron en el mismo canal (A1 y A2 pertenecen ambos al Canal A). La solución es apagar el equipo y reinstalar los módulos en las ranuras alternadas **A2 y B2** para activar los canales A y B simultáneamente.
* **Caso 1.2**: La memoria está funcionando a la frecuencia JEDEC base de inicio por defecto (2666 MT/s). Para alcanzar los 3600 MT/s nominales, se debe acceder a la BIOS/UEFI y activar el perfil **XMP / EXPO**.
* **Caso 2.1**: El sistema sí activará el Dual Channel (Flex/Asimétrico si corresponde), pero ajustará automáticamente la velocidad y latencias de todo el conjunto al módulo más lento instalado (2666 MT/s CL19 a 1.20V) para garantizar la estabilidad, perdiendo el rendimiento superior del módulo Corsair de 3200 MT/s.
-->

---
MONTAJE Y MANTENIMIENTO DE EQUIPOS - Prof. Ezequiel Llarena Borges  
