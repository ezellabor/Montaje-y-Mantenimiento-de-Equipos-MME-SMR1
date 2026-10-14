### Montaje y Mantenimiento de Equipos 

# Configuración y verificación de memoria RAM Dual Channel
```Guía práctica con CPU-Z```  


## 1. Introducción Teórica: Configuración de la tecnología Dual Channel

Configurar la memoria RAM en **Dual Channel** (doble canal) permite al controlador de la placa base utilizar **dos buses de 64 bits funcionando de manera concurrente**, lo que duplica el ancho de banda efectivo y optimiza sustancialmente el rendimiento general del sistema.

Para realizar la configuración correctamente, se deben cumplir tres requisitos y reglas clave:

1. **Requisitos de los módulos:** Se recomienda emplear dos módulos de RAM del mismo kit o con las mismas especificaciones (misma capacidad, frecuencia, latencias y voltaje) para evitar problemas de estabilidad o bajadas automáticas de rendimiento.
2. **Instalación en las ranuras (Slots DIMM):** La mayoría de las placas base con 4 ranuras DIMM organizan sus canales en dos pares codificados por colores o serigrafiados como A1, A2, B1 y B2 (donde A representa el Canal 1 y B el Canal 2). Para instalar 2 módulos, la regla general para activar el Dual Channel es insertarlos en las ranuras **A2 y B2** (la segunda y cuarta ranura contando desde el socket del procesador).
3. **Ajuste en BIOS (XMP / EXPO):** Tras insertar los módulos en sus ranuras correspondientes, se debe acceder a la BIOS/UEFI al arrancar el equipo para activar el perfil de memoria **XMP** (en plataformas Intel) o **EXPO** (en plataformas AMD). Esto garantiza que la RAM funcione a la frecuencia y latencias publicitadas por el fabricante y no a la velocidad base por defecto.

---

## 2. Ejercicio Práctico: Verificación de Dual Channel con CPU-Z

**Objetivo de la práctica:** Diagnosticar y verificar desde el sistema operativo Windows si la memoria RAM está operando correctamente en modo Dual Channel y a su frecuencia efectiva nominal empleando la herramienta de software CPU-Z.

**Material necesario:** Equipo informático con Windows y el software CPU-Z instalado (utilidad gratuita de diagnóstico de hardware).

### Procedimiento Paso a Paso

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

## 3. Ficha de Registro y Diagnóstico del Alumno

Rellena la siguiente tabla con los datos obtenidos durante la inspección con CPU-Z:

| Parámetro a comprobar | Valor obtenido en CPU-Z | Evaluación / Diagnóstico |
| :--- | :--- | :--- |
| **Pestaña Memory → Channel #** | *(ej. Dual / Single)* | ¿El modo Dual Channel está activo? (Sí / No) |
| **Pestaña Memory → DRAM Frequency** | *(ej. 1600 MHz)* | Frecuencia de reloj física de bus |
| **Velocidad Efectiva Calculada** | *(DRAM Frequency × 2)* | ¿Coincide con la velocidad nominal? (ej. 3200 MT/s) |
| **Pestaña SPD → Slots ocupados** | *(ej. Slot #2 y Slot #4)* | ¿Los módulos están en la combinación A2 / B2? |
| **Perfil XMP / EXPO activo** | *(ej. XMP 2.0 / JEDEC)* | ¿El perfil de rendimiento está activado en BIOS? |
