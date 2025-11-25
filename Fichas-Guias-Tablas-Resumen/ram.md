
# Memoria Principal: Randon Access Memory (RAM)


## 1. Tipos

| Generación | Año aprox | Velocidad típica | Voltaje |
| ---------- | --------- | ---------------- | ------- |
| **DDR1**   | 2000      | 200–400 MT/s     | 2.5 V   |
| **DDR2**   | 2004      | 400–1066 MT/s    | 1.8 V   |
| **DDR3**   | 2007      | 800–2133 MT/s    | 1.5 V   |
| **DDR4**   | 2014      | 2133–3600+ MT/s  | 1.2 V   |
| **DDR5**   | 2021      | 4800–8400+ MT/s  | 1.1 V   |

| Acrónimo | Significado           | Descripción                              |
| -------- | --------------------- | ---------------------------------------- |
| **MT/s** | MT/s = MegaTransfers por segundo | Es la unidad que mide la velocidad real de transferencia de la RAM |

>**IMPORTANTE:**  
>- MT/s NO es exactamente lo mismo que MHz.
>- MT/s es la medida correcta de velocidad de RAM, no MHz.
>- DDR4 3200 MHz → en realidad trabaja a 1600 MHz pero con doble transferencia → 3200 MT/s.
>- DDR significa Double Data Rate, por eso transmite 2 datos por ciclo.
>- DDR no es compatible entre generaciones (muesca distinta).

---


## 2. Especificaciones clave 

| Parámetro | Valores típicos | Recomendación por uso |
|---------------|-----------------|----------------------|
| **Capacidad** | 4 GB, 8 GB, 16 GB, 32-64 GB | • 4 GB → Básico<br>• 8 GB → Uso general<br>• 16 GB → Gaming/Productividad<br>• 32-64 GB → Edición/Máquinas virtuales |
| **Frecuencia** | 3200 MHz, 3600 MHz, 5200 MHz | Mayor frecuencia = Mayor ancho de banda |
| **Latencias (CL)** | CL16, CL18, CL22 | Latencia baja = Mejor (diferencias pequeñas en uso real) |
| **Voltaje** | DDR4: 1.2V, DDR5: 1.1V | XMP/EXPO puede subir voltaje para overclock seguro |
| **Canales** | Single, Dual, Quad | • Single → Más lento<br>• Dual → Recomendado<br>• Quad → Estaciones y servidores |

| Acrónimo | Significado           | Descripción                              |
| -------- | --------------------- | ---------------------------------------- |
| **CAS**  | Column Address Strobe | Pulso/orden para seleccionar una columna |
| **CL**   | CAS Latency (latencia CAS) | Es el número de ciclos que tarda la RAM en entregar un dato después de que el controlador de memoria lo pide. |  

>Cuanto menor es el CL → más rápida es la respuesta.  
>_Ejemplo:_ CL16 responde antes que CL18, aunque tengan misma velocidad.

## 3. Factores físicos

| Formato     | Uso        | Imagen mental        |
| ----------- | ---------- | -------------------- |
| **DIMM**    | Sobremesa  | Módulo largo (13 cm) |
| **SO-DIMM** | Portátiles | Módulo corto (7 cm)  |


## 4. Identificación de una RAM

Etiqueta del fabricante:  
- Tipo → DDR3 / DDR4 / DDR5
- Velocidad → 3200 MHz, 5200 MT/s…
- Latencia → CL16, CL40…
- Capacidad → 8 GB / 16 GB
- Voltaje → 1.2 V, 1.35 V (XMP)

## 5. Compatibilidad

Factores clave:  
- Placa base (chipset)  
- Tipo soportado (DDR3/4/5)
- Frecuencia máxima
- Slots disponibles
- CPU (controlador de memoria integrado)

>- No mezclar DDR3 con DDR4, ni DDR4 con DDR5.
>- Mezclar módulos distintos funciona, pero baja al rendimiento.

---

## 6. Fallos típicos de la RAM

- Pantallazos azules (BSOD)
- Bloqueos aleatorios
- Reinicios
- Programas que fallan sin motivo
- No arranca / pitidos de BIOS

>Recomendación: Herramienta _MemTest86_ (diagnóstico completo)

---

## 7. Buenas prácticas  

- Usar dual channel (2 módulos iguales)
- No mezclar marcas/modelos si puedes evitarlo
- Activar XMP/EXPO en BIOS para rendimiento real
- Mantener módulos limpios (polvo) y bien insertados
- Comprobar compatibilidad antes de comprar

---

## 8. Síntesis  

>- TIPO → DDR4 / DDR5  
>- VELOCIDAD → MHz / MT/s
>- LATENCIA → CL
>- CANAL → Single / Dual
>- FORMATO → DIMM / SO-DIMM
>- VOLTAJE → 1.2–1.35 V
>- USO → Sistema operativo, programas, datos temporales








