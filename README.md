# Diagramas

```mermaid
graph LR
  A[Nodo: Cámara/Vigilante] -- Publica en /obstaculos --> B((Tópico: /obstaculos))
  B -- Suscribe --> C[Nodo: Motor/Cocinero]
  B -- Suscribe --> D[Nodo: Grabadora/Auditor]

  %% Estilos de nodos
  style A fill:#f9f,stroke:#333,stroke-width:2px
  style C fill:#bbf,stroke:#333,stroke-width:2px
  style D fill:#bbf,stroke:#333,stroke-width:2px

  %% Estilo del tópico (nodo en borde)
  style B fill:#ff9,stroke:#f66,stroke-width:2px,stroke-dasharray: 5 5
```
```mermaid  
flowchart TD  
    RT["Ubuntu PREEMPT_RT Kernel"] --- GUI["Algoritmo Python GUI"]  
    GUI -->|"RJ45 Gigabit Ethernet (Socket TCP/IP)"| SOCK["Servidor Socket RAPID"]  
    SOCK -->|"Buses de Campo Internos"| ACT["Robot ABB YuMi IRB 14000"]  

    ACT -->|"Retroalimentación"| SOCK  
    SOCK -->|"Respuestas y datos"| GUI  

```
```mermaid  
flowchart LR
    A["Puente de Wheatstone
(Conversión Resistencia a V)"] --V_diff (mV)--> B
    B["¿?
(Etapa de Hardware a Seleccionar)"] --V_ampli (V)--> C
    C["Filtro Activo Paso Bajas
(Atenuación de Ruido 60 Hz)"] --V_filtrado--> D
    D["ADC
(Conversión Digital de 0-5 V)"]

```
