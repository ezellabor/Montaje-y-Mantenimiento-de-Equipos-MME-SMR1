# SMR1 | Montaje y Mantenimiento de Equipos 

![imagen-interior-pc](img/imagen-interior-pc-smaller.png)  

### Componentes principales de un equipo informático

* [Esquema de elementos de Hardware y Buses de Comunicación de un Sistema Informático (Mapa interactivo)](https://github.com/ezellabor/Montaje-y-Mantenimiento-de-Equipos-MME-SMR1/blob/main/Fichas-Guias-Tablas-Resumen/esquema-componentes-hw-interactivo.html)
* [Guía Resumen de Arquitectura y Componentes de un Sistema Microinformático](https://github.com/ezellabor/Montaje-y-Mantenimiento-de-Equipos-MME-SMR1/blob/main/Fichas-Guias-Tablas-Resumen/sintesis-mme-smr1.html)

--- 
### Arquitectura Von-Neumann  

![Arquitectura-Von-Neumann](img/arquitectura_von_newmann.png)  

### Esquema de Buses  
![arquitectura-buses](img/arquitectura-detalle.png)

```mermaid
graph LR
    subgraph PERIFÉRICOS
        IN[Entrada: Teclado / Ratón]
        OUT[Salida: Monitor / Impresora]
        STORE[Almacenamiento: SSD / HDD]
    end

    subgraph CPU ["UCP / CPU (Procesador)"]
        UC[Unidad de Control]
        ALU[Unidad Aritmético-Lógica]
        REG[Registros Internos]
    end

    RAM[("Memoria RAM\n(Datos e Instrucciones)")]
    ES[Módulos E/S]

    %% Conexiones
    CPU <===> |Bus de Datos / Control| RAM
    CPU ===> |Bus de Direcciones| RAM
    CPU <===> |Buses del Sistema| ES
    
    ES <---> IN
    ES <---> OUT
    ES <---> STORE

    %% Estilos
    style CPU fill:#1e293b,stroke:#3b82f6,stroke-width:2px,color:#fff
    style RAM fill:#0f172a,stroke:#10b981,stroke-width:2px,color:#fff
    style ES fill:#1e293b,stroke:#f59e0b,stroke-width:2px,color:#fff
    style PERIFÉRICOS fill:#0f172a,stroke:#64748b,stroke-width:1px,color:#fff
```

### Esquema de placa base (Motherboard)  

![Esquema de placa base](img/placabase-esquema.jpg/)

>Profesor: Ezequiel Llarena Borges
>elb733@educa.madrid.org
---


