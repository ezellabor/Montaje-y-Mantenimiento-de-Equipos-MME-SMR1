![Módulo](https://img.shields.io/badge/Módulo-Montaje_y_Mantenimiento_de_Equipos-brown?style=for-the-badge)
![Grupo](https://img.shields.io/badge/Grupo-SMR1-blue?style=for-the-badge)
![Profesor](https://img.shields.io/badge/Profesor-Ezequiel_Llarena_Borges-blue?style=for-the-badge)  
```Guía técnica``` 
  
## Creación de USB booteable con Windows

---

## 1. Objetivo

Crear un dispositivo USB de arranque con el instalador oficial de Windows para:

- Instalación limpia del sistema operativo.
- Reparación del sistema.
- Recuperación del entorno de arranque.
- Mantenimiento en entornos de taller o laboratorio.

---

## 2. Requisitos técnicos

### 2.1 Hardware

- Memoria USB mínimo 8 GB (recomendado 16 GB).
- Equipo con conexión a Internet.
- Equipo compatible con UEFI o BIOS heredada (Legacy).

### 2.2 Software

Opción A (recomendada):
- Media Creation Tool oficial de Microsoft.

Opción B:
- Imagen ISO oficial de Windows.
- Herramienta de grabación USB (por ejemplo, Rufus).

---

## 3. Conceptos técnicos previos

### 3.1 BIOS vs UEFI

- BIOS: firmware tradicional que carga el sector de arranque (MBR).
- UEFI: firmware moderno que utiliza partición EFI y tabla GPT.

### 3.2 GPT vs MBR

- MBR (Master Boot Record):
  - Máximo 2 TB.
  - Hasta 4 particiones primarias.
  - Compatible con BIOS heredada.

- GPT (GUID Partition Table):
  - Soporta discos mayores de 2 TB.
  - Más particiones.
  - Requerido para sistemas UEFI modernos.

---

## 4. Método 1: Media Creation Tool (Procedimiento Oficial)

### 4.1 Descarga

1. Acceder al sitio oficial de Microsoft.
2. Descargar la herramienta correspondiente a la versión de Windows.
3. Ejecutar como administrador.

### 4.2 Procedimiento paso a paso

1. Conectar la memoria USB.
2. Ejecutar la herramienta.
3. Aceptar términos de licencia.
4. Seleccionar:
   Crear medio de instalación (USB, DVD o archivo ISO).
5. Elegir:
   - Idioma.
   - Edición.
   - Arquitectura (64 bits recomendada).
6. Seleccionar:
   Unidad flash USB.
7. Elegir el dispositivo correcto.
8. Confirmar y esperar a que:
   - Se descargue la imagen.
   - Se formatee el USB.
   - Se copien los archivos.
   - Se configure el entorno de arranque.

### 4.3 Qué hace internamente la herramienta

- Descarga la imagen ISO oficial.
- Crea la tabla de particiones adecuada.
- Copia el gestor de arranque (Boot Manager).
- Instala Windows PE (entorno de preinstalación).
- Configura archivos BCD (Boot Configuration Data).

---

## 5. Método 2: ISO + Rufus

### 5.1 Cuándo usar este método

- Necesidad de elegir manualmente GPT o MBR.
- Trabajo en laboratorio.
- Configuración específica para hardware antiguo.
- Personalización del medio de instalación.

### 5.2 Procedimiento

1. Descargar ISO oficial.
2. Ejecutar Rufus.
3. Seleccionar dispositivo USB.
4. Seleccionar la imagen ISO.
5. Configurar según el equipo destino:

#### Para equipos modernos (UEFI)

- Esquema de partición: GPT.
- Sistema destino: UEFI (no CSM).
- Sistema de archivos: NTFS.
- Tamaño de clúster: por defecto.

#### Para equipos antiguos (Legacy BIOS)

- Esquema de partición: MBR.
- Sistema destino: BIOS o UEFI-CSM.
- Sistema de archivos: NTFS.

6. Pulsar Iniciar.
7. Confirmar borrado del USB.
8. Esperar finalización.

---

## 6. Proceso de arranque desde USB

1. Insertar el USB en el equipo destino.
2. Encender el equipo.
3. Acceder al menú de arranque (Boot Menu):
   - F12 (común en muchos fabricantes).
   - F9, F8 o Esc según modelo.
4. Seleccionar dispositivo USB.
5. Iniciar Windows Setup.

---

## 7. Proceso técnico de arranque

### 7.1 En modo BIOS (Legacy)

- El firmware carga el MBR.
- Se ejecuta el código del sector 0.
- Se transfiere control al cargador de arranque.
- Se inicia Windows PE.

### 7.2 En modo UEFI

- El firmware busca partición EFI.
- Carga archivo bootx64.efi.
- Ejecuta Windows Boot Manager.
- Se inicia el entorno de instalación.

---

## 8. Verificación del USB creado

Para comprobar que el USB es correcto:

1. Acceder al USB desde el explorador.
2. Verificar presencia de:
   - Carpeta sources.
   - Archivo bootmgr.
   - Carpeta EFI (si GPT).
3. Probar arranque en equipo de pruebas.

---

## 9. Problemas frecuentes y soluciones

### 9.1 El USB no aparece en el menú de arranque

- Secure Boot activado.
- USB mal configurado.
- Puerto USB defectuoso.
- Orden de arranque incorrecto.

Solución:
- Desactivar Secure Boot temporalmente.
- Recrear el USB.
- Probar otro puerto.

### 9.2 Error de partición GPT/MBR durante instalación

Mensaje típico:
"Windows no se puede instalar en este disco."

Causa:
Modo de arranque no coincide con esquema de partición.

Solución:
- Verificar si el equipo está en UEFI o Legacy.
- Recrear el USB con el esquema correcto.
- Convertir disco con diskpart si es necesario.

---

## 10. Buenas prácticas

- Utilizar siempre imágenes oficiales.
- Etiquetar los USB por versión.
- Mantener un USB maestro actualizado.
- Verificar modo de arranque antes de iniciar instalación.
- No mezclar GPT con BIOS Legacy.
- Documentar configuración utilizada.

---

## 11. Conclusión técnica

Crear un USB booteable con Windows implica:

- Preparar correctamente la tabla de particiones.
- Instalar un cargador de arranque compatible.
- Configurar entorno Windows PE.
- Alinear esquema GPT/MBR con modo UEFI/BIOS.

*Una correcta comprensión de estos elementos evita errores de instalación y mejora la eficiencia en entornos de soporte técnico y formación profesional.*

---
