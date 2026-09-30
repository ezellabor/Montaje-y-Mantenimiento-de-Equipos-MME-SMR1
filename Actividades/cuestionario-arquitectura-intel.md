# Cuestionario — Introducción a la Arquitectura Intel®

**Módulo:** MME · 1º SMR
**Profesor:** Ezequiel Llarena Borges

**Nombre y apellidos:** ______________________________ **Grupo:** __________ **Fecha:** __________

Marca con una X la opción correcta en cada pregunta.

---

**1. ¿Qué es la arquitectura Intel®?**

☐ a) Un único modelo de procesador
☐ b) El conjunto de microprocesadores y hardware de soporte que forma la base de muchos sistemas informáticos
☐ c) Un sistema operativo desarrollado por Intel
☐ d) Una marca exclusiva para ordenadores portátiles

**2. ¿Cuál fue el primer microprocesador de Intel®, fabricado en 1971?**

☐ a) Intel 8086
☐ b) Intel 80386
☐ c) Intel 4004
☐ d) Intel Pentium®

**3. ¿De dónde viene el término "x86" usado para referirse a esta familia de procesadores?**

☐ a) De la velocidad en MHz de los primeros chips
☐ b) De los dos últimos dígitos de los números de referencia de chips como el 8086 o el 80386
☐ c) Del número de núcleos del procesador
☐ d) Del año de lanzamiento del primer chip

**4. ¿Qué ventaja aporta la compatibilidad hacia atrás entre generaciones de procesadores Intel®?**

☐ a) Cada generación requiere reescribir todo el software desde cero
☐ b) El software y las herramientas de desarrollo antiguas se pueden seguir usando en el nuevo hardware
☐ c) Solo funciona el software más reciente
☐ d) Obliga a comprar una nueva licencia de sistema operativo en cada generación

**5. ¿Qué es el DMI (Direct Media Interface)?**

☐ a) Un tipo de memoria RAM
☐ b) El enlace de alta velocidad entre el procesador y su chip complementario, el PCH
☐ c) Un puerto USB de nueva generación
☐ d) El sistema de refrigeración del procesador

**6. ¿Qué es el PCH (Platform Controller Hub)?**

☐ a) El disipador de calor del procesador
☐ b) Un tipo de memoria caché interna del procesador
☐ c) Un chip complementario que aporta funciones e interfaces como USB, SATA, red o audio
☐ d) El conector físico donde se coloca el procesador

**7. ¿Qué interfaz se usa principalmente para conectar discos duros y unidades de almacenamiento?**

☐ a) SATA
☐ b) LPC
☐ c) SPI
☐ d) GPIO

**8. ¿Cuál es la principal diferencia entre un sistema basado en Intel® Core™ i7 y uno basado en Intel® Atom™ (SoC)?**

☐ a) El Core™ i7 no necesita memoria RAM
☐ b) El Atom™ integra en un solo chip las funciones que en el Core™ i7 están repartidas entre el procesador y el PCH
☐ c) El Atom™ solo funciona con sistemas operativos móviles
☐ d) No hay ninguna diferencia real entre ambos

**9. ¿Cuál es la función principal de la BIOS?**

☐ a) Reproducir archivos multimedia
☐ b) Arrancar el procesador, detectar los componentes y ceder el control al sistema operativo
☐ c) Gestionar la conexión Wi-Fi del equipo
☐ d) Sustituir al sistema operativo por completo

**10. ¿Qué interfaz se utiliza habitualmente para conectar la memoria flash que contiene la BIOS?**

☐ a) SATA
☐ b) SPI
☐ c) USB
☐ d) PCIe

---

## Verdadero o falso

Marca V o F en cada afirmación.

**11.** El primer microprocesador de Intel®, el 4004, ya trabajaba con arquitectura de 64 bits. &nbsp;&nbsp; V ☐ &nbsp; F ☐

**12.** El DMI conecta exclusivamente un procesador con su PCH, a diferencia del QPI, que sí admite varios procesadores en el mismo sistema. &nbsp;&nbsp; V ☐ &nbsp; F ☐

**13.** Todos los sistemas basados en arquitectura Intel® necesitan obligatoriamente un chip PCH independiente del procesador. &nbsp;&nbsp; V ☐ &nbsp; F ☐

**14.** La compatibilidad hacia atrás permite que el software escrito para una generación anterior siga funcionando en procesadores más nuevos. &nbsp;&nbsp; V ☐ &nbsp; F ☐

**15.** La interfaz LPC ofrece mayor ancho de banda que PCI Express (PCIe). &nbsp;&nbsp; V ☐ &nbsp; F ☐

---

## Preguntas de reflexión (respuesta breve)

Estas preguntas no se responden literalmente con el documento: requieren que apliques o relaciones lo aprendido.

**16.** Si tuvieras que montar un equipo de bajo coste y tamaño reducido para un proyecto de dispositivo embebido, ¿elegirías un procesador de la familia Core™ i7 o uno de la familia Atom™? Justifica tu respuesta.

_____________________________________________________________________________
_____________________________________________________________________________

**17.** Estás diagnosticando un equipo en el que los puertos USB no funcionan, pero el procesador arranca y funciona con normalidad. ¿Qué componente del sistema revisarías primero y por qué?

_____________________________________________________________________________
_____________________________________________________________________________

**18.** ¿Por qué crees que la compatibilidad hacia atrás es tan importante comercialmente para una empresa como Intel®, más allá de la ventaja técnica que supone para el programador?

_____________________________________________________________________________
_____________________________________________________________________________

---

## Hoja de correcciones (uso del profesor)

### Preguntas 1-10 (test)

| Pregunta | Respuesta correcta |
|---|---|
| 1 | b |
| 2 | c |
| 3 | b |
| 4 | b |
| 5 | b |
| 6 | c |
| 7 | a |
| 8 | b |
| 9 | b |
| 10 | b |

### Preguntas 11-15 (verdadero/falso)

| Pregunta | Respuesta correcta |
|---|---|
| 11 | F (el 4004 era de 8 bits; los 64 bits llegaron mucho después) |
| 12 | V |
| 13 | F (Intel Atom en configuración SoC no necesita PCH) |
| 14 | V |
| 15 | F (PCIe ofrece mucho más ancho de banda que LPC) |

### Preguntas 16-18 (reflexión)

No tienen una única respuesta correcta; se valora el razonamiento. Orientación para la corrección:

- **16.** Se espera que el alumno elija Atom™ y justifique con tamaño reducido, bajo consumo, bajo coste y la integración en un solo chip (SoC).
- **17.** Se espera que el alumno señale el PCH, ya que es el chip que gestiona los controladores USB, y razone que el procesador no es responsable directo de esa interfaz.
- **18.** Se valora cualquier razonamiento coherente: por ejemplo, que protege la inversión de los clientes en software, reduce la resistencia a actualizar el hardware, y fideliza a los desarrolladores y fabricantes en el ecosistema Intel®.

---

*Profesor: Ezequiel Llarena Borges · Módulo MME · 1º SMR*
