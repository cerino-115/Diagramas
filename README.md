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

flowchart LR
    subgraph N1["Capa 1: Computación"]
        A["Rubik Pi 3<br/><small>Ubuntu PREEMPT_RT</small>"]
        B["Algoritmo Python<br/>Interfaz Gráfica"]
    end

    subgraph N2["Capa 2: Control"]
        C["Controlador IRC5"]
        D["Servidor Socket<br/>RAPID"]
    end

    subgraph N3["Capa 3: Actuación"]
        E["Robot ABB YuMi<br/>IRB 14000"]
    end

    B <-->|"① Comandos y datos%%BR%%② Ethernet RJ45 GbE"| D
    D <-->|"③ Instrucciones internas%%BR%%④ Buses de campo"| E
    E -.->|"⑤ Retroalimentación%%BR%%en tiempo real"| D
    D -.->|"⑥ Actualización de estado"| B
