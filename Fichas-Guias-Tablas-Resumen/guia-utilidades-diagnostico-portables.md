# Utilidades de chequeo y diagnóstico  
```CPU-Z, HWMonitor y AIDA64 (versión portable)```  

**Guía resumen para llevar en una memoria USB** · Módulo MME
Ezequiel Llarena Borges

---

## ⚠️ Lo primero: ¿funcionan sin derechos de administrador?

**Solo en parte.** Las tres utilidades necesitan un controlador de kernel para leer directamente el hardware (sensores, memoria SPD, chipset...), y cargarlo requiere privilegios de administrador. Sin ellos, **el programa puede arrancar, pero con información incompleta**:

| Utilidad | Qué ocurre sin derechos de administrador |
|---|---|
| **CPU-Z** | Los catálogos de software portable la listan con dependencia de derechos de administrador; las guías recomiendan ejecutarla como administrador para obtener lecturas completas. |
| **HWMonitor** | Sin permisos de administrador, las lecturas de sensores quedan muy limitadas (según usuarios en foros). |
| **AIDA64** | Los propios desarrolladores indican que se puede usar sin derechos de administrador, pero se pierden lecturas. Sin su controlador de kernel se pierden sensores, información de GPU, lista de módulos de memoria SPD, detalles del chipset y más. Además, el ejecutable solicita elevación al arrancar. |

**Recomendación:** antes de depender de ellas en el aula, **pruébalas con una cuenta de usuario estándar** en un equipo representativo y comprueba qué datos aparecen.

**Alternativas dentro de la política de seguridad del centro:**
- Usar las herramientas del propio Windows, que suelen funcionar con cuenta estándar: *Configuración → Sistema → Acerca de*, *Información del sistema* (`msinfo32`), *Administrador de tareas → Rendimiento* y `dxdiag`.
- Pedir al administrador del centro un equipo de pruebas con una cuenta de administrador local, o la autorización para elevar estas utilidades.

---

## Resumen de cada utilidad

### CPU-Z — identificar el hardware
- **Para qué sirve:** muestra información detallada de procesador (modelo, núcleos, frecuencias, caché), placa base (modelo, chipset, BIOS), memoria (tipo, tamaño, tiempos) y sistema operativo.
- **Licencia:** gratuita.
- **Portable:** sí, paquete **ZIP** oficial. La versión portable **no deja el controlador instalado** en el equipo (el instalador sí lo deja).
- **Truco:** edita `cpuz.ini` y cambia `CheckUpdates=1` por `CheckUpdates=0` para desactivar la búsqueda de actualizaciones.
- **Descarga oficial:** <https://www.cpuid.com/softwares/cpu-z.html> → elige el paquete **ZIP** (no el instalador).

### HWMonitor — vigilar sensores
- **Para qué sirve:** lee voltajes, temperaturas, velocidad de ventiladores, potencias, corrientes, utilización y frecuencias de CPU y GPU, chips de monitorización de la placa, módulos de memoria con sensor térmico, discos mediante S.M.A.R.T. y baterías. Muestra valores actuales, mínimos y máximos.
- **Licencia:** gratuita (existe una versión ampliada de pago, HWMonitor PRO).
- **Portable:** sí, paquete **ZIP** oficial (ejecutables de 32 y 64 bits).
- **Descarga oficial:** <https://www.cpuid.com/softwares/hwmonitor.html> → elige el paquete **ZIP**.

### AIDA64 — diagnóstico completo y pruebas
- **Para qué sirve:** información detallada del sistema, monitorización de sensores, benchmarks y pruebas de estabilidad (estrés de CPU/FPU...), informes en texto, HTML y MHTML.
- **Licencia:** **de pago**. La versión descargable es una **prueba de 30 días**; durante la prueba puede ofrecer funcionalidad limitada y no mostrar todos los datos.
- **Portable:** sí, **"AIDA64 Extreme Trial version, portable ZIP package"** (también hay ZIP portable de Engineer, Business y Network Audit). Tamaño aproximado: 60 MB. En la última consulta, la versión más reciente publicada era la 8.35 (julio de 2026).
- **Ediciones:** Extreme (uso doméstico), Engineer, Business y Network Audit; solo estas tres últimas admiten opciones de línea de comandos.
- **Descarga oficial:** <https://www.aida64.com/downloads> → fila **"AIDA64 Extreme Trial version, portable ZIP package"**.
- **Alternativa gratuita para diagnóstico completo:** HWiNFO (<https://www.hwinfo.com/download/>, paquete "Portable").

---

## Comparativa rápida

| | CPU-Z | HWMonitor | AIDA64 |
|---|---|---|---|
| **Función principal** | Identificar componentes | Monitorizar sensores | Diagnóstico completo + pruebas |
| **Licencia** | Gratuita | Gratuita | Prueba 30 días, luego de pago |
| **Paquete portable** | ZIP oficial | ZIP oficial | ZIP oficial (Trial) |
| **Peso aprox.** | Pequeño | Pequeño | ~60 MB |
| **Necesita admin para datos completos** | Sí | Sí | Sí |

---

## Cómo preparar la memoria USB

1. Crea una carpeta en el USB (por ejemplo `Diagnostico`) con una subcarpeta por herramienta.
2. Descarga cada **ZIP** desde su **página oficial** (enlaces de arriba). Evita los primeros resultados patrocinados de los buscadores: es donde aparecen los falsos instaladores.
3. **Extrae** cada ZIP en su subcarpeta (no ejecutes el programa desde dentro del ZIP).
4. Comprueba, si quieres, el hash **SHA256** que CPUID publica en su página de descarga.
5. Ejecutable según el equipo (los nombres pueden variar ligeramente según la versión):
   - CPU-Z: `cpuz_x64.exe` o `cpuz_x32.exe`
   - HWMonitor: `HWMonitor_x64.exe` o `HWMonitor_x32.exe`
   - AIDA64: `aida64.exe`
6. El USB **no debe estar protegido contra escritura**: los programas guardan su configuración en su propia carpeta.
7. Prueba todo con una cuenta estándar antes de usarlo con el alumnado.

**Posibles problemas:**
- Algunos antivirus pueden marcar los ejecutables como falso positivo; si los has descargado del sitio oficial, suele serlo.
- Las directivas del centro (por ejemplo, bloqueo de ejecución desde unidades USB) pueden impedir su uso.

---

## Fuentes consultadas
Páginas oficiales de CPUID y AIDA64 · foros oficiales de AIDA64 · Portable Freeware Collection · PortableApps.com

*Guía de Ezequiel Llarena Borges. Las versiones y enlaces pueden cambiar: contrasta siempre en las páginas oficiales.*
