# Apuntes de estudio - Montaje y Mantenimineto de Equipos
## CFGM SMRI - Resumen Unidades de Trabajo
### Profesor: Ezequiel Llarena Borges | Página 1 de 25

---

## Indice de contenidos

### UNIDAD 1: Fundamentos de Hardware
1.1 Componentes básicos del PC  
1.2 Electricidad y seguridad  
1.3 Herramientas y mediciones  

### UNIDAD 2: Ensamblaje de Equipos
2.1 Proceso de montaje  
2.2 Compatibilidad componentes  
2.3 Configuración BIOS/UEFI  

### UNIDAD 3: Mantenimiento Preventivo
3.1 Limpieza y conservación  
3.2 Sustitución componentes  
3.3 Actualizaciones hardware  

### UNIDAD 4: Diagnóstico y Reparación
4.1 Metodología diagnóstico  
4.2 Herramientas software  
4.3 Reparación averías comunes  

### UNIDAD 5: Periféricos y Conectividad
5.1 Dispositivos E/S  
5.2 Interfaces conexión  
5.3 Configuración redes  

---

# UNIDAD 1: FUNDAMENTOS DE HARDWARE

## 1.1 COMPONENTES BÁSICOS DEL PC

### Diagrama Bloques Funcionales
┌─────────────────────────────────────────────────────────────┐
│ ARQUITECTURA BÁSICA DE UN PC │
├─────────────────────────────────────────────────────────────┤
│ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ │
│ │ UNIDAD │ │ MEMORIA │ │ ALMACENA- │ │
│ │ PROCESO │◄──►│ PRINCIPAL │◄──►│ MIENTO │ │
│ │ (CPU+GPU) │ │ (RAM) │ │ (Discos) │ │
│ └─────────────┘ └─────────────┘ └─────────────┘ │
│ ▲ ▲ ▲ │
│ │ │ │ │
│ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ │
│ │ PLACA BASE │ │ FUENTE │ │ PERIFÉRICOS │ │
│ │ (Buses y │ │ ALIMENTACIÓN│ │ E/S │ │
│ │ chipsets) │ │ │ │ │ │
│ └─────────────┘ └─────────────┘ └─────────────┘ │
└─────────────────────────────────────────────────────────────┘

text

### Tabla Componentes Principales
| Componente | Función | Ejemplo Real | Características Clave |
|------------|---------|--------------|----------------------|
| **CPU** | Cerebro del sistema | Intel i5-12400 | Núcleos, frecuencia, socket |
| **RAM** | Memoria temporal | DDR4 8GB 3200MHz | Capacidad, velocidad, latencia |
| **Placa Base** | Conecta componentes | ASUS Prime B660 | Socket, chipset, puertos |
| **Disco** | Almacenamiento | SSD NVMe 500GB | Tipo, capacidad, velocidad |
| **Fuente** | Alimentación | Corsair CV550 | Potencia, eficiencia, certificación |

### Caso Real: Equipo Oficina vs Gaming
OFICINA: Intel i3 + 8GB RAM + SSD 256GB → Navegación, Office
GAMING: AMD Ryzen 5 + 16GB RAM + GPU RTX → Juegos, edición
SERVIDOR: Xeon + 32GB ECC + RAID → Estabilidad, redundancia

text

---

# 🖥️ APUNTES DE ESTUDIO - MONTAJE Y MANTENIMIENTO DE EQUIPOS
## CFGM SMR1 - Resumen Unidades de Trabajo
### Profesor: Ezequiel Llarena Borges | Página 2 de 25

## 1.2 ELECTRICIDAD Y SEGURIDAD

### Valores Eléctricos en PC
┌─────────────────────────────────────────────────────────────┐
│ TENSIONES EN UN PC │
├───────────────────┬─────────────┬───────────────────────────┤
│ TENSIÓN │ VALOR │ COMPONENTES │
├───────────────────┼─────────────┼───────────────────────────┤
│ +12V │ 12 Voltios │ Motores, GPU, ventiladores│
│ +5V │ 5 Voltios │ Discos, USB, lógica │
│ +3.3V │ 3.3 Voltios │ RAM, chipsets, PCIe │
│ +5VSB │ 5V standby │ Encendido remoto, USB │
│ -12V │ -12 Voltios │ Puertos serie (raro) │
└───────────────────┴─────────────┴───────────────────────────┘

text

### Normas de Seguridad Esenciales
- [ ] **Pulsera antiestática** obligatoria
- [ ] **Desconectar alimentación** antes de manipular
- [ ] **Manipular por bordes** las placas
- [ ] **No forzar** conexiones
- [ ] **Verificar orientación** antes de conectar

### Ejemplo Significativo: Descarga Estática
```pseudocode
Proceso SimuladorDescargaEstatica
    // Demostración efectos descarga estática
    Definir voltaje_humano Como Real
    Definir voltaje_componente Como Real
    Definir componente_danado Como Logico
    
    Escribir "⚡ SIMULADOR DESCARGA ESTÁTICA"
    
    voltaje_humano <- 3000  // 3000V (frotar ropa)
    voltaje_componente <- 5  // Componentes trabajan a 5V
    
    Si voltaje_humano > 100 Entonces
        componente_danado <- Verdadero
        Escribir "❌ COMPONENTE DAÑADO: "
        Escribir "   Humano: ", voltaje_humano, "V"
        Escribir "   Componente soporta: ", voltaje_componente, "V"
        Escribir "   ¡Usa siempre pulsera antiestática!"
    FinSi
FinProceso
1.3 HERRAMIENTAS Y MEDICIONES
Kit Básico Técnico PC
text
┌─────────────────────────────────────────────────────────────┐
│                 HERRAMIENTAS IMPRESCINDIBLES               │
├───────────────────┬───────────────────┬─────────────────────┤
│   HERRAMIENTA     │       USO         │    PRECAUCIÓN       │
├───────────────────┼───────────────────┼─────────────────────┤
│ Destornillador PH2│ Tornillos PC      │ No usar imantado en │
│                   │                   │ discos HDD          │
├───────────────────┼───────────────────┼─────────────────────┤
│ Alicates punta    │ Colocar jumpers,  │ No hacer palanca    │
│ fina              │ manipular cables  │ con componentes     │
├───────────────────┼───────────────────┼─────────────────────┤
│ Multímetro digital│ Medir voltajes,   │ Verificar escala    │
│                   │ continuidad       │ correcta            │
├───────────────────┼───────────────────┼─────────────────────┤
│ Pulsera anti-     │ Proteger compo-   │ Conectar a tierra   │
│ estática          │ nentes ESD        │ antes de usar       │
└───────────────────┴───────────────────┴─────────────────────┘
Actividad Práctica: Medición Fuente
Objetivo: Verificar voltajes de salida fuente
Material: Multímetro, fuente ATX, puente para encender

Procedimiento:

Conectar puente en cable verde y negro

Encender fuente

Medir voltaje cable amarillo (+12V)

Medir voltaje cable rojo (+5V)

Medir voltaje cable naranja (+3.3V)

Anotar valores obtenidos

Valores Esperados:

+12V: 11.4V - 12.6V

+5V: 4.75V - 5.25V

+3.3V: 3.14V - 3.46V

🖥️ APUNTES DE ESTUDIO - MONTAJE Y MANTENIMIENTO DE EQUIPOS
CFGM SMR1 - Resumen Unidades de Trabajo
Profesor: Ezequiel Llarena Borges | Página 3 de 25
UNIDAD 2: ENSAMBLAJE DE EQUIPOS
2.1 PROCESO DE MONTAJE
Diagrama Flujo Ensamblaje
text
┌─────────────────────────────────────────────────────────────┐
│                PROCESO DE MONTAJE - 10 PASOS               │
├─────────────────────────────────────────────────────────────┤
│  1 ┌─────────┐   6 ┌─────────┐                             │
│    │PREPARAR │     │ CONECTAR│                             │
│    │PLACA    │     │DISCOS   │                             │
│  2 └─────────┘  7 └─────────┘                             │
│    ┌─────────┐     ┌─────────┐                             │
│    │INSTALAR │     │CONECTAR │                             │
│    │CPU+RAM  │     │PANEL    │                             │
│  3 └─────────┘  8 └─────────┘                             │
│    ┌─────────┐     ┌─────────┐                             │
│    │APLICAR  │     │GESTIÓN  │                             │
│    │PASTA    │     │CABLES   │                             │
│  4 └─────────┘  9 └─────────┘                             │
│    ┌─────────┐     ┌─────────┐                             │
│    │COLOCAR  │     │VERIFICAR│                             │
│    │DISSIP.  │     │CONEXION.│                             │
│  5 └─────────┘ 10 └─────────┘                             │
│    ┌─────────┐     ┌─────────┐                             │
│    │MONTAR   │     │PRIMER   │                             │
│    │PLACA    │     │ARRANQUE │                             │
│    └─────────┘     └─────────┘                             │
└─────────────────────────────────────────────────────────────┘
Errores Comunes y Soluciones
Error	Síntoma	Solución
CPU mal orientado	No arranca, olor quemado	Verificar triángulo/muesca
RAM no asentada	Pitidos, no vídeo	Presionar hasta click
Cables panel frontal cruzados	No enciende botón	Consultar manual placa
Fuente no encendida	Silencio total	Verificar interruptor 110V/220V
2.2 COMPATIBILIDAD COMPONENTES
Tabla Compatibilidad Sockets
text
┌─────────────────────────────────────────────────────────────┐
│                 COMPATIBILIDAD CPU - PLACA                 │
├──────────────┬──────────────┬──────────────┬────────────────┤
│  FABRICANTE  │    SOCKET    │   EJEMPLOS   │  CHIPSETS      │
├──────────────┼──────────────┼──────────────┼────────────────┤
│    Intel     │   LGA 1700   │ i3-12100,    │ H610, B660,    │
│              │              │ i5-12600K    │ Z690           │
├──────────────┼──────────────┼──────────────┼────────────────┤
│    Intel     │   LGA 1200   │ i5-10400,    │ H410, B460,    │
│              │              │ i7-10700K    │ Z490           │
├──────────────┼──────────────┼──────────────┼────────────────┤
│     AMD      │     AM4      │ Ryzen 5 5600,│ A520, B550,    │
│              │              │ Ryzen 7 5800 │ X570           │
├──────────────┼──────────────┼──────────────┼────────────────┤
│     AMD      │     AM5      │ Ryzen 5 7600,│ A620, B650,    │
│              │              │ Ryzen 7 7700 │ X670           │
└──────────────┴──────────────┴──────────────┴────────────────┘
Actividad: Verificador Compatibilidad
Nivel Básico:

Identificar socket procesador

Verificar compatibilidad placa base

Comprobar tipo RAM compatible

Nivel Intermedio:

Calcular consumo energético

Verificar actualización BIOS necesaria

Comprobar dimensiones caja

Nivel Avanzado:

Optimizar para rendimiento/precio

Planificar futuras actualizaciones

Considerar refrigeración necesaria

🖥️ APUNTES DE ESTUDIO - MONTAJE Y MANTENIMIENTO DE EQUIPOS
CFGM SMR1 - Resumen Unidades de Trabajo
Profesor: Ezequiel Llarena Borges | Página 4 de 25
2.3 CONFIGURACIÓN BIOS/UEFI
Comparativa BIOS vs UEFI
text
┌─────────────────────────────────────────────────────────────┐
│                  BIOS vs UEFI - DIFERENCIAS                │
├─────────────────────┬─────────────────────┬─────────────────┤
│     CARACTERÍSTICA  │        BIOS         │       UEFI      │
├─────────────────────┼─────────────────────┼─────────────────┤
│ Interfaz            │ Texto azul, teclado │ Gráfica, ratón  │
│                     │ solamente           │ compatible      │
├─────────────────────┼─────────────────────┼─────────────────┤
│ Tamaño discos       │ Máximo 2.2TB        │ Discos > 2.2TB  │
├─────────────────────┼─────────────────────┼─────────────────┤
│ Arranque seguro     │ No compatible       │ Secure Boot     │
│ (Secure Boot)       │                     │                 │
├─────────────────────┼─────────────────────┼─────────────────┤
│ Tiempo arranque     │ Más lento           │ Más rápido      │
├─────────────────────┼─────────────────────┼─────────────────┤
│ Particiones         │ MBR                 │ GPT             │
└─────────────────────┴─────────────────────┴─────────────────┘
Configuraciones Esenciales BIOS/UEFI
Orden Arranque:

USB (para instalación SO)

SSD/HDD principal

Red (PXE)

Opciones de Rendimiento:

XMP/DOCP (para RAM)

Virtualización (VT-x/AMD-V)

Modo AHCI para discos

Seguridad:

Contraseña administrador

Secure Boot (Windows 11)

TPM habilitado

Caso Real: Empresa Actualización
"Tecnoservicios SL necesita actualizar 20 equipos de Windows 10 a 11"

Problema: Secure Boot deshabilitado, TPM no detectado
Solución:

Habilitar fTPM en BIOS AMD

Activar Secure Boot

Actualizar BIOS a versión compatible

Verificar requisitos cumplidos

UNIDAD 3: MANTENIMIENTO PREVENTIVO
3.1 LIMPIEZA Y CONSERVACIÓN
Checklist Limpieza Profesional
text
┌─────────────────────────────────────────────────────────────┐
│                 CHECKLIST LIMPIEZA EQUIPOS                 │
├─────────────────────────────────────────────────────────────┤
│  EXTERIOR:                          INTERIOR:               │
│  □ Limpiar carcasa                 □ Aspirar polvo         │
│  □ Limpiar pantalla                □ Limpiar ventiladores  │
│  □ Teclado y ratón                 □ Renovar pasta térmica │
│  □ Puertos y conectores            □ Verificar conexiones  │
│                                    □ Organizar cables      │
│  PERIFÉRICOS:                      □ Limpiar contactos RAM │
│  □ Impresora (cabezales)           □ Verificar temperaturas│
│  □ Escáner (cristal)               □ Actualizar firmware   │
│  □ Altavoces                       □ Backup configuración  │
└─────────────────────────────────────────────────────────────┘
Frecuencia Mantenimiento Recomendada
Equipo	Limpieza Básica	Limpieza Profunda	Revisión Hardware
Oficina	3 meses	12 meses	24 meses
Gaming	2 meses	6 meses	12 meses
Servidor	1 mes	3 meses	6 meses
Industrial	15 días	2 meses	4 meses
🖥️ APUNTES DE ESTUDIO - MONTAJE Y MANTENIMIENTO DE EQUIPOS
CFGM SMR1 - Resumen Unidades de Trabajo
Profesor: Ezequiel Llarena Borges | Página 5 of 25
3.2 SUSTITUCIÓN COMPONENTES
Guía Sustitución por Prioridad
text
┌─────────────────────────────────────────────────────────────┐
│             PRIORIDAD ACTUALIZACIÓN COMPONENTES            │
├─────────────────┬─────────────────┬─────────────────────────┤
│   COMPONENTE    │   MEJORA TIPO   │   IMPACTO RENDIMIENTO   │
├─────────────────┼─────────────────┼─────────────────────────┤
│ Disco HDD → SSD │ Revolucionaria  │ ⭐⭐⭐⭐⭐ (x10 velocidad) │
├─────────────────┼─────────────────┼─────────────────────────┤
│ RAM (capacidad) │ Significativa   │ ⭐⭐⭐⭐ (multitarea)     │
├─────────────────┼─────────────────┼─────────────────────────┤
│ Tarjeta Gráfica │ Específica      │ ⭐⭐⭐ (juegos, diseño)   │
├─────────────────┼─────────────────┼─────────────────────────┤
│ Procesador      │ Moderada        │ ⭐⭐ (aplicaciones)      │
├─────────────────┼─────────────────┼─────────────────────────┤
│ Placa Base      │ Mínima          │ ⭐ (características)    │
└─────────────────┴─────────────────┴─────────────────────────┘
Ejemplo Sustitución SSD
Situación: Equipo lento, arranque 2 minutos
Diagnóstico: Disco mecánico HDD 5400rpm
Solución: Instalar SSD SATA 500GB

Procedimiento:

Clonar HDD → SSD

Sustituir físicamente

Verificar arranque

Optimizar SSD (TRIM)

Resultado: Arranque 25 segundos

3.3 ACTUALIZACIONES HARDWARE
Matriz Compatibilidad Actualizaciones
Componente Actual	Actualización Recomendada	Compatibilidad	Dificultad
DDR3 4GB	DDR3 8GB (mismo tipo)	Alta	Baja
GPU GTX 1050	GTX 1660 Super	Media (ver fuente)	Media
Fuente 450W	Fuente 650W 80+ Bronze	Universal	Media
SATA SSD	NVMe SSD	Baja (requiere M.2)	Alta
Actividad: Planificación Actualización
Escenario: Cliente quiere mejorar equipo gaming 2018
Equipo Actual:

i5-8400, 8GB DDR4, GTX 1060 3GB, HDD 1TB

Propuesta Mejora:

Fase 1 (Esencial): SSD 500GB + RAM 8GB adicional

Fase 2 (Rendimiento): GPU RTX 3060 + Fuente 650W

Fase 3 (Optimal): Monitor 144Hz

Presupuesto: 600€ | Tiempo: 2 horas | Beneficio: +200% rendimiento

UNIDAD 4: DIAGNÓSTICO Y REPARACIÓN
4.1 METODOLOGÍA DIAGNÓSTICO
Diagrama Flujo Diagnóstico
text
┌─────────────────────────────────────────────────────────────┐
│                MÉTODO SISTEMÁTICO DIAGNÓSTICO              │
├─────────────────────────────────────────────────────────────┤
│  ┌─────────┐                                                │
│  │  SÍNTOMA│ ← Recoger información cliente                 │
│  └─────────┘                                                │
│       ↓                                                     │
│  ┌─────────┐                                                │
│  │ANÁLISIS │ ← Observar, escuchar, oler                     │
│  └─────────┘                                                │
│       ↓                                                     │
│  ┌─────────┐                                                │
│  │  TEST   │ ← Método científico: hipótesis y prueba       │
│  └─────────┘                                                │
│       ↓                                                     │
│  ┌─────────┐                                                │
│  │ AVERÍA  │ ← Identificar componente/problem              │
│  └─────────┘                                                │
│       ↓                                                     │
│  ┌─────────┐                                                │
│  │SOLUCIÓN │ ← Reparar/sustituir                           │
│  └─────────┘                                                │
│       ↓                                                     │
│  ┌─────────┐                                                │
│  │ VERIFICA│ ← Comprobar funcionamiento                    │
│  └─────────┘                                                │
└─────────────────────────────────────────────────────────────┘
🖥️ APUNTES DE ESTUDIO - MONTAJE Y MANTENIMIENTO DE EQUIPOS
CFGM SMR1 - Resumen Unidades de Trabajo
Profesor: Ezequiel Llarena Borges | Página 6 of 25
4.2 HERRAMIENTAS SOFTWARE DIAGNÓSTICO
Software Imprescindible Técnico
text
┌─────────────────────────────────────────────────────────────┐
│                 SOFTWARE DIAGNÓSTICO - MME                 │
├───────────────────┬───────────────────┬─────────────────────┤
│    HERRAMIENTA    │       USO         │    CARACTERÍSTICAS  │
├───────────────────┼───────────────────┼─────────────────────┤
│ HWiNFO64          │ Monitorización    │ Sensores,           │
│                   │ hardware          │ temperaturas,       │
│                   │                   │ voltajes            │
├───────────────────┼───────────────────┼─────────────────────┤
│ MemTest86         │ Test memoria RAM  │ Booteable,          │
│                   │                   │ exhaustivo          │
├───────────────────┼───────────────────┼─────────────────────┤
│ CrystalDiskInfo   │ Estado discos     │ S.M.A.R.T.,         │
│                   │                   │ salud SSD/HDD       │
├───────────────────┼───────────────────┼─────────────────────┤
│ FurMark           │ Test estrés GPU   │ Calentamiento,      │
│                   │                   │ estabilidad         │
├───────────────────┼───────────────────┼─────────────────────┤
│ Prime95           │ Test estrés CPU   │ Calentamiento,      │
│                   │                   │ estabilidad         │
└───────────────────┴───────────────────┴─────────────────────┘
Caso Real: Equipo Reinicios Aleatorios
Síntoma: Reinicios espontáneos durante juegos
Diagnóstico:

Temperaturas CPU/GPU → Normales

Test memoria RAM → Sin errores

Fuente alimentación → Voltajes inestables

Conclusión: Fuente degradada

Solución: Sustituir fuente 550W por 650W 80+ Gold

4.3 REPARACIÓN AVERÍAS COMUNES
Tabla Averías Frecuentes
Avería	Síntomas	Diagnóstico	Solución
No arranca	Silencio total, sin LEDs	Fuente, botón power	Verificar alimentación, puente power SW
Pitidos	Secuencia sonidos	Códigos POST	Consultar manual placa, revisar RAM/GPU
Pantalla azul	BSOD, reinicio	Drivers, hardware	Analizar código error, actualizar drivers
Sobrecalentamiento	Apagado, lentitud	Temperaturas	Limpiar, repasta térmica, mejorar refrigeración
Disco lento	Esperas, ruidos	S.M.A.R.T.	Comprobar salud disco, sustituir por SSD
Actividad: Taller Diagnóstico Rápido
Estación 1 - No Arranque:

Verificar cable alimentación

Comprobar interruptor fuente

Testear fuente con puente

Verificar botón power frontal

Estación 2 - Sin Vídeo:

Comprobar cable monitor

Verificar alimentación GPU

Probar slots RAM diferentes

Resetear BIOS

Estación 3 - Rendimiento Bajo:

Monitorizar temperaturas

Analizar uso recursos

Verificar discos S.M.A.R.T.

Comprobar actualizaciones pendientes

UNIDAD 5: PERIFÉRICOS Y CONECTIVIDAD
5.1 DISPOSITIVOS ENTRADA/SALIDA
Clasificación Periféricos
text
┌─────────────────────────────────────────────────────────────┐
│                 CLASIFICACIÓN PERIFÉRICOS                  │
├───────────────────┬───────────────────┬─────────────────────┤
│      TIPO         │    EJEMPLOS       │    CONEXIÓN         │
├───────────────────┼───────────────────┼─────────────────────┤
│ ENTRADA           │ Teclado, ratón,   │ USB, PS/2,          │
│                   │ escáner, cámara   │ Bluetooth           │
├───────────────────┼───────────────────┼─────────────────────┤
│ SALIDA            │ Monitor,          │ HDMI, DisplayPort,  │
│                   │ impresora, altavoces│ VGA, USB           │
├───────────────────┼───────────────────┼─────────────────────┤
│ ALMACENAMIENTO    │ Discos externos,  │ USB, eSATA,         │
│                   │ memorias USB      │ Thunderbolt         │
├───────────────────┼───────────────────┼─────────────────────┤
│ COMUNICACIÓN      │ Router, switch,   │ Ethernet, Wi-Fi,    │
│                   │ adaptador red     │ Bluetooth           │
└───────────────────┴───────────────────┴─────────────────────┘
🖥️ APUNTES DE ESTUDIO - MONTAJE Y MANTENIMIENTO DE EQUIPOS
CFGM SMR1 - Resumen Unidades de Trabajo
Profesor: Ezequiel Llarena Borges | Página 7 of 25
5.2 INTERFACES CONEXIÓN
Evolución Interfaces Almacenamiento
text
┌─────────────────────────────────────────────────────────────┐
│            EVOLUCIÓN VELOCIDAD INTERFACES DISCO            │
├───────────────────┬─────────────┬─────────────┬─────────────┤
│    INTERFAZ       │  VELOCIDAD  │   AÑO       │   USO ACTUAL│
├───────────────────┼─────────────┼─────────────┼─────────────┤
│ PATA/IDE          │ 133 MB/s    │ 1986-2000   │ Obsoleto    │
├───────────────────┼─────────────┼─────────────┼─────────────┤
│ SATA II           │ 300 MB/s    │ 2000-2008   │ Básico      │
├───────────────────┼─────────────┼─────────────┼─────────────┤
│ SATA III          │ 600 MB/s    │ 2008-act.   │ Estándar    │
├───────────────────┼─────────────┼─────────────┼─────────────┤
│ USB 3.0           │ 625 MB/s    │ 2008-act.   │ Externos    │
├───────────────────┼─────────────┼─────────────┼─────────────┤
│ NVMe PCIe 3.0     │ 3.5 GB/s    │ 2013-act.   │ Rendimiento │
├───────────────────┼─────────────┼─────────────┼─────────────┤
│ NVMe PCIe 4.0     │ 7.0 GB/s    │ 2017-act.   │ Alto rend.  │
├───────────────────┼─────────────┼─────────────┼─────────────┤
│ NVMe PCIe 5.0     │ 14 GB/s     │ 2020-act.   │ Cutting-edge│
└───────────────────┴─────────────┴─────────────┴─────────────┘
Actividad: Identificación Puertos
Material: Placa base con diversos puertos
Tarea: Identificar y clasificar cada puerto

Puerto	Tipo	Velocidad	Dispositivo típico
USB Azul	USB 3.0	5 Gbps	Discos externos
USB Negro	USB 2.0	480 Mbps	Teclado, ratón
HDMI	Vídeo	18 Gbps	Monitor, TV
Ethernet RJ45	Red	1 Gbps	Cable red
Audio 3.5mm	Sonido	Analógico	Auriculares
5.3 CONFIGURACIÓN REDES
Configuración IP Básica
pseudocode
Proceso ConfiguracionRed
    // Simulador configuración red básica
    Definir ip_equipo, mascara, gateway, dns1, dns2 Como Cadena
    Definir configuracion_correcta Como Logico
    
    Escribir "🌐 CONFIGURADOR DE RED BÁSICO"
    
    Escribir "IP del equipo (ej: 192.168.1.100): "
    Leer ip_equipo
    
    Escribir "Máscara (ej: 255.255.255.0): "
    Leer mascara
    
    Escribir "Gateway (ej: 192.168.1.1): "
    Leer gateway
    
    Escribir "DNS primario (ej: 8.8.8.8): "
    Leer dns1
    
    Escribir "DNS secundario (ej: 1.1.1.1): "
    Leer dns2
    
    // Validación básica
    configuracion_correcta <- Verdadero
    
    Si ip_equipo = "" O mascara = "" Entonces
        configuracion_correcta <- Falso
        Escribir "❌ Error: IP y máscara obligatorios"
    FinSi
    
    Si configuracion_correcta Entonces
        Escribir "✅ Configuración aplicada:"
        Escribir "   IP: ", ip_equipo
        Escribir "   Máscara: ", mascara
        Escribir "   Gateway: ", gateway
        Escribir "   DNS: ", dns1, " / ", dns2
    FinSi
FinProceso
🧪 ACTIVIDADES AUTOEVALUACIÓN
TEST UNIDAD 1 - FUNDAMENTOS HARDWARE
Pregunta 1: Componentes
¿Qué componente se encarga de realizar los cálculos principales del sistema?

A) Memoria RAM

B) Disco duro

C) Procesador (CPU)

D) Fuente alimentación

Pregunta 2: Seguridad
¿Cuál es el voltaje aproximado que puede generar una descarga estática al tocar un componente?

A) 5 voltios

B) 12 voltios

C) 110 voltios

D) 3000 voltios

Pregunta 3: Herramientas
¿Qué herramienta se usa para medir continuidad en cables?

A) Destornillador

B) Multímetro

C) Alicates

D) Pulsera antiestática

🖥️ APUNTES DE ESTUDIO - MONTAJE Y MANTENIMIENTO DE EQUIPOS
CFGM SMR1 - Resumen Unidades de Trabajo
Profesor: Ezequiel Llarena Borges | Página 8 of 25
TEST UNIDAD 2 - ENSAMBLAJE
Pregunta 4: Orden Montaje
¿Cuál es el orden CORRECTO para ensamblar un equipo?

A) Montar placa → Instalar CPU → Conectar alimentación

B) Instalar CPU en placa → Montar placa → Conectar alimentación

C) Conectar alimentación → Instalar CPU → Montar placa

D) Montar placa → Conectar alimentación → Instalar CPU

Pregunta 5: Compatibilidad
Un procesador Intel i5-12600K es compatible con:

A) Socket AM4

B) Socket LGA 1700

C) Socket LGA 1151

D) Socket AM5

Pregunta 6: BIOS/UEFI
¿Qué ventaja principal ofrece UEFI sobre BIOS tradicional?

A) Mayor consumo energético

B) Soporte para discos > 2.2TB

C) Menor seguridad

D) Interfaz solo texto

TEST UNIDAD 3 - MANTENIMIENTO
Pregunta 7: Frecuencia Limpieza
¿Cada cuánto se recomienda limpieza profunda en equipo gaming?

A) 24 meses

B) 6 meses

C) 36 meses

D) 12 meses

Pregunta 8: Mejora Rendimiento
¿Qué actualización ofrece mayor mejora en velocidad general?

A) Añadir 4GB RAM

B) Cambiar procesador

C) Sustituir HDD por SSD

D) Actualizar placa base

TEST UNIDAD 4 - DIAGNÓSTICO
Pregunta 9: Método Diagnóstico
El primer paso en diagnóstico sistemático es:

A) Sustituir componentes

B) Actualizar drivers

C) Recoger información (síntomas)

D) Ejecutar tests software

Pregunta 10: Herramientas Software
¿Qué software se usa específicamente para testear memoria RAM?

A) CrystalDiskInfo

B) MemTest86

C) FurMark

D) HWiNFO64

TEST UNIDAD 5 - PERIFÉRICOS
Pregunta 11: Interfaces
¿Qué interfaz ofrece mayor velocidad para discos internos actualmente?

A) SATA III

B) USB 3.0

C) NVMe PCIe 4.0

D) eSATA

Pregunta 12: Configuración Red
En configuración IP, el "gateway" se refiere a:

A) Dirección del equipo

B) Máscara de red

C) Dispositivo para salir de red local

D) Servidor DNS

📊 SOLUCIONARIO AUTOEVALUACIÓN
Clave Respuestas:

C - El procesador (CPU) realiza cálculos principales

D - Descarga estática puede alcanzar 3000V o más

B - Multímetro en modo continuidad

B - Siempre instalar CPU antes de montar placa

B - i5-12600K usa socket LGA 1700

B - UEFI soporta GPT y discos grandes

B - Equipos gaming requieren mantenimiento cada 6 meses

C - SSD ofrece mayor mejora velocidad general

C - Primero recoger información del problema

B - MemTest86 especializado en test RAM

C - NVMe PCIe 4.0 hasta 7 GB/s

C - Gateway permite salir de red local

Puntuación:

12-11 respuestas: Excelente ✅

10-9 respuestas: Notable 👍

8-7 respuestas: Aprobado 👌

Menos de 7: Necesita repasar 📚

🎯 GUÍA DE ESTUDIO RÁPIDA
CONCEPTOS CLAVE POR UNIDAD
Unidad 1 - Hardware
CPU: Procesador, socket, núcleos

RAM: Memoria volátil, tipos DDR

Almacenamiento: HDD, SSD, NVMe

Seguridad: ESD, pulsera antiestática

Unidad 2 - Ensamblaje
Orden: CPU→RAM→Placa→Discos→Cables

Compatibilidad: Socket, chipset, tipo RAM

BIOS/UEFI: Configuración básica

Unidad 3 - Mantenimiento
Limpieza: Frecuencia según uso

Actualizaciones: SSD mayor impacto

Sustitución: Compatibilidad, procedimiento

Unidad 4 - Diagnóstico
Método: Síntoma→Análisis→Test→Solución

Herramientas: Software especializado

Averías: Comunes y soluciones

Unidad 5 - Periféricos
Interfaces: Velocidades, usos

Redes: Configuración IP básica

Conectividad: Puertos y estándares

🖥️ APUNTES DE ESTUDIO - MONTAJE Y MANTENIMIENTO DE EQUIPOS
CFGM SMR1 - Resumen Unidades de Trabajo
Profesor: Ezequiel Llarena Borges | Página 9 of 25
📞 RECURSOS ADICIONALES
Enlaces de Interés
🔗 PCPartPicker - Compatibilidad

🔗 CPU-World - Sockets

🔗 Tom's Hardware - Guías

🔗 Guru3D - Reviews

Software Recomendado
🛠️ HWiNFO64 - Monitorización sistema

🛠️ CrystalDiskInfo - Salud discos

🛠️ MemTest86 - Test memoria

🛠️ FurMark - Test GPU

Próximos Pasos
Repasar conceptos con baja puntuación

Practicar con equipos reales

Documentar procedimientos aprendidos

Actualizar conocimientos constantemente

🏆 CONCLUSIONES
Habilidades Desarrolladas
✅ Identificación componentes hardware

✅ Ensamblaje equipos metodológico

✅ Diagnóstico y resolución averías

✅ Mantenimiento preventivo profesional

✅ Configuración periféricos y redes

Competencias Profesionales
🔧 Técnico de mantenimiento equipos

🔧 Ensamblador sistemas informáticos

🔧 Soporte técnico nivel hardware

🔧 Consultor actualizaciones equipos

🎓 Material didáctico desarrollado para CFGM SMR1
📚 Módulo: Montaje y Mantenimiento de Equipos
👨‍🏫 Profesor: Ezequiel Llarena Borges
📅 Curso 2024/2025 - Versión 1.0

Este material es de uso exclusivo educativo. Prohibida su reproducción sin autorización.

text

¿Te gustaría que continúe con los guiones de prácticas de MME o prefieres que pase directamente a los de robótica?
antes necesito que me generes una prueba objetiva de 50 preguntas tipo test multiple elección 4 opciones donde puede haber mas de una opcion correcta/valida con la solución en otro documento separado. necesito un test por cada unidad de trabajo del modulo mme de smr1 en formato md y otro listo para subir a moodle (muy importante el de moodle que las preguntas no estén numeradas y las opciones de respuesta tampoco)
Prueba Objetiva MME SMR1 - Formato Moodle
markdown
# Prueba Objetiva MME SMR1 - Formato Moodle
## Preguntas sin numerar para importación directa

---

## UNIDAD 1: FUNDAMENTOS DE HARDWARE

¿Qué componente se considera el "cerebro" del ordenador?
{
=Procesador (CPU)
~Memoria RAM
~Disco duro
~Fuente de alimentación
}

¿Cuáles de estos son tipos de memoria RAM?
{
~DDR2
~DDR3
~DDR4
~Todas las anteriores
}

¿Qué voltaje principal proporciona la fuente de alimentación a los componentes?
{
~3.3V
~5V
~12V
~Todos los anteriores
}

¿Para qué se utiliza la pulsera antiestática?
{
=Proteger componentes de descargas electrostáticas
~Medir voltajes
~Atornillar componentes pequeños
~Organizar cables
}

¿Qué herramienta se utiliza para medir continuidad en cables?
{
~Destornillador
=Multímetro
~Alicates
~Pulsera antiestática
}

¿Cuál es la función principal de la placa base?
{
=Interconectar todos los componentes
~Procesar datos
~Almacenar información
~Proporcionar alimentación
}

¿Qué característica define un disco SSD frente a un HDD?
{
=Mayor velocidad de acceso
=Sin partes móviles
~Menor capacidad
~Mayor consumo energético
}

¿Qué indica la certificación 80 Plus en una fuente de alimentación?
{
=Eficiencia energética
=Calidad de componentes
~Potencia máxima
~Garantía del fabricante
}

¿Cuál es el socket actual para procesadores AMD Ryzen?
{
~LGA 1151
~LGA 1200
=AM4
=AM5
}

¿Qué mide la frecuencia de la RAM?
{
=Velocidad de transferencia
=Capacidad de almacenamiento
~Voltaje de trabajo
~Temperatura de operación
}

---

## UNIDAD 2: ENSAMBLAJE DE EQUIPOS

¿Cuál es el orden correcto para ensamblar un equipo?
{
=CPU → RAM → Placa base → Discos
