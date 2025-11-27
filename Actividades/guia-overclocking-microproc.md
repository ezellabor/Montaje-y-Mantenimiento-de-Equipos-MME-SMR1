# Guía de Overclocking para Microprocesadores

---

## **1. ¿Por qué se hace overclocking?**
- **Mejorar el rendimiento:** Aumentar la velocidad del procesador para tareas intensivas como gaming, edición de video, renderizado 3D, etc.
- **Extender la vida útil del hardware:** Sacar más provecho de componentes antiguos antes de actualizarlos.
- **Entusiasmo y personalización:** Muchos usuarios disfrutan optimizar y experimentar con su hardware.

---

## **2. Consecuencias del overclocking**

### **Ventajas:**
- Mayor velocidad de procesamiento.
- Mejor experiencia en juegos (más FPS).
- Mejor rendimiento en aplicaciones intensivas.

### **Desventajas:**
- Mayor consumo de energía.
- Aumento de temperatura (puede requerir sistemas de enfriamiento adicionales).
- Reducción de la vida útil del hardware.
- Inestabilidad del sistema (fallos, reinicios, "pantallazos azules").
- Pérdida de garantía (muchos fabricantes no cubren daños por overclocking).

---

## **3. ¿En qué casos se hace overclocking?**
- **Gaming:** Para mejorar el rendimiento en juegos.
- **Edición de video y 3D:** Acelerar procesos de renderizado.
- **Minería de criptomonedas:** Maximizar el rendimiento de la GPU/CPU.
- **Benchmarking:** Probar los límites del hardware.

---

## **4. ¿Qué se necesita para hacer overclocking?**
- **Hardware compatible:** Procesador, placa base y memoria RAM que soporten overclocking (ej: procesadores Intel con sufijo "K" o "X", o AMD Ryzen).
- **Sistema de enfriamiento avanzado:** Refrigeración líquida o disipadores de alta gama.
- **Fuente de alimentación robusta:** Para manejar el mayor consumo de energía.
- **Herramientas de software:** Programas como **Intel Extreme Tuning Utility (XTU)**, **AMD Ryzen Master**, o ajustes en la BIOS/UEFI.
- **Conocimientos básicos:** Saber cómo acceder a la BIOS y ajustar voltajes y frecuencias.

#

>**Nota importante:**
>El overclocking también se puede realizar aumentando la frecuencia del reloj base o **BCLK.** Es el reloj principal de la placa base que controla prácticamente todos los componentes, como CPU, RAM, PCIe y Chipset. Si aumentamos este reloj, estamos aumentado la frecuencia de otros componentes que incluso tienen el multiplicador bloqueado, aunque   conlleva aún más riesgos y es un método muy inestable.  
>  
>El **Undervolting** por su parte, es justo lo contrario, disminuir el voltaje para evitar que un procesador haga _thermal throttling_. Es una práctica usada en portátiles o   tarjetas gráficas con sistemas de refrigeración ineficaces.

---

## **5. Procedimiento paso a paso para overclocking de un microprocesador**

### **Paso 1: Preparación**
- Investiga tu hardware: Asegúrate de que tu CPU, placa base y RAM sean compatibles con overclocking.
- Actualiza la BIOS: Asegúrate de tener la última versión de la BIOS.
- Instala herramientas de monitoreo: Usa programas como **HWMonitor**, **Core Temp**, o **CPU-Z**.

### **Paso 2: Accede a la BIOS/UEFI**
- Reinicia tu PC y entra en la BIOS/UEFI (generalmente presionando `Del`, `F2`, o `F12` durante el arranque).

### **Paso 3: Ajusta la frecuencia del reloj**
- Busca opciones como **CPU Ratio**, **Multiplier**, o **CPU Clock Ratio** y auméntalas gradualmente (ej: de 3.5 GHz a 3.7 GHz).

### **Paso 4: Ajusta el voltaje (Vcore)**
- Aumenta el voltaje de la CPU (**CPU Vcore**) en pequeños incrementos (ej: +0.01V) para mantener la estabilidad.

### **Paso 5: Prueba de estabilidad**
- Usa herramientas como **Prime95**, **AIDA64**, o **IntelBurnTest** para probar la estabilidad del sistema.
- Monitorea las temperaturas con **HWMonitor**. Si superan los 85-90°C, reduce la frecuencia o mejora el enfriamiento.

### **Paso 6: Guarda y reinicia**
- Si el sistema es estable, guarda los cambios en la BIOS y reinicia.

---

## **7. Consejos finales**
- Empieza con incrementos pequeños: Aumenta la frecuencia en pasos de 100-200 MHz y prueba la estabilidad.
- No excedas los límites térmicos: Mantén las temperaturas por debajo de 85°C bajo carga.
- Documenta tus cambios: Anota los ajustes que haces para poder revertirlos si algo sale mal.
