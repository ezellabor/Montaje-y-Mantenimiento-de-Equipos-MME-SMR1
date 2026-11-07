# COMPATIBILIDAD Y CONFIGURACIÓN DE MEMORIA RAM

**Módulo:** Montaje y Mantenimiento de Equipos (MME)  
**Ciclo:** Sistemas Microinformáticos y Redes (SMR1)

**Alumno/a:** ______________________________________

**Fecha:** ___________________

## Objetivos

- Identificar los diferentes formatos de módulos de memoria RAM.
- Comprobar la compatibilidad entre memoria, placa base y procesador.
- Interpretar características técnicas: DDR, capacidad, frecuencia de transferencia (MT/s), latencia CAS (CL), voltaje y organización.
- Comprender el funcionamiento de Dual Channel.
- Resolver situaciones reales de ampliación, sustitución y mantenimiento de memoria RAM.
- Justificar técnicamente las decisiones de montaje.

## Instrucciones

Lee cada supuesto práctico y responde razonadamente a las cuestiones planteadas.

Cuando sea necesario, consulta las especificaciones técnicas de los fabricantes de placas base, procesadores y módulos de memoria.

No es suficiente responder únicamente «compatible» o «incompatible»: debes explicar el motivo.

---

## SUPUESTO 1. Ampliación de memoria en un ordenador de sobremesa

Un cliente tiene un ordenador de sobremesa con las siguientes características:

**Placa base:** ASUS PRIME B450M-A II.

- 4 ranuras DIMM.
- Compatible con DDR4.
- Capacidad máxima: 128 GB.
- Arquitectura Dual Channel.

**Memoria instalada:**
- 1 módulo DDR4 de 8 GB.
- Frecuencia: DDR4-2666.
- Formato DIMM.
- Voltaje: 1,2 V.

El cliente quiere ampliar su equipo hasta 16 GB comprando un módulo DDR4 de 8 GB, pero ha encontrado uno con las siguientes características:

- DDR4-3200.
- Formato DIMM.
- Capacidad: 8 GB.
- Voltaje: 1,35 V (perfil XMP).

**Cuestiones:**

1. ¿Es compatible el nuevo módulo con la placa base?
2. ¿Podrá instalarse junto al módulo de 2666 MT/s?
3. ¿A qué velocidad podrían funcionar ambos módulos?
4. ¿Funcionaría la tecnología Dual Channel?
5. ¿Qué precauciones debería tomar el técnico antes de realizar la ampliación?

**Justificación técnica:**

________________________________________________________________

________________________________________________________________

## SUPUESTO 2. Una memoria RAM que no encaja físicamente

Un técnico recibe un ordenador de sobremesa que necesita ampliar de 8 GB a 16 GB.

La placa base dispone de dos ranuras DDR4 DIMM.

Un compañero ha comprado por error un módulo con estas características:

- Capacidad: 8 GB.
- Tecnología: DDR4.
- Formato: SO-DIMM.
- Frecuencia: 3200 MT/s.
- Voltaje: 1,2 V.

**Cuestiones:**

1. ¿Es compatible eléctricamente este módulo con la placa base?
2. ¿Se puede instalar físicamente en una ranura DIMM?
3. ¿Qué diferencia existe entre DIMM y SO-DIMM?
4. ¿Qué módulo debería comprar el técnico para solucionar el problema?
5. ¿En qué tipo de equipos es habitual encontrar memorias SO-DIMM?

**Justificación técnica:**

________________________________________________________________

________________________________________________________________

## SUPUESTO 3. Configuración de Dual Channel

Un usuario quiere montar un equipo con 32 GB de memoria RAM.

La placa base dispone de cuatro ranuras:

- A1 y A2: canal A.
- B1 y B2: canal B.

El fabricante recomienda instalar dos módulos en las ranuras A2 y B2 para una configuración de dos módulos.

El usuario dispone de los siguientes módulos:

- Módulo 1: 16 GB DDR4-3200 CL16.
- Módulo 2: 16 GB DDR4-3200 CL16.

**Cuestiones:**

1. ¿En qué ranuras deberías instalar los módulos?
2. ¿Qué significa Dual Channel?
3. ¿Qué ventajas ofrece frente a una configuración Single Channel?
4. ¿Es obligatorio que ambos módulos sean exactamente del mismo fabricante?
5. ¿Qué podría ocurrir si instalamos los dos módulos en A1 y A2?

**Justificación técnica:**

________________________________________________________________

________________________________________________________________

## SUPUESTO 4. Diferencias de frecuencia y velocidad de transferencia

Un cliente quiere ampliar su ordenador con un módulo de memoria DDR4.

La memoria actualmente instalada presenta estas características:

- DDR4-2666.
- Frecuencia de reloj: aproximadamente 1333 MHz.
- Capacidad: 8 GB.

El nuevo módulo que quiere comprar presenta estas características:

- DDR4-3600.
- Frecuencia de reloj: aproximadamente 1800 MHz.
- Capacidad: 8 GB.

La placa base admite DDR4 hasta 3200 MT/s y el procesador admite oficialmente hasta 2666 MT/s.

**Cuestiones:**

1. ¿Qué significa MT/s?
2. ¿Por qué una memoria DDR4-2666 tiene un reloj real aproximado de 1333 MHz?
3. ¿Es compatible el nuevo módulo con la plataforma?
4. ¿A qué velocidad máxima podrían funcionar las memorias en esta configuración?
5. ¿Qué diferencia existe entre la velocidad anunciada de un módulo y la velocidad efectiva a la que trabaja?

**Justificación técnica:**

________________________________________________________________

________________________________________________________________

## SUPUESTO 5. Interpretación de la latencia CAS

Un técnico debe elegir entre dos módulos DDR4 de 3200 MT/s para ampliar un ordenador.

**Opción A:**
- DDR4-3200.
- Latencia CL16.
- Capacidad: 16 GB.

**Opción B:**
- DDR4-3200.
- Latencia CL22.
- Capacidad: 16 GB.

Ambos módulos son compatibles con la placa base.

**Cuestiones:**

1. ¿Qué significa CL?
2. ¿Qué módulo presenta una menor latencia CAS?
3. ¿Cuál de los dos módulos ofrece una respuesta más rápida en términos de latencia CAS?
4. ¿Significa que el módulo CL16 siempre ofrecerá un rendimiento global superior?
5. Calcula la latencia CAS aproximada en nanosegundos de ambos módulos utilizando:

   Latencia (ns) = CL × 2000 / MT/s

**Justificación técnica y cálculos:**

________________________________________________________________

________________________________________________________________

## SUPUESTO 6. Ampliación de RAM en un portátil

Un usuario tiene un portátil con las siguientes características:

- 8 GB DDR4-3200 SO-DIMM.
- Una ranura de memoria SO-DIMM accesible.
- 8 GB de memoria soldados a la placa base.
- Capacidad máxima admitida: 24 GB.

El usuario quiere ampliar la memoria hasta 24 GB.

Dispone de estas opciones:

**Opción A:** módulo DDR4-3200 SO-DIMM de 16 GB.

**Opción B:** módulo DDR4-3200 DIMM de 16 GB.

**Cuestiones:**

1. ¿Qué opción debe elegir?
2. ¿Por qué no puede instalar la opción B?
3. ¿Cuál será la capacidad total de memoria después de la ampliación?
4. ¿Qué significa que una parte de la RAM esté soldada a la placa base?
5. ¿Podrá disponer de Dual Channel? Razona tu respuesta teniendo en cuenta la configuración de memoria del portátil.

**Justificación técnica:**

________________________________________________________________

________________________________________________________________

## SUPUESTO 7. Memoria ECC frente a memoria convencional

Una empresa necesita ampliar un servidor que utiliza una placa base compatible con:

- DDR4 ECC Registered (RDIMM).
- Memoria de hasta 128 GB por módulo.
- Cuatro ranuras de memoria.

El técnico recibe dos módulos:

**Módulo A:**
- 32 GB DDR4 ECC Registered.
- Formato DIMM.
- 3200 MT/s.

**Módulo B:**
- 32 GB DDR4 Non-ECC Unbuffered (UDIMM).
- Formato DIMM.
- 3200 MT/s.

**Cuestiones:**

1. ¿Son compatibles ambos módulos con la placa base?
2. ¿Qué diferencia existe entre ECC y Non-ECC?
3. ¿Qué significa Registered (RDIMM)?
4. ¿Por qué no basta con que los dos módulos sean DDR4 y tengan formato DIMM?
5. ¿Qué tipo de memoria debe utilizar el técnico?

**Justificación técnica:**

________________________________________________________________

________________________________________________________________

## SUPUESTO 8. Mezcla de módulos con diferentes latencias y frecuencias

Un usuario tiene instalados dos módulos de memoria:

- 8 GB DDR4-3200 CL16.
- 8 GB DDR4-3200 CL16.

Quiere añadir otros dos módulos que ha conseguido:

- 8 GB DDR4-2666 CL19.
- 8 GB DDR4-2666 CL19.

Todos son módulos DIMM DDR4 de escritorio y no presentan incompatibilidades de formato ni de tipo de memoria.

La placa base admite cuatro módulos y Dual Channel.

**Cuestiones:**

1. ¿Es posible instalar los cuatro módulos?
2. ¿Cuál será la capacidad total instalada?
3. ¿A qué velocidad podrían funcionar las memorias?
4. ¿Qué sucede cuando se mezclan módulos con diferentes latencias?
5. ¿Se puede seguir utilizando Dual Channel?
6. ¿Recomendarías esta ampliación o utilizarías otro tipo de configuración? Justifica tu decisión.

**Justificación técnica:**

________________________________________________________________

________________________________________________________________

## SUPUESTO 9. Compatibilidad de memoria DDR4 y DDR5

Un cliente compra una placa base nueva compatible exclusivamente con DDR5.

Sin embargo, quiere reutilizar dos módulos DDR4 de su antiguo ordenador:

- 2 × 8 GB DDR4-3200 DIMM.
- Voltaje: 1,2 V.
- Latencia: CL16.

La nueva placa base dispone de cuatro ranuras DIMM DDR5 y admite módulos de hasta 6000 MT/s mediante perfiles de memoria.

**Cuestiones:**

1. ¿Puede instalar los módulos DDR4 en la nueva placa base?
2. ¿Qué diferencias físicas y eléctricas existen entre DDR4 y DDR5?
3. ¿Es posible utilizar un adaptador para solucionar el problema?
4. ¿Qué tipo de memoria debe comprar?
5. ¿Qué significa que una placa base admita una velocidad mediante un perfil de memoria y no necesariamente de forma estándar?

**Justificación técnica:**

________________________________________________________________

________________________________________________________________

## SUPUESTO 10. Diagnóstico de un equipo que no arranca después de ampliar la RAM

Un técnico realiza una ampliación de memoria en un ordenador de sobremesa.

Antes de la intervención, el equipo funcionaba correctamente con:

- 2 × 8 GB DDR4-3200.
- Dual Channel.
- Placa base con cuatro ranuras DIMM.

Después de instalar dos módulos adicionales de 16 GB DDR4-3600, el ordenador presenta estos síntomas:

- Los ventiladores arrancan.
- La pantalla permanece negra.
- El equipo no completa el POST.
- El LED de diagnóstico de memoria de la placa base permanece encendido.

**Cuestiones:**

1. ¿Qué puede estar provocando el problema?
2. ¿Qué comprobaciones realizarías antes de sustituir ningún componente?
3. ¿Cómo comprobarías si los módulos nuevos son compatibles con la placa base y el procesador?
4. ¿Por qué puede ser más difícil alcanzar frecuencias elevadas al instalar cuatro módulos?
5. ¿Qué papel desempeña la BIOS/UEFI en la configuración de la memoria?
6. Describe un procedimiento ordenado para diagnosticar y solucionar el problema.

**Propuesta de diagnóstico:**

________________________________________________________________

________________________________________________________________

________________________________________________________________

---

## ENTREGA Y VALORACIÓN

Para cada supuesto debes:

- Indicar si la configuración es compatible, incompatible o compatible con limitaciones.
- Identificar las características técnicas que justifican tu decisión.
- Explicar las posibles consecuencias de realizar un montaje incorrecto.
- Proponer una solución cuando exista incompatibilidad.

**Importante:** consulta documentación técnica de fabricantes cuando sea necesario. No todas las placas base admiten las mismas capacidades, frecuencias, módulos y configuraciones de memoria.

**Conclusión:** explica qué tres aspectos considerarías más importantes antes de comprar o instalar un módulo de memoria RAM.

________________________________________________________________

________________________________________________________________
