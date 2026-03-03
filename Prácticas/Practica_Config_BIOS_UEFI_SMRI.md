# Práctica: Configuración de BIOS / UEFI  

---

## 1. Objetivos  

El alumno será capaz de:

- Identificar el tipo de firmware de una placa base.
- Acceder a BIOS/UEFI.
- Modificar el orden de arranque.
- Configurar fecha y hora del sistema.
- Activar virtualización por hardware.
- Comprender el impacto técnico de cada configuración.

---

## 2. Placas base a configurar

1. ASUS Prime B760-Plus  
2. Gigabyte B550M DS3H  
3. MSI PRO H610M-B  
4. ASRock B450M-HDV  
5. Intel Desktop Board DH61WW  

---

## 3. Identificación del Firmware

Todas las placas modernas utilizan **UEFI (basado en AMI)** excepto modelos antiguos que pueden incluir modo Legacy/CSM.

Características comunes:

- Soporte GPT
- Secure Boot
- Virtualización (Intel VT-x o AMD SVM)
- Interfaz gráfica

---

## 4. Parámetro 1: Cambio de orden de arranque

### Objetivo
Arrancar desde USB o segundo disco.

### Ruta típica

```
Boot → Boot Option Priorities
```

---

### Captura simulada UEFI

![UEFI Boot Menu](img/01_UEFI_Boot_Menu.png)  


### Acción esperada:
Cambiar Boot Option #1 a USB.

---

## 5. Parámetro 2: Fecha y Hora

### Ruta típica

```
Main → System Date / System Time
```

---

### Captura simulada

![System Date Time](img/02_System_Date_Time.png)


### Explicación Técnica

- La fecha se almacena en el RTC.
- Si la pila CMOS se agota → se pierde la configuración.
- Puede afectar certificados, dominio, actualizaciones.

---

## 6. Parámetro 3: Activar virtualización

### Ruta Intel

```
Advanced → CPU Configuration → Intel VT-x
```

### Ruta AMD

```
Advanced → SVM Mode
```

---

### Captura simulada Virtualización


![Virtualization](img/03_Virtualization_Enable.png)


### Impacto Técnico

Si está desactivado:
- VirtualBox mostrará error VT-x disabled
- No se podrá usar virtualización por hardware

---

## 7. Parámetro adicional: Secure Boot

### Ruta

```
Boot → Secure Boot
```

---

### Captura simulada


### Secure Boot

![Secure Boot](img/04_Secure_Boot.png)


---

## 8. Procedimiento general

1. Reiniciar equipo.
2. Pulsar DEL o F2.
3. Entrar en modo Advanced.
4. Modificar parámetro.
5. Guardar con F10.
6. Confirmar reinicio.

---

## 9. Errores típicos

- No guardar cambios.
- Activar Legacy sin convertir disco a MBR.
- Desactivar Secure Boot sin necesidad.
- Confundir SVM con SMT.

---

## 10. Síntesis técnica

UEFI reemplaza al BIOS tradicional ofreciendo:

- Mayor seguridad
- Soporte GPT
- Arranque más rápido
- Soporte virtualización avanzada
- Interfaz gráfica moderna

La correcta configuración del firmware es esencial en:

- Instalaciones de sistema operativo
- Recuperación técnica
- Virtualización
- Seguridad del arranque

---

## 11. Entregable
Debe incluir:

- Identificación de firmware de cada placa.
- Ruta exacta de cada parámetro.
- Explicación técnica.
- Capturas reales o esquemas.
- Conclusión final.

---

## 12. Criterios de evaluación

| Criterio | Puntos |
|----------|--------|
| Identificación correcta | 4 |
| Cambio orden arranque | 4 |
| Fecha y hora | 3 |
| Virtualización | 4 |
| Explicación técnica | 3 |
| Presentación | 2 |

---



