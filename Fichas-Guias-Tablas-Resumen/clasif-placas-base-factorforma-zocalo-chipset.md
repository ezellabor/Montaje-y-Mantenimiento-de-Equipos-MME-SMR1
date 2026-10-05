# Clasificación de las placas base
```Placas base y sus características principales```  

## 1. Criterios de clasificación  

Una placa base puede clasificarse atendiendo principalmente a **tres criterios**:

| Criterio | ¿Qué nos indica? | Ejemplos |
|---|---|---|
| **Factor de forma** | Tamaño y distribución física de la placa | ATX, Micro-ATX, Mini-ITX, E-ATX |
| **Zócalo o socket** | Qué procesadores son físicamente compatibles | LGA1700, LGA1851, AM4, AM5 |
| **Chipset** | Funciones, conectividad y posibilidades de expansión | B760, Z890, B650, X870 |

> **Importante:** estos tres conceptos son diferentes y no deben confundirse.

---

## 2. Clasificación según el factor de forma

El **factor de forma** describe principalmente las dimensiones físicas de la placa base y la distribución de sus componentes, conectores y ranuras de expansión.

También condiciona el tipo de caja compatible y, en general, las posibilidades de expansión.

### Principales formatos

| Formato | Dimensiones aproximadas | Características |
|---|---:|---|
| **ATX** | 305 × 244 mm | Formato estándar. Buen equilibrio entre tamaño y posibilidades de expansión. |
| **Micro-ATX** | 244 × 244 mm | Más compacto que ATX y normalmente con menos ranuras de expansión. |
| **Mini-ITX** | 170 × 170 mm | Muy compacto. Utilizado en equipos pequeños. |
| **E-ATX** | ≈ 305 × 330 mm | Mayor tamaño. Utilizado en placas de altas prestaciones y determinados equipos profesionales. |
| **Mini-DTX** | ≈ 203 × 170 mm | Formato compacto intermedio. |

### Idea clave

> **El factor de forma nos indica el tamaño y distribución física.**

---

## 3. Clasificación según el zócalo del procesador

El **zócalo**, **socket** o **zócalo de CPU** es la conexión física y eléctrica entre el procesador y la placa base.

El socket determina qué familias de procesadores pueden instalarse físicamente en la placa.

### 3.1. Principales sockets de Intel

| Socket | Ejemplos de procesadores / generaciones |
|---|---|
| **LGA775** | Pentium 4, Pentium D, Core 2 Duo, Core 2 Quad |
| **LGA1151** | Intel Core de 6.ª a 9.ª generación |
| **LGA1200** | Intel Core de 10.ª y 11.ª generación |
| **LGA1700** | Intel Core de 12.ª, 13.ª y 14.ª generación |
| **LGA1851** | Intel Core Ultra de escritorio |

---

### 3.2. Principales sockets de AMD

| Socket | Ejemplos / plataforma |
|---|---|
| **AM2** | Athlon 64 y Sempron de determinadas generaciones |
| **AM2+** | Evolución de AM2 |
| **AM3** | Phenom II y Athlon II |
| **AM3+** | Procesadores FX |
| **FM2 / FM2+** | Determinadas APU y procesadores de la familia FM |
| **AM4** | Ryzen y otras generaciones compatibles |
| **AM5** | Plataforma Ryzen actual basada en AM5 |

### Idea clave

> **El socket es el primer dato que debemos comprobar para saber si un procesador puede instalarse físicamente en una placa base.**

Pero:

> **Mismo socket ≠ compatibilidad garantizada.**

También debemos comprobar el **chipset**, el modelo concreto de procesador y, en determinados casos, la versión de **BIOS/UEFI**.

---

## 4. Clasificación según el chipset

El **chipset** es un conjunto de circuitos y funciones de la plataforma que permite gestionar buena parte de la comunicación y las características adicionales de la placa base.

Entre otras cuestiones, puede influir en:

- Conectividad.
- Puertos USB.
- Líneas y ranuras PCI Express disponibles.
- Almacenamiento.
- Posibilidades de expansión.
- Algunas funciones específicas de la plataforma.
- Características orientadas a diferentes gamas de usuario.

> **Importante:** las características exactas dependen del chipset concreto y también del modelo específico de placa base.

---

### 4.1 Chipsets Intel

Intel utiliza diferentes familias de chipsets.

| Familia | Ejemplos | Orientación general |
|---|---|---|
| **H** | H610, H670, H770, H810 | Entrada / equipos generales |
| **B** | B660, B760, B860 | Gama media / equilibrio |
| **Z** | Z690, Z790, Z890 | Gama alta / más prestaciones |
| **W** | W680, W790 | Estaciones de trabajo |

### Ejemplo

Una placa con:

**Intel Z890 + LGA1851**

nos indica una plataforma orientada a equipos de altas prestaciones basada en procesadores Intel de escritorio compatibles con **LGA1851**.

---

### 4.2 Chipsets AMD

AMD también utiliza diferentes familias de chipsets.

| Familia | Ejemplos | Orientación general |
|---|---|---|
| **A** | A320, A520, A620, A620A | Entrada |
| **B** | B350, B450, B550, B650, B850 | Gama media / equilibrio |
| **X** | X370, X470, X570, X670, X870 | Gama alta |
| **X...E** | X670E, X870E | Prestaciones y expansión avanzadas |

### Ejemplo

Una placa con:

**AMD B650 + AM5**

indica una placa de la plataforma **AM5**, con un chipset **B650**, orientado a un equilibrio entre prestaciones, conectividad y precio.

---

## 5. Los tres conceptos juntos

Una placa base puede describirse combinando sus tres características principales:

```text
                    PLACA BASE
                         │
          ┌──────────────┼──────────────┐
          │              │              │
          ▼              ▼              ▼
   FACTOR DE FORMA    SOCKET         CHIPSET
          │              │              │
          ▼              ▼              ▼
      ¿Qué tamaño?   ¿Qué CPU?    ¿Qué funciones?
          │              │              │
       ATX            AM5           B650
   Micro-ATX        LGA1851        Z890
    Mini-ITX        LGA1700        B760
```

---

## 6. Ejemplo de placa base 1

Supongamos una placa con estas características:

| Característica | Valor |
|---|---|
| Fabricante de CPU | AMD |
| Factor de forma | ATX |
| Socket | AM5 |
| Chipset | B650 |
| Memoria | DDR5 |

### ¿Cómo debemos interpretarla?

- **ATX** → nos indica el tamaño y distribución física.
- **AM5** → nos indica la plataforma de procesador compatible.
- **B650** → nos indica el chipset y buena parte de las características de la plataforma.
- **DDR5** → nos indica el tipo de memoria compatible con esa placa.

> Una placa ATX no tiene por qué ser AMD. También existen placas ATX para Intel.

---

## 7. Ejemplo de placa base 2:

Supongamos una placa con:

| Característica | Valor |
|---|---|
| Fabricante de CPU | Intel |
| Factor de forma | ATX |
| Socket | LGA1851 |
| Chipset | Z890 |

### ¿Cómo debemos interpretarla?

- **ATX** → tamaño y distribución física.
- **LGA1851** → socket de la CPU.
- **Z890** → chipset de gama alta de la plataforma.
- **Intel** → fabricante de los procesadores compatibles con esta plataforma.

Además, una placa Intel LGA1851 puede existir en diferentes factores de forma:

- ATX.
- Micro-ATX.
- Mini-ITX.

Por tanto:

> **Socket y factor de forma son características independientes.**

---

## 8. Tabla resumen

| Criterio | Pregunta que responde | Ejemplos |
|---|---|---|
| **Factor de forma** | ¿Qué tamaño y distribución tiene? | ATX, Micro-ATX, Mini-ITX |
| **Socket** | ¿Qué procesador/plataforma es compatible? | LGA1700, LGA1851, AM4, AM5 |
| **Chipset** | ¿Qué funciones y posibilidades de expansión ofrece? | B760, Z890, B650, X870 |

---

## 9. Regla para recordar

Para identificar rápidamente una placa base debemos buscar:

```text
FACTOR DE FORMA
       +
    SOCKET
       +
    CHIPSET
```

### Ejemplo

```text
ATX + AM5 + B650
```

Se interpreta como:

> **Placa ATX → plataforma AM5 → chipset B650**

Otro ejemplo:

```text
ATX + LGA1851 + Z890
```

Se interpreta como:

> **Placa ATX → socket LGA1851 → chipset Z890**

---

## 10. Preguntas de repaso

### 1. ¿Qué característica determina principalmente el tamaño físico de la placa?

**Respuesta:** el factor de forma.

### 2. ¿Qué característica debemos comprobar para saber si un procesador puede instalarse físicamente?

**Respuesta:** el socket.

### 3. ¿Qué es AM5?

**Respuesta:** un socket/plataforma de procesador de AMD.

### 4. ¿Qué es LGA1851?

**Respuesta:** un socket de procesador de Intel.

### 5. ¿Qué es B650?

**Respuesta:** un chipset de AMD para la plataforma AM5.

### 6. ¿Qué es Z890?

**Respuesta:** un chipset de Intel para la plataforma de escritorio asociada a LGA1851.

### 7. ¿Una placa ATX tiene que ser necesariamente Intel?

**Respuesta:** no. ATX solamente indica el factor de forma.

### 8. ¿Dos placas AM5 tienen que ser exactamente iguales?

**Respuesta:** no. Pueden utilizar diferentes chipsets, formatos, conectividad, ranuras de expansión y características.

---

## Resumen final

> **FACTOR DE FORMA → tamaño físico**

> **SOCKET → compatibilidad física con el procesador**

> **CHIPSET → funciones, conectividad y expansión**

Estos tres conceptos permiten realizar una primera identificación técnica de cualquier placa base y comprobar si sus componentes principales son compatibles.

---

**Montaje y Mantenimiento de Equipos | Profesor: Ezequiel Llarena Borges**
