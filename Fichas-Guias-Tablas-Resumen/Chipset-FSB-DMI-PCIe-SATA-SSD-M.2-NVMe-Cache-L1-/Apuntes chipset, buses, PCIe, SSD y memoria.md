# Apuntes: chipset, buses, PCIe, SSD y memoria
```Montaje y mantenimiento de Equipos - Prof. Ezequiel LLarena Borges```  

## 1. Del Northbridge al PCH

Hoy queda un solo chipset, el PCH. El Northbridge desapareció porque su trabajo se mudó dentro de la CPU.

### Antes: dos chipsets

- **Northbridge (puente norte).** Pegado a la CPU. Llevaba lo rápido: la memoria RAM y la tarjeta gráfica. Hacía de puente entre la CPU y el Southbridge.
- **Southbridge (puente sur).** Llevaba lo lento: discos (SATA), USB, audio, red y ranuras PCI.

La RAM siempre hablaba con la CPU a través del Northbridge. El camino de un dato era: CPU → FSB → Northbridge → bus de memoria → RAM.

### Los dos buses antiguos

- **FSB (Front Side Bus).** Unía la CPU con el Northbridge. Era la salida principal del procesador hacia el resto del equipo.
- **Bus de memoria.** Unía el Northbridge con la RAM.

### El controlador de memoria

Es el circuito que gestiona el diálogo con la RAM. La CPU no busca los datos directamente en los chips: le pide al controlador "tráeme lo que hay en tal dirección". El controlador activa la fila y la columna correctas, respeta los tiempos (timings) y refresca las celdas para que no se borren.

Analogía: es el bibliotecario. No entras tú a los pasillos; se lo pides a él y te trae el libro.

El controlador siempre ha existido. Lo que cambió es dónde vive: antes en el Northbridge, ahora dentro de la CPU.

### Por qué se mudó a la CPU

Por la distancia. Cada petición a la RAM salía de la CPU, viajaba al Northbridge y volvía. La CPU, a miles de millones de ciclos por segundo, se quedaba esperando. Meter el controlador dentro del procesador reduce la distancia y el retardo y aumenta el ancho de banda.

- AMD lo hizo primero, con los Athlon 64 (2003).
- Intel lo hizo con la arquitectura Nehalem (2008).

Lo mismo pasó con las líneas PCI Express de la gráfica: también se metieron en la CPU.

Consecuencia práctica: como el controlador vive en la CPU, es el procesador quien decide qué tipo de RAM admite el equipo (DDR4 o DDR5).

### Ahora: un solo chipset

Sin controlador de memoria ni PCIe de la gráfica, el Northbridge se quedó sin función y desapareció. No es que se fusionaran norte y sur: el norte se mudó dentro de la CPU y el sur se quedó solo fuera.

- **PCH (Platform Controller Hub).** Es el antiguo Southbridge. Es el único chipset que queda.
- **DMI (Direct Media Interface).** Une la CPU con el PCH. Es, en cierto modo, el heredero del FSB. Ojo: Media, no Memory.

El mapa actual:

- RAM → directa a la CPU.
- Gráfica principal (PCIe x16) → directa a la CPU.
- SSD M.2 principal → normalmente directo a la CPU.
- SATA, USB, red, audio y PCIe secundario → a través del PCH, que llega a la CPU por el DMI.

**Idea clave:** el chipset no gestiona "lo lento". Mezcla cosas lentas (USB, SATA) con cosas rápidas (PCIe secundario). La diferencia es *directo a la CPU* o *a través del chipset*.

### Gráficas

- **Integrada y dedicada conviven.** Muchas CPU traen gráfica integrada. Si el usuario necesita más potencia, añade una dedicada en la ranura x16.
- **Dos gráficas dedicadas.** Se puede si hay dos ranuras x16. Antes se juntaban para sumar potencia (SLI de NVIDIA, CrossFire de AMD), pero eso está casi abandonado. Hoy, si se ponen dos, suele ser para tareas separadas: una para juegos y otra para cálculo o más monitores.

## 2. Ranuras PCI Express

El tamaño de una ranura PCIe indica cuántos carriles tiene, es decir, su ancho de banda. No indica su función: no existe una ranura "solo de vídeo".

### Qué va en cada ranura

| Ranura | Carriles | Usos típicos | Dónde se ve |
| --- | --- | --- | --- |
| x1 | 1 | Sonido, red de 1 Gb, wifi y bluetooth, USB extra, captura sencilla, controladora SATA | Muy común en placas de casa |
| x4 | 4 | SSD NVMe en adaptador, RAID mediana, red de 10 Gb modesta | Poco visible; a menudo disfrazada de x16 física |
| x8 | 8 | Segunda gráfica con carriles repartidos, controladoras potentes, red rápida, aceleradoras | Gama alta, estaciones de trabajo, servidores |
| x16 | 16 | Gráfica principal y tarjetas muy exigentes | Todas las placas |

En placas ATX o micro ATX de casa lo normal es ver una o dos x16 y varias x1. Las x4 y x8 como ranura física son de gama alta.

### Qué más cabe en una x16

En un PC de casa o de aula, el 99 % de las veces va la gráfica. Pero técnicamente admite cualquier tarjeta de alto rendimiento:

- Tarjetas de captura de vídeo profesionales.
- Controladoras RAID o HBA, para conectar muchos discos (servidores).
- Tarjetas de red de 10, 25 o 40 Gb.
- Adaptadores con varios SSD NVMe a la vez.
- Aceleradoras de cálculo o de inteligencia artificial.
- Tarjetas de sonido de gama muy alta.

Sobre la red: la de 1 Gb va integrada en la placa y no necesita ranura. Las de 10 Gb o más sí, porque necesitan muchos carriles para aprovechar el canal. En una ranura con pocos carriles se ahogarían.

### Física no es igual a eléctrica

- La ranura x16 más cercana a la CPU suele salir directa del procesador, con los 16 carriles reales. Es la buena para la gráfica.
- Una segunda x16 más abajo suele colgar del PCH y funcionar a x4 o x8. Tiene tamaño de x16 para que quepa cualquier tarjeta, pero lleva menos carriles.
- El manual de la placa indica cuántos carriles reales tiene cada ranura.

### Por qué hay varias ranuras grandes

No es desperdicio, es flexibilidad.

1. Caben tarjetas grandes donde el usuario quiera (compatibilidad).
2. La CPU tiene un número limitado de carriles y la placa los reparte: con una sola gráfica, x16; con dos tarjetas, x8 + x8.
3. La misma placa sirve para un PC de casa, una estación de trabajo o un pequeño servidor.

### Generaciones de PCIe

Cada generación dobla la velocidad de la anterior con los mismos carriles. Ejemplo con un SSD NVMe de 4 carriles (valores aproximados):

| Generación | Velocidad aprox. con x4 |
| --- | --- |
| PCIe 3.0 | 3.500 MB/s |
| PCIe 4.0 | 7.000 MB/s |
| PCIe 5.0 | 14.000 MB/s |

Por eso no basta con mirar los carriles: también importa la generación. Cuatro carriles de generación 5 van más rápido que ocho de generación 3. La placa y la CPU tienen que soportar esa generación.

## 3. Unidades SSD

La velocidad de un SSD la marcan la conexión (SATA o PCIe) y el protocolo (AHCI o NVMe), no el conector donde se enchufa.

### Tres conceptos que no hay que mezclar

| Concepto | Qué es | Ejemplos | Analogía |
| --- | --- | --- | --- |
| Conector | Dónde se enchufa | Cable SATA, ranura M.2 | El grifo |
| Conexión | Por dónde viajan los datos | SATA, PCIe | La tubería |
| Protocolo | Cómo se piden los datos | AHCI, NVMe | El idioma en que pides el agua |

- **AHCI.** Protocolo antiguo, pensado para discos duros mecánicos. Funciona, pero con el freno de mano puesto.
- **NVMe (Non-Volatile Memory Express).** Protocolo diseñado desde cero para memoria flash. Permite muchas más órdenes a la vez y aprovecha el PCIe.

### La ranura M.2

M.2 es una ranura física pequeña donde el SSD se pincha directo a la placa, sin cables. No es un tercer sistema: por debajo de un M.2 siempre hay PCIe o SATA.

- M.2 cableado a **PCIe** (4 carriles, x4) → SSD NVMe, rápido.
- M.2 cableado a **SATA** → mismo tope que un SSD SATA de cable, unos 550-600 MB/s.
- Algunas ranuras M.2 admiten los dos tipos y otras solo uno. Lo dice el manual.

Un NVMe usa sus propios 4 carriles PCIe, reservados para el M.2. No ocupa una ranura PCIe de tarjetas.

### Los tres tipos reales de SSD

| Tipo | Conector | Conexión | Protocolo | Velocidad aprox. |
| --- | --- | --- | --- | --- |
| SSD SATA 2,5" | Cable SATA | SATA | AHCI | 550-600 MB/s |
| SSD M.2 SATA | Ranura M.2 | SATA | AHCI | 550-600 MB/s |
| SSD M.2 NVMe | Ranura M.2 | PCIe x4 | NVMe | 3.500-14.000 MB/s |

Los dos primeros van igual de rápido: cambia la forma, no la velocidad. Por eso no se pueden dividir los SSD en "M.2 o SATA". Un SSD M.2 puede ser lento o rápido; hay que mirar la ficha.

### Disco duro mecánico frente a SSD SATA

El disco duro (HDD) y el SSD SATA usan el mismo cable y el mismo puerto. Pero el HDD se queda en unos 100-150 MB/s porque lo frena la mecánica: platos que giran y un cabezal que se mueve. El SSD SATA no tiene partes móviles y llega al tope del SATA.

Escalera de velocidad, de menos a más:

1. Disco duro mecánico: unos 150 MB/s.
2. SSD SATA (cable o M.2): unos 550 MB/s.
3. SSD NVMe por PCIe: de 3.500 a 14.000 MB/s, según la generación.

### Avisos de montaje

- Muchas placas comparten carriles entre M.2 y SATA: al usar cierta ranura M.2 se desactivan algunos puertos SATA.
- Un M.2 puede colgar de la CPU o del PCH. El de la CPU va algo más fino, aunque en el día a día casi no se nota.
- Regla de oro: leer el manual de la placa antes de montar.

## 4. Jerarquía de memoria y caché

La caché se divide en tres niveles porque es el mejor equilibrio entre velocidad, tamaño y coste. No existe una memoria que sea a la vez enorme y muy rápida.

### La pirámide

| Nivel | Dónde está | Tamaño orientativo |
| --- | --- | --- |
| Registros | Dentro del núcleo | Bytes |
| Caché L1 | Pegada a cada núcleo | Decenas de KB |
| Caché L2 | Junto a cada núcleo | Cientos de KB a pocos MB |
| Caché L3 | Dentro de la CPU, compartida por todos los núcleos | Varios MB |
| RAM | Fuera de la CPU | GB |
| SSD / HDD | Almacenamiento permanente | TB |

Cuanto más arriba, más rápida, más cara y más pequeña. Cuanto más abajo, más grande, más barata y más lenta. Los registros y la L1 son primos hermanos: lo más alto de la pirámide.

### Qué hace cada nivel de caché

- **L1.** Minúscula y rapidísima. Guarda lo que la CPU va a usar ahora mismo. Es tan cara y ocupa tanto que cabe muy poca.
- **L2.** Más grande y algo más lenta. Es el segundo cajón.
- **L3.** Bastante más grande y más lenta. Compartida por todos los núcleos. Es el último colchón antes de ir a la RAM.

### Por qué tres niveles

- **Uno solo no basta:** no puede ser rápido y grande a la vez.
- **Antes había dos (L1 y L2).** Al meter muchos núcleos en un procesador hizo falta una capa grande y compartida: nació la L3.
- **Un cuarto nivel apenas compensa:** cada capa es un sitio más donde buscar antes de encontrar el dato, y eso cuesta tiempo y complejidad. Algunos procesadores muy potentes añaden caché extra apilada, pero la regla general son tres niveles.

### Cómo busca la CPU un dato

1. Mira en los registros.
2. Si no está, baja a la L1; después a la L2 y a la L3.
3. Si tampoco está, va a la RAM, que es un viaje largo.
4. Si no está en la RAM, va al SSD o disco, que para la CPU es una eternidad.
5. Cuando encuentra el dato abajo, lo sube a los niveles de arriba por si lo vuelve a necesitar.

- **Acierto (hit):** el dato está en el nivel donde se busca.
- **Fallo (miss):** no está y hay que bajar al siguiente.

Funciona tan bien por la **localidad**: los programas usan los mismos datos una y otra vez en poco tiempo, y datos que están cerca unos de otros. Por eso subir a la caché lo que se acaba de usar acierta muy a menudo.

## 5. Extra: electricidad estática en el taller

La pulsera antiestática protege al componente, no a la persona.

- **Descarga electrostática (ESD, ElectroStatic Discharge).** Es el fenómeno. El cuerpo acumula carga al moverse, al rozar la ropa o al caminar sobre moqueta, y puede llegar a miles de voltios sin notarlo. Al tocar un componente, esa carga se descarga de golpe a través de él y puede dañarlo.
- **Pulsera antiestática.** Es la protección. Mantiene a la persona al mismo potencial que el equipo y drena la carga poco a poco a tierra. Sin diferencia de potencial no hay chispazo.

Truco para no confundirse: la descarga es *electrostática* (nombra el fenómeno) y la pulsera es *antiestática* (va contra él).

### Demostración con polímetro

Un polímetro no sirve para medir la carga estática: su impedancia de entrada (unos 10 MΩ) descarga lo poco que hay y el número no es fiable. Para medirla de verdad se usa un electrómetro o un medidor de campo electrostático.

Sí sirve para **comparar** entre alumnos, siempre con el mismo aparato y en las mismas condiciones: quien marca más lleva más carga que quien marca menos. El número no vale; la diferencia sí. Buena actividad distendida al principio o al final del taller.

## 6. Resumen para memorizar

1. Antes había dos chipsets: Northbridge (RAM y gráfica) y Southbridge (lo demás).
2. FSB = CPU ↔ Northbridge. Bus de memoria = Northbridge ↔ RAM.
3. El controlador de memoria se mudó del Northbridge a la CPU (AMD 2003, Intel 2008). Motivo: menos distancia, más velocidad.
4. El Northbridge desapareció. RAM y gráfica principal van directas a la CPU.
5. Queda un chipset, el PCH (antiguo Southbridge), unido a la CPU por el DMI (Direct Media Interface).
6. La diferencia no es rápido o lento: es directo a la CPU o a través del chipset.
7. Ranuras PCIe: el tamaño son carriles (ancho de banda), no función. x1 para lo ligero, x16 para lo más exigente.
8. Una x16 física puede funcionar a x4 o x8. La de arriba, junto a la CPU, es la buena.
9. Cada generación de PCIe dobla la velocidad con los mismos carriles.
10. SSD: lo que manda es conexión + protocolo. SATA/AHCI ≈ 550 MB/s. PCIe/NVMe = miles de MB/s.
11. M.2 es solo el conector: por debajo hay PCIe o SATA. Tres tipos: SATA 2,5", M.2 SATA y M.2 NVMe.
12. Caché en tres niveles: el mejor equilibrio entre velocidad, tamaño y coste. Registros → L1 → L2 → L3 → RAM → SSD.
13. Siempre: leer el manual de la placa antes de montar.
