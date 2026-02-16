![Módulo](https://img.shields.io/badge/Módulo-Montaje%20y%20Mantenimiento-lightgrey)
![Grupo](https://img.shields.io/badge/Grupo-SMR1-blue)
![Tema](https://img.shields.io/badge/Tema-BIOS%20%2F%20UEFI-success)
  
---

## 1. ¿Qué es la BIOS?

La **BIOS (Basic Input/Output System)** es un firmware almacenado en memoria ROM/Flash de la placa base. Es el primer "software" que se ejecuta al encender el equipo y sus funciones principales son:  
- Inicializar el hardware
- Ejecutar el POST
- Permitir configuración del sistema
- Cargar el sistema operativo en memoria

La versión moderna de la BIOS es la **UEFI (Unified Extensible Firmware Interface).**

## 2. BIOS vs UEFI 

| Característica | BIOS Legacy | UEFI |
|---------------|------------|------|
| Interfaz | Texto | Gráfica |
| Disco máximo | 2TB (MBR) | >2TB (GPT) |
| Secure Boot | ❌ | ✅ |
| Velocidad | Más lenta | Más rápida |

## 2. Fases del arranque

### 1️⃣ POST (Power-On Self Test)
- Verificación CPU
- Comprobación RAM
- Inicialización chipset
- Detección dispositivos SATA/NVMe
- Señales acústicas (beep codes)

### 2️⃣ Inicialización Hardware
- Controladores básicos integrados
- Inicialización buses PCIe
- Enumeración dispositivos

### 3️⃣ Boot Manager
- Selección dispositivo de arranque
- Carga MBR (BIOS) o EFI Bootloader (UEFI)


## 3. Comparativa técnica BIOS vs UEFI   

| Característica | BIOS | UEFI |
|---------------|------|------|
| Arquitectura | 16 bits | 32/64 bits |
| Particiones | MBR (2TB máx) | GPT (9.4 ZB) |
| Secure Boot | No | Sí |
| Interfaz | Texto | Gráfica |
| Drivers propios | No | Sí |

## 4️. Configuración avanzada

- AHCI vs RAID
- XMP (perfiles de memoria)
- Virtualización (Intel VT-x / AMD SVM)
- Secure Boot
- Fast Boot
- TPM
- Overclocking básico

## 5. Errores típicos BIOS
- Boot loop (pitidos continuos) → RAM mal instalada
- No detecta disco → Modo SATA incorrecto
- Error Secure Boot → SO incompatible
- No arranca USB → Orden de arranque mal configurado

## Idea técnica clave  

>  **UEFI** es un mini-sistema operativo previo al sistema operativo principal.  

## 6. Simulador de BIOS/UEFI online de Lenovo  

[Simulador BIOS/UEFI online](https://download.lenovo.com/bsco/index.html)





