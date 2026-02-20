![Módulo](https://img.shields.io/badge/Módulo-Montaje%20y%20Mantenimiento-lightgrey)
![Grupo](https://img.shields.io/badge/Grupo-SMR1-blue)
![Tema](https://img.shields.io/badge/Tema-BIOS%20%2F%20UEFI-success)
  
---

## 1. ¿Qué es la BIOS?
 
La **BIOS (Basic Input/Output System)** es el sistema básico de entrada/salida almacenado en memoria ROM/Flash en la placa base. Es el primer programa *(firmware)* que se ejecuta al encender el equipo y sus funciones principales son:  
- Inicializar el hardware
- Ejecutar el POST
- Configuración del sistema
- Cargar el sistema operativo en memoria
 
La versión moderna de la BIOS es la **UEFI (Unified Extensible Firmware Interface).**

## 2. BIOS vs UEFI   

| Característica | BIOS (Legacy) | UEFI |
|----------------|------|------|
| Interfaz | Texto | Gráfica |
| Arquitectura | 16 bits | 32/64 bits |
| Tabla particiones | MBR (2TB máx) | GPT (9.4 ZB) |
| Secure Boot | No | Sí |
| Drivers propios | No | Sí |
| Velocidad | Más lenta | Más rápida |  

## 3. Fases de arranque (POST)  

### 1️⃣ POST (Power-On Self Test)
- Verificación CPU
- Comprobación RAM
- Inicialización chipset
- Detección dispositivos de almacenamiento (SATA/NVMe)
- Detección GPU
- Señales acústicas (beep codes)

### 2️⃣ Inicialización Hardware
- Controladores básicos integrados
- Inicialización buses PCIe
- Enumeración dispositivos

### 3️⃣ Boot Manager
- Selección dispositivo de arranque
- Carga MBR (BIOS) o EFI Bootloader (UEFI)  

## 4. Configuración 

-   Boot Order
-   Modo SATA (AHCI/IDE/RAID)
-   Virtualización (Intel VT-x / AMD SVM)
-   Fecha y Hora
-   Secure Boot
-   Fast Boot
-   Overclocking básico

## 5. Errores típicos BIOS
- Boot loop (pitidos continuos) → RAM mal instalada
- No detecta disco → Modo SATA incorrecto
- Error Secure Boot → SO incompatible
- No arranca USB → Orden de arranque mal configurado  

## 6. Simulador de BIOS/UEFI online  

[Simulador BIOS/UEFI online](https://download.lenovo.com/bsco/index.html)   

## 7. Síntesis
>- La BIOS/UEFI es el firmware que prepara el equipo antes de que cargue el sistema operativo.
>- La UEFI es un mini-sistema operativo previo al sistema operativo principal.

## 8. Autoevaluación  

[Test de autoevaluación BIOS](https://github.com/ezellabor/Montaje-y-Mantenimiento-de-Equipos-MME-SMR1/blob/main/Tests%20y%20Autoevaluaci%C3%B3n/bios-basico-test.md)











