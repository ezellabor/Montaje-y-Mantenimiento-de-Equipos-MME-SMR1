# Memoria RAM
```Ficha resumen```


La **RAM (Random Access Memory)** es la memoria donde el ordenador guarda datos temporales mientras está en uso.  
Cuanta más RAM y mejor configurada esté, mejor rendimiento tendrá el sistema.

---

## Módulos y ranuras (slots DIMM)

- La RAM se instala en ranuras **DIMM** de la placa base.
- Cada módulo es independiente, pero pueden trabajar en conjunto.
- La placa base y su **factor de forma** determinan el tipo y la cantidad máxima de RAM soportada.
- Factor de forma **SO-DIMM**: placa base incorpora módulos de RAM **extraíbles** para ampliar fácilmente.
- **Row of Chips** (Fila de chips): los módulos RAM están **soldados** a la placa base y no se podrá ampliar.

---

## Dual Channel

Las ranuras de distinto color indican los **canales de memoria**.

- La mayoría de placas base usan **Dual Channel**.
- Cada canal suele tener dos ranuras del mismo color.

**Regla básica:**
Si tienes 2 módulos de RAM, colócalos en las ranuras del mismo color  
(normalmente A2 y B2) para activar el Dual Channel y mejorar el rendimiento.

---

### DDR3
- Año aproximado: 2007–2014
- 240 pines
- Muesca casi centrada
- Voltaje típico: 1.5 V

---

### DDR4
- Año aproximado: 2014–2022
- 288 pines
- Muesca desplazada respecto a DDR3
- Voltaje típico: 1.2 V

---

### DDR5
- El estándar actual (desde 2021)
- 288 pines (no compatible con DDR4)
- Muesca en distinta posición
- Incluye chip PMIC (gestión de energía)
- Mayor velocidad y eficiencia
- Voltaje típico: 1.1 V

---

## Cómo reconocer módulo RAM visualmente

| Tipo | Pines | Muesca | Detalle distintivo | Capacidad/Módulo |
|------|-------|--------|--------------------|------------------|
| **DDR3** | 240   | Casi centrada | Más antigua | 1GB-8GB |
| **DDR4** | 288   | Desplazada | Muy común | 8GB-16GB |
| **DDR5** | 288   | Más desplazada | Chip PMIC visible | 16GB-128GB |

---

## Compatibilidad DDR3, DDR4 y DDR5

- Los distintos tipos de RAM **no son compatibles entre sí** (la tecnología DDR4, no podrá soportar módulos DDR5).
- Cada tipo de memoria tiene diferentes ubicaciones de muesca (importantes para la instalación) y las placas madre soportan sólo una ubicación de muesca.
- Las placas base son generalmente capaces de soportar sólo un tipo de tecnología de memoria.

---

## Recomendaciones

- Nunca fuerces un módulo de RAM (si no encaja fácilmente, no es compatible)
- Consulta siempre las **especificaciones y/o manual** de la placa base.
- Usa ranuras del **mismo color** para Dual Channel.
- No mezcles DDR3, DDR4 y DDR5.
- La placa base determina qué RAM puedes usar.
