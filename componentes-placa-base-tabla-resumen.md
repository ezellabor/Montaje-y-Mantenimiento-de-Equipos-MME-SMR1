## Componentes de placa base
# Esquema

| Archivo        | Componente | Imagen        | Descripción corta           | Lista de funciones         | Tabla de parámetros            | Tabla de evolución           |
| -------------- | ---------- | ------------- | --------------------------- | -------------------------- | ------------------------------ | ---------------------------- |
| `ram.html`     | RAM        | `ram.png`     | Memoria de acceso aleatorio | leer/escribir datos        | Tamaño, velocidad, canales     | EDO → DDR4 → DDR5            |
| `chipset.html` | Chipset    | `chipset.png` | Controlador principal       | gestión buses, periféricos | Tipo, versión, TDP             | Chipsets antiguos → modernos |
| `storage.html` | Storage    | `storage.png` | Almacenamiento              | leer/escribir datos        | Capacidad, interfaz, velocidad | PATA → SATA → M.2            |
| `io.html`      | (I/O)      | `io.png`      | Puertos de entrada/salida   | USB, HDMI, Ethernet        | Tipo, versión                  | PS/2 → USB 2.0 → USB 3.2     |
| `psu.html`     | PSU        | `psu.png`     | Fuente de alimentación      | Suministra energía         | Potencia, eficiencia           | AT → ATX → modular           |
| `pcie.html`    | PCIe       | `pcie.png`    | Slot de expansión           | GPU, tarjetas de red       | Versión, lanes                 | PCI → PCI-X → PCIe 1-5       |
| `rom.html`     | ROM        | `rom.png`     | BIOS/UEFI                   | Inicializa sistema         | Tamaño, versión                | BIOS clásico → UEFI          |
| `cmos.html`    | CMOS       | `cmos.png`    | Batería CMOS                | Mantiene configuración     | Voltaje, duración              | Pilas CR2032                 |
