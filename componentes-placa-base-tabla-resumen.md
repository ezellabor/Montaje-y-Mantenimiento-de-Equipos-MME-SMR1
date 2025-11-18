# Arquitectura: componentes de placa base
## Esquema-Resumen

| Componente | Descripción                 | Funciones         | Parámetros críticos            | Evolución           |
| ---------- | --------------------------- | -------------------------- | ------------------------------ | ---------------------------- |
| RAM      | Memoria de acceso aleatorio   | leer/escribir datos        | Tamaño, velocidad, canales     | EDO → DDR4 → DDR5            |
| Chipset  | Controlador principal         | gestión buses, periféricos | Tipo, versión, TDP             | Chipsets antiguos → modernos |
| Storage  | Almacenamiento                | leer/escribir datos        | Capacidad, interfaz, velocidad | PATA → SATA → M.2            |
| I/O      | Puertos de entrada/salida     | USB, HDMI, Ethernet        | Tipo, versión                  | PS/2 → USB 2.0 → USB 3.2     |
| PSU      | Fuente de alimentación        | Suministra energía         | Potencia, eficiencia           | AT → ATX → modular           |
| PCIe     | Slot de expansión             | GPU, tarjetas de red       | Versión, lanes                 | PCI → PCI-X → PCIe 1-5       |
| BIOS     | BIOS/UEFI                     | Inicializa sistema         | Tamaño, versión                | BIOS clásico → UEFI          |
| CMOS     | Batería CMOS                  | Mantiene configuración     | Voltaje, duración              | Pilas CR2032                 |
