# Memoria RAM
```Ficha resumen```


La RAM (Random Access Memory) es la memoria donde el ordenador guarda datos temporales mientras está en uso.  
Cuanta más RAM y mejor configurada esté, mejor rendimiento tendrá el sistema.

---

## Módulos y ranuras (slots DIMM)

- La RAM se instala en ranuras DIMM de la placa base.
- Cada módulo es independiente, pero pueden trabajar en conjunto.
- La placa base determina el tipo y la cantidad máxima soportada.
- Factor de forma **SO-DIMM**: placa base incorpora módulos de RAM extraíbles para ampliar fácilmente.
- **Row of Chips**: los módulos de RAM están soldados a la placa base y no se podrá ampliar.

---

## Dual Channel

Las ranuras de distinto color indican los **canales de memoria**.

- La mayoría de placas base usan **Dual Channel**.
- Cada canal suele tener dos ranuras del mismo color.

**Regla básica:**
Si tienes 2 módulos de RAM, colócalos en las ranuras del mismo color  
(normalmente A2 y B2) para activar el Dual Channel y mejorar el rendimiento.

---

## Compatibilidad DDR3, DDR4 y DDR5

Los distintos tipos de RAM **no son compatibles entre sí**.  
Cada placa base solo admite un tipo concreto.

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

## Cómo diferenciarlas rápidamente

| Tipo | Pines | Muesca | Detalle distintivo | Fecha Lanzamiento | Capacidad/Módulo
|------|-------|--------|--------------------|-------------------|-----------------|
| DDR3 | 240   | Casi centrada | Más antigua | 2007 | 1GB-8GB |
| DDR4 | 288   | Desplazada | Muy común | 2014 | 8GB-16GB |
| DDR5 | 288   | Más desplazada | Chip PMIC visible |2020 | 16GB-128GB)

---

## Consejos prácticos

- Nunca fuerces un módulo de RAM.
- Si no encaja fácilmente, no es compatible.
- Consulta siempre las especificaciones de la placa base.
- Busca: `modelo placa base + memory support`.

---

## Resumen rápido

- Usa ranuras del mismo color para Dual Channel.
- No mezcles DDR3, DDR4 y DDR5.
- La placa base determina qué RAM puedes usar.
