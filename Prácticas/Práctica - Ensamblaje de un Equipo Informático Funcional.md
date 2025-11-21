# MÓDULO: MONTAJE Y MANTENIMIENTO DE EQUIPOS (MME)

---

## Práctica 1: Ensamblaje de un equipo informático funcional

Aspecto	Detalles
Título:	Ensamblaje de un Equipo Informático Funcional
RA a Cubrir:	RA1: Ensamblar y configurar equipos informáticos, siguiendo especificaciones y normativas de seguridad.
Objetivo:	Montar todos los componentes internos de un PC de sobremesa de forma segura y correcta, verificando su encendido inicial.
Duración Estimada:	2-3 horas
1. Materiales Necesarios (Por grupo/pareja de alumnos)
Kit de componentes: Caja, Placa base, CPU, Pasta térmica, RAM, Fuente de alimentación (PSU), Disco de almacenamiento (HDD/SSD/M.2), Tarjeta gráfica (GPU, si aplica), Tornillería variada.
Herramientas: Pulsera antiestática (obligatorio), Destornilladores (Phillips PH2, plano), Bridas de plástico.
Documentación: Manual de la placa base (impreso o digital).
2. Medidas de Seguridad y Prevención de Riesgos
Descarga electrostática (ESD): Obligatorio el uso de pulsera antiestática conectada a tierra.
Desconexión: Asegurarse de que la fuente de alimentación está apagada (interruptor trasero en "0").
Manejo de componentes: Manipular siempre las placas por los bordes.
3. Procedimiento Detallado (Paso a Paso)
Preparación de la Placa Base: Instalar CPU, pasta térmica, disipador y RAM fuera de la caja.
Preparación de la Carcasa: Instalar el I/O Shield (placa trasera de puertos).
Montaje de la Placa Base en la Carcasa: Asegurar con separadores y tornillos.
Instalación de la Fuente de Alimentación (PSU): Montar la PSU en su ubicación.
Instalación de Discos de Almacenamiento: Instalar SSD/HDD/M.2.
Conexionado de Cables de Alimentación: Conectar 24 pines ATX, alimentación CPU y alimentación SATA.
Conexiones del Panel Frontal (Crítico): Conectar los pequeños cables (Power SW, Reset SW, LEDs, USB, Audio) usando el manual como guía.
Instalación de la Tarjeta Gráfica (si aplica): Insertar en slot PCIe y conectar alimentación.
Gestión de Cables y Cierre: Usar bridas para ordenar.
Test Inicial: Conectar periféricos y encender el equipo.
Ficha de Trabajo del Alumno (Práctica 1)
Nombre del Alumno/Grupo: _________________________
Fecha: _______________
Equipo Asignado (Nº Serie/ID): ____________________
Tarea a Realizar	Checklist Alumno	Notas / Incidencias
Seguridad: Uso de pulsera antiestática	[ ] OK	
Paso 1: CPU y Disipador instalados en Placa	[ ] OK	
Paso 2: RAM instalada en slots correctos (Dual Channel)	[ ] OK	
Paso 3: I/O Shield colocado en la caja	[ ] OK	
Paso 4: Placa base fijada a la caja (con separadores)	[ ] OK	
Paso 5: Fuente de alimentación instalada y apagada	[ ] OK	
Paso 6: Almacenamiento (SSD/HDD) instalado	[ ] OK	
Paso 7: Cables de alimentación (24pin ATX, CPU) conectados	[ ] OK	
Paso 8: Cables Panel Frontal conectados (Power SW, LEDs, USB)	[ ] OK	
Paso 9: Tarjeta Gráfica y alimentación (si aplica) instaladas	[ ] OK	
Paso 10: Gestión de cables realizada (bridas)	[ ] OK	
Test Final: El equipo enciende y muestra BIOS	[ ] OK	
Práctica 2: Configuración Inicial de BIOS/UEFI y Dual-Boot
Aspecto	Detalles
Título:	Configuración de Firmware e Instalación Multi-Sistema
RA a Cubrir:	RA1, RA2: Instalar y actualizar software de base (BIOS/UEFI, controladores, SO).
Objetivo:	Configurar los parámetros básicos del sistema e instalar Windows y Linux en el mismo equipo.
Duración Estimada:	3-4 horas
1. Materiales Necesarios
Equipo de la Práctica 1.
2 USB bootables (Windows y Linux ISOs).
Acceso a internet para drivers.
2. Procedimiento Detallado (Paso a Paso)
Acceso y Configuración de la BIOS/UEFI: Entrar en BIOS/UEFI (teclas Supr, F2, etc.), verificar fecha/hora, configurar orden de arranque USB y habilitar virtualización. Guardar y salir.
Instalación de Windows: Arrancar desde USB. Punto Clave: Usar solo la mitad del disco duro, dejar el resto "Espacio sin asignar".
Instalación de Linux: Arrancar desde USB de Linux. Punto Clave: Instalar en el "Espacio sin asignar", eligiendo la opción "Instalar junto a Windows".
Verificación del Dual-Boot: Comprobar que aparece el menú GRUB y que ambos sistemas arrancan.
Instalación de Controladores (Drivers) en Windows: Instalar drivers de GPU, chipset, audio y red.
Ficha de Trabajo del Alumno (Práctica 2)
Nombre del Alumno/Grupo: _________________________
Fecha: _______________
Sistemas Operativos Instalados: Windows [Versión] / Linux [Distribución]
Tarea a Realizar	Checklist Alumno	Notas / Incidencias
Paso 1: Acceso a BIOS/UEFI	[ ] OK	Tecla utilizada: ____
Paso 2: Fecha/Hora y Orden de Arranque configurados	[ ] OK	
Paso 3: Instalación de Windows completada	[ ] OK	Tamaño Partición Windows: ____ GB
Paso 4: Instalación de Linux completada	[ ] OK	Tamaño Partición Linux: ____ GB
Paso 5: Menú de Dual-Boot (GRUB) funcional	[ ] OK	
Paso 6: Ambos sistemas operativos arrancan correctamente	[ ] OK	
Paso 7: Drivers de GPU y Red instalados en Windows	[ ] OK	
Resultado Final: Sistemas operativos funcionales	[ ] OK	
Práctica 3: Diagnóstico, Mantenimiento Preventivo y Reparación
Aspecto	Detalles
Título:	Laboratorio de Averías: Detección y Solución de Fallos
RA a Cubrir:	RA3: Diagnosticar y reparar averías de hardware, utilizando herramientas de testeo.
Objetivo:	Desarrollar habilidades de diagnóstico sistemático y resolver problemas comunes de hardware.
Duración Estimada:	2-3 horas
1. Materiales Necesarios
Equipos preparados por el profesor con fallos intencionados.
Herramientas y componentes de repuesto.
Software de diagnóstico en USB booteable (Hiren's BootCD, MemTest86, HWMonitor).
2. Procedimiento Detallado (Paso a Paso) - Modo Servicio Técnico
Recepción del Equipo y Síntoma: Recibir la "orden de trabajo" del profesor con la descripción del fallo.
Fase de Diagnóstico Sistemático: Observación visual, testeo con software, método de descarte de componentes.
Identificación de la Avería: Determinar la causa raíz.
Reparación y Verificación: Sustituir/reconectar el componente y verificar el funcionamiento.
Documentación y Cierre: Rellenar el informe de servicio técnico (OT).
Ficha de Causa-Avería-Solución (Plantilla de Referencia Rápida)
Causa Común	Avería Típica	Síntoma Principal	Solución Propuesta
Cable CPU 4/8 pines suelto	Falta de alimentación CPU	El PC no enciende nada o se apaga al instante	Conectar correctamente el cable de alimentación CPU
Módulo RAM mal insertado	Fallo de memoria	Pitidos (Beeps) al arrancar, no hay imagen	Reinsertar correctamente los módulos en los slots
Cable SATA de datos suelto/roto	Disco no detectado	"No bootable device found", Windows no carga	Reconectar/sustituir cable SATA, verificar en BIOS
Tarjeta gráfica mal insertada	Fallo de vídeo	El monitor permanece negro (no hay señal)	Reinsertar la GPU firmemente, verificar alimentación
Exceso de polvo / Pasta térmica seca	Sobrecalentamiento	Apagones repentinos tras un tiempo de uso	Limpieza interna, reaplicar pasta térmica
Informe Final del Técnico (Práctica 3)
Nombre del Alumno/Grupo: _________________________
Fecha: _______________
OT (Orden de Trabajo) Nº: _________________________
1. Síntoma Reportado por el "Cliente":
2. Proceso de Diagnóstico Realizado:
3. Informe Final del Técnico:
Apartado	Descripción Específica del Caso
Avería Identificada:	
Solución Aplicada:	
Verificación Final:	

---
*(End of the content in Markdown format)*
---
