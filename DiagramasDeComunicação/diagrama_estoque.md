# Diagrama de Comunicação: Consultar Estoque de Insumos

```mermaid
sequenceDiagram
    participant F as Funcionário
    participant S as Sistema
    participant I as Insumo

    F->>S: Consultar Estoque
    S->>I: Buscar Insumos
    I-->>S: Lista de Insumos
    S-->>F: Exibir Estoque
