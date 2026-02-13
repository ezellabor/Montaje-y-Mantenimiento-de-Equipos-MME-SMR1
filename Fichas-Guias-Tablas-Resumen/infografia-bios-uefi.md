# BIOS / UEFI 

![Nivel](https://img.shields.io/badge/Nivel-SMR1-blue)
![Módulo](https://img.shields.io/badge/Módulo-Montaje%20y%20Mantenimiento-lightgrey)
![Tema](https://img.shields.io/badge/Tema-BIOS%20%2F%20UEFI-success)

---

## 1. ¿Qué es la BIOS?

La **BIOS (Basic Input/Output System)** es un firmware almacenado en memoria ROM/Flash que:

- Inicializa el hardware
- Ejecuta el POST
- Permite configurar el sistema
- Carga el sistema operativo

La versión moderna es **UEFI (Unified Extensible Firmware Interface).**

---

## 2. BIOS vs UEFI

| Característica | BIOS Legacy | UEFI |
|---------------|------------|------|
| Interfaz | Texto | Gráfica |
| Disco máximo | 2TB (MBR) | >2TB (GPT) |
| Secure Boot | ❌ | ✅ |
| Velocidad | Más lenta | Más rápida |

---

## 3. POST (Power-On Self Test)

Secuencia automática al encender el equipo:

1. CPU
2. RAM
3. Tarjeta gráfica
4. Discos
5. Periféricos

## 4. Errores típicos BIOS

- Pitidos continuos → RAM mal colocada
- No detecta disco → Modo SATA incorrecto
- No arranca USB → Orden de arranque mal configurado

---

## 5. Configuración básica 

### Boot Order
USB → SSD → HDD

### Modo SATA
- IDE (obsoleto)
- AHCI (recomendado)
- RAID

### Secure Boot
- Activado: solo sistemas firmados
- Desactivado: instalaciones manuales

### Virtualización
Activar si se usan máquinas virtuales.

---  

## 6. Simulador de BIOS/UEFI online de Lenovo  

[Simulador BIOS/UEFI online](https://download.lenovo.com/bsco/index.html)





