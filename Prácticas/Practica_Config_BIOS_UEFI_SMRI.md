# PRÁCTICA 05  
# CONFIGURACIÓN DE BIOS / UEFI  
## Manual Técnico Guiado con Simulación Visual

---

# 1. Objetivos

El alumno será capaz de:

- Identificar el tipo de firmware de una placa base.
- Acceder a BIOS/UEFI.
- Modificar el orden de arranque.
- Configurar fecha y hora del sistema.
- Activar virtualización por hardware.
- Comprender el impacto técnico de cada configuración.

---

# 2. Placas Base Analizadas

1. ASUS Prime B760-Plus  
2. Gigabyte B550M DS3H  
3. MSI PRO H610M-B  
4. ASRock B450M-HDV  
5. Intel Desktop Board DH61WW  

---

# 3. IDENTIFICACIÓN DEL FIRMWARE

Todas las placas modernas utilizan **UEFI (basado en AMI)** excepto modelos antiguos que pueden incluir modo Legacy/CSM.

Características comunes:

- Soporte GPT
- Secure Boot
- Virtualización (Intel VT-x o AMD SVM)
- Interfaz gráfica

---

# 4. PARÁMETRO 1 – CAMBIO DE ORDEN DE ARRANQUE

## Objetivo
Arrancar desde USB o segundo disco.

## Ruta típica

```
Boot → Boot Option Priorities
```

---

## Captura simulada UEFI (SVG Profesional)

<svg width="700" height="420" xmlns="http://www.w3.org/2000/svg">
<rect width="700" height="420" fill="#1e1e1e"/>
<text x="20" y="40" fill="#00ffcc" font-size="22">UEFI BIOS Utility - Boot</text>

<rect x="50" y="80" width="600" height="60" fill="#2c2c2c" stroke="#00ffcc"/>
<text x="70" y="115" fill="white" font-size="18">Boot Option #1   → Windows Boot Manager</text>

<rect x="50" y="160" width="600" height="60" fill="#2c2c2c" stroke="#00ffcc"/>
<text x="70" y="195" fill="white" font-size="18">Boot Option #2   → Samsung SSD</text>

<rect x="50" y="240" width="600" height="60" fill="#003366" stroke="#00ffcc"/>
<text x="70" y="275" fill="white" font-size="18">Boot Option #3   → USB Kingston</text>

<text x="50" y="350" fill="#00ffcc" font-size="16">F10 → Save Changes & Reset</text>
</svg>


### Acción esperada:
Cambiar Boot Option #1 a USB.

---

# 5. PARÁMETRO 2 – CONFIGURAR FECHA Y HORA

## Ruta típica

```
Main → System Date / System Time
```

---

## Captura simulada

<svg width="700" height="350" xmlns="http://www.w3.org/2000/svg">
<rect width="700" height="350" fill="#1a1a1a"/>
<text x="20" y="40" fill="#4fc3f7" font-size="22">UEFI BIOS Utility - Main</text>

<rect x="80" y="100" width="540" height="70" fill="#2e2e2e" stroke="#4fc3f7"/>
<text x="100" y="140" fill="white" font-size="20">System Date  →  03 / 03 / 2026</text>

<rect x="80" y="200" width="540" height="70" fill="#2e2e2e" stroke="#4fc3f7"/>
<text x="100" y="240" fill="white" font-size="20">System Time  →  10 : 45 : 22</text>
</svg>


### Explicación Técnica

- La fecha se almacena en el RTC.
- Si la pila CMOS se agota → se pierde la configuración.
- Puede afectar certificados, dominio, actualizaciones.

---

# 6. PARÁMETRO 3 – ACTIVAR VIRTUALIZACIÓN

## Ruta Intel

```
Advanced → CPU Configuration → Intel VT-x
```

## Ruta AMD

```
Advanced → SVM Mode
```

---

## Captura simulada Virtualización


<svg width="700" height="380" xmlns="http://www.w3.org/2000/svg">
<rect width="700" height="380" fill="#121212"/>
<text x="20" y="40" fill="#81c784" font-size="22">Advanced - CPU Configuration</text>

<rect x="80" y="110" width="540" height="80" fill="#1f1f1f" stroke="#81c784"/>
<text x="100" y="150" fill="white" font-size="20">Intel Virtualization Technology → Disabled</text>

<rect x="80" y="230" width="540" height="80" fill="#003300" stroke="#81c784"/>
<text x="100" y="270" fill="white" font-size="20">Cambiar a → Enabled</text>
</svg>


### Impacto Técnico

Si está desactivado:
- VirtualBox mostrará error VT-x disabled
- No se podrá usar virtualización por hardware

---

# 7. PARÁMETRO ADICIONAL – SECURE BOOT

## Ruta

```
Boot → Secure Boot
```

---

## Captura simulada


<svg width="700" height="360" xmlns="http://www.w3.org/2000/svg">
<rect width="700" height="360" fill="#101820"/>
<text x="20" y="40" fill="#ffcc00" font-size="22">Security - Secure Boot</text>

<rect x="100" y="130" width="500" height="90" fill="#2b2b2b" stroke="#ffcc00"/>
<text x="120" y="180" fill="white" font-size="20">Secure Boot → Enabled</text>

<text x="100" y="280" fill="#ffcc00" font-size="16">
Desactivar solo si se instala sistema no firmado
</text>
</svg>


---

# 8. PROCEDIMIENTO GENERAL PASO A PASO

1. Reiniciar equipo.
2. Pulsar DEL o F2.
3. Entrar en modo Advanced.
4. Modificar parámetro.
5. Guardar con F10.
6. Confirmar reinicio.

---

# 9. ERRORES COMUNES

- No guardar cambios.
- Activar Legacy sin convertir disco a MBR.
- Desactivar Secure Boot sin necesidad.
- Confundir SVM con SMT.

---

# 10. ENTREGABLE DEL ALUMNO

Debe incluir:

- Identificación de firmware de cada placa.
- Ruta exacta de cada parámetro.
- Explicación técnica.
- Capturas reales o esquemas.
- Conclusión final.

---

# 11. CRITERIOS DE EVALUACIÓN

| Criterio | Puntos |
|----------|--------|
| Identificación correcta | 4 |
| Cambio orden arranque | 4 |
| Fecha y hora | 3 |
| Virtualización | 4 |
| Explicación técnica | 3 |
| Presentación | 2 |

---

# 12. CONCLUSIÓN TÉCNICA

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

FIN DEL DOCUMENTO
