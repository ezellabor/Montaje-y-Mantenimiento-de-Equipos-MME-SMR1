#  Unidad 1 | Ley de Ohm y Circuitos Eléctricos de Corriente Continua
> "Entender la electricidad es dominar la energía del futuro."

**Módulo:** Montaje y Mantenimiento de Equipos (SMR1)    
**Profesor:** Ezequiel Llarena Borges  

---

##  1. Magnitudes eléctricas

| Magnitud              | Símbolo | Unidad (SI) | Símbolo unidad | Fórmula principal |
|-----------------------|---------|-------------|----------------|-----------------|
| Tensión o Voltaje     | V       | Voltio      | V              | $V = I \times R$ |
| Corriente eléctrica   | I       | Amperio     | A              | $I = V / R$      |
| Resistencia eléctrica | R       | Ohmio       | Ω              | $R = V / I$      |
| Potencia eléctrica    | P       | Vatio       | W              | $P = V \times I$ |
| Energía eléctrica     | E       | Julio       | J              | $E = P \times t$ |
| Tiempo                | t       | Segundo     | s              | —                |

---

## 2. Símbolos eléctricos (ANSI / IEC)

| Componente / Dispositivo | Símbolo ANSI | Símbolo IEC | Descripción                          |
|-------------------------|-------------|-------------|--------------------------------------|
| Fuente de tensión continua | ⎓           | ─⎓─         | Generador de corriente continua      |
| Resistencia             | ⏤⏤⏤⏤       | ─///─       | Oposición al paso de corriente       |
| Interruptor             | —o/ o—      | ─o/ o─      | Abre o cierra el circuito           |
| Lámpara o LED           | (X) o ⊙     | ◉ o ⊙→      | Elemento luminoso                   |
| Conductor o hilo        | ─────       | ─────       | Unión entre componentes             |
| Unión de conductores    | •           | •           | Punto de conexión                    |
| Tierra o masa           | ⏚           | ⏚           | Conexión a masa                      |
| Fusible                 | ⎯⎯⎯         | ─⎯⎯─       | Protección contra sobrecorrientes   |
| Motor DC                | M           | Ⓜ           | Conversión de energía eléctrica en mecánica |

---

##  3. Ejercicios básicos | Ley de Ohm

**Instrucciones:** Calcula la magnitud desconocida en cada caso. Expresa el resultado con dos decimales.

| Ejercicio | V (V) | I (A) | R (Ω) | Cálculo    |
|-----------|-------|-------|-------|------------|
| 1         | 12    | 2     | ?     | $R = V / I$  |
| 2         | ?     | 1.5   | 10    | $I = V / R$  |
| 3         | 24    | ?     | 12    | $I = V / R$  |
| 4         | 5     | 0.02  | ?     | $R = V / I$  |
| 5         | ?     | 0.5   | 100   | $V = I \times R$ |

**Conclusión:**  
La Ley de Ohm establece una relación directa entre la tensión, la corriente y la resistencia:  
→ A mayor resistencia, menor corriente para una misma tensión.

---

##  4. Circuitos en serie  

**Características:**

- La corriente es igual en todos los componentes.  
- La tensión total es la suma de las tensiones parciales.  
- La resistencia total es la suma de todas las resistencias.  

**Fórmulas:**

- $R_T = R_1 + R_2 + R_3$  
- $V_T = V_1 + V_2 + V_3$  
- $I = \text{constante}$  

**Ejercicios:**

| Ejercicio | R₁ (Ω) | R₂ (Ω) | R₃ (Ω) | V<sub>T</sub> (V) | R<sub>T</sub> (Ω) | I (A) |
|-----------|--------|--------|--------|-----------------|-----------------|-------|
| 1         | 10     | 20     | 30     | 12              | ?               | ?     |
| 2         | 5      | 15     | 10     | 9               | ?               | ?     |
| 3         | 47     | 33     | 56     | 24              | ?               | ?     |
| 4         | 100    | 220    | 330    | 12              | ?               | ?     |
| 5         | 1 kΩ   | 1 kΩ   | 1 kΩ   | 9               | ?               | ?     |

**Esquema tipo:**  

---

## 5. Circuitos en paralelo

**Características:**

- La tensión es igual en todas las ramas.  
- La corriente total es la suma de las corrientes parciales.  
- La **resistencia total** o equvalente se calcula como:

  $\frac{1}{R_T} = \frac{1}{R_1} + \frac{1}{R_2} + \frac{1}{R_3}$

**Ejercicios:**

| Ejercicio | R₁ (Ω) | R₂ (Ω) | R₃ (Ω) | V<sub>T</sub> (V) | R<sub>T</sub> (Ω) | I<sub>T</sub> (A) |
|-----------|--------|--------|--------|-----------------|-----------------|----------------|
| 1         | 100    | 200    | 300    | 12              | ?               | ?              |
| 2         | 10     | 15     | 20     | 9               | ?               | ?              |
| 3         | 22     | 33     | 47     | 12              | ?               | ?              |
| 4         | 150    | 220    | 330    | 5               | ?               | ?              |
| 5         | 470    | 680    | 1 kΩ   | 9               | ?               | ?              |

**Esquema tipo:**  

---

## 6. Circuitos mixtos (serie + paralelo)

**Características:**

- Combinan partes en serie y partes en paralelo.  
- Calcular primero las resistencias en paralelo, luego sumar en serie.

**Ejercicios:**

| Ejercicio | Descripción | Datos | Cálculos requeridos |
|-----------|------------|-------|-------------------|
| 1         | R₁ = 10 Ω en serie con (R₂ = 20 Ω ‖ R₃ = 30 Ω), V<sub>T</sub> = 12 V | — | R<sub>T</sub>, I<sub>T</sub>, V en cada resistencia |
| 2         | (R₁ = 100 Ω ‖ R₂ = 200 Ω) en serie con R₃ = 50 Ω, V<sub>T</sub> = 9 V | — | R<sub>T</sub>, I<sub>T</sub>, V₃ |
| 3         | (R₁ = 47 Ω + R₂ = 33 Ω) en paralelo con R₃ = 100 Ω, V<sub>T</sub> = 12 V | — | R<sub>T</sub>, corrientes parciales |

**Tabla de resultados:**

| Ejercicio | R<sub>T</sub> (Ω) | I<sub>T</sub> (A) | V<sub>R₁</sub> | V<sub>R₂</sub> | V<sub>R₃</sub> |
|-----------|-----------------|-----------------|----------------|----------------|----------------|
| 1         |                 |                 |                |                |                |
| 2         |                 |                 |                |                |                |
| 3         |                 |                 |                |                |                |

---

## 7. Tabla resumen general de resultados

| Tipo de circuito | Fórmula R<sub>T</sub>                     | Corriente constante | Tensión constante |
|-----------------|-----------------------------------------|------------------|-----------------|
| Serie           | $R_T = R_1 + R_2 + R_3$                 | I                | —               |
| Paralelo        | $\frac{1}{R_T} = \frac{1}{R_1} + \frac{1}{R_2} + \frac{1}{R_3}$  | — | V |
| Mixto           | Combinación de ambas                     | —                | —               |

---

## 8. Conclusión final

- La Ley de Ohm relaciona voltaje, corriente y resistencia.  
- En los circuitos en serie, la corriente es la misma en todos los elementos.  
- En los circuitos en paralelo, la tensión es igual en todas las ramas.  
- En los circuitos mixtos, se aplican ambas leyes combinadas.

---

**Montaje y Mantenimiento de Equipos | SMR1**  
Profesor: Ezequiel Llarena Borges
