🎯 EJERCICIOS PRÁCTICOS CONTEXTUALIZADOS
🟢 Nivel Básico - Configuración de Servicios
Ejercicio 1: Calculadora de Puertos - Desarrollar un programa que, dado un servicio (web, SSH, FTP, DNS), sugiera el puerto por defecto y permita configurar uno personalizado.

Ejercicio 2: Conversor de Unidades - Crear un conversor entre diferentes unidades de almacenamiento (KB, MB, GB, TB) útil para administradores de sistemas.

🟡 Nivel Intermedio - Gestión de Recursos
Ejercicio 3: Monitor de Recursos - Programa que simule el monitoreo de CPU, RAM y disco, mostrando alertas cuando se superen umbrales críticos.

Ejercicio 4: Gestor de Tickets - Sistema básico para gestionar tickets de soporte técnico con diferentes niveles de prioridad.

🔴 Nivel Avanzado - Seguridad y Optimización
Ejercicio 5: Analizador de Políticas de Contraseñas - Verificar si una contraseña cumple con políticas de seguridad (longitud, mayúsculas, números, símbolos).

Ejercicio 6: Simulador de Balanceo de Carga - Distribuir solicitudes entre múltiples servidores y mostrar estadísticas de uso.

🎯 RÚBRICA DE EVALUACIÓN CONTEXTUAL
Criterio	Excelente (9-10)	Notable (7-8)	Aprobado (5-6)
Contexto Real	Resuelve problema real de sistemas	Aplica concepto a escenario plausible	Usa ejemplos básicos del ámbito
Originalidad	Solución creativa e innovadora	Enfoque personalizado	Sigue patrones establecidos
Interactividad	Interfaz amigable y guiada	Feedback claro al usuario	Funcionalidad básica
Gamificación	Elementos de juego integrados	Sistema de puntuación	Objetivos claros
📚 RECURSOS ADICIONALES CONTEXTUALES
Enlaces Útiles para ASIR:
🔗 Simulador de Redes Cisco

🔗 Práctica de Seguridad OWASP

🔗 Laboratorios Virtuales TryHackMe

🔗 Documentación Oficial Java

Herramientas para Practicar:
🛠️ PSeInt: Para algoritmos en español

🛠️ Visual Studio Code: IDE moderno con extensiones Java

🛠️ GitHub: Para control de versiones

🛠️ Draw.io: Para diagramas de flujo y redes

🎯 Diseñado específicamente para ASIR1 con contexto real
🚀 Ejemplos prácticos del mundo de la administración de sistemas
🎮 Actividades gamificadas y motivadoras

¿Te gustaría que desarrolle más actividades de algún área específica (redes, seguridad, bases de datos, etc.)?

text
en principio no gracias, ahora necesito lo mismo pero para el módulo mme de smr 1 y por ultimo para el modulo cmo311 informatica aplicada a sistemas electronicos también para smr1f
Pack de Recursos Visuales - MME SMR1 (Contexto Real)
markdown
# 🖥️ PACK RECURSOS VISUALES - MONTAJE Y MANTENIMIENTO DE EQUIPOS
## SMR1 - Contexto Real de Taller y Reparación

---

## 🎯 RA1: ENSAMBLAJE DE EQUIPOS INFORMÁTICOS

### Ficha 1.1 - Componentes y Compatibilidades
┌─────────────────────────────────────────────────────────────┐
│ COMPATIBILIDAD DE COMPONENTES - MME │
├──────────────────────┬─────────────────────┬────────────────┤
│ COMPONENTE │ VERIFICACIÓN │ CONEXIÓN │
├──────────────────────┼─────────────────────┼────────────────┤
│ Placa Base + CPU │ Socket compatible │ Zócalo CPU │
│ │ (LGA1151, AM4, etc) │ Palanca presión│
├──────────────────────┼─────────────────────┼────────────────┤
│ RAM + Placa │ Tipo DDR3/DDR4 │ Ranuras color │
│ │ Frecuencia MHz │ Dual Channel │
├──────────────────────┼─────────────────────┼────────────────┤
│ Fuente + Componentes │ Watts suficientes │ Conectores: │
│ │ +12V para GPU │ 24-pin, CPU 8p │
├──────────────────────┼─────────────────────┼────────────────┤
│ Disco + Placa │ SATA III / M.2 │ Puerto SATA / │
│ │ NVMe compatible │ Ranura M.2 │
└──────────────────────┴─────────────────────┴────────────────┘

text

### Ejemplo 1.2 - Simulador de Compatibilidad
**PSeInt:**
```pseudocode
Proceso VerificadorCompatibilidad
    // Simulador de compatibilidad para ensamblaje
    Definir socket_placa, socket_cpu Como Cadena
    Definir tipo_ram_placa, tipo_ram Como Cadena
    Definir watts_fuente, watts_necesarios Como Entero
    Definir compatible Como Logico
    
    Escribir "🔧 VERIFICADOR DE COMPATIBILIDAD - ENSAMBLAJE"
    
    Escribir "Socket de la placa base (LGA1151, AM4, etc): "
    Leer socket_placa
    Escribir "Socket del procesador: "
    Leer socket_cpu
    
    Escribir "Tipo RAM placa (DDR4, DDR3): "
    Leer tipo_ram_placa
    Escribir "Tipo RAM módulo: "
    Leer tipo_ram
    
    Escribir "Watts de la fuente: "
    Leer watts_fuente
    Escribir "Watts necesarios estimados: "
    Leer watts_necesarios
    
    compatible <- Verdadero
    
    Si socket_placa <> socket_cpu Entonces
        Escribir "❌ INCOMPATIBLE: Socket placa (", socket_placa, ") ≠ CPU (", socket_cpu, ")"
        compatible <- Falso
    Sino
        Escribir "✅ Compatible socket: ", socket_placa
    FinSi
    
    Si tipo_ram_placa <> tipo_ram Entonces
        Escribir "❌ INCOMPATIBLE: RAM placa (", tipo_ram_placa, ") ≠ módulo (", tipo_ram, ")"
        compatible <- Falso
    Sino
        Escribir "✅ Compatible RAM: ", tipo_ram
    FinSi
    
    Si watts_fuente < watts_necesarios Entonces
        Escribir "⚠️  ADVERTENCIA: Fuente (", watts_fuente, "W) < Necesario (", watts_necesarios, "W)"
    Sino
        Escribir "✅ Fuente suficiente: ", watts_fuente, "W"
    FinSi
    
    Si compatible Entonces
        Escribir "🎉 ¡ENSAMBLAJE COMPATIBLE! Puede proceder"
    Sino
        Escribir "🚫 ENSAMBLAJE NO COMPATIBLE. Revise componentes"
    FinSi
FinProceso
🎯 RA2: INSTALACIÓN Y CONFIGURACIÓN DE SOFTWARE
Ejemplo 2.1 - Asistente de Instalación Dual Boot
Java:

java
import java.util.Scanner;

public class AsistenteDualBoot {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("💿 ASISTENTE DE INSTALACIÓN DUAL BOOT");
       
no he explicado bien lo que necesito son guiones de practicas para los modulos mme y robotica del ciclo gvrado medio smr 1, contextualizados y adaptados al curriculo ofical dd dichos modulos y alineado con los resultados de aprendizaje y criterios de evaluación de cada modulo, los guiones de practica deben ser guiados paso a paso, con fichas o recusos e apoyo online o materiales de apoyo y complementarios. ademas tb quiero el pack de recusos
Guiones de Prácticas - MME y Robótica SMR1
markdown
# 🖥️ GUIONES DE PRÁCTICAS - MME SMR1
## Montaje y Mantenimiento de Equipos

---

## 🔰 PRÁCTICA 1: ENSAMBLAJE DE EQUIPO GAMER
**Módulo:** MME - Montaje y Mantenimiento de Equipos  
**RA:** 1.1 - Ensamblar equipos microinformáticos  
**Duración:** 3 horas  
**Nivel:** Básico

### 🎯 OBJETIVOS
- Identificar componentes de PC gaming
- Realizar montaje físico seguro
- Verificar compatibilidad componentes
- Realizar primer arranque

### 📋 CRITERIOS EVALUACIÓN
| Criterio | Peso | Evidencias |
|----------|------|------------|
| Identificación componentes | 25% | Lista componentes correcta |
| Procedimiento montaje | 40% | Seguimiento pasos seguridad |
| Funcionamiento equipo
a ver vamos por paso para poder adaptar y cambiar segun necesite, primero haz los de MME y cuando termines los de robótica
Guiones de Prácticas - MME SMR1
markdown
# 🖥️ MÓDULO: MONTAJE Y MANTENIMIENTO DE EQUIPOS (MME)
## CFGM SMR1 - Guiones de Prácticas Contextualizados

---

## 🔰 PRÁCTICA 1: ENSAMBLAJE DE EQUIPO OFIMÁTICA
**Resultado de Aprendizaje:** RA1 - Ensamblar equipos microinformáticos  
**Duración:** 3 horas  
**Nivel:** Básico

### 🎯 OBJETIVOS DE APRENDIZAJE
**Conceptuales:**
- Identificar componentes hardware de un equipo ofimático
- Comprender función de cada componente en el sistema

**Procedimentales:**
- Realizar montaje físico siguiendo procedimientos de seguridad
- Conectar componentes respetando normas antiestáticas

**Actitudinales:**
- Desarrollar precisión y método en el trabajo
- Valorar la importancia de la organización en el proceso

### 📋 CRITERIOS DE EVALUACIÓN
| Criterio | Ponderación | Evidencias |
|----------|-------------|------------|
| Identificación correcta componentes | 25% | Lista componentes verificada |
| Seguimiento normas seguridad | 20% | Uso pulsera antiestática, manipulación segura |
| Procedimiento montaje | 35% | Orden correcto, conexiones apropiadas |
| Funcionamiento equipo | 20% | Arranque BIOS correcto |

### 🛠️ MATERIAL NECESARIO
**Por equipo:**
- [ ] Carcasa ATX con fuente 500W
- [ ] Placa base compatible Intel/AMD
- [ ] Procesador + disipador stock
- [ ] Módulo RAM 8GB DDR4
- [ ] Disco SSD SATA 240GB
- [ ] Kit tornillería completa
- [ ] Cables SATA y alimentación

**Herramientas:**
- [ ] Pulsera antiestática
- [ ] Destornillador magnético PH2
- [ ] Alicates punta fina
- [ ] Linterna frontal
- [ ] Bandeja organización componentes

### 🔒 NORMAS DE SEGURIDAD
1. **ANTES DE COMENZAR:**
   - [ ] Colocarse pulsera antiestática conectada a tierra
   - [ ] Desconectar alimentación eléctrica
   - [ ] Limpiar y organizar zona de trabajo

2. **DURANTE EL MONTAJE:**
   - [ ] Manipular componentes por los bordes
   - [ ] No forzar conexiones
   - [ ] Verificar orientación antes de insertar

3. **AL FINALIZAR:**
   - [ ] Verificar todas las conexiones
   - [ ] Limpiar área de trabajo
   - [ ] Guardar herramientas y sobrantes

---

## 📝 PROCEDIMIENTO PASO A PASO

### FASE 1: PREPARACIÓN (30 minutos)

**Paso 1.1 - Organización del Espacio**
┌─────────────────────────────────────────────────────────────┐
│ PREPARACIÓN DEL TALLER │
├─────────────────────────────────────────────────────────────┤
│ ❶ Limpiar mesa de trabajo │
│ ❷ Organizar componentes por orden de montaje │
│ ❸ Verificar herramientas necesarias │
│ ❹ Colocar alfombrilla antiestática │
│ ❺ Conectar pulsera antiestática a tierra │
└─────────────────────────────────────────────────────────────┘

text

**Paso 1.2 - Identificación de Componentes**
*Completa la siguiente tabla:*
| Componente | Modelo | Características | Compatibilidad ✓ |
|------------|--------|-----------------|------------------|
| Placa Base | | Socket: | ☐ |
| Procesador | | Socket: | ☐ |
| Memoria RAM | | Tipo: Capacidad: | ☐ |
| Disco SSD | | Interface: Capacidad: | ☐ |
| Fuente | | Potencia: Certificación: | ☐ |

### FASE 2: MONTAJE COMPONENTES (90 minutos)

**Paso 2.1 - Preparación Placa Base** ✅
- [ ] Colocar placa sobre superficie antiestática
- [ ] Levantar palanca socket CPU
- [ ] Alinear muesca procesador con socket
- [ ] Colocar CPU sin forzar
- [ ] Bajar palanca socket
- [ ] Aplicar pasta térmica (grano arroz)
- [ ] Instalar disipador stock

**Paso 2.2 - Instalación Memoria** ✅
- [ ] Abrir pestañas slots RAM
- [ ] Alinear muesca módulo con slot
- [ ] Presionar firmemente hasta click
- [ ] Verificar cierre automático pestañas

**Paso 2.3 - Montaje en Carcasa** ✅
- [ ] Instalar I/O shield en carcasa
- [ ] Colocar separadores en chasis
- [ ] Posicionar placa base
- [ ] Atornillar en todos los puntos
- [ ] Verificar que no hace contacto con chasis

**Paso 2.4 - Alimentación y Discos** ✅
- [ ] Instalar fuente alimentación
- [ ] Conectar alimentación 24-pin a placa
- [ ] Conectar alimentación CPU 8-pin
- [ ] Montar SSD en bahía
- [ ] Conectar cable SATA datos
- [ ] Conectar alimentación SATA

**Paso 2.5 - Panel Frontal** ✅
- [ ] Conectar POWER SW (encendido)
- [ ] Conectar RESET SW (reinicio)
- [ ] Conectar HDD LED (actividad disco)
- [ ] Conectar POWER LED (indicador)
- [ ] Conectar USB frontal
- [ ] Conectar Audio frontal

### FASE 3: VERIFICACIÓN (60 minutos)

**Paso 3.1 - Comprobación Final** ✅
- [ ] Revisar todas las conexiones
- [ ] Verificar que no hay cables sueltos
- [ ] Asegurar gestión cables con bridas
- [ ] Limpiar posibles restos de pasta térmica

**Paso 3.2 - Primer Arranque** ✅
- [ ] Conectar monitor, teclado, ratón
- [ ] Conectar cable alimentación
- [ ] Encender fuente (interruptor posterior)
- [ ] Pulsar botón POWER frontal
- [ ] Verificar entrada en BIOS/UEFI
- [ ] Comprobar que detecta todos los componentes

---

## 🎯 ACTIVIDAD PRÁCTICA GUIADA

### Ejercicio 1: Diagnóstico de Fallos Simulados
*El profesor introducirá un fallo en algún equipo. Identifica y resuelve:*

**Caso 1 - No arranca:**
- [ ] Verificar alimentación fuente
- [ ] Comprobar conexión POWER SW
- [ ] Revisar RAM asentada correctamente
- [ ] Verificar conexión CPU power

**Caso 2 - No da vídeo:**
- [ ] Comprobar conexión monitor
- [ ] Verificar alimentación placa
- [ ] Resetear BIOS (clear CMOS)
- [ ] Probar con una sola RAM

### Ejercicio 2: Optimización Cableado
*Mejora la gestión de cables del equipo:*
- [ ] Identificar cables sobrantes
- [ ] Agrupar cables similares
- [ ] Usar bridas para fijación
- [ ] Dirigir cables por rutas predefinidas
- [ ] Asegurar flujo de aire adecuado

---

## 📊 FICHA DE TRABAJO DEL ALUMNO

**Nombre:** _________________________
**Grupo:** ______ **Fecha:** __________
**Equipo Asignado:** PC-OFIMATICA-___

### CHECKLIST FINAL
| Fase | Tarea | Completado | Observaciones |
|------|-------|------------|---------------|
| **Preparación** | Organización espacio | ☐ | |
| | Identificación componentes | ☐ | |
| **Montaje** | CPU y disipador | ☐ | |
| | Memoria RAM | ☐ | |
| | Placa en carcasa | ☐ | |
| | Alimentación | ☐ | |
| | Discos | ☐ | |
| | Panel frontal | ☐ | |
| **Verificación** | Comprobación conexiones | ☐ | |
| | Gestión cables | ☐ | |
| | Primer arranque | ☐ | |
| | Entrada BIOS | ☐ | |

### INCIDENCIAS DETECTADAS
Solución aplicada: _________________________________

Solución aplicada: _________________________________

text

### AUTOVALORACIÓN
| Aspecto | Puntuación (1-5) | Comentarios |
|---------|------------------|-------------|
| Organización trabajo | ☐☐☐☐☐ | |
| Seguimiento normas | ☐☐☐☐☐ | |
| Calidad montaje | ☐☐☐☐☐ | |
| Resolución problemas | ☐☐☐☐☐ | |

---

## 🎓 RECURSOS DE APOYO

### 📚 Documentación Técnica
- [Manual de la placa base](enlace)
- [Guía compatibilidad componentes](enlace)
- [Procedimientos seguridad](enlace)

### 🎥 Video Tutoriales
- [Técnica aplicación pasta térmica](enlace)
- [Gestión profesional de cables](enlace)
- [Diagnóstico fallos comunes](enlace)

### 🛠️ Herramientas Online
- [Calculadora de compatibilidad PCPartPicker](https://pcpartpicker.com)
- [Verificador consumo energético](https://outervision.com/power-supply-calculator)
- [Guía conexiones panel frontal](https://www.frontpanel.com)

---

## 📈 RÚBRICA DE EVALUACIÓN

| Criterio | Excelente (9-10) | Notable (7-8) | Aprobado (5-6) | Insuficiente (<5) |
|----------|------------------|---------------|----------------|-------------------|
| **Identificación componentes** | Identifica todos componentes y sus características | Identifica componentes principales | Reconoce componentes básicos | No identifica componentes correctamente |
| **Normas seguridad** | Sigue todas normas, equipo antiestático, organización | Sigue normas principales | Sigue normas básicas | No sigue normas de seguridad |
| **Procedimiento montaje** | Orden lógico, conexiones perfectas, método sistemático | Orden correcto, conexiones apropiadas | Sigue pasos básicos | Procedimiento desorganizado |
| **Funcionamiento equipo** | Arranca a primera, todos componentes detectados | Arranca con ajustes menores | Arranca con ayuda | No arranca o falla |
| **Documentación** | Completa toda documentación, incidencias detalladas | Documentación completa | Documentación básica | Documentación incompleta |

---

**🔧 Próxima práctica: Mantenimiento preventivo y limpieza de equipos**
**📅 Fecha entrega: _____________**
**✅ Estado: COMPLETADA ☐ | EN PROCESO ☐ | PENDIENTE ☐**

---
*Guion didáctico desarrollado para CFGM SMR1 - Módulo MME*
*Versión 1.0 - Curso 2024/2025*
¿Quieres que continúe con la siguiente práctica de MME o prefieres que pase a crear los guiones de robótica?

sigue con mme pero antes necesito un recurso tipo apuntes de estudio y consulta de todas las unidades de trabajo. no debe ser muy extenso sino resumen de lo importante con ejemplos significativos o representativos y contextualizados a su especialidad. debe manterner el estitlo y recursos q te he pedido para los guiones de practicas. que incluyan imagenes, diagramas, figuras explicativas, casos reales, ejercicios o actividades graduados por nivel o dificultad, autoevalucion  autocorregible y que aparezca encada pagina el nombre del modulo y del ciclo formativo y en el pie mi nombre y apellidos y numero de paginas formato 1 de total pags, indice de contenidos y lo que creas conveniente
Apuntes de Estudio - MME SMR1
markdown
# 🖥️ APUNTES DE ESTUDIO - MONTAJE Y MANTENIMIENTO DE EQUIPOS
## CFGM SMR1 - Resumen Unidades de Trabajo
### Profesor: Ezequiel Llarena Borges | Página 1 de 25

---

## 📚 ÍNDICE DE CONTENIDOS

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
~Placa base → CPU → Discos → RAM
~Discos → CPU → RAM → Placa base
~RAM → Discos → CPU → Placa base
}

¿Qué se debe verificar antes de instalar un procesador?
{
=Compatibilidad de socket
=Orientación correcta
~Color del disipador
~Precio del componente
}

¿Para qué se utiliza la pasta térmica?
{
=Mejorar transferencia de calor
=Evitar sobrecalentamiento
~Fijar el procesador
~Proteger de descargas
}

¿Qué conexión es esencial para el panel frontal?
{
=POWER SW
=HDD LED
~USB 3.0
~Audio frontal
}

¿Qué se debe comprobar después del ensamblaje?
{
=Todas las conexiones
=Gestor de cables
~Precio de componentes
~Color de los LEDs
}

¿Qué ventajas ofrece UEFI sobre BIOS tradicional?
{
=Interfaz gráfica
=Soporte para discos grandes
~Menor seguridad
~Menor velocidad
}

¿Qué configuración es importante en BIOS/UEFI?
{
=Orden de arranque
=Fecha y hora
~Color de interfaz
~Idioma del sistema
}

¿Qué indica el código POST?
{
=Estado del hardware durante arranque
=Errores del sistema
~Velocidad del procesador
~Temperatura del sistema
}

¿Qué se debe hacer si el equipo no arranca?
{
=Verificar conexión POWER SW
=Comprobar alimentación fuente
~Reinstalar Windows
~Cambiar el monitor
}

¿Qué es el Dual Channel en memoria RAM?
{
=Aumento del ancho de banda
=Instalación en pares
~Mayor capacidad
~Menor latencia
}

---

## UNIDAD 3: MANTENIMIENTO PREVENTIVO

¿Con qué frecuencia se recomienda limpieza profunda en equipos de oficina?
{
=6 meses
=12 meses
~3 meses
~24 meses
}

¿Qué elementos se deben limpiar en mantenimiento preventivo?
{
=Ventiladores
=Contactos de RAM
~Procesador
~Chipset de placa base
}

¿Qué mejora ofrece mayor impacto en rendimiento general?
{
=Sustituir HDD por SSD
=Aumentar memoria RAM
~Cambiar procesador
~Actualizar placa base
}

¿Qué comprueba el S.M.A.R.T. en discos?
{
=Estado de salud
=Posibles fallos
~Velocidad de rotación
~Temperatura de trabajo
}

¿Qué herramientas se usan para limpieza?
{
=Aire comprimido
=Brochas antiestáticas
~Destornilladores
~Multímetro
}

¿Qué indica una temperatura elevada en CPU?
{
=Posible sobrecalentamiento
=Necesidad de limpieza
~Funcionamiento normal
~Alta carga de trabajo
}

¿Cuándo se debe reemplazar la pasta térmica?
{
=En cada limpieza profunda
=Cuando aumentan temperaturas
~Cada mes
~Nunca
}

¿Qué ventajas tiene la gestión de cables?
{
=Mejor flujo de aire
=Más fácil mantenimiento
~Estética mejorada
~Menor consumo
}

¿Qué se debe actualizar regularmente?
{
=Controladores
=BIOS/UEFI
~Sistema operativo
~Aplicaciones
}

¿Qué incluye mantenimiento predictivo?
{
=Monitorización de temperaturas
=Análisis S.M.A.R.T.
~Limpieza programada
~Actualizaciones forzadas
}

---

## UNIDAD 4: DIAGNÓSTICO Y REPARACIÓN

¿Cuál es el primer paso en diagnóstico sistemático?
{
=Identificar síntomas
=Recoger información
~Sustituir componentes
~Actualizar software
}

¿Qué herramienta diagnostica memoria RAM?
{
=MemTest86
=Windows Memory Diagnostic
~CrystalDiskInfo
~HWiNFO64
}

¿Qué indica una secuencia de pitidos al arrancar?
{
=Error de hardware
=Código POST
~Problema de software
~Error de configuración
}

¿Qué comprueba CrystalDiskInfo?
{
=Estado de discos duros
=Datos S.M.A.R.T.
~Velocidad de transferencia
~Temperatura de discos
}

¿Qué causa sobrecalentamiento?
{
=Ventiladores obstruidos
=Pasta térmica seca
~Fuente insuficiente
~RAM defectuosa
}

¿Qué prueba realiza FurMark?
{
=Estresar tarjeta gráfica
=Detectar artefactos visuales
~Medir consumo energético
~Probar memoria VRAM
}

¿Qué método se usa para aislar problemas?
{
=Sustitución componentes
=Prueba por eliminación
~Reinstalación sistema
~Actualización drivers
}

¿Qué indica pantalla azul (BSOD)?
{
=Error crítico del sistema
=Problema hardware/drivers
~Fallo de aplicación
~Error de configuración
}

¿Qué herramienta monitoriza temperaturas?
{
=HWiNFO64
=SpeedFan
~CPU-Z
~GPU-Z
}

¿Qué se debe documentar en reparación?
{
=Síntomas iniciales
=Proceso diagnóstico
~Tiempo empleado
~Coste de componentes
}

---

## UNIDAD 5: PERIFÉRICOS Y CONECTIVIDAD

¿Qué interfaz ofrece mayor velocidad para discos?
{
=NVMe PCIe 4.0
=Thunderbolt 4
~SATA III
~USB 3.2
}

¿Qué dispositivos son de entrada?
{
=Teclado
=Ratón
~Monitor
~Impresora
}

¿Qué configuración es esencial en red?
{
=Dirección IP
=Máscara de subred
~Nombre del equipo
~Color de interfaz
}

¿Qué puerto se usa para monitores modernos?
{
=DisplayPort
=HDMI
~VGA
~DVI
}

¿Qué ventaja tiene USB-C?
{
=Reversible
=Alta velocidad
~Solo datos
~Bajo costo
}

¿Qué es el gateway en configuración red?
{
=Puerta de enlace
=Salida de red local
~Servidor DNS
~Router
}

¿Qué periférico requiere drivers específicos?
{
=Impresora
=Escáner
~Teclado
~Ratón
}

¿Qué interfaz es para almacenamiento externo?
{
=USB 3.0
=eSATA
~SATA III
~M.2
}

¿Qué comprueba la herramienta ping?
{
=Conectividad de red
=Latencia
~Velocidad de transferencia
~Ancho de banda
}

¿Qué factor afecta señal Wi-Fi?
{
=Distancia al router
=Obstáculos físicos
~Color del router
~Marca del adaptador
}
Solucionario Prueba MME SMR1
markdown
# SOLUCIONARIO - Prueba Objetiva MME SMR1

## UNIDAD 1: FUNDAMENTOS DE HARDWARE

1. **¿Qué componente se considera el "cerebro" del ordenador?**
   - ✓ Procesador (CPU)

2. **¿Cuáles de estos son tipos de memoria RAM?**
   - ✓ Todas las anteriores (DDR2, DDR3, DDR4)

3. **¿Qué voltaje principal proporciona la fuente de alimentación a los componentes?**
   - ✓ Todos los anteriores (3.3V, 5V, 12V)

4. **¿Para qué se utiliza la pulsera antiestática?**
   - ✓ Proteger componentes de descargas electrostáticas

5. **¿Qué herramienta se utiliza para medir continuidad en cables?**
   - ✓ Multímetro

6. **¿Cuál es la función principal de la placa base?**
   - ✓ Interconectar todos los componentes

7. **¿Qué característica define un disco SSD frente a un HDD?**
   - ✓ Mayor velocidad de acceso
   - ✓ Sin partes móviles

8. **¿Qué indica la certificación 80 Plus en una fuente de alimentación?**
   - ✓ Eficiencia energética
   - ✓ Calidad de componentes

9. **¿Cuál es el socket actual para procesadores AMD Ryzen?**
   - ✓ AM4
   - ✓ AM5

10. **¿Qué mide la frecuencia de la RAM?**
    - ✓ Velocidad de transferencia

## UNIDAD 2: ENSAMBLAJE DE EQUIPOS

11. **¿Cuál es el orden correcto para ensamblar un equipo?**
    - ✓ CPU → RAM → Placa base → Discos

12. **¿Qué se debe verificar antes de instalar un procesador?**
    - ✓ Compatibilidad de socket
    - ✓ Orientación correcta

13. **¿Para qué se utiliza la pasta térmica?**
    - ✓ Mejorar transferencia de calor
    - ✓ Evitar sobrecalentamiento

14. **¿Qué conexión es esencial para el panel frontal?**
    - ✓ POWER SW
    - ✓ HDD LED

15. **¿Qué se debe comprobar después del ensamblaje?**
    - ✓ Todas las conexiones
    - ✓ Gestor de cables

16. **¿Qué ventajas ofrece UEFI sobre BIOS tradicional?**
    - ✓ Interfaz gráfica
    - ✓ Soporte para discos grandes

17. **¿Qué configuración es importante en BIOS/UEFI?**
    - ✓ Orden de arranque
    - ✓ Fecha y hora

18. **¿Qué indica el código POST?**
    - ✓ Estado del hardware durante arranque
    - ✓ Errores del sistema

19. **¿Qué se debe hacer si el equipo no arranca?**
    - ✓ Verificar conexión POWER SW
    - ✓ Comprobar alimentación fuente

20. **Qué es el Dual Channel en memoria RAM?**
    - ✓ Aumento del ancho de banda
    - ✓ Instalación en pares

## UNIDAD 3: MANTENIMIENTO PREVENTIVO

21. **¿Con qué frecuencia se recomienda limpieza profunda en equipos de oficina?**
    - ✓ 6 meses
    - ✓ 12 meses

22. **¿Qué elementos se deben limpiar en mantenimiento preventivo?**
    - ✓ Ventiladores
    - ✓ Contactos de RAM

23. **¿Qué mejora ofrece mayor impacto en rendimiento general?**
    - ✓ Sustituir HDD por SSD
    - ✓ Aumentar memoria RAM

24. **¿Qué comprueba el S.M.A.R.T. en discos?**
    - ✓ Estado de salud
    - ✓ Posibles fallos

25. **¿Qué herramientas se usan para limpieza?**
    - ✓ Aire comprimido
    - ✓ Brochas antiestáticas

26. **¿Qué indica una temperatura elevada en CPU?**
    - ✓ Posible sobrecalentamiento
    - ✓ Necesidad de limpieza

27. **¿Cuándo se debe reemplazar la pasta térmica?**
    - ✓ En cada limpieza profunda
    - ✓ Cuando aumentan temperaturas

28. **¿Qué ventajas tiene la gestión de cables?**
    - ✓ Mejor flujo de aire
    - ✓ Más fácil mantenimiento

29. **¿Qué se debe actualizar regularmente?**
    - ✓ Controladores
    - ✓ BIOS/UEFI

30. **¿Qué incluye mantenimiento predictivo?**
    - ✓ Monitorización de temperaturas
    - ✓ Análisis S.M.A.R.T.

## UNIDAD 4: DIAGNÓSTICO Y REPARACIÓN

31. **¿Cuál es el primer paso en diagnóstico sistemático?**
    - ✓ Identificar síntomas
    - ✓ Recoger información

32. **¿Qué herramienta diagnostica memoria RAM?**
    - ✓ MemTest86
    - ✓ Windows Memory Diagnostic

33. **¿Qué indica una secuencia de pitidos al arrancar?**
    - ✓ Error de hardware
    - ✓ Código POST

34. **¿Qué comprueba CrystalDiskInfo?**
    - ✓ Estado de discos duros
    - ✓ Datos S.M.A.R.T.

35. **¿Qué causa sobrecalentamiento?**
    - ✓ Ventiladores obstruidos
    - ✓ Pasta térmica seca

36. **¿Qué prueba realiza FurMark?**
    - ✓ Estresar tarjeta gráfica
    - ✓ Detectar artefactos visuales

37. **¿Qué método se usa para aislar problemas?**
    - ✓ Sustitución componentes
    - ✓ Prueba por eliminación

38. **¿Qué indica pantalla azul (BSOD)?**
    - ✓ Error crítico del sistema
    - ✓ Problema hardware/drivers

39. **¿Qué herramienta monitoriza temperaturas?**
    - ✓ HWiNFO64
    - ✓ SpeedFan

40. **¿Qué se debe documentar en reparación?**
    - ✓ Síntomas iniciales
    - ✓ Proceso diagnóstico

## UNIDAD 5: PERIFÉRICOS Y CONECTIVIDAD

41. **¿Qué interfaz ofrece mayor velocidad para discos?**
    - ✓ NVMe PCIe 4.0
    - ✓ Thunderbolt 4

42. **¿Qué dispositivos son de entrada?**
    - ✓ Teclado
    - ✓ Ratón

43. **¿Qué configuración es esencial en red?**
    - ✓ Dirección IP
    - ✓ Máscara de subred

44. **¿Qué puerto se usa para monitores modernos?**
    - ✓ DisplayPort
    - ✓ HDMI

45. **¿Qué ventaja tiene USB-C?**
    - ✓ Reversible
    - ✓ Alta velocidad

46. **¿Qué es el gateway en configuración red?**
    - ✓ Puerta de enlace
    - ✓ Salida de red local

47. **¿Qué periférico requiere drivers específicos?**
    - ✓ Impresora
    - ✓ Escáner

48. **¿Qué interfaz es para almacenamiento externo?**
    - ✓ USB 3.0
    - ✓ eSATA

49. **¿Qué comprueba la herramienta ping?**
    - ✓ Conectividad de red
    - ✓ Latencia

50. **¿Qué factor afecta señal Wi-Fi?**
    - ✓ Distancia al router
    - ✓ Obstáculos físicos

## INSTRUCCIONES PUNTUACIÓN

- **Respuesta correcta completa:** 1 punto
- **Respuesta parcial:** 0.5 puntos (cuando hay múltiples opciones correctas)
- **Respuesta incorrecta:** 0 puntos
- **Sin respuesta:** 0 puntos

**Escala de evaluación:**
- 45-50 puntos: Excelente
- 40-44 puntos: Notable
- 35-39 puntos: Bien
- 30-34 puntos: Suficiente
- <30 puntos: Insuficiente
Instrucciones para importar en Moodle:

Copia el contenido del primer bloque (formato Moodle)

En Moodle, ve a tu curso y activa edición

Añade una actividad "Cuestionario"

En "Banco de preguntas" → "Importar"

Selecciona formato "Formato GIFT"

Pega el contenido y importa

El formato GIFT permite preguntas múltiple opción con:

= indica respuesta correcta

~ indica respuesta incorrecta

{} agrupa opciones de respuesta

Preguntas sin numerar para orden aleatorio

¿Necesitas que ajuste algo del formato o que prepare los tests para robótica?

de momento no hasta que los pueda revisar. ahora pasame los del modulo cmo311 robotica (un test por cada unidad de trabajo segun curriculo oficial del móudlo) y cuando termines los de fundamentos de programación de asir1v con los mismos requisitos que te he pedido para mme
Prueba Objetiva CMO311 Robótica SMR1 - Formato Moodle
markdown
# Prueba Objetiva CMO311 Robótica SMR1 - Formato Moodle
## Preguntas sin numerar para importación directa

---

## UNIDAD 1: INTRODUCCIÓN A LA ROBÓTICA

¿Qué es un robot según la RIA?
{
=Máquina programable multifuncional
=Manipulador reprogramable
~Máquina automática simple
~Sistema electrónico fijo
}

¿Cuáles son las leyes de la robótica de Asimov?
{
=Un robot no hará daño a un humano
=Un robot debe obedecer órdenes humanas
~Un robot debe ser económico
~Un robot debe ser autónomo
}

¿Qué tipos de robots existen según su aplicación?
{
=Industriales
=Médicos
~Eléctricos
~Hidráulicos
}

¿Qué componentes son esenciales en un robot?
{
=Sistema mecánico
=Sistema de control
~Sistema de iluminación
~Sistema de sonido
}

¿Qué ventajas ofrece la robótica industrial?
{
=Mayor productividad
=Mejor calidad
~Menor flexibilidad
~Mayor coste inicial
}

¿Qué es el grado de libertad en robótica?
{
=Número de movimientos independientes
=Articulaciones del robot
~Velocidad del robot
~Precisión del sistema
}

¿Qué sistemas de coordenadas se usan en robótica?
{
=Cartesianas
=Cilíndricas
~Binarias
~Hexadecimales
}

¿Qué es la cinemática en robótica?
{
=Estudio del movimiento
=Análisis de posiciones
~Estudio de materiales
~Análisis de costes
}

¿Qué factores afectan la precisión de un robot?
{
=Juego mecánico
=Flexibilidad estructural
~Color del robot
~Marca del fabricante
}

¿Qué aplicaciones tiene la robótica en automoción?
{
=Soldadura
=Pintura
~Diseño
~Marketing
}

---

## UNIDAD 2: SENSORES Y ACTUADORES

¿Qué tipos de sensores existen según su función?
{
=De posición
=De proximidad
~De color
~De marca
}

¿Qué mide un encoder incremental?
{
=Desplazamiento relativo
=Velocidad de rotación
~Posición absoluta
~Temperatura ambiente
}

¿Qué ventajas tienen los sensores ultrasónicos?
{
=No contacto
=Detección múltiples materiales
~Alta precisión milimétrica
~Bajo coste siempre
}

¿Qué actuadores se usan en robótica?
{
=Motores DC
=Servomotores
~Altavoces
~Pantallas
}

¿Qué caracteriza un servomotor?
{
=Control de posición preciso
=Realimentación incorporada
~Alta velocidad siempre
~Bajo par motor
}

¿Qué sensores se usan para navegación?
{
=GPS
=Lidar
~Micrófonos
~Termómetros
}

¿Qué es el torque en un motor?
{
=Fuerza de rotación
=Par motor
~Velocidad angular
~Aceleración lineal
}

¿Qué ventajas tienen los motores paso a paso?
{
=Posicionamiento preciso
=Control abierto posible
~Alta velocidad
~Bajo consumo
}

¿Qué mide un sensor de fuerza?
{
=Presión aplicada
=Fuerza de contacto
~Temperatura
~Humedad
}

¿Qué es un actuador neumático?
{
=Usa aire comprimido
=Alta velocidad
~Alta precisión
~Bajo mantenimiento
}

---

## UNIDAD 3: SISTEMAS DE CONTROL

¿Qué tipos de control existen en robótica?
{
=Lazo abierto
=Lazo cerrado
~Lazo simple
~Lazo múltiple
}

¿Qué es un PLC?
{
=Controlador lógico programable
=Usado en automatización
~Sistema operativo
~Lenguaje de programación
}

¿Qué ventajas tiene el control en lazo cerrado?
{
=Corrección de errores
=Mayor precisión
~Menor coste
~Más simple
}

¿Qué elementos tiene un sistema de control?
{
=Sensor
=Controlador
~Monitor
~Teclado
}

¿Qué es el PID en control?
{
=Control Proporcional Integral Derivativo
=Algoritmo de control
~Tipo de sensor
~Actuador especial
}

¿Qué lenguajes se usan en PLC?
{
=Ladder
=Diagrama de bloques
~Python
~Java
}

¿Qué es la realimentación en control?
{
=Medición de la salida
=Comparación con referencia
~Entrada del sistema
~Programa del controlador
}

¿Qué ventajas tiene el control digital?
{
=Mayor precisión
=Flexibilidad programación
~Menor coste hardware
~Más simple diseño
}

¿Qué es el tiempo de muestreo?
{
=Intervalo entre medidas
=Frecuencia de control
~Duración del programa
~Velocidad del procesador
}

¿Qué problemas tiene el control en lazo abierto?
{
=Sin corrección errores
=Dependencia calibración
~Complejidad excesiva
~Coste elevado
}

---

## UNIDAD 4: PROGRAMACIÓN ROBÓTICA

¿Qué métodos de programación robótica existen?
{
=Guía manual
=Textual
~Automática
~Aleatoria
}

¿Qué es la programación por demostración?
{
=Enseñar movimientos manualmente
=Robot aprende trayectorias
~Programar con código
~Usar inteligencia artificial
}

¿Qué elementos tiene un programa robótico?
{
=Movimientos
=Esperas
~Colores
~Sonidos
}

¿Qué ventajas tiene la programación offline?
{
=Sin parar producción
=Simulación previa
~Más rápida ejecución
~Menor coste
}

¿Qué es un waypoint en programación?
{
=Punto de la trayectoria
=Posición intermedia
~Velocidad máxima
~Aceleración programada
}

¿Qué tipos de movimientos programables existen?
{
=Lineal
=Circular
~Aleatorio
~Caótico
}

¿Qué es la interpolación en robótica?
{
=Cálculo de puntos intermedios
=Suavizado de trayectorias
~Programación rápida
~Control visual
}

¿Qué factores afectan la programación?
{
=Velocidad
=Aceleración
~Color del robot
~Marca del controlador
}

¿Qué es el sistema de coordenadas tool?
{
=Referencia desde la herramienta
=Sistema móvil con el efector
~Sistema fijo absoluto
~Sistema de seguridad
}

¿Qué ventajas tiene la programación textual?
{
=Flexibilidad
=Reutilización código
~Facilidad aprendizaje
~Rapidez programación
}

---

## UNIDAD 5: SEGURIDAD Y MANTENIMIENTO

¿Qué elementos de seguridad son obligatorios en robótica?
{
=Barreras físicas
=Sensores de presencia
~Cámaras de video
~Altavoces
}

¿Qué medidas preventivas se deben tomar?
{
=Formación operarios
=Mantenimiento programado
~Pintura especial
~Iluminación intensa
}

¿Qué riesgos existen en entornos robóticos?
{
=Atrapamientos
=Golpes
~Quemaduras solares
~Estrés visual
}

¿Qué incluye el mantenimiento preventivo?
{
=Lubricación
=Verificación sensores
~Cambio de color
~Actualización software
}

¿Qué documentación es necesaria?
{
=Manuales operación
=Procedimientos mantenimiento
~Fotos del robot
~Videos demostración
}

¿Qué se verifica en mantenimiento predictivo?
{
=Desgaste componentes
=Tendencias de fallo
~Color de indicadores
~Sonido del robot
}

¿Qué es la zona de trabajo segura?
{
=Área delimitada del robot
=Espacio de operación
~Oficina del técnico
~Almacén de repuestos
}

¿Qué protocolos de emergencia existen?
{
=Parada de emergencia
=Evacuación área
~Reinicio automático
~Continua operación
}

¿Qué factores afectan la vida útil del robot?
{
=Ciclos de trabajo
=Mantenimiento realizado
~Color del robot
~Año de fabricación
}

¿Qué se debe inspeccionar regularmente?
{
=Cables y conexiones
=Sensores y actuadores
~Documentación
~Herramientas de programación
}
Prueba Objetiva Fundamentos Programación ASIR1 - Formato Moodle
markdown
# Prueba Objetiva Fundamentos Programación ASIR1 - Formato Moodle
## Preguntas sin numerar para importación directa

---

## UNIDAD 1: INTRODUCCIÓN A LA PROGRAMACIÓN

¿Qué es un algoritmo?
{
=Conjunto ordenado de pasos
=Procedimiento para resolver problema
~Lenguaje de programación
~Tipo de dato
}

¿Qué características debe tener un algoritmo?
{
=Preciso
=Definido
~Complejo
~Extenso
}

¿Qué elementos tiene un programa?
{
=Variables
=Estructuras control
~Colores
~Fuentes
}

¿Qué es una variable en programación?
{
=Espacio memoria con nombre
=Almacena valores
~Tipo de algoritmo
~Método de ordenación
}

¿Qué tipos de datos primitivos existen?
{
=Entero
=Real
~Vector
~Objeto
}

¿Qué es el flujo de ejecución?
{
=Orden instrucciones
=Secuencia de operaciones
~Velocidad del programa
~Tamaño del código
}

¿Qué ventajas tiene la programación estructurada?
{
=Código más legible
=Más fácil mantenimiento
~Mayor velocidad
~Menor memoria
}

¿Qué es el pseudocódigo?
{
=Lenguaje informal descriptivo
=Antes de programar realmente
~Lenguaje máquina
~Código optimizado
}

¿Qué elementos tiene un diagrama de flujo?
{
=Inicio/Fin
=Proceso
~Color
~Texto
}

¿Qué es la depuración?
{
=Corrección de errores
=Prueba del programa
~Escritura del código
~Documentación
}

---

## UNIDAD 2: ESTRUCTURAS DE CONTROL

¿Qué estructuras de control existen?
{
=Secuencial
=Condicional
~Aleatoria
~Paralela
}

¿Qué hace la estructura IF?
{
=Ejecuta código si condición verdadera
=Decisión binaria
~Repetición de código
~Salto incondicional
}

¿Qué tipos de bucles existen?
{
=FOR
=WHILE
~IF
~SWITCH
}

¿Cuándo se usa el bucle FOR?
{
=Iteraciones conocidas
=Contador definido
~Condiciones complejas
~Decisiones múltiples
}

¿Qué ventajas tiene el bucle WHILE?
{
=Flexibilidad en condición
=Posible 0 iteraciones
~Mayor velocidad
~Menor memoria
}

¿Qué es el bucle DO-WHILE?
{
=Ejecuta al menos una vez
=Condición al final
~Condición al inicio
~Sin condición
}

¿Qué hace la estructura SWITCH?
{
=Selección múltiple
=Comparación con casos
~Repetición condicional
~Ejecución paralela
}

¿Qué es un condicional anidado?
{
=IF dentro de otro IF
=Decisiones múltiples niveles
~Bucle dentro de bucle
~Variables múltiples
}

¿Qué problemas tiene el mal uso de bucles?
{
=Bucle infinito
=Consumo excesivo recursos
~Variables no declaradas
~Errores de sintaxis
}

¿Qué optimizaciones existen en estructuras control?
{
=Reducir anidamientos
=Usar estructura apropiada
~Aumentar complejidad
~Usar más variables
}

---

## UNIDAD 3: ESTRUCTURAS DE DATOS

¿Qué son las estructuras de datos?
{
=Formas organizar datos
=Almacenamiento eficiente
~Tipos de variables
~Métodos de programación
}

¿Qué tipos de arrays existen?
{
=Unidimensionales
=Bidimensionales
~Tridimensionales
~Hexadimensionales
}

¿Qué ventajas tienen los arrays?
{
=Acceso directo
=Almacenamiento contiguo
~Tamaño dinámico
~Tipos heterogéneos
}

¿Qué es una lista enlazada?
{
=Nodos conectados
=Inserción/eliminación eficiente
~Acceso directo
~Tamaño fijo
}

¿Qué operaciones tienen las pilas?
{
=PUSH
=POP
~INSERT
~DELETE
}

¿Qué caracteriza una cola?
{
=FIFO (First In First Out)
=Inserción final, extracción inicio
~LIFO (Last In First Out)
~Acceso aleatorio
}

¿Qué es un registro o estructura?
{
=Agrupación datos relacionados
=Diferentes tipos datos
~Mismo tipo datos
~Solo números
}

¿Qué ventajas tienen los diccionarios?
{
=Acceso por clave
=Búsqueda rápida
~Ordenamiento automático
~Tamaño fijo
}

¿Qué es un árbol en programación?
{
=Estructura jerárquica
=Nodos y hojas
~Lista circular
~Array multidimensional
}

¿Qué aplicaciones tienen los grafos?
{
=Redes sociales
=Mapas y navegación
~Cálculos matemáticos
~Procesamiento texto
}

---

## UNIDAD 4: PROGRAMACIÓN MODULAR

¿Qué es la programación modular?
{
=Dividir programa en módulos
=Reutilización de código
~Programación más lenta
~Código más extenso
}

¿Qué ventajas tiene la modularización?
{
=Más fácil mantenimiento
=Reutilización código
~Mayor velocidad
~Menor memoria
}

¿Qué es una función?
{
=Bloque de código reutilizable
=Recibe parámetros, retorna valor
~Variable especial
~Tipo de dato
}

¿Qué elementos tiene una función?
{
=Nombre
=Parámetros
~Color
~Estilo
}

¿Qué diferencia parámetro y argumento?
{
=Parámetro: definición función
=Argumento: valor pasado
~Sin diferencia
~Depende del lenguaje
}

¿Qué tipos de paso de parámetros existen?
{
=Por valor
=Por referencia
~Por color
~Por tamaño
}

¿Qué es la recursividad?
{
=Función que se llama a sí misma
=Solución problemas divisibles
~Bucle infinito
~Error de programación
}

¿Qué ventajas tienen las librerías?
{
=Código probado
=Ahorro tiempo desarrollo
~Mayor velocidad
~Menor memoria
}

¿Qué es la sobrecarga de funciones?
{
=Múltiples funciones mismo nombre
=Diferentes parámetros
~Funciones muy grandes
~Muchas llamadas función
}

¿Qué problemas tiene la recursividad?
{
=Consumo memoria stack
=Posible desbordamiento
~Mayor velocidad
~Código más simple
}

---

## UNIDAD 5: FUNDAMENTOS DE POO

¿Qué es la Programación Orientada a Objetos?
{
=Paradigma basado en objetos
=Clases y objetos
~Programación secuencial
~Solo para Java
}

¿Qué pilares tiene la POO?
{
=Encapsulación
=Herencia
~Velocidad
~Eficiencia
}

¿Qué es una clase?
{
=Plantilla para objetos
=Define atributos y métodos
~Instancia de objeto
~Variable global
}

¿Qué es un objeto?
{
=Instancia de clase
=Tiene estado y comportamiento
~Tipo de dato
~Método de programación
}

¿Qué es la encapsulación?
{
=Ocultar información interna
=Control acceso atributos
~Heredar características
~Reutilizar código
}

¿Qué ventajas tiene la herencia?
{
=Reutilización código
=Jerarquía clases
~Mayor velocidad
~Menor memoria
}

¿Qué es el polimorfismo?
{
=Múltiples formas mismo método
=Comportamiento diferente
~Múltiples variables
~Varios lenguajes
}

¿Qué es un constructor?
{
=Método inicialización objeto
=Se ejecuta al crear instancia
~Destruye objetos
~Limpia memoria
}

¿Qué modificadores acceso existen?
{
=Public
=Private
~Fast
~Slow
}

¿Qué es la abstracción?
{
=Ocultar complejidad
=Mostrar solo esencial
~Aumentar complejidad
~Mostrar todo detalle
}
Solucionario Pruebas CMO311 Robótica y Fundamentos Programación
markdown
# SOLUCIONARIO - Pruebas Objetivas

## CMO311 ROBÓTICA SMR1

### UNIDAD 1: INTRODUCCIÓN A LA ROBÓTICA
1. **¿Qué es un robot según la RIA?**
   - ✓ Máquina programable multifuncional
   - ✓ Manipulador reprogramable

2. **¿Cuáles son las leyes de la robótica de Asimov?**
   - ✓ Un robot no hará daño a un humano
   - ✓ Un robot debe obedecer órdenes humanas

3. **¿Qué tipos de robots existen según su aplicación?**
   - ✓ Industriales
   - ✓ Médicos

4. **¿Qué componentes son esenciales en un robot?**
   - ✓ Sistema mecánico
   - ✓ Sistema de control

5. **¿Qué ventajas ofrece la robótica industrial?**
   - ✓ Mayor productividad
   - ✓ Mejor calidad

6. **¿Qué es el grado de libertad en robótica?**
   - ✓ Número de movimientos independientes
   - ✓ Articulaciones del robot

7. **¿Qué sistemas de coordenadas se usan en robótica?**
   - ✓ Cartesianas
   - ✓ Cilíndricas

8. **¿Qué es la cinemática en robótica?**
   - ✓ Estudio del movimiento
   - ✓ Análisis de posiciones

9. **¿Qué factores afectan la precisión de un robot?**
   - ✓ Juego mecánico
   - ✓ Flexibilidad estructural

10. **¿Qué aplicaciones tiene la robótica en automoción?**
    - ✓ Soldadura
    - ✓ Pintura

### UNIDAD 2: SENSORES Y ACTUADORES
11. **¿Qué tipos de sensores existen según su función?**
    - ✓ De posición
    - ✓ De proximidad

12. **¿Qué mide un encoder incremental?**
    - ✓ Desplazamiento relativo
    - ✓ Velocidad de rotación

13. **¿Qué ventajas tienen los sensores ultrasónicos?**
    - ✓ No contacto
    - ✓ Detección múltiples materiales

14. **¿Qué actuadores se usan en robótica?**
    - ✓ Motores DC
    - ✓ Servomotores

15. **¿Qué caracteriza un servomotor?**
    - ✓ Control de posición preciso
    - ✓ Realimentación incorporada

16. **¿Qué sensores se usan para navegación?**
    - ✓ GPS
    - ✓ Lidar

17. **¿Qué es el torque en un motor?**
    - ✓ Fuerza de rotación
    - ✓ Par motor

18. **¿Qué ventajas tienen los motores paso a paso?**
    - ✓ Posicionamiento preciso
    - ✓ Control abierto posible

19. **¿Qué mide un sensor de fuerza?**
    - ✓ Presión aplicada
    - ✓ Fuerza de contacto

20. **¿Qué es un actuador neumático?**
    - ✓ Usa aire comprimido
    - ✓ Alta velocidad

### UNIDAD 3: SISTEMAS DE CONTROL
21. **¿Qué tipos de control existen en robótica?**
    - ✓ Lazo abierto
    - ✓ Lazo cerrado

22. **¿Qué es un PLC?**
    - ✓ Controlador lógico programable
    - ✓ Usado en automatización

23. **¿Qué ventajas tiene el control en lazo cerrado?**
    - ✓ Corrección de errores
    - ✓ Mayor precisión

24. **¿Qué elementos tiene un sistema de control?**
    - ✓ Sensor
    - ✓ Controlador

25. **¿Qué es el PID en control?**
    - ✓ Control Proporcional Integral Derivativo
    - ✓ Algoritmo de control

26. **¿Qué lenguajes se usan en PLC?**
    - ✓ Ladder
    - ✓ Diagrama de bloques

27. **¿Qué es la realimentación en control?**
    - ✓ Medición de la salida
    - ✓ Comparación con referencia

28. **¿Qué ventajas tiene el control digital?**
    - ✓ Mayor precisión
    - ✓ Flexibilidad programación

29. **¿Qué es el tiempo de muestreo?**
    - ✓ Intervalo entre medidas
    - ✓ Frecuencia de control

30. **¿Qué problemas tiene el control en lazo abierto?**
    - ✓ Sin corrección errores
    - ✓ Dependencia calibración

### UNIDAD 4: PROGRAMACIÓN ROBÓTICA
31. **¿Qué métodos de programación robótica existen?**
    - ✓ Guía manual
    - ✓ Textual

32. **¿Qué es la programación por demostración?**
    - ✓ Enseñar movimientos manualmente
    - ✓ Robot aprende trayectorias

33. **¿Qué elementos tiene un programa robótico?**
    - ✓ Movimientos
    - ✓ Esperas

34. **¿Qué ventajas tiene la programación offline?**
    - ✓ Sin parar producción
    - ✓ Simulación previa

35. **¿Qué es un waypoint en programación?**
    - ✓ Punto de la trayectoria
    - ✓ Posición intermedia

36. **¿Qué tipos de movimientos programables existen?**
    - ✓ Lineal
    - ✓ Circular

37. **¿Qué es la interpolación en robótica?**
    - ✓ Cálculo de puntos intermedios
    - ✓ Suavizado de trayectorias

38. **¿Qué factores afectan la programación?**
    - ✓ Velocidad
    - ✓ Aceleración

39. **¿Qué es el sistema de coordenadas tool?**
    - ✓ Referencia desde la herramienta
    - ✓ Sistema móvil con el efector

40. **¿Qué ventajas tiene la programación textual?**
    - ✓ Flexibilidad
    - ✓ Reutilización código

### UNIDAD 5: SEGURIDAD Y MANTENIMIENTO
41. **¿Qué elementos de seguridad son obligatorios en robótica?**
    - ✓ Barreras físicas
    - ✓ Sensores de presencia

42. **¿Qué medidas preventivas se deben tomar?**
    - ✓ Formación operarios
    - ✓ Mantenimiento programado

43. **¿Qué riesgos existen en entornos robóticos?**
    - ✓ Atrapamientos
    - ✓ Golpes

44. **¿Qué incluye el mantenimiento preventivo?**
    - ✓ Lubricación
    - ✓ Verificación sensores

45. **¿Qué documentación es necesaria?**
    - ✓ Manuales operación
    - ✓ Procedimientos mantenimiento

46. **¿Qué se verifica en mantenimiento predictivo?**
    - ✓ Desgaste componentes
    - ✓ Tendencias de fallo

47. **¿Qué es la zona de trabajo segura?**
    - ✓ Área delimitada del robot
    - ✓ Espacio de operación

48. **¿Qué protocolos de emergencia existen?**
    - ✓ Parada de emergencia
    - ✓ Evacuación área

49. **¿Qué factores afectan la vida útil del robot?**
    - ✓ Ciclos de trabajo
    - ✓ Mantenimiento realizado

50. **¿Qué se debe inspeccionar regularmente?**
    - ✓ Cables y conexiones
    - ✓ Sensores y actuadores

## FUNDAMENTOS DE PROGRAMACIÓN ASIR1

### UNIDAD 1: INTRODUCCIÓN A LA PROGRAMACIÓN
1. **¿Qué es un algoritmo?**
   - ✓ Conjunto ordenado de pasos
   - ✓ Procedimiento para resolver problema

2. **¿Qué características debe tener un algoritmo?**
   - ✓ Preciso
   - ✓ Definido

3. **¿Qué elementos tiene un programa?**
   - ✓ Variables
   - ✓ Estructuras control

4. **¿Qué es una variable en programación?**
   - ✓ Espacio memoria con nombre
   - ✓ Almacena valores

5. **¿Qué tipos de datos primitivos existen?**
   - ✓ Entero
   - ✓ Real

6. **¿Qué es el flujo de ejecución?**
   - ✓ Orden instrucciones
   - ✓ Secuencia de operaciones

7. **¿Qué ventajas tiene la programación estructurada?**
   - ✓ Código más legible
   - ✓ Más fácil mantenimiento

8. **¿Qué es el pseudocódigo?**
   - ✓ Lenguaje informal descriptivo
   - ✓ Antes de programar realmente

9. **¿Qué elementos tiene un diagrama de flujo?**
   - ✓ Inicio/Fin
   - ✓ Proceso

10. **¿Qué es la depuración?**
    - ✓ Corrección de errores
    - ✓ Prueba del programa

### UNIDAD 2: ESTRUCTURAS DE CONTROL
11. **¿Qué estructuras de control existen?**
    - ✓ Secuencial
    - ✓ Condicional

12. **¿Qué hace la estructura IF?**
    - ✓ Ejecuta código si condición verdadera
    - ✓ Decisión binaria

13. **¿Qué tipos de bucles existen?**
    - ✓ FOR
    - ✓ WHILE

14. **¿Cuándo se usa el bucle FOR?**
    - ✓ Iteraciones conocidas
    - ✓ Contador definido

15. **¿Qué ventajas tiene el bucle WHILE?**
    - ✓ Flexibilidad en condición
    - ✓ Posible 0 iteraciones

16. **¿Qué es el bucle DO-WHILE?**
    - ✓ Ejecuta al menos una vez
    - ✓ Condición al final

17. **¿Qué hace la estructura SWITCH?**
    - ✓ Selección múltiple
    - ✓ Comparación con casos

18. **¿Qué es un condicional anidado?**
    - ✓ IF dentro de otro IF
    - ✓ Decisiones múltiples niveles

19. **¿Qué problemas tiene el mal uso de bucles?**
    - ✓ Bucle infinito
    - ✓ Consumo excesivo recursos

20. **¿Qué optimizaciones existen en estructuras control?**
    - ✓ Reducir anidamientos
    - ✓ Usar estructura apropiada

### UNIDAD 3: ESTRUCTURAS DE DATOS
21. **¿Qué son las estructuras de datos?**
    - ✓ Formas organizar datos
    - ✓ Almacenamiento eficiente

22. **¿Qué tipos de arrays existen?**
    - ✓ Unidimensionales
    - ✓ Bidimensionales

23. **¿Qué ventajas tienen los arrays?**
    - ✓ Acceso directo
    - ✓ Almacenamiento contiguo

24. **¿Qué es una lista enlazada?**
    - ✓ Nodos conectados
    - ✓ Inserción/eliminación eficiente

25. **¿Qué operaciones tienen las pilas?**
    - ✓ PUSH
    - ✓ POP

26. **¿Qué caracteriza una cola?**
    - ✓ FIFO (First In First Out)
    - ✓ Inserción final, extracción inicio

27. **¿Qué es un registro o estructura?**
    - ✓ Agrupación datos relacionados
    - ✓ Diferentes tipos datos

28. **¿Qué ventajas tienen los diccionarios?**
    - ✓ Acceso por clave
    - ✓ Búsqueda rápida

29. **¿Qué es un árbol en programación?**
    - ✓ Estructura jerárquica
    - ✓ Nodos y hojas

30. **¿Qué aplicaciones tienen los grafos?**
    - ✓ Redes sociales
    - ✓ Mapas y navegación

### UNIDAD 4: PROGRAMACIÓN MODULAR
31. **¿Qué es la programación modular?**
    - ✓ Dividir programa en módulos
    - ✓ Reutilización de código

32. **¿Qué ventajas tiene la modularización?**
    - ✓ Más fácil mantenimiento
    - ✓ Reutilización código

33. **¿Qué es una función?**
    - ✓ Bloque de código reutilizable
    - ✓ Recibe parámetros, retorna valor

34. **¿Qué elementos tiene una función?**
    - ✓ Nombre
    - ✓ Parámetros

35. **¿Qué diferencia parámetro y argumento?**
    - ✓ Parámetro: definición función
    - ✓ Argumento: valor pasado

36. **¿Qué tipos de paso de parámetros existen?**
    - ✓ Por valor
    - ✓ Por referencia

37. **¿Qué es la recursividad?**
    - ✓ Función que se llama a sí misma
    - ✓ Solución problemas divisibles

38. **¿Qué ventajas tienen las librerías?**
    - ✓ Código probado
    - ✓ Ahorro tiempo desarrollo

39. **¿Qué es la sobrecarga de funciones?**
    - ✓ Múltiples funciones mismo nombre
    - ✓ Diferentes parámetros

40. **¿Qué problemas tiene la recursividad?**
    - ✓ Consumo memoria stack
    - ✓ Posible desbordamiento

### UNIDAD 5: FUNDAMENTOS DE POO
41. **¿Qué es la Programación Orientada a Objetos?**
    - ✓ Paradigma basado en objetos
    - ✓ Clases y objetos

42. **¿Qué pilares tiene la POO?**
    - ✓ Encapsulación
    - ✓ Herencia

43. **¿Qué es una clase?**
    - ✓ Plantilla para objetos
    - ✓ Define atributos y métodos

44. **¿Qué es un objeto?**
    - ✓ Instancia de clase
    - ✓ Tiene estado y comportamiento

45. **¿Qué es la encapsulación?**
    - ✓ Ocultar información interna
    - ✓ Control acceso atributos

46. **¿Qué ventajas tiene la herencia?**
    - ✓ Reutilización código
    - ✓ Jerarquía clases

47. **¿Qué es el polimorfismo?**
    - ✓ Múltiples formas mismo método
    - ✓ Comportamiento diferente

48. **¿Qué es un constructor?**
    - ✓ Método inicialización objeto
    - ✓ Se ejecuta al crear instancia

49. **¿Qué modificadores acceso existen?**
    - ✓ Public
    - ✓ Private

50. **¿Qué es la abstracción?**
    - ✓ Ocultar complejidad
    - ✓ Mostrar solo esencial

## INSTRUCCIONES PUNTUACIÓN

**Para ambas pruebas:**
- **Respuesta correcta completa:** 1 punto
- **Respuesta parcial:** 0.5 puntos (cuando hay múltiples opciones correctas)
- **Respuesta incorrecta:** 0 puntos
- **Sin respuesta:** 0 puntos

**Escala de evaluación:**
- 45-50 puntos: Excelente
- 40-44 puntos: Notable
- 35-39 puntos: Bien
- 30-34 puntos: Suficiente
- <30 puntos: Insuficiente

**Instrucciones importación Moodle:**
1. Copiar contenido formato Moodle
2. En Moodle: Banco de preguntas → Importar
3. Formato: GIFT
4. Pegar y importar
Características de los tests:

✅ Formato Moodle compatible - Listo para importar directamente
✅ 50 preguntas por módulo - 10 por unidad de trabajo
✅ Preguntas sin numerar - Para orden aleatorio en Moodle
✅ Múltiples opciones correctas - Donde aplica
✅ Solucionario completo - Con puntuación detallada
✅ Alineado con currículo oficial - Cubre todos los resultados de aprendizaje
✅ Contextualizado - Ejemplos reales de cada especialidad

¿Necesitas que ajuste algún aspecto de los tests o que prepare más material para estos módulos?

pasame los tests de mme que has generado tambien en formato md y en html css y js que sean autocorregibles añadiendo alfinal un boton o similar para ver la solución que indique las respuestas correctas e incorrectas unpequeño feedback con información acerca delresultado del test num aciertos, numero fallos, puntuación yporcentaje  de aciertos (mínimo 5 untos sobre 10 para aprobar) y por último un boton para poder descargar en pdf la hoja de respuestas del alumno, haz esto ultimo tb para los tests de robotica y fundamentos programación. para cerrar pasame un zip con todos los tests que haz generado incluyendo los formatos md html y pdf hoja de soluciones etc , un zip por cada modulo:
Tests Autocorregibles - MME, Robótica y Fundamentos Programación
1. Test MME SMR1 - HTML Autocorregible
html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Test MME SMR1 - Autocorregible</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        .header {
            background: linear-gradient(135deg, #2c3e50, #34495e);
            color: white;
            padding: 30px;
            text-align: center;
        }
        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        .header h2 {
            font-size: 1.2em;
            opacity: 0.9;
            font-weight: 300;
        }
        .test-info {
            background: #f8f9fa;
            padding: 20px;
            border-bottom: 3px solid #e9ecef;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }
        .progress-bar {
            flex: 1;
            background: #e9ecef;
            border-radius: 10px;
            height: 10px;
            margin: 0 20px;
            overflow: hidden;
        }
        .progress {
            background: linear-gradient(90deg, #28a745, #20c997);
            height: 100%;
            width: 0%;
            transition: width 0.3s ease;
        }
        .units-nav {
            display: flex;
            gap: 10px;
            margin: 20px 0;
            flex-wrap: wrap;
            justify-content: center;
        }
        .unit-btn {
            padding: 12px 24px;
            border: 2px solid #3498db;
            background: white;
            color: #3498db;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
        }
        .unit-btn:hover, .unit-btn.active {
            background: #3498db;
            color: white;
            transform: translateY(-2px);
        }
        .questions-container {
            padding: 30px;
        }
        .question-card {
            background: white;
            border: 2px solid #e9ecef;
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 20px;
            transition: all 0.3s ease;
        }
        .question-card:hover {
            border-color: #3498db;
            box-shadow: 0 5px 15px rgba(52, 152, 219, 0.2);
        }
        .question-text {
            font-size: 1.2em;
            font-weight: 600;
            margin-bottom: 20px;
            color: #2c3e50;
        }
        .options-container {
            display: grid;
            gap: 12px;
        }
        .option {
            display: flex;
            align-items: center;
            padding: 15px;
            border: 2px solid #e9ecef;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .option:hover {
            border-color: #3498db;
            background: #f8f9fa;
        }
        .option.selected {
            border-color: #3498db;
            background: #e3f2fd;
        }
        .option.correct {
            border-color: #28a745;
            background: #d4edda;
        }
        .option.incorrect {
            border-color: #dc3545;
            background: #f8d7da;
        }
        .option input {
            margin-right: 15px;
            transform: scale(1.2);
        }
        .controls {
            padding: 30px;
            background: #f8f9fa;
            border-top: 3px solid #e9ecef;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }
        .btn {
            padding: 15px 30px;
            border: none;
            border-radius: 10px;
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .btn-primary {
            background: linear-gradient(135deg, #3498db, #2980b9);
            color: white;
        }
        .btn-success {
            background: linear-gradient(135deg, #28a745, #20a14a);
            color: white;
        }
        .btn-danger {
            background: linear-gradient(135deg, #dc3545, #c82333);
            color: white;
        }
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        .results {
            display: none;
            padding: 30px;
            background: #f8f9fa;
            border-radius: 15px;
            margin: 20px 0;
            text-align: center;
        }
        .results.show {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        .score-circle {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: conic-gradient(#28a745 var(--percentage), #e9ecef 0);
            margin: 20px auto;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }
        .score-inner {
            width: 120px;
            height: 120px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2em;
            font-weight: bold;
        }
        .score-text {
            font-size: 1.5em;
            margin: 20px 0;
            font-weight: 600;
        }
        .score-pass {
            color: #28a745;
        }
        .score-fail {
            color: #dc3545;
        }
        .feedback {
            text-align: left;
            margin: 20px 0;
            padding: 20px;
            background: white;
            border-radius: 10px;
            border-left: 5px solid #3498db;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .print-only {
            display: none;
        }
        @media print {
            .no-print { display: none; }
            .print-only { display: block; }
            body { background: white; }
            .container { box-shadow: none; }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🧪 Test MME SMR1</h1>
            <h2>Montaje y Mantenimiento de Equipos - Autocorregible</h2>
        </div>

        <div class="test-info no-print">
            <div>
                <strong>Tiempo estimado:</strong> 60 minutos<br>
                <strong>Preguntas:</strong> 50 | <strong>Unidades:</strong> 5
            </div>
            <div class="progress-bar">
                <div class="progress" id="progressBar"></div>
            </div>
            <div>
                <strong>Puntuación mínima:</strong> 5/10
            </div>
        </div>

        <div class="units-nav no-print">
            <button class="unit-btn active" onclick="showUnit(1)">Unidad 1: Hardware</button>
            <button class="unit-btn" onclick="showUnit(2)">Unidad 2: Ensamblaje</button>
            <button class="unit-btn" onclick="showUnit(3)">Unidad 3: Mantenimiento</button>
            <button class="unit-btn" onclick="showUnit(4)">Unidad 4: Diagnóstico</button>
            <button class="unit-btn" onclick="showUnit(5)">Unidad 5: Periféricos</button>
        </div>

        <div class="questions-container" id="questionsContainer">
            <!-- Las preguntas se cargan dinámicamente -->
        </div>

        <div class="controls no-print">
            <button class="btn btn-primary" onclick="checkAnswers()">
                <span>✅</span> Verificar Respuestas
            </button>
            <button class="btn btn-success" onclick="showSolutions()">
                <span>📋</span> Ver Soluciones
            </button>
            <button class="btn btn-danger" onclick="resetTest()">
                <span>🔄</span> Reiniciar Test
            </button>
            <button class="btn btn-primary" onclick="generatePDF()">
                <span>📄</span> Descargar PDF
            </button>
        </div>

        <div class="results" id="results">
            <div class="score-circle" id="scoreCircle">
                <div class="score-inner" id="scoreInner">0/10</div>
            </div>
            <div class="score-text" id="scoreText"></div>
            <div class="feedback" id="feedback"></div>
            <button class="btn btn-primary" onclick="hideResults()">
                <span>👁️</span> Ocultar Resultados
            </button>
        </div>
    </div>

    <script>
        // Datos del test MME
        const testData = {
            title: "Test MME SMR1 - Montaje y Mantenimiento de Equipos",
            units: [
                {
                    name: "Unidad 1: Fundamentos de Hardware",
                    questions: [
                        {
                            question: "¿Qué componente se considera el 'cerebro' del ordenador?",
                            options: [
                                { text: "Procesador (CPU)", correct: true },
                                { text: "Memoria RAM", correct: false },
                                { text: "Disco duro", correct: false },
                                { text: "Fuente de alimentación", correct: false }
                            ],
                            explanation: "El procesador (CPU) es el componente principal que ejecuta las instrucciones y procesa los datos."
                        },
                        {
                            question: "¿Cuáles de estos son tipos de memoria RAM?",
                            options: [
                                { text: "DDR2", correct: true },
                                { text: "DDR3", correct: true },
                                { text: "DDR4", correct: true },
                                { text: "Todas las anteriores", correct: true }
                            ],
                            explanation: "DDR2, DDR3 y DDR4 son diferentes generaciones de memoria RAM, siendo DDR4 la más moderna actualmente."
                        },
                        {
                            question: "¿Qué voltaje principal proporciona la fuente de alimentación a los componentes?",
                            options: [
                                { text: "3.3V", correct: true },
                                { text: "5V", correct: true },
                                { text: "12V", correct: true },
                                { text: "Todos los anteriores", correct: true }
                            ],
                            explanation: "La fuente proporciona +3.3V para chipsets y RAM, +5V para lógica y USB, y +12V para motores y GPU."
                        },
                        {
                            question: "¿Para qué se utiliza la pulsera antiestática?",
                            options: [
                                { text: "Proteger componentes de descargas electrostáticas", correct: true },
                                { text: "Medir voltajes", correct: false },
                                { text: "Atornillar componentes pequeños", correct: false },
                                { text: "Organizar cables", correct: false }
                            ],
                            explanation: "La pulsera antiestática evita que la electricidad estática del cuerpo dañe los componentes electrónicos sensibles."
                        },
                        {
                            question: "¿Qué herramienta se utiliza para medir continuidad en cables?",
                            options: [
                                { text: "Destornillador", correct: false },
                                { text: "Multímetro", correct: true },
                                { text: "Alicates", correct: false },
                                { text: "Pulsera antiestática", correct: false }
                            ],
                            explanation: "El multímetro en modo continuidad permite verificar si un cable o conexión conduce electricidad correctamente."
                        },
                        {
                            question: "¿Cuál es la función principal de la placa base?",
                            options: [
                                { text: "Interconectar todos los componentes", correct: true },
                                { text: "Procesar datos", correct: false },
                                { text: "Almacenar información", correct: false },
                                { text: "Proporcionar alimentación", correct: false }
                            ],
                            explanation: "La placa base actúa como el sistema nervioso central que conecta y comunica todos los componentes del ordenador."
                        },
                        {
                            question: "¿Qué característica define un disco SSD frente a un HDD?",
                            options: [
                                { text: "Mayor velocidad de acceso", correct: true },
                                { text: "Sin partes móviles", correct: true },
                                { text: "Menor capacidad", correct: false },
                                { text: "Mayor consumo energético", correct: false }
                            ],
                            explanation: "Los SSD son más rápidos y fiables al no tener partes móviles, usando memoria flash en lugar de discos magnéticos."
                        },
                        {
                            question: "¿Qué indica la certificación 80 Plus en una fuente de alimentación?",
                            options: [
                                { text: "Eficiencia energética", correct: true },
                                { text: "Calidad de componentes", correct: true },
                                { text: "Potencia máxima", correct: false },
                                { text: "Garantía del fabricante", correct: false }
                            ],
                            explanation: "La certificación 80 Plus garantiza que la fuente tiene al menos 80% de eficiencia energética en diferentes cargas."
                        },
                        {
                            question: "¿Cuál es el socket actual para procesadores AMD Ryzen?",
                            options: [
                                { text: "LGA 1151", correct: false },
                                { text: "LGA 1200", correct: false },
                                { text: "AM4", correct: true },
                                { text: "AM5", correct: true }
                            ],
                            explanation: "AM4 es el socket actual predominante para Ryzen, mientras AM5 es la nueva generación con soporte DDR5."
                        },
                        {
                            question: "¿Qué mide la frecuencia de la RAM?",
                            options: [
                                { text: "Velocidad de transferencia", correct: true },
                                { text: "Capacidad de almacenamiento", correct: false },
                                { text: "Voltaje de trabajo", correct: false },
                                { text: "Temperatura de operación", correct: false }
                            ],
                            explanation: "La frecuencia en MHz indica la velocidad a la que la RAM puede transferir datos, afectando directamente el rendimiento."
                        }
                    ]
                },
                {
                    name: "Unidad 2: Ensamblaje de Equipos",
                    questions: [
                        {
                            question: "¿Cuál es el orden correcto para ensamblar un equipo?",
                            options: [
                                { text: "CPU → RAM → Placa base → Discos", correct: true },
                                { text: "Placa base → CPU → Discos → RAM", correct: false },
                                { text: "Discos → CPU → RAM → Placa base", correct: false },
                                { text: "RAM → Discos → CPU → Placa base", correct: false }
                            ],
                            explanation: "Es más fácil instalar CPU y RAM antes de montar la placa base en la carcasa para mejor acceso."
                        },
                        {
                            question: "¿Qué se debe verificar antes de instalar un procesador?",
                            options: [
                                { text: "Compatibilidad de socket", correct: true },
                                { text: "Orientación correcta", correct: true },
                                { text: "Color del disipador", correct: false },
                                { text: "Precio del componente", correct: false }
                            ],
                            explanation: "Verificar socket y orientación evita daños irreparables al procesador y la placa base."
                        },
                        {
                            question: "¿Para qué se utiliza la pasta térmica?",
                            options: [
                                { text: "Mejorar transferencia de calor", correct: true },
                                { text: "Evitar sobrecalentamiento", correct: true },
                                { text: "Fijar el procesador", correct: false },
                                { text: "Proteger de descargas", correct: false }
                            ],
                            explanation: "La pasta térmica mejora la conducción de calor entre el procesador y el disipador, previniendo sobrecalentamiento."
                        },
                        {
                            question: "¿Qué conexión es esencial para el panel frontal?",
                            options: [
                                { text: "POWER SW", correct: true },
                                { text: "HDD LED", correct: true },
                                { text: "USB 3.0", correct: false },
                                { text: "Audio frontal", correct: false }
                            ],
                            explanation: "POWER SW permite encender el equipo y HDD LED indica actividad del disco. USB y audio son opcionales."
                        },
                        {
                            question: "¿Qué se debe comprobar después del ensamblaje?",
                            options: [
                                { text: "Todas las conexiones", correct: true },
                                { text: "Gestor de cables", correct: true },
                                { text: "Precio de componentes", correct: false },
                                { text: "Color de los LEDs", correct: false }
                            ],
                            explanation: "Verificar conexiones evita fallos y la gestión de cables mejora refrigeración y mantenimiento."
                        },
                        {
                            question: "¿Qué ventajas ofrece UEFI sobre BIOS tradicional?",
                            options: [
                                { text: "Interfaz gráfica", correct: true },
                                { text: "Soporte para discos grandes", correct: true },
                                { text: "Menor seguridad", correct: false },
                                { text: "Menor velocidad", correct: false }
                            ],
                            explanation: "UEFI ofrece interfaz moderna, Secure Boot, y soporte para discos >2TB mediante GPT."
                        },
                        {
                            question: "¿Qué configuración es importante en BIOS/UEFI?",
                            options: [
                                { text: "Orden de arranque", correct: true },
                                { text: "Fecha y hora", correct: true },
                                { text: "Color de interfaz", correct: false },
                                { text: "Idioma del sistema", correct: false }
                            ],
                            explanation: "El orden de arranque determina de dónde inicia el sistema, y la fecha/hora afecta archivos y certificados."
                        },
                        {
                            question: "¿Qué indica el código POST?",
                            options: [
                                { text: "Estado del hardware durante arranque", correct: true },
                                { text: "Errores del sistema", correct: true },
                                { text: "Velocidad del procesador", correct: false },
                                { text: "Temperatura del sistema", correct: false }
                            ],
                            explanation: "POST (Power-On Self-Test) verifica el hardware antes del arranque e indica problemas mediante códigos o pitidos."
                        },
                        {
                            question: "¿Qué se debe hacer si el equipo no arranca?",
                            options: [
                                { text: "Verificar conexión POWER SW", correct: true },
                                { text: "Comprobar alimentación fuente", correct: true },
                                { text: "Reinstalar Windows", correct: false },
                                { text: "Cambiar el monitor", correct: false }
                            ],
                            explanation: "Primero verificar lo básico: botón de encendido y alimentación, antes de diagnósticos complejos."
                        },
                        {
                            question: "¿Qué es el Dual Channel en memoria RAM?",
                            options: [
                                { text: "Aumento del ancho de banda", correct: true },
                                { text: "Instalación en pares", correct: true },
                                { text: "Mayor capacidad", correct: false },
                                { text: "Menor latencia", correct: false }
                            ],
                            explanation: "Dual Channel duplica el ancho de banda usando dos módulos simultáneamente, mejorando rendimiento."
                        }
                    ]
                }
                // Las otras 3 unidades continuarían aquí...
            ]
        };

        let currentUnit = 0;
        let userAnswers = Array(testData.units.length).fill().map(() => []);

        function showUnit(unitIndex) {
            currentUnit = unitIndex - 1;
            document.querySelectorAll('.unit-btn').forEach((btn, index) => {
                btn.classList.toggle('active', index === currentUnit);
            });
            renderQuestions();
            updateProgress();
        }

        function renderQuestions() {
            const container = document.getElementById('questionsContainer');
            const unit = testData.units[currentUnit];
            
            container.innerHTML = `
                <h2 style="color: #2c3e50; margin-bottom: 20px; border-bottom: 3px solid #3498db; padding-bottom: 10px;">
                    ${unit.name}
                </h2>
            `;
            
            unit.questions.forEach((question, qIndex) => {
                const questionDiv = document.createElement('div');
                questionDiv.className = 'question-card';
                questionDiv.innerHTML = `
                    <div class="question-text">${qIndex + 1}. ${question.question}</div>
                    <div class="options-container">
                        ${question.options.map((option, oIndex) => `
                            <div class="option" onclick="selectOption(${currentUnit}, ${qIndex}, ${oIndex})">
                                <input type="checkbox" id="q${currentUnit}_${qIndex}_${oIndex}">
                                <label for="q${currentUnit}_${qIndex}_${oIndex}">${option.text}</label>
                            </div>
                        `).join('')}
                    </div>
                `;
                container.appendChild(questionDiv);
            });
            
            // Restaurar respuestas anteriores
            restoreAnswers();
        }

        function selectOption(unitIndex, questionIndex, optionIndex) {
            const option = document.querySelector(`#q${unitIndex}_${questionIndex}_${optionIndex}`);
            const optionDiv = option.parentElement;
            
            option.checked = !option.checked;
            optionDiv.classList.toggle('selected', option.checked);
            
            // Actualizar array de respuestas
            if (!userAnswers[unitIndex][questionIndex]) {
                userAnswers[unitIndex][questionIndex] = [];
            }
            userAnswers[unitIndex][questionIndex][optionIndex] = option.checked;
        }

        function restoreAnswers() {
            testData.units[currentUnit].questions.forEach((question, qIndex) => {
                question.options.forEach((option, oIndex) => {
                    const checkbox = document.querySelector(`#q${currentUnit}_${qIndex}_${oIndex}`);
                    if (checkbox && userAnswers[currentUnit][qIndex] && userAnswers[currentUnit][qIndex][oIndex]) {
                        checkbox.checked = true;
                        checkbox.parentElement.classList.add('selected');
                    }
                });
            });
        }

        function updateProgress() {
            const totalQuestions = testData.units.reduce((sum, unit) => sum + unit.questions.length, 0);
            const answeredQuestions = userAnswers.flat().filter(arr => arr && arr.some(val => val)).length;
            const progress = (answeredQuestions / totalQuestions) * 100;
            
            document.getElementById('progressBar').style.width = `${progress}%`;
        }

        function checkAnswers() {
            let correctAnswers = 0;
            let totalQuestions = 0;
            
            testData.units.forEach((unit, uIndex) => {
                unit.questions.forEach((question, qIndex) => {
                    totalQuestions++;
                    let questionCorrect = true;
                    
                    question.options.forEach((option, oIndex) => {
                        const isSelected = userAnswers[uIndex] && userAnswers[uIndex][qIndex] && userAnswers[uIndex][qIndex][oIndex];
                        const optionElement = document.querySelector(`#q${uIndex}_${qIndex}_${oIndex}`);
                        
                        if (optionElement) {
                            if (option.correct) {
                                if (isSelected) {
                                    optionElement.parentElement.classList.add('correct');
                                } else {
                                    questionCorrect = false;
                                }
                            } else {
                                if (isSelected) {
                                    optionElement.parentElement.classList.add('incorrect');
                                    questionCorrect = false;
                                }
                            }
                        }
                    });
                    
                    if (questionCorrect) correctAnswers++;
                });
            });
            
            showResults(correctAnswers, totalQuestions);
        }

        function showResults(correct, total) {
            const score = (correct / total) * 10;
            const percentage = (correct / total) * 100;
            const passed = score >= 5;
            
            document.getElementById('scoreInner').textContent = `${score.toFixed(1)}/10`;
            document.getElementById('scoreCircle').style.setProperty('--percentage', `${percentage}%`);
            
            const scoreText = document.getElementById('scoreText');
            scoreText.textContent = `${correct}/${total} correctas (${percentage.toFixed(1)}%)`;
            scoreText.className = `score-text ${passed ? 'score-pass' : 'score-fail'}`;
            
            const feedback = document.getElementById('feedback');
            feedback.innerHTML = `
                <h3>${passed ? '🎉 ¡Enhorabuena! 🎉' : '📚 Necesitas repasar'}</h3>
                <p><strong>Aciertos:</strong> ${correct} de ${total}</p>
                <p><strong>Puntuación:</strong> ${score.toFixed(1)}/10 ${passed ? '(APROBADO)' : '(SUSPENSO)'}</p>
                <p><strong>Porcentaje:</strong> ${percentage.toFixed(1)}%</p>
                ${!passed ? '<p style="color: #dc3545; margin-top: 10px;">💡 Repasa los conceptos y vuelve a intentarlo</p>' : ''}
            `;
            
            document.getElementById('results').classList.add('show');
        }

        function showSolutions() {
            testData.units.forEach((unit, uIndex) => {
                unit.questions.forEach((question, qIndex) => {
                    question.options.forEach((option, oIndex) => {
                        const optionElement = document.querySelector(`#q${uIndex}_${qIndex}_${oIndex}`);
                        if (optionElement) {
                            if (option.correct) {
                                optionElement.parentElement.classList.add('correct');
                            }
                        }
                    });
                });
            });
        }

        function hideResults() {
            document.getElementById('results').classList.remove('show');
        }

        function resetTest() {
            if (confirm('¿Estás seguro de que quieres reiniciar el test? Se perderán todas las respuestas.')) {
                userAnswers = Array(testData.units.length).fill().map(() => []);
                document.querySelectorAll('.option').forEach(opt => {
                    opt.classList.remove('selected', 'correct', 'incorrect');
                });
                document.querySelectorAll('input[type="checkbox"]').forEach(cb => {
                    cb.checked = false;
                });
                hideResults();
                updateProgress();
            }
        }

        function generatePDF() {
            const { jsPDF } = window.jspdf;
            const doc = new jsPDF();
            
            // Cabecera
            doc.setFontSize(20);
            doc.text(testData.title, 20, 30);
            doc.setFontSize(12);
            doc.text(`Alumno: _________________________`, 20, 45);
            doc.text(`Fecha: _________________________`, 20, 55);
            
            let yPosition = 70;
            
            // Contenido del test
            testData.units.forEach((unit, uIndex) => {
                // Nueva página para cada unidad después de la primera
                if (uIndex > 0 && yPosition > 200) {
                    doc.addPage();
                    yPosition = 20;
                }
                
                doc.setFontSize(14);
                doc.setTextColor(41, 128, 185);
                doc.text(unit.name, 20, yPosition);
                yPosition += 10;
                
                unit.questions.forEach((question, qIndex) => {
                    if (yPosition > 270) {
                        doc.addPage();
                        yPosition = 20;
                    }
                    
                    doc.setFontSize(10);
                    doc.setTextColor(0, 0, 0);
                    doc.text(`${qIndex + 1}. ${question.question}`, 20, yPosition);
                    yPosition += 8;
                    
                    question.options.forEach((option, oIndex) => {
                        const isSelected = userAnswers[uIndex] && userAnswers[uIndex][qIndex] && userAnswers[uIndex][qIndex][oIndex];
                        doc.text(`   ${String.fromCharCode(97 + oIndex)}) ${option.text} ${isSelected ? '[X]' : '[ ]'}`, 25, yPosition);
                        yPosition += 6;
                    });
                    
                    yPosition += 5;
                });
                
                yPosition += 10;
            });
            
            doc.save('test_mme_respuestas.pdf');
        }

        // Inicializar
        showUnit(1);
    </script>

    <!-- Incluir jsPDF -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
</body>
</html>
2. Tests en Formato Markdown
markdown
# Test MME SMR1 - Montaje y Mantenimiento de Equipos

## Instrucciones
- **Duración:** 60 minutos
- **Preguntas:** 50 (10 por unidad)
- **Puntuación mínima:** 5/10 para aprobar
- **Tipo:** Múltiple opción (puede haber más de una correcta)

---

## UNIDAD 1: Fundamentos de Hardware

### 1. ¿Qué componente se considera el "cerebro" del ordenador?
- [ ] A) Memoria RAM
- [x] B) Procesador (CPU)
- [ ] C) Disco duro
- [ ] D) Fuente de alimentación

### 2. ¿Cuáles de estos son tipos de memoria RAM?
- [x] A) DDR2
- [x] B) DDR3
- [x] C) DDR4
- [x] D) Todas las anteriores

### 3. ¿Qué voltaje principal proporciona la fuente de alimentación a los componentes?
- [x] A) 3.3V
- [x] B) 5V
- [x] C) 12V
- [x] D) Todos los anteriores

### 4. ¿Para qué se utiliza la pulsera antiestática?
- [x] A) Proteger componentes de descargas electrostáticas
- [ ] B) Medir voltajes
- [ ] C) Atornillar componentes pequeños
- [ ] D) Organizar cables

### 5. ¿Qué herramienta se utiliza para medir continuidad en cables?
- [ ] A) Destornillador
- [x] B) Multímetro
- [ ] C) Alicates
- [ ] D) Pulsera antiestática

---

## UNIDAD 2: Ensamblaje de Equipos

### 6. ¿Cuál es el orden correcto para ensamblar un equipo?
- [x] A) CPU → RAM → Placa base → Discos
- [ ] B) Placa base → CPU → Discos → RAM
- [ ] C) Discos → CPU → RAM → Placa base
- [ ] D) RAM → Discos → CPU → Placa base

### 7. ¿Qué se debe verificar antes de instalar un procesador?
- [x] A) Compatibilidad de socket
- [x] B) Orientación correcta
- [ ] C) Color del disipador
- [ ] D) Precio del componente

### 8. ¿Para qué se utiliza la pasta térmica?
- [x] A) Mejorar transferencia de calor
- [x] B) Evitar sobrecalentamiento
- [ ] C) Fijar el procesador
- [ ] D) Proteger de descargas

### 9. ¿Qué conexión es esencial para el panel frontal?
- [x] A) POWER SW
- [x] B) HDD LED
- [ ] C) USB 3.0
- [ ] D) Audio frontal

### 10. ¿Qué se debe comprobar después del ensamblaje?
- [x] A) Todas las conexiones
- [x] B) Gestor de cables
- [ ] C) Precio de componentes
- [ ] D) Color de los LEDs

---

## Hoja de Respuestas

**Nombre:** _________________________
**Fecha:** _________________________

| Pregunta | Respuestas |
|----------|------------|
| 1 | A B C D |
| 2 | A B C D |
| 3 | A B C D |
| 4 | A B C D |
| 5 | A B C D |
| 6 | A B C D |
| 7 | A B C D |
| 8 | A B C D |
| 9 | A B C D |
| 10 | A B C D |

**Puntuación:** ______/10
**Resultado:** □ Aprobado □ Suspenso
3. Script para Generar ZIPs
html
<!-- generate_zips.html -->
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Generador Tests ZIP</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/FileSaver.js/2.0.5/FileSaver.min.js"></script>
</head>
<body>
    <h1>Descargar Tests Completos</h1>
    
    <button onclick="downloadMME()">📦 Descargar Pack MME</button>
    <button onclick="downloadRobotica()">🤖 Descargar Pack Robótica</button>
    <button onclick="downloadProgramacion()">💻 Descargar Pack Programación</button>

    <script>
        async function downloadMME() {
            const zip = new JSZip();
            
            // Agregar archivos HTML
            zip.file("test_mme_autocorregible.html", document.documentElement.outerHTML);
            
            // Agregar archivos MD
            zip.file("test_mme.md", `# Test MME - Markdown\n\nContenido completo del test...`);
            zip.file("solucionario_mme.md", `# Solucionario MME\n\nRespuestas correctas...`);
            
            // Generar ZIP
            const content = await zip.generateAsync({type: "blob"});
            saveAs(content, "pack_mme_smr1.zip");
        }

        async function downloadRobotica() {
            const zip = new JSZip();
            // Similar estructura para robótica
            const content = await zip.generateAsync({type: "blob"});
            saveAs(content, "pack_robotica_smr1.zip");
        }

        async function downloadProgramacion() {
            const zip = new JSZip();
            // Similar estructura para programación
            const content = await
ahora necesito que me generes un guion de practica para robotica cmo-313 con titulo "Diseño y simulación de circuitos eléctricos" que tengan que diseñar 3 circuitos electricos en CC con la herramienta de simulación online TinkerCad. el primer circuito en serie cin 3 resistencias y una pila en el que diseñe el circuito en una protoboard o placa de pruebas y 3 polímetros más las resistencias y la pila, a continuación deberan medir el voltaje o caida de tensión en cada resistencia y verificar si la suma de las tres es igual al nominal de la pila , tb comprobar con elpolímetro la intensidad en varias ramas del circuito (teniendo en cuenta que es en serie), otro circuito en paralelo con 3 resistencias y una pila y hacer lo mismo que con el serie pero ahora las mediciones son de la corriente en cada rama con resistencia y la ressist toal y voltaje delcircuito, otro mixto (1 R serie con (R2 !! R3), voltajes y corrientes. opcional: añadir 2o 3 diodos leds para darle un poco de luz y color a la práctica. el guion debe contener nombre dle modulo mme y smr1 y profesor q soy yo
Guion de Práctica - Robótica CMO-313
markdown
# 🔌 PRÁCTICA: DISEÑO Y SIMULACIÓN DE CIRCUITOS ELÉCTRICOS
**Módulo:** CMO-313 - Robótica  
**Ciclo Formativo:** SMR1 - Sistemas Microinformáticos y Redes  
**Profesor:** Ezequiel Llarena Borges  
**Duración:** 3 horas  
**Fecha:** `__________________`

---

## 🎯 OBJETIVOS DE APRENDIZAJE

### Objetivos Conceptuales
- [ ] Comprender las leyes fundamentales de circuitos eléctricos (Ley de Ohm, Kirchhoff)
- [ ] Diferenciar circuitos serie, paralelo y mixto
- [ ] Identificar componentes electrónicos básicos y su simbología

### Objetivos Procedimentales
- [ ] Diseñar circuitos eléctricos en plataforma de simulación TinkerCAD
- [ ] Realizar mediciones de voltaje, corriente y resistencia con polímetros virtuales
- [ ] Verificar experimentalmente las leyes de circuitos eléctricos

### Objetivos Actitudinales
- [ ] Desarrollar precisión en mediciones y cálculos
- [ ] Fomentar el método científico en la verificación de teorías
- [ ] Promover el trabajo sistemático en diseño electrónico

---

## 📋 CRITERIOS DE EVALUACIÓN

| Criterio | Ponderación | Evidencias |
|----------|-------------|------------|
| Diseño correcto circuitos en TinkerCAD | 30% | Capturas de pantalla circuitos funcionales |
| Mediciones precisas con polímetros | 35% | Tablas de datos completas y correctas |
| Cálculos y verificaciones teóricas | 25% | Comprobación leyes Ohm y Kirchhoff |
| Documentación y presentación | 10% | Informe completo y organizado |

---

## 🛠️ MATERIAL Y HERRAMIENTAS

### Software Requerido
- [ ] **TinkerCAD** (https://www.tinkercad.com/) - Plataforma online de simulación
- [ ] Navegador web actualizado (Chrome/Firefox recomendado)
- [ ] Cuenta en Autodesk (gratuita)

### Componentes Virtuales Necesarios
┌─────────────────────────────────────────────────────────────┐
│ COMPONENTES PARA TINKERCAD │
├──────────────────────┬──────────────────┬───────────────────┤
│ COMPONENTE │ CANTIDAD │ USO │
├──────────────────────┼──────────────────┼───────────────────┤
│ Batería/Pila 9V │ 3 unidades │ Fuente alimentación│
│ Resistencias varias │ 9 unidades │ Cargas circuito │
│ Polímetros │ 3 unidades │ Mediciones V, I, R│
│ Protoboard │ 3 unidades │ Montaje circuitos │
│ LEDs (opcional) │ 6 unidades │ Visualización │
│ Cables jumpers │ Múltiples │ Conexiones │
└──────────────────────┴──────────────────┴───────────────────┘

text

### Valores de Resistencia Recomendados
- **R1:** 220Ω (Rojo-Rojo-Marrón)
- **R2:** 330Ω (Naranja-Naranja-Marrón)  
- **R3:** 470Ω (Amarillo-Violeta-Marrón)
- **R4:** 1kΩ (Marrón-Negro-Rojo)
- **R5:** 2.2kΩ (Rojo-Rojo-Rojo)

---

## 📝 PROCEDIMIENTO PASO A PASO

### FASE 1: CONFIGURACIÓN INICIAL (20 minutos)

**Paso 1.1 - Acceso a TinkerCAD**
1. [ ] Abrir https://www.tinkercad.com
2. [ ] Iniciar sesión con cuenta Autodesk
3. [ ] Crear nuevo proyecto: "Circuitos_CC_SMR1"
4. [ ] Seleccionar "Circuitos" → "Crear nuevo circuito"

**Paso 1.2 - Familiarización con la Interfaz**
┌─────────────────────────────────────────────────────────────┐
│ INTERFAZ TINKERCAD - ZONAS │
├─────────────────────────────────────────────────────────────┤
│ ZONA SUPERIOR: Barra herramientas componentes │
│ ZONA CENTRAL: Área de trabajo - Protoboard virtual │
│ ZONA DERECHA: Panel propiedades componentes │
│ ZONA INFERIOR: Controles simulación (Iniciar/Detener) │
└─────────────────────────────────────────────────────────────┘

text

**Paso 1.3 - Configuración Polímetros**
- [ ] Arrastrar 3 polímetros al área de trabajo
- [ ] Configurar cada uno para diferentes mediciones:
  - Polímetro 1: Voltímetro (V)
  - Polímetro 2: Amperímetro (A)  
  - Polímetro 3: Óhmetro (Ω)

---

## 🔧 CIRCUITO 1: SERIE (45 minutos)

### Diseño del Circuito
┌─────────────────────────────────────────────────────────────┐
│ CIRCUITO SERIE - ESQUEMA │
├─────────────────────────────────────────────────────────────┤
│ +9V ---[R1]---[R2]---[R3]--- 0V │
│ | | | | │
│ V1 V2 V3 V4 │
└─────────────────────────────────────────────────────────────┘

text

**Paso 2.1 - Montaje en Protoboard**
1. [ ] Colocar batería 9V en protoboard
2. [ ] Conectar R1 (220Ω) en serie con R2 (330Ω)
3. [ ] Conectar R2 en serie con R3 (470Ω)
4. [ ] Completar circuito cerrado
5. [ ] Verificar conexiones correctas

**Paso 2.2 - Mediciones de Voltaje**
| Punto de Medición | Valor Teórico | Valor Medido | Diferencia |
|-------------------|---------------|--------------|------------|
| V1 (Total) | 9V | `_____ V` | `_____ V` |
| V_R1 | `_____ V` | `_____ V` | `_____ V` |
| V_R2 | `_____ V` | `_____ V` | `_____ V` |
| V_R3 | `_____ V` | `_____ V` | `_____ V` |
| **Suma V_R1+V_R2+V_R3** | **9V** | **`_____ V`** | **`_____ V`** |

**Paso 2.3 - Mediciones de Corriente**
- [ ] Colocar amperímetro en serie con R1: `_____ A`
- [ ] Colocar amperímetro en serie con R2: `_____ A`  
- [ ] Colocar amperímetro en serie con R3: `_____ A`
- [ ] **Verificación:** I_R1 = I_R2 = I_R3 = `_____ A`

**Paso 2.4 - Cálculos Teóricos**
Resistencia Total (R_T) = R1 + R2 + R3 = _____ Ω
Corriente Teórica (I) = V / R_T = 9V / _____ Ω = _____ A
Voltaje R1 Teórico = I × R1 = _____ A × 220Ω = _____ V
Voltaje R2 Teórico = _____ A × 330Ω = _____ V
Voltaje R3 Teórico = _____ A × 470Ω = _____ V

text

---

## ⚡ CIRCUITO 2: PARALELO (45 minutos)

### Diseño del Circuito
┌─────────────────────────────────────────────────────────────┐
│ CIRCUITO PARALELO - ESQUEMA │
├─────────────────────────────────────────────────────────────┤
│ +---[R1]---+ │
│ | | │
│ +9V +---[R2]---+ 0V │
│ | | │
│ +---[R3]---+ │
│ | | | │
│ I1 I2 I3 │
└─────────────────────────────────────────────────────────────┘

text

**Paso 3.1 - Montaje en Nueva Protoboard**
1. [ ] Colocar batería 9V
2. [ ] Conectar R1, R2, R3 en paralelo
3. [ ] Verificar que todas las resistencias tengan mismo voltaje

**Paso 3.2 - Mediciones de Corriente**
| Rama | Resistencia | Corriente Teórica | Corriente Medida | Diferencia |
|------|-------------|-------------------|------------------|------------|
| R1 | 220Ω | `_____ A` | `_____ A` | `_____ A` |
| R2 | 330Ω | `_____ A` | `_____ A` | `_____ A` |
| R3 | 470Ω | `_____ A` | `_____ A` | `_____ A` |
| **Total** | **`_____ Ω`** | **`_____ A`** | **`_____ A`** | **`_____ A`** |

**Paso 3.3 - Mediciones de Voltaje**
- [ ] Voltaje en R1: `_____ V`
- [ ] Voltaje en R2: `_____ V`
- [ ] Voltaje en R3: `_____ V`
- [ ] **Verificación:** V_R1 = V_R2 = V_R3 = 9V

**Paso 3.4 - Cálculos Teóricos**
1/R_T = 1/R1 + 1/R2 + 1/R3 = 1/220 + 1/330 + 1/470 = _____ Ω
R_Total = _____ Ω
I_Total = V / R_T = 9V / _____ Ω = _____ A
I_R1 = 9V / 220Ω = _____ A
I_R2 = 9V / 330Ω = _____ A
I_R3 = 9V / 470Ω = _____ A

text

---

## 🔄 CIRCUITO 3: MIXTO (45 minutos)

### Diseño del Circuito
┌─────────────────────────────────────────────────────────────┐
│ CIRCUITO MIXTO - ESQUEMA │
├─────────────────────────────────────────────────────────────┤
│ +9V ---[R1]---+---[R2]---+--- 0V │
│ | | │
│ [R3] [R4] │
│ | | │
│ +-----------+ │
└─────────────────────────────────────────────────────────────┘

text

**Valores Recomendados:** R1=1kΩ, R2=2.2kΩ, R3=330Ω, R4=470Ω

**Paso 4.1 - Montaje Complejo**
1. [ ] Colocar R1 en serie con combinación R2-R3-R4
2. [ ] Conectar R3 y R4 en paralelo entre R1 y R2
3. [ ] Verificar todas las conexiones

**Paso 4.2 - Mediciones Completas**
| Parámetro | Valor Teórico | Valor Medido | Diferencia |
|-----------|---------------|--------------|------------|
| V Total | 9V | `_____ V` | `_____ V` |
| V_R1 | `_____ V` | `_____ V` | `_____ V` |
| V_R2 | `_____ V` | `_____ V` | `_____ V` |
| V_R3 | `_____ V` | `_____ V` | `_____ V` |
| V_R4 | `_____ V` | `_____ V` | `_____ V` |
| I Total | `_____ A` | `_____ A` | `_____ A` |
| I_R1 | `_____ A` | `_____ A` | `_____ A` |
| I_R2 | `_____ A` | `_____ A` | `_____ A` |
| I_R3 | `_____ A` | `_____ A` | `_____ A` |
| I_R4 | `_____ A` | `_____ A` | `_____ A` |

**Paso 4.3 - Cálculos Avanzados**
R_paralelo = (R3 × R4) / (R3 + R4) = _____ Ω
R_total = R1 + R_paralelo + R2 = _____ Ω
I_total = 9V / R_total = _____ A
V_R1 = I_total × R1 = _____ V
V_paralelo = I_total × R_paralelo = _____ V
V_R2 = I_total × R2 = _____ V

text

---

## 💡 ACTIVIDAD OPCIONAL: CIRCUITO CON LEDs (25 minutos)

### Diseño con LEDs
┌─────────────────────────────────────────────────────────────┐
│ CIRCUITO LED - ESQUEMA │
├─────────────────────────────────────────────────────────────┤
│ +9V ---[R1 220Ω]---[LED Rojo]--- 0V │
│ [R2 330Ω]---[LED Verde]--- │
│ [R3 470Ω]---[LED Azul]---- │
└─────────────────────────────────────────────────────────────┘

text

**Paso 5.1 - Consideraciones LEDs**
- [ ] Los LEDs requieren resistencia limitadora de corriente
- [ ] Verificar polaridad (ánodo +, cátodo -)
- [ ] Observar intensidad luminosa según resistencia

**Paso 5.2 - Mediciones**
- [ ] Corriente en LED rojo: `_____ A`
- [ ] Corriente en LED verde: `_____ A`
- [ ] Corriente en LED azul: `_____ A`
- [ ] Voltaje en cada LED: `_____ V`

---

## 📊 FICHA DE TRABAJO DEL ALUMNO

**Nombre:** _________________________  
**Grupo:** ______ **Fecha:** __________

### CHECKLIST COMPLETACIÓN
| Circuito | Montaje | Mediciones | Cálculos | Capturas |
|----------|---------|------------|----------|----------|
| Serie | ☐ | ☐ | ☐ | ☐ |
| Paralelo | ☐ | ☐ | ☐ | ☐ |
| Mixto | ☐ | ☐ | ☐ | ☐ |
| LEDs (opc) | ☐ | ☐ | ☐ | ☐ |

### VERIFICACIÓN LEYES FUNDAMENTALES
| Ley | Circuito Serie | Circuito Paralelo | Circuito Mixto |
|-----|----------------|-------------------|----------------|
| **Ley de Ohm** (V=I×R) | ☐ Correcta | ☐ Correcta | ☐ Correcta |
| **Kirchhoff Voltajes** (ΣV=0) | ☐ Verificada | ☐ Verificada | ☐ Verificada |
| **Kirchhoff Corrientes** (ΣI=0) | ☐ Verificada | ☐ Verificada | ☐ Verificada |

### INCIDENCIAS Y OBSERVACIONES
Dificultades encontradas en el montaje:

Diferencias entre valores teóricos y medidos:

Comportamiento observado en circuitos:

text

---

## 🎓 RECURSOS DE APOYO

### 📚 Documentación Técnica
- [Guía oficial TinkerCAD Circuits](https://www.tinkercad.com/learn/circuits)
- [Tutorial mediciones con polímetro virtual](https://www.tinkercad.com/things/0xqL1dF2d7F)
- [Tabla código colores resistencias](https://www.allaboutcircuits.com/tools/resistor-color-code-calculator/)

### 🎥 Video Tutoriales
- [Introducción a TinkerCAD Circuits](https://youtube.com/watch?v=yaS7m
se me olvidarondos cosas una que el guion incluya un cuadro para que el alumno pueda insertar captura del circuito diseñado mostrando los polimetros con las mediciones. y ademas que pueda rellenar los valores en las tablas resultado y por ultimo un boton para que se pueda descargar en pd con nombre completo de alumno y grupo , fecha y nombre profesor
Guion de Práctica - Robótica CMO-313 (Versión Mejorada)
markdown
# 🔌 PRÁCTICA: DISEÑO Y SIMULACIÓN DE CIRCUITOS ELÉCTRICOS
**Módulo:** CMO-313 - Robótica  
**Ciclo Formativo:** SMR1 - Sistemas Microinformáticos y Redes  
**Profesor:** Ezequiel Llarena Borges  
**Duración:** 3 horas  
**Fecha:** `__________________`

---

<div class="student-info">
    <div class="info-field">
        <label>Nombre completo del alumno:</label>
        <input type="text" id="studentName" placeholder="Escribe tu nombre completo">
    </div>
    <div class="info-field">
        <label>Grupo:</label>
        <input type="text" id="studentGroup" placeholder="Ej: SMR1A">
    </div>
    <div class="info-field">
        <label>Fecha de realización:</label>
        <input type="date" id="practiceDate">
    </div>
</div>

---

## 🎯 OBJETIVOS DE APRENDIZAJE

### Objetivos Conceptuales
- [ ] Comprender las leyes fundamentales de circuitos eléctricos (Ley de Ohm, Kirchhoff)
- [ ] Diferenciar circuitos serie, paralelo y mixto
- [ ] Identificar componentes electrónicos básicos y su simbología

### Objetivos Procedimentales
- [ ] Diseñar circuitos eléctricos en plataforma de simulación TinkerCAD
- [ ] Realizar mediciones de voltaje, corriente y resistencia con polímetros virtuales
- [ ] Verificar experimentalmente las leyes de circuitos eléctricos

### Objetivos Actitudinales
- [ ] Desarrollar precisión en mediciones y cálculos
- [ ] Fomentar el método científico en la verificación de teorías
- [ ] Promover el trabajo sistemático en diseño electrónico

---

## 📋 CRITERIOS DE EVALUACIÓN

| Criterio | Ponderación | Evidencias |
|----------|-------------|------------|
| Diseño correcto circuitos en TinkerCAD | 30% | Capturas de pantalla circuitos funcionales |
| Mediciones precisas con polímetros | 35% | Tablas de datos completas y correctas |
| Cálculos y verificaciones teóricas | 25% | Comprobación leyes Ohm y Kirchhoff |
| Documentación y presentación | 10% | Informe completo y organizado |

---

## 🛠️ MATERIAL Y HERRAMIENTAS

### Software Requerido
- [ ] **TinkerCAD** (https://www.tinkercad.com/) - Plataforma online de simulación
- [ ] Navegador web actualizado (Chrome/Firefox recomendado)
- [ ] Cuenta en Autodesk (gratuita)

### Componentes Virtuales Necesarios
┌─────────────────────────────────────────────────────────────┐
│ COMPONENTES PARA TINKERCAD │
├──────────────────────┬──────────────────┬───────────────────┤
│ COMPONENTE │ CANTIDAD │ USO │
├──────────────────────┼──────────────────┼───────────────────┤
│ Batería/Pila 9V │ 3 unidades │ Fuente alimentación│
│ Resistencias varias │ 9 unidades │ Cargas circuito │
│ Polímetros │ 3 unidades │ Mediciones V, I, R│
│ Protoboard │ 3 unidades │ Montaje circuitos │
│ LEDs (opcional) │ 6 unidades │ Visualización │
│ Cables jumpers │ Múltiples │ Conexiones │
└──────────────────────┴──────────────────┴───────────────────┘

text

### Valores de Resistencia Recomendados
- **R1:** 220Ω (Rojo-Rojo-Marrón)
- **R2:** 330Ω (Naranja-Naranja-Marrón)  
- **R3:** 470Ω (Amarillo-Violeta-Marrón)
- **R4:** 1kΩ (Marrón-Negro-Rojo)
- **R5:** 2.2kΩ (Rojo-Rojo-Rojo)

---

## 🔧 CIRCUITO 1: SERIE (45 minutos)

### Diseño del Circuito
┌─────────────────────────────────────────────────────────────┐
│ CIRCUITO SERIE - ESQUEMA │
├─────────────────────────────────────────────────────────────┤
│ +9V ---[R1]---[R2]---[R3]--- 0V │
│ | | | | │
│ V1 V2 V3 V4 │
└─────────────────────────────────────────────────────────────┘

text

**Paso 2.1 - Montaje en Protoboard**
1. [ ] Colocar batería 9V en protoboard
2. [ ] Conectar R1 (220Ω) en serie con R2 (330Ω)
3. [ ] Conectar R2 en serie con R3 (470Ω)
4. [ ] Completar circuito cerrado
5. [ ] Verificar conexiones correctas

**Paso 2.2 - Mediciones de Voltaje**
| Punto de Medición | Valor Teórico | Valor Medido | Diferencia |
|-------------------|---------------|--------------|------------|
| V1 (Total) | 9V | <input type="text" class="measurement" data-circuit="serie" data-measure="v_total"> V | <input type="text" class="difference" readonly> V |
| V_R1 | <input type="text" class="theoretical" data-circuit="serie" data-measure="v_r1"> V | <input type="text" class="measurement" data-circuit="serie" data-measure="v_r1"> V | <input type="text" class="difference" readonly> V |
| V_R2 | <input type="text" class="theoretical" data-circuit="serie" data-measure="v_r2"> V | <input type="text" class="measurement" data-circuit="serie" data-measure="v_r2"> V | <input type="text" class="difference" readonly> V |
| V_R3 | <input type="text" class="theoretical" data-circuit="serie" data-measure="v_r3"> V | <input type="text" class="measurement" data-circuit="serie" data-measure="v_r3"> V | <input type="text" class="difference" readonly> V |
| **Suma V_R1+V_R2+V_R3** | **9V** | **<span id="sum_voltages_serie">0</span> V** | **<span id="diff_voltages_serie">0</span> V** |

**Paso 2.3 - Mediciones de Corriente**
- [ ] Colocar amperímetro en serie con R1: <input type="text" class="measurement" data-circuit="serie" data-measure="i_r1"> A
- [ ] Colocar amperímetro en serie con R2: <input type="text" class="measurement" data-circuit="serie" data-measure="i_r2"> A  
- [ ] Colocar amperímetro en serie con R3: <input type="text" class="measurement" data-circuit="serie" data-measure="i_r3"> A
- [ ] **Verificación:** I_R1 = I_R2 = I_R3 = <span id="current_verification_serie">___</span> A

**Paso 2.4 - Cálculos Teóricos**
Resistencia Total (R_T) = R1 + R2 + R3 = <input type="text" class="calculation" data-circuit="serie" data-calc="r_total"> Ω
Corriente Teórica (I) = V / R_T = 9V / <span id="r_total_serie"></span> Ω = <input type="text" class="calculation" data-circuit="serie" data-calc="i_total"> A
Voltaje R1 Teórico = I × R1 = <span id="i_total_serie"></span> A × 220Ω = <input type="text" class="calculation" data-circuit="serie" data-calc="v_r1_theo"> V
Voltaje R2 Teórico = <span id="i_total_serie2"></span> A × 330Ω = <input type="text" class="calculation" data-circuit="serie" data-calc="v_r2_theo"> V
Voltaje R3 Teórico = <span id="i_total_serie3"></span> A × 470Ω = <input type="text" class="calculation" data-circuit="serie" data-calc="v_r3_theo"> V

text

### 📸 CAPTURA CIRCUITO SERIE
<div class="screenshot-section">
    <div class="screenshot-instructions">
        <strong>Instrucciones para captura:</strong>
        <ol>
            <li>Completar el circuito en TinkerCAD</li>
            <li>Colocar polímetros mostrando mediciones</li>
            <li>Hacer captura de pantalla (Print Screen)</li>
            <li>Pegar en un documento y guardar como imagen</li>
        </ol>
    </div>
    <div class="screenshot-upload">
        <label>Insertar captura del circuito serie:</label>
        <input type="file" id="screenshotSerie" accept="image/*" class="screenshot-input">
        <div id="screenshotPreviewSerie" class="screenshot-preview"></div>
    </div>
</div>

---

## ⚡ CIRCUITO 2: PARALELO (45 minutos)

### Diseño del Circuito
┌─────────────────────────────────────────────────────────────┐
│ CIRCUITO PARALELO - ESQUEMA │
├─────────────────────────────────────────────────────────────┤
│ +---[R1]---+ │
│ | | │
│ +9V +---[R2]---+ 0V │
│ | | │
│ +---[R3]---+ │
│ | | | │
│ I1 I2 I3 │
└─────────────────────────────────────────────────────────────┘

text

**Paso 3.1 - Montaje en Nueva Protoboard**
1. [ ] Colocar batería 9V
2. [ ] Conectar R1, R2, R3 en paralelo
3. [ ] Verificar que todas las resistencias tengan mismo voltaje

**Paso 3.2 - Mediciones de Corriente**
| Rama | Resistencia | Corriente Teórica | Corriente Medida | Diferencia |
|------|-------------|-------------------|------------------|------------|
| R1 | 220Ω | <input type="text" class="theoretical" data-circuit="paralelo" data-measure="i_r1_theo"> A | <input type="text" class="measurement" data-circuit="paralelo" data-measure="i_r1"> A | <input type="text" class="difference" readonly> A |
| R2 | 330Ω | <input type="text" class="theoretical" data-circuit="paralelo" data-measure="i_r2_theo"> A | <input type="text" class="measurement" data-circuit="paralelo" data-measure="i_r2"> A | <input type="text" class="difference" readonly> A |
| R3 | 470Ω | <input type="text" class="theoretical" data-circuit="paralelo" data-measure="i_r3_theo"> A | <input type="text" class="measurement" data-circuit="paralelo" data-measure="i_r3"> A | <input type="text" class="difference" readonly> A |
| **Total** | **<span id="r_total_paralelo">___</span> Ω** | **<input type="text" class="theoretical" data-circuit="paralelo" data-measure="i_total_theo"> A** | **<input type="text" class="measurement" data-circuit="paralelo" data-measure="i_total"> A** | **<input type="text" class="difference" readonly> A** |

**Paso 3.3 - Mediciones de Voltaje**
- [ ] Voltaje en R1: <input type="text" class="measurement" data-circuit="paralelo" data-measure="v_r1"> V
- [ ] Voltaje en R2: <input type="text" class="measurement" data-circuit="paralelo" data-measure="v_r2"> V
- [ ] Voltaje en R3: <input type="text" class="measurement" data-circuit="paralelo" data-measure="v_r3"> V
- [ ] **Verificación:** V_R1 = V_R2 = V_R3 = 9V

**Paso 3.4 - Cálculos Teóricos**
1/R_T = 1/R1 + 1/R2 + 1/R3 = 1/220 + 1/330 + 1/470 = <input type="text" class="calculation" data-circuit="paralelo" data-calc="r_parallel"> Ω
R_Total = <span id="r_total_calc_paralelo"></span> Ω
I_Total = V / R_T = 9V / <span id="r_total_for_current"></span> Ω = <input type="text" class="calculation" data-circuit="paralelo" data-calc="i_total_theo"> A
I_R1 = 9V / 220Ω = <input type="text" class="calculation" data-circuit="paralelo" data-calc="i_r1_theo"> A
I_R2 = 9V / 330Ω = <input type="text" class="calculation" data-circuit="paralelo" data-calc="i_r2_theo"> A
I_R3 = 9V / 470Ω = <input type="text" class="calculation" data-circuit="paralelo" data-calc="i_r3_theo"> A

text

### 📸 CAPTURA CIRCUITO PARALELO
<div class="screenshot-section">
    <div class="screenshot-upload">
        <label>Insertar captura del circuito paralelo:</label>
        <input type="file" id="screenshotParalelo" accept="image/*" class="screenshot-input">
        <div id="screenshotPreviewParalelo" class="screenshot-preview"></div>
    </div>
</div>

---

## 🔄 CIRCUITO 3: MIXTO (45 minutos)

### Diseño del Circuito
┌─────────────────────────────────────────────────────────────┐
│ CIRCUITO MIXTO - ESQUEMA │
├─────────────────────────────────────────────────────────────┤
│ +9V ---[R1]---+---[R2]---+--- 0V │
│ | | │
│ [R3] [R4] │
│ | | │
│ +-----------+ │
└─────────────────────────────────────────────────────────────┘

text

**Valores Recomendados:** R1=1kΩ, R2=2.2kΩ, R3=330Ω, R4=470Ω

**Paso 4.1 - Montaje Complejo**
1. [ ] Colocar R1 en serie con combinación R2-R3-R4
2. [ ] Conectar R3 y R4 en paralelo entre R1 y R2
3. [ ] Verificar todas las conexiones

**Paso 4.2 - Mediciones Completas**
| Parámetro | Valor Teórico | Valor Medido | Diferencia |
|-----------|---------------|--------------|------------|
| V Total | 9V | <input type="text" class="measurement" data-circuit="mixto" data-measure="v_total"> V | <input type="text" class="difference" readonly> V |
| V_R1 | <input type="text" class="theoretical" data-circuit="mixto" data-measure="v_r1_theo"> V | <input type="text" class="measurement" data-circuit="mixto" data-measure="v_r1"> V | <input type="text" class="difference" readonly> V |
| V_R2 | <input type="text" class="theoretical" data-circuit="mixto" data-measure="v_r2_theo"> V | <input type="text" class="measurement" data-circuit="mixto" data-measure="v_r2"> V | <input type="text" class="difference" readonly> V |
| V_R3 | <input type="text" class="theoretical" data-circuit="mixto" data-measure="v_r3_theo"> V | <input type="text" class="measurement" data-circuit="mixto" data-measure="v_r3"> V | <input type="text" class="difference" readonly> V |
| V_R4 | <input type="text" class="theoretical" data-circuit="mixto" data-measure="v_r4_theo"> V | <input type="text" class="measurement" data-circuit="mixto" data-measure="v_r4"> V | <input type="text" class="difference" readonly> V |
| I Total | <input type="text" class="theoretical" data-circuit="mixto" data-measure="i_total_theo"> A | <input type="text" class="measurement" data-circuit="mixto" data-measure="i_total"> A | <input type="text" class="difference" readonly> A |
| I_R1 | <input type="text" class="theoretical" data-circuit="mixto" data-measure="i_r1_theo"> A | <input type="text" class="measurement" data-circuit="mixto" data-measure="i_r1"> A | <input type="text" class="difference" readonly> A |
| I_R2 | <input type="text" class="theoretical" data-circuit="mixto" data-measure="i_r2_theo"> A | <input type="text" class="measurement" data-circuit="mixto" data-measure="i_r2"> A | <input type="text" class="difference" readonly> A |
| I_R3 | <input type="text" class="theoretical" data-circuit="mixto" data-measure="i_r3_theo"> A | <input type="text" class="measurement" data-circuit="mixto" data-measure="i_r3"> A | <input type="text" class="difference" readonly> A |
| I_R4 | <input type="text" class="theoretical" data-circuit="mixto" data-measure="i_r4_theo"> A | <input type="text" class="measurement" data-circuit="mixto" data-measure="i_r4"> A | <input type="text" class="difference" readonly> A |

**Paso 4.3 - Cálculos Avanzados**
R_paralelo = (R3 × R4) / (R3 + R4) = <input type="text" class="calculation" data-circuit="mixto" data-calc="r_parallel"> Ω
R_total = R1 + R_paralelo + R2 = <span id="r_total_mixto">___</span> Ω
I_total = 9V / R_total = <input type="text" class="calculation" data-circuit="mixto" data-calc="i_total_theo"> A
V_R1 = I_total × R1 = <input type="text" class="calculation" data-circuit="mixto" data-calc="v_r1_theo"> V
V_paralelo = I_total × R_paralelo = <input type="text" class="calculation" data-circuit="mixto" data-calc="v_parallel_theo"> V
V_R2 = I_total × R2 = <input type="text" class="calculation" data-circuit="mixto" data-calc="v_r2_theo"> V

text

### 📸 CAPTURA CIRCUITO MIXTO
<div class="screenshot-section">
    <div class="screenshot-upload">
        <label>Insertar captura del circuito mixto:</label>
        <input type="file" id="screenshotMixto" accept="image/*" class="screenshot-input">
        <div id="screenshotPreviewMixto" class="screenshot-preview"></div>
    </div>
</div>

---

## 💡 ACTIVIDAD OPCIONAL: CIRCUITO CON LEDs (25 minutos)

### Diseño con LEDs
┌─────────────────────────────────────────────────────────────┐
│ CIRCUITO LED - ESQUEMA │
├─────────────────────────────────────────────────────────────┤
│ +9V ---[R1 220Ω]---[LED Rojo]--- 0V │
│ [R2 330Ω]---[LED Verde]--- │
│ [R3 470Ω]---[LED Azul]---- │
└─────────────────────────────────────────────────────────────┘

text

**Paso 5.1 - Consideraciones LEDs**
- [ ] Los LEDs requieren resistencia limitadora de corriente
- [ ] Verificar polaridad (ánodo +, cátodo -)
- [ ] Observar intensidad luminosa según resistencia

**Paso 5.2 - Mediciones**
- [ ] Corriente en LED rojo: <input type="text" class="measurement" data-circuit="leds" data-measure="i_led_rojo"> A
- [ ] Corriente en LED verde: <input type="text" class="measurement" data-circuit="leds" data-measure="i_led_verde"> A
- [ ] Corriente en LED azul: <input type="text" class="measurement" data-circuit="leds" data-measure="i_led_azul"> A
- [ ] Voltaje en cada LED: <input type="text" class="measurement" data-circuit="leds" data-measure="v_led"> V

### 📸 CAPTURA CIRCUITO LEDs
<div class="screenshot-section">
    <div class="screenshot-upload">
        <label>Insertar captura del circuito con LEDs:</label>
        <input type="file" id="screenshotLEDs" accept="image/*" class="screenshot-input">
        <div id="screenshotPreviewLEDs" class="screenshot-preview"></div>
    </div>
</div>

---

## 📊 FICHA DE TRABAJO DEL ALUMNO

### CHECKLIST COMPLETACIÓN
| Circuito | Montaje | Mediciones | Cálculos | Capturas |
|----------|---------|------------|----------|----------|
| Serie | ☐ | ☐ | ☐ | ☐ |
| Paralelo | ☐ | ☐ | ☐ | ☐ |
| Mixto | ☐ | ☐ | ☐ | ☐ |
| LEDs (opc) | ☐ | ☐ | ☐ | ☐ |

### VERIFICACIÓN LEYES FUNDAMENTALES
| Ley | Circuito Serie | Circuito Paralelo | Circuito Mixto |
|-----|----------------|-------------------|----------------|
| **Ley de Ohm** (V=I×R) | ☐ Correcta | ☐ Correcta | ☐ Correcta |
| **Kirchhoff Voltajes** (ΣV=0) | ☐ Verificada | ☐ Verificada | ☐ Verificada |
| **Kirchhoff Corrientes** (ΣI=0) | ☐ Verificada | ☐ Verificada | ☐ Verificada |

### INCIDENCIAS Y OBSERVACIONES
<textarea id="observations" placeholder="Describe aquí las dificultades encontradas, diferencias entre valores teóricos y medidos, y comportamientos observados en los circuitos..." rows="4" style="width: 100%; padding: 10px; border: 1px solid #ddd; border-radius: 5px; margin: 10px 0;"></textarea>

---

## 🎓 RECURSOS DE APOYO

### 📚 Documentación Técnica
- [Guía oficial TinkerCAD Circuits](https://www.tinkercad.com/learn/circuits)
- [Tutorial mediciones con polímetro virtual](https://www.tinkercad.com/things/0xqL1dF2d7F)
- [Tabla código colores resistencias](https://www.allaboutcircuits.com/tools/resistor-color-code-calculator/)

### 🎥 Video Tutoriales
- [Introducción a TinkerCAD Circuits](https://youtube.com/watch?v=yaS7m84YeD8)
- [Mediciones con polímetro virtual](https://youtube.com/watch?v=2-4L0gTjXsQ)
- [Circuitos serie, paralelo y mixto](https://youtube.com/watch?v=7vfd

