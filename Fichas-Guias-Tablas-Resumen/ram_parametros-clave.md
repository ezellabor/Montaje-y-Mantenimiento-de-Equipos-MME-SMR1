# Parámetros clave memorias RAM  
---


| **Concepto**                  | **Significado**                 | **Detalle técnico / Fórmula**                                                          | **Ejemplo**                         |
| ----------------------------- | ------------------------------- | -------------------------------------------------------------------------------------- | ----------------------------------- |
| **MHz (Frecuencia real)**     | Reloj real de la RAM            | Indica cuántos ciclos por segundo ejecuta. Las DDR hacen *2 transferencias por ciclo*. | 1600 MHz                            |
| **MT/s (Velocidad efectiva)** | MegaTransferencias por segundo  | **MT/s = MHz × 2**                                                                     | 1600 MHz = 3200 MT/s                |
| **DDR-xxxx**                  | Nombre comercial basado en MT/s | DDR4-3200 = 3200 MT/s (≈ 1600 MHz)                                                     | DDR5-6000                           |
| **CL (CAS Latency)**          | Latencia medida en ciclos       | Ciclos que tarda la RAM en entregar datos tras recibir CAS (Column Address Strobe).    | CL16, CL36                          |
| **Relación rendimiento**      | Cómo comparar memorias          | **Tiempo real (ns) ≈ (CL / MHz) × 1000**                                               | CL16 @1600 MHz ≈ 10 ns              |
| **Ancho de banda**            | Velocidad de transferencia      | Aumenta con MT/s                                                                       | DDR5-6000 → ancho de banda muy alto |
| **Latencia real (ns)**        | Tiempo de respuesta             | Menor = más rápida respondiendo                                                        | DDR4-3200 CL16 → ~10 ns             |
| **Comparación típica**        | Ancho de banda vs latencia      | DDR5: mayor ancho de banda, peor latencia pura                                         | DDR5-6000 CL36 ≈ 12 ns              |


- **MHz:** frecuencia real del reloj.
- **MT/s:** velocidad efectiva (doble de MHz en DDR).
- **CL:** número de ciclos de espera.

>Rendimiento óptimo:
>
>👉 Más MT/s + Menos CL = Mejor rendimiento general
