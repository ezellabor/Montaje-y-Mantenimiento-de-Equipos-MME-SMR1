# Diagnosis, Compatibilidad y Montaje de Memoria RAM

**Módulo Profesional:** Montaje y Mantenimiento de Equipos (MME)  
**Ciclo Formativo:** Formación Profesional de Grado Medio en Sistemas Microinformáticos y Redes (SMR1)  

---

## Introducción

En el entorno profesional del mantenimiento informático, la selección, ampliación y reparación de módulos de memoria RAM requiere **interpretar especificaciones técnicas de fabricantes y herramientas de diagnóstico.** Un error de compatibilidad o montaje puede provocar desde la inestabilidad del sistema operativo hasta daños irreversibles en los zócalos de la placa base.

La presente hoja de trabajo plantea **10 situaciones reales de taller**. Cada actividad exige analizar el escenario propuesto, consultar los datos técnicos de los componentes, realizar los cálculos oportunos y justificar técnicamente la decisión o procedimiento a seguir.

---

## Caso Práctico 1: Interpretación de Etiquetas Técnicas y Frecuencia de Bus Real

### Escenario de Taller
Un cliente entrega en el taller un módulo de memoria RAM empaquetado y solicita saber si es adecuado para su equipo. La etiqueta serigrafiada en el módulo indica el código: **`32GB DDR4-3200 PC4-25600 CL16 1.35V`**.

### Datos de Partida
* Módulo entregado por el cliente con codificación estándar de fabricante.
* Bus de datos de arquitectura de memoria estándar de 64 bits (8 bytes).

### Preguntas para el Alumno
1. Identifica y desglosa cada uno de los parámetros reflejados en la etiqueta comercial: capacidad total, tecnología DDR, velocidad efectiva, clasificación de ancho de banda, latencia CAS y voltaje de operación.
2. Demuestra matemáticamente la relación entre la velocidad efectiva ($3200\text{ MT/s}$) y la nomenclatura comercial PC4-25600.
3. Si abres la utilidad de diagnóstico CPU-Z en el sistema operativo, ¿qué valor exacto indicará en la casilla *DRAM Frequency* de la pestaña *Memory*? Justifica la respuesta según la tecnología de transferencia de datos DDR.

### Solución y Criterios de Evaluación
* **Desglose de etiqueta:**
  * Capacidad: $32\text{ GB}$.
  * Generación: DDR4 (*Double Data Rate 4*).
  * Velocidad efectiva: $3200\text{ MT/s}$ (*MegaTransfers por segundo*).
  * Clasificación de ancho de banda: PC4-25600 (ancho de banda pico de $25.600\text{ MB/s}$).
  * Latencia CAS: CL16 ($16\text{ ciclos}$ de reloj de retardo de acceso).
  * Voltaje: $1,35\text{ V}$ (indica la activación de perfil XMP de sobrevoltaje seguro).
* **Demostración matemática:**
  $$\text{Ancho de Banda (MB/s)} = \text{Velocidad Efectiva (MT/s)} \times \text{Ancho del Bus (8 bytes)}$$
  $$\text{Ancho de Banda} = 3200 \times 8 = 25.600 \text{ MB/s} \quad \rightarrow \quad \text{PC4-25600}$$
* **Frecuencia en CPU-Z:**
  Indicará **1600 MHz**. Al tratarse de tecnología DDR (*Double Data Rate*), la memoria realiza dos transferencias por cada ciclo de reloj. La frecuencia física real del bus se calcula como:
  $$\text{Frecuencia Física (MHz)} = \frac{\text{Velocidad Efectiva (MT/s)}}{2} = \frac{3200}{2} = 1600 \text{ MHz}$$

---

## Caso Práctico 2: Evaluación de Compatibilidad en Placa Base Legacy GIGABYTE GA-G41MT-S2

### Escenario de Taller
Un centro educativo desea ampliar la memoria RAM de sus ordenadores de aula de informática equipados con la placa base **GIGABYTE GA-G41MT-S2**. El responsable de compras ha seleccionado un kit comercial compuesto por **1 módulo de 8 GB DDR3L-1600 (1.35V)**.

### Datos de Partida (Manual del Fabricante GIGABYTE GA-G41MT-S2)
* Factor de forma: Micro-ATX ($24,4 \text{ cm} \times 19,4 \text{ cm}$).
* Zócalo de procesador: LGA 775 (soporta Intel Core 2 Duo / Quad).
* Chipset: Puente Norte Intel G41 Express / Puente Sur Intel ICH7.
* Especificación de memoria según manual:
  * $2 \times$ Zócalos DIMM DDR3 a $1,5\text{ V}$.
  * Capacidad máxima total de memoria del sistema: $8\text{ GB}$.
  * Arquitectura de memoria: Dual Channel.

### Preguntas para el Alumno
1. Revisa las especificaciones técnicas oficiales de la placa base GIGABYTE GA-G41MT-S2 e indica si el módulo de 8 GB seleccionado es compatible.
2. Identifica al menos tres limitaciones o incompatibilidades técnicas que impiden el correcto funcionamiento de dicha ampliación.
3. Diseña la combinación exacta de módulos que deberías adquirir para alcanzar la capacidad máxima permitida por la placa base aprovechando el rendimiento del sistema.

### Solución y Criterios de Evaluación
* **Dictamen de compatibilidad:** Incompatible. El módulo de 8 GB en un solo zócalo no funcionará en la placa base.
* **Justificación de incompatibilidades:**
  1. **Capacidad máxima por ranura:** La placa base admite un máximo total de $8\text{ GB}$ distribuidos obligatoriamente entre sus 2 zócalos DIMM, lo que impone un límite de **4 GB por slot**. Un único módulo de $8\text{ GB}$ excede la densidad máxima direccionable por el puente norte Intel G41.
  2. **Tensión de alimentación:** La placa especifica zócalos estándar de $1,5\text{ V}$ para DDR3. Aunque algunos módulos DDR3L ($1,35\text{ V}$) admiten doble voltaje, las placas antiguas LGA 775 no gestionan correctamente las especificaciones de bajo voltaje si la ROM de BIOS no está actualizada.
  3. **Pérdida de arquitectura de canal:** Al instalar un solo módulo se pierde la tecnología Dual Channel integrada en el controlador de memoria del chipset G41.
* **Configuración óptima recomendada:** Adquirir un kit idéntico de **2 módulos de 4 GB DDR3 a 1,5 V** (frecuencia de $1066\text{ MHz}$ o $1333\text{ MHz}$ según el FSB del procesador instalado), ocupando las 2 ranuras DIMM para habilitar el Dual Channel y alcanzar el tope de $8\text{ GB}$.

---

## Caso Práctico 3: Seguro Mecánico e Incompatibilidad Física entre Generaciones DDR

### Escenario de Taller
Durante una práctica de ensamblaje, un estudiante intenta insertar un módulo **DDR4 (288 pines, 1.2V)** en una ranura de expansión de una placa base diseñada para **DDR3 (240 pines, 1.5V)**. Al notar resistencia, el estudiante se dispone a aplicar mayor fuerza para hacer encajar las pestañas laterales.

### Datos de Partida
* Módulo A: DDR3 DIMM ($240\text{ pines}$, voltaje estándar $1,5\text{ V}$, muesca desplazada del centro).
* Módulo B: DDR4 DIMM ($288\text{ pines}$, voltaje estándar $1,2\text{ V}$, muesca casi central con curvatura inferior).
* Módulo C: DDR5 DIMM ($288\text{ pines}$, voltaje estándar $1,1\text{ V}$, muesca central con chip PMIC integrado).

### Preguntas para el Alumno
1. ¿Qué norma de seguridad mecánica de taller está violando el estudiante al intentar forzar la memoria?
2. Explica la función de la muesca de clave (*key notch*) presente en el conector dorado inferior de las memorias RAM.
3. Elabora una tabla comparativa entre las generaciones DDR3, DDR4 y DDR5 indicando: número de contactos/pines, voltaje estándar nominal y ubicación visual de la muesca.

### Solución y Criterios de Evaluación
* **Norma de seguridad violada:** Regla fundamental del ensamblador: *Nunca forzar un módulo de RAM*. Las tecnologías DDR no son retrocompatibles ni compatibles entre sí. Si un módulo no asienta con una presión suave y uniforme, el zócalo exige una generación diferente. Forzar la inserción fractura las pestañas de retención del zócalo o quiebra la placa de circuito impreso (PCB).
* **Función de la muesca:** Actúa como un seguro mecánico físico de posición que impide la inserción invertida del módulo y evita conectar generaciones con voltajes de operación incompatibles que quemarían los buses de la placa base.
* **Tabla comparativa:**

| Generación DDR | Recuento de Pines | Voltaje Estándar | Posición Visual de la Muesca | Características Distintivas |
| :--- | :--- | :--- | :--- | :--- |
| **DDR3** | 240 pines | 1,5 V | Ligeramente desplazada del centro | Pines planos estándar |
| **DDR4** | 288 pines | 1,2 V | Desplazada hacia el centro | Contactos con ligera curvatura en borde inferior |
| **DDR5** | 288 pines | 1,1 V | Prácticamente central (incompatible con DDR4) | Chip PMIC de gestión de energía integrado en el módulo |

---

## Caso Práctico 4: Configuración de Dual Channel y Selección de Zócalos DIMM

### Escenario de Taller
Un usuario ha comprado un ordenador de sobremesa para edición de vídeo equipado con una placa base con 4 ranuras de memoria RAM serigrafiadas como **A1, A2, B1 y B2**. El usuario instaló por su cuenta un kit de **2x16 GB DDR4-3600** colocándolos en los zócalos consecutivos **A1 y A2**. Al realizar un test de rendimiento, comprueba que el equipo funciona en modo *Single Channel*.

### Datos de Partida
* Placa base con 4 ranuras DIMM organizadas en 2 canales independientes:
  * Canal A: Ranuras A1 (primera) y A2 (segunda).
  * Canal B: Ranuras B1 (tercera) y B2 (cuarta).
* Kit de memoria: 2 módulos de $16\text{ GB}$ DDR4-3600 MT/s.

### Preguntas para el Alumno
1. Explica técnicamente por qué la colocación de las memorias en los zócalos A1 y A2 provoca que el controlador trabaje en *Single Channel*.
2. ¿En qué ranuras exactas se deben instalar los 2 módulos para activar correctamente la arquitectura *Dual Channel*?
3. Calcula el ancho de banda máximo teórico del sistema funcionando en Single Channel frente a la configuración corregida en Dual Channel.

### Solución y Criterios de Evaluación
* **Causa del problema:** Al insertar los dos módulos en A1 y A2, ambos quedan conectados al mismo canal del controlador de memoria (Canal A). El controlador direcciona un único bus de datos de 64 bits.
* **Disposición correcta:** Se deben instalar en ranuras pertenecientes a canales alternos, siguiendo la recomendación estándar del fabricante de placas base: **Ranuras A2 y B2** (segunda y cuarta ranura contando desde el zócalo del procesador). Esto activa los dos buses concurrentes de 64 bits (Canal A + Canal B).
* **Cálculo de Ancho de Banda:**
  * **Single Channel (64 bits / 8 bytes):**
    $$\text{Ancho de Banda} = 3600 \text{ MT/s} \times 8 \text{ bytes} = 28.800 \text{ MB/s} \quad (28,8 \text{ GB/s})$$
  * **Dual Channel (128 bits / 16 bytes concurrentes):**
    $$\text{Ancho de Banda} = 3600 \text{ MT/s} \times 16 \text{ bytes} = 57.600 \text{ MB/s} \quad (57,6 \text{ GB/s})$$
  * *Resultado:* El modo Dual Channel duplica el ancho de banda efectivo entre la memoria RAM y el microprocesador.

---

## Caso Práctico 5: Factores de Forma (DIMM vs. SO-DIMM) y Memorias Soldadas en Placa (LPDDR / RoC)

### Escenario de Taller
Llega al taller un cliente con dos equipos: un ordenador de sobremesa formato semitorre y un portátil ultraportátil (*ultrabook*). El cliente ha comprado en internet dos módulos de memoria RAM **DIMM DDR4 de 16 GB** con la intención de instalar uno en el sobremesa y otro en el portátil. Además, en la ficha técnica del portátil se indica la anotación *"Row of Chips (RoC) - LPDDR4x"*.

### Datos de Partida
* Módulo adquirido: DIMM DDR4 ($13\text{ cm}$ de longitud aproximadamente, 288 pines).
* Equipo 1: Sobremesa con ranuras DIMM estándar.
* Equipo 2: Ultraportátil con memoria LPDDR4x integrada.

### Preguntas para el Alumno
1. Compara las diferencias físicas de longitud y factor de forma entre los módulos para sobremesa (DIMM) y los módulos para equipos portátiles (SO-DIMM).
2. Explica la razón física por la cual el módulo DIMM no se puede instalar en un equipo portátil.
3. Interpreta el significado del término *"Row of Chips (RoC) / LPDDR"* en la ficha del portátil e indica si dicho equipo admite ampliación modular de memoria RAM.

### Solución y Criterios de Evaluación
* **Diferencias de factor de forma:**
  * **DIMM (*Dual In-line Memory Module*):** Diseñado para ordenadores de sobremesa y servidores. Tiene una longitud de unos $13\text{ cm}$.
  * **SO-DIMM (*Small Outline DIMM*):** Diseñado para portátiles, Mini-PCs e impresoras. Tiene una longitud reducida de unos $7\text{ cm}$ (aproximadamente la mitad) y un recuento de pines diferente (260 pines en DDR4 SO-DIMM).
* **Incompatibilidad en portátil:** El módulo DIMM de $13\text{ cm}$ no cabe físicamente en el zócalo de un portátil por discrepancia de dimensiones mecánicas y de zócalo.
* **Memoria LPDDR / RoC:**
  * *LPDDR (Low-Power Double Data Rate):* Memoria de bajo voltaje y alta eficiencia energética ideada para dispositivos móviles y ultraportátiles.
  * *Row of Chips (RoC):* Indica que los chips de memoria están **soldados directamente a la placa de circuito impreso (PCB)** de la placa base del equipo.
  * *Conclusión:* El portátil no dispone de ranuras de expansión de memoria y **no admite ampliación modular**.

---

## Caso Práctico 6: Mezcla de Módulos con Distintas Especificaciones y Ajustes JEDEC

### Escenario de Taller
Para economizar una reparación, un usuario decide reutilizar un módulo de memoria antiguo que tenía guardado y combinarlo con uno nuevo en su placa base en Dual Channel:
* **Módulo A (Existente):** $8\text{ GB}$ DDR4-2133 MT/s, CL15, voltaje $1,2\text{ V}$.
* **Módulo B (Nuevo):** $8\text{ GB}$ DDR4-3200 MT/s, CL16, voltaje $1,35\text{ V}$ (Perfil XMP).

### Datos de Partida
* Configuración: 2 módulos de 8 GB instalados en ranuras A2 y B2.
* Ambos módulos pertenecen a la tecnología DDR4 pero difieren en frecuencia, latencias y voltaje nominal.

### Preguntas para el Alumno
1. ¿Arrancará el sistema informático con esta combinación de módulos? Justifica el comportamiento del controlador de memoria de la BIOS/UEFI.
2. ¿A qué frecuencia de trabajo y latencia CAS operará la memoria RAM del equipo una vez encendido?
3. Evalúa las consecuencias en el rendimiento y la estabilidad del sistema al utilizar módulos heterogéneos.

### Solución y Criterios de Evaluación
* **Comportamiento del sistema:** Sí, el equipo arrancará. Durante la fase de POST, la BIOS/UEFI lee los chips EEPROM SPD de ambos módulos y aplica una regla de conservación: **el controlador ajusta la velocidad del conjunto al nivel del módulo con menores prestaciones**.
* **Valores finales de operación:**
  * Frecuencia efectiva: **2133 MT/s** (la velocidad del Módulo A).
  * Latencia: **CL15** (o el perfil JEDEC común más estable a 2133 MT/s).
  * Voltaje: **1,2 V** (voltaje estándar JEDEC sin activar perfil XMP).
* **Evaluación de consecuencias:**
  * *Rendimiento:* El Módulo B queda "infrautilizado", perdiendo la velocidad de 3200 MT/s por la que se pagó.
  * *Estabilidad:* Aunque se mantiene la arquitectura Dual Channel (al tener 8 GB por canal), el uso de controladores con voltajes y latencias dispares puede generar latencias de temporización inestables o bloqueos esporádicos en cargas de trabajo intensivas.

---

## Caso Práctico 7: Configuración de Perfiles de Alto Rendimiento XMP / EXPO en BIOS/UEFI

### Escenario de Taller
Un cliente ha adquirido un equipo de gama alta con memoria **DDR5-6000 CL30 (1.35V)**. Al ejecutar herramientas de prueba y supervisión en Windows, el cliente protesta porque el sistema le indica que la memoria está funcionando a **4800 MT/s a 1.1V**, creyendo que le han vendido componentes defectuosos.

### Datos de Partida
* Memoria instalada: Kit DDR5 etiquetado como 6000 MT/s a $1,35\text{ V}$.
* Lectura actual en sistema: 4800 MT/s a $1,1\text{ V}$.

### Preguntas para el Alumno
1. Explica por qué la memoria RAM funciona por defecto a 4800 MT/s en lugar de los 6000 MT/s anunciados en la caja.
2. ¿Qué significan las siglas **XMP** (Intel) y **EXPO** (AMD)? Explica su función en el chip de memoria.
3. Redacta el procedimiento paso a paso que debe realizar el técnico en la BIOS/UEFI para solucionar la reclamación del cliente.

### Solución y Criterios de Evaluación
* **Causa del funcionamiento a 4800 MT/s:** Por motivos de seguridad y compatibilidad universal, la BIOS/UEFI arranca siempre la memoria RAM aplicando los perfiles estándar **JEDEC** (en DDR5 el estándar base suele ser $4800\text{ MT/s}$ a $1,1\text{ V}$). La velocidad de 6000 MT/s exige un perfil de alto rendimiento (*overclocking* de fábrica seguro) que requiere ser activado voluntariamente.
* **Significado de XMP / EXPO:**
  * **XMP (*Extreme Memory Profile*):** Estándar propietario de Intel.
  * **EXPO (*Extended Profiles for Overclocking*):** Estándar abierto de AMD para plataformas AM5.
  * *Función:* Son perfiles de configuración almacenados en el chip SPD de la RAM que indican a la placa base la combinación probada de frecuencia superior, latencias optimizadas y sobrevoltaje seguro (ej. subir de $1,1\text{ V}$ a $1,35\text{ V}$).
* **Procedimiento técnico en BIOS/UEFI:**
  1. Reiniciar el equipo y pulsar repetidamente la tecla de acceso a la BIOS (habitualmente `Supr` o `F2`).
  2. Entrar en el modo avanzado (*Advanced Mode*) o apartado de configuración de memoria (*Overclocking / Ai Overclock Tuner / DRAM Frequency*).
  3. Localizar la opción *Memory Profile* (XMP o EXPO) y cambiar de *Disabled / Auto* a **Profile 1**.
  4. Guardar los cambios y salir pulsando `F10` (*Save & Exit*). El equipo se reiniciará aplicando los 6000 MT/s a $1,35\text{ V}$.

---

## Caso Práctico 8: Diagnóstico del Chip EEPROM SPD mediante CPU-Z

### Escenario de Taller
En el taller de mantenimiento se recibe un ordenador que sufre bloqueos aleatorios (*freezes*) al ejecutar aplicaciones pesadas. Sospechas que los módulos de memoria RAM instalados no son idénticos o tienen tablas de latencias desajustadas. No es posible abrir la caja del equipo por conservar el sello de garantía de fábrica.

### Datos de Partida
* Sistema operativo en marcha.
* Herramienta de software disponible: **CPU-Z**.
* Chip integrado en la RAM: **SPD (*Serial Presence Detect*)**.

### Preguntas para el Alumno
1. ¿Qué es el chip SPD y qué tipo de tecnología de memoria no volátil utiliza?
2. Enumera 4 datos clave grabados por el fabricante que se pueden inspeccionar a través de la pestaña *SPD* de CPU-Z.
3. Describe cómo usar el desplegable *Memory Slot Selection* de CPU-Z para verificar si las ranuras de la placa base contienen módulos compatibles en Dual Channel.

### Solución y Criterios de Evaluación
* **Definición de SPD:** El *Serial Presence Detect* es un pequeño chip de memoria no volátil de tipo **EEPROM** (*Electrically Erasable Programmable Read-Only Memory*) soldado en el circuito impreso del módulo de RAM.
* **Información almacenada en la EEPROM SPD:**
  1. Marca, fabricante (ej. Kingston, Corsair, Samsung) y número de serie del módulo.
  2. Capacidad del módulo y ancho de bus.
  3. Generación y estándar de memoria (ej. DDR4-3200 / PC4-25600).
  4. Tabla de tiempos (*JEDEC Timings Table*): frecuencias, latencias CAS (CL, tRCD, tRP, tRAS) y voltajes asignados para cada escalón de velocidad.
* **Procedimiento de diagnóstico en CPU-Z:**
  1. Abrir CPU-Z y seleccionar la pestaña **SPD**.
  2. En *Memory Slot Selection*, seleccionar `Slot #1` y anotar el fabricante, número de pieza (*Part Number*), frecuencia y latencias.
  3. Cambiar al resto de ranuras (`Slot #2`, `Slot #3`, `Slot #4`).
  4. *Criterio de validación:* Si los módulos difieren en fabricante o perfiles de frecuencia en las ranuras alternas del mismo canal, se confirma la fuente de inestabilidad del sistema.

---

## Caso Práctico 9: Protocolo de Seguridad Antiestática (ESD) y Secuencia Mecánica de Ensamblaje

### Escenario de Taller
Un alumno en prácticas se dispone a reemplazar un módulo de memoria RAM defectuoso. Sin desconectar el cable de corriente del ordenador ni utilizar elementos de protección ESD, toma el nuevo módulo tocando directamente con los dedos los contactos dorados inferiores e intenta colocarlo con las pestañas de retención del zócalo cerradas.

### Datos de Partida
* Componente a manipular: Módulo de memoria RAM sobremesa.
* Riesgos identificados: Descarga electrostática (ESD), daños por cortocircuito por corriente en placa en modo *standby* y rotura mecánica de pestañas.

### Preguntas para el Alumno
1. Identifica los errores cometidos en el protocolo de seguridad y manipulación de hardware.
2. Explica el riesgo técnico que supone una descarga electrostática (ESD) sobre los chips de semiconductor de la memoria RAM.
3. Redacta la secuencia paso a paso correcta para el desmontaje e inserción mecánica de un módulo RAM en el taller informático.

### Solución y Criterios de Evaluación
* **Errores cometidos:**
  1. Manipular componentes internos sin desconectar físicamente la alimentación de corriente alterna.
  2. Tocar directamente las zonas de contacto doradas del conector.
  3. No utilizar protección antiestática (pulsera ESD o descarga previa).
  4. No abrir las pestañas de bloqueo del zócalo antes de la inserción.
* **Riesgo ESD:** La acumulación de carga estática en el cuerpo humano (que puede superar los miles de voltios) puede perforar la delgada capa de óxido de los transistores y condensadores de las celdas DRAM o SRAM, destruyendo el componente de forma instantánea o provocando degradación latente (fallos aleatorios futuros).
* **Secuencia correcta de montaje:**
  1. **Desconexión:** Apagar el equipo y retirar el cable de alimentación CA de la fuente. Pulsar el botón de encendido del chasis para descargar condensadores residuales.
  2. **Protección ESD:** Colocarse la pulsera antiestática conectada a masa o tocar una superficie金属ica no pintada del chasis del ordenador.
  3. **Manipulación:** Sujetar el módulo de memoria **estrictamente por los bordes superiores de la PCB**, evitando tocar los chips integrados y los contactos dorados.
  4. **Preparación de zócalo:** Abrir manualmente las pestañas laterales de retención de la ranura DIMM seleccionada.
  5. **Alineación:** Hacer coincidir la muesca del módulo con el resalte mecánico del zócalo.
  6. **Inserción y bloqueo:** Aplicar una presión firme y uniforme con ambos pulgares en las esquinas superiores del módulo hasta escuchar un **clic claro** que indica que las pestañas laterales se han cerrado y bloqueado automáticamente.

---

## Caso Práctico 10: Árbol de Resolución de Averías (Pitidos de BIOS, BSOD y MemTest86)

### Escenario de Taller
Un cliente trae un ordenador que ha dejado de funcionar tras intentar hacer una limpieza interna en su casa. Al pulsar el botón de encendido, el equipo enciende los ventiladores pero no muestra imagen en el monitor y la placa base emite una serie de **pitidos continuos e ininterrumpidos**. Tras una primera intervención del técnico, el equipo arranca pero sufre pantallas azules (*BSOD - Blue Screen of Death*) al cabo de un tiempo de uso.

### Datos de Partida
* Síntoma A: El equipo no realiza el POST y emite pitidos continuos de BIOS.
* Síntoma B: El equipo arranca pero muestra pantallas azules aleatorias en el sistema operativo.

### Preguntas para el Alumno
1. ¿Qué indica el código de pitidos continuos del POST de la BIOS en relación con la memoria RAM?
2. Elabora un árbol de prescripción técnica de 3 pasos para aislar y resolver el fallo de hardware.
3. Describe el procedimiento de diagnóstico avanzado empleando la herramienta ejecutable **MemTest86**.

### Solución y Criterios de Evaluación
* **Diagnóstico de pitidos:** Los pitidos continuos e ininterrumpidos durante la fase de inicialización del POST señalan la ausencia de memoria RAM detectada, un módulo mal asentado en el zócalo o un cortocircuito en el bus de datos.
* **Árbol de prescripción técnica:**
  1. **Reasentamiento (*Reseat*):** Apagar el equipo, extraer el módulo, limpiar los contactos dorados con una goma de borrar suave o alcohol isopropílico, soplado de polvo en el zócalo y volver a insertar aplicando el protocolo mecánico de bloqueo.
  2. **Aislamiento de módulos y ranuras:** Probar encender el equipo con **un solo módulo** instalado en el primer zócalo recomendado (A2). Si arranca, probar el segundo módulo en la misma ranura para determinar si la avería está en la RAM o en la ranura de la placa base.
  3. **Diagnóstico mediante software:** Si el equipo arranca pero genera pantallas azules (BSOD), ejecutar un software de testeo profundo de memoria a nivel de celdas.
* **Procedimiento con MemTest86:**
  1. Crear un pendrive USB arrancable con la utilidad MemTest86.
  2. Conectar el USB al equipo defectuoso y encender seleccionando el arranque desde USB (*Boot Menu*).
  3. Ejecutar el test automatizado de 4 pasadas que escribe y lee patrones de bits en cada celda y condensador DRAM.
  4. *Evaluación de resultados:* Si la herramienta registra errores en rojo (fallos en la dirección de memoria), el módulo está dañado físicamente y debe ser reemplazado.
