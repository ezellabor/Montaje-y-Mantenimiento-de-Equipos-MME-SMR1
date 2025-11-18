# | Ley de Ohm y Circuitos Eléctricos en CC/DC
*Sistemas Microinformáticos y Redes* 
>- MME-SMRI - Montaje y Mantenimiento de Equipos 
>- CMO311/SMRI - Informática aplicada a sistemas electrónicos (Robótica)
>  
>Profesor: Ezequiel Llarena Borges




### Ley de Ohm  
>$V = I \cdot R$ 

Esta ley afirma que la **intensidad de la corriente (I)** que circula por un conductor eléctrico es *directamente proporcional* a la **diferencia de potencial (V)** y, paralelamente, *inversamente proporcional* a la **resistencia (R).**

![Triangulo Ley Ohm](img/ley-ohm-triangle.jpg)

---

###  1. Magnitudes eléctricas

| Magnitud              | Símbolo | Unidad (SI) | Símbolo unidad | Fórmula principal |
|-----------------------|---------|-------------|----------------|-----------------|
| Tensión o Voltaje     | V       | Voltio      | V              | $V = I \cdot R$ |
| Corriente eléctrica   | I       | Amperio     | A              | $I = \frac{V}{R}$      |
| Resistencia eléctrica | R       | Ohmio       | Ω              | $R = \frac{V}{I}$      |
| Potencia eléctrica    | P       | Vatio       | W              | $P = V \cdot I$ |
| Energía eléctrica     | E       | Julio       | J              | $E = P \cdot t$ |
| Tiempo                | t       | Segundo     | s              | —                |

---

##  2. Ejercicios básicos | Ley de Ohm

### 2.1. Indicaciones
Calcula la magnitud desconocida en cada caso. Expresa el resultado con dos decimales.

| Ejercicio | V (V) | I (A) | R (Ω) | Cálculo    |
|-----------|-------|-------|-------|------------|
| 1         | 12    | 2     | `?`    | $R = \frac{V}{I}$  |
| 2         | `?`     | 1.5   | 10    | $I = \frac{V}{R}$  |
| 3         | 24    | `?`     | 12    | $I =\frac{V}{R}$  |
| 4         | 5     | 0.02  | `?`     | $R = \frac{V}{I}$  |
| 5         | `?`     | 0.5   | 100   | $V = I \cdot R$ |

### 2.3. Conclusión
La Ley de Ohm establece una **relación directa** entre la tensión **(V), la corriente (I) y la resistencia (R)**    
>- [ ] a mayor resistencia → menor corriente para una misma tensión.

---

##  3. Circuitos en serie  

### 3.1. Características

- La corriente es igual en todos los componentes.  
- La tensión total es la suma de las tensiones parciales.  
- La resistencia total es la suma de todas las resistencias.  

### 3.2. Síntesis

- $R_T = R_1 + R_2 + R_3$  
- $V_T = V_1 + V_2 + V_3$  
- $I = \text{constante}$  

### 3.3. Esquema tipo
![Circuito en serie](img/circuito-serie.jpg)

### 3.4. Ejercicios

| Ejercicio | R₁ (Ω) | R₂ (Ω) | R₃ (Ω) | V<sub>T</sub> (V) | R<sub>T</sub> (Ω) | I (A) |
|-----------|--------|--------|--------|-----------------|-----------------|-------|
| 1         | 10     | 20     | 30     | 12              | ?               | ?     |
| 2         | 5      | 15     | 10     | 9               | ?               | ?     |
| 3         | 47     | 33     | 56     | 24              | ?               | ?     |
| 4         | 100    | 220    | 330    | 12              | ?               | ?     |
| 5         | 1 kΩ   | 1 kΩ   | 1 kΩ   | 9               | ?               | ?     |


---

## 5. Circuitos en paralelo

### 5.1. Características

- La tensión es igual en todas las ramas.  
- La corriente total es la suma de las corrientes parciales.  
- La **resistencia total** o **equvalente** se calcula como: $\frac{1}{R_T} = \frac{1}{R_1} + \frac{1}{R_2} + \frac{1}{R_3}$

### 5.2. Síntesis

- $\frac{1}{R_T} = \frac{1}{R_1} + \frac{1}{R_2} + \frac{1}{R_3}$
- $V = \text{constante}$  

### 5.3. Esquema tipo

![Circuito en paralelo](img/circuito-paralelo.jpg)

### 5.4. Ejercicios

| Ejercicio | R₁ (Ω) | R₂ (Ω) | R₃ (Ω) | V<sub>T</sub> (V) | R<sub>T</sub> (Ω) | I<sub>T</sub> (A) |
|-----------|--------|--------|--------|-----------------|-----------------|----------------|
| 1         | 100    | 200    | 300    | 12              | ?               | ?              |
| 2         | 10     | 15     | 20     | 9               | ?               | ?              |
| 3         | 22     | 33     | 47     | 12              | ?               | ?              |
| 4         | 150    | 220    | 330    | 5               | ?               | ?              |
| 5         | 470    | 680    | 1 kΩ   | 9               | ?               | ?              |


---

## 6. Circuitos mixtos

**Características:**

- Combinan partes en serie y partes en paralelo.  
- Calcular primero las resistencias en paralelo, luego sumar en serie.

**Ejercicios:**

| Ejercicio | Descripción | Datos | Cálculos requeridos |
|-----------|------------|-------|-------------------|
| 1         | R₁ en serie con (R₂ ‖ R₃) | R₁ = 10 Ω, R₂ = 20 Ω, R₃ = 30 Ω, V<sub>T</sub> = 12 V  | R<sub>T</sub>, I<sub>T</sub>, V en cada resistencia |
| 2         | (R₁ ‖ R₂) en serie con R₃ | R₁ = 100 Ω, R₂ = 200 Ω, R₃ = 50 Ω, V<sub>T</sub> = 9 V | R<sub>T</sub>, I<sub>T</sub>, V₃ |
| 3         | (R₁ en serie con R₂) ‖ R₃ | R₁ = 47 Ω, R₂ = 33 Ω, R₃ = 100 Ω, V<sub>T</sub> = 12 V | R<sub>T</sub>, corrientes parciales |

**Tabla de resultados:**

| Ejercicio | R<sub>T</sub> (Ω) | I<sub>T</sub> (A) | V<sub>R₁</sub> | V<sub>R₂</sub> | V<sub>R₃</sub> |
|-----------|-----------------|-----------------|----------------|----------------|----------------|
| 1         |                 |                 |                |                |                |
| 2         |                 |                 |                |                |                |
| 3         |                 |                 |                |                |                |

---

## 7. Síntesis

| Tipo de circuito | Fórmula R<sub>T</sub>                     | Corriente constante | Tensión constante |
|-----------------|-----------------------------------------|------------------|-----------------|
| Serie           | $R_T = R_1 + R_2 + R_3$                 | I                | —               |
| Paralelo        | $\frac{1}{R_T} = \frac{1}{R_1} + \frac{1}{R_2} + \frac{1}{R_3}$  | — | V |
| Mixto           | Combinación de ambas                     | —                | —               |

---

## 8. Conclusión 

- La Ley de Ohm relaciona voltaje, corriente y resistencia.  
- En los circuitos en serie, la corriente es la misma en todos los elementos.  
- En los circuitos en paralelo, la tensión es igual en todas las ramas.  
- En los circuitos mixtos, se aplican ambas leyes combinadas.

---

**Montaje y Mantenimiento de Equipos - SMRI**  
```Profesor: Ezequiel Llarena Borges```
