# Diagrama de Comunicação 1: Registrar Entrada de Insumo

```mermaid
sequenceDiagram
    participant F as Funcionário
    participant S as Sistema
    participant I as Insumo

    F->>S: Registrar Entrada
    S->>I: Validar Insumo
    S->>S: Atualizar Estoque
    S->>I: Atualiza Quantidade
    S->>F: Confirmação de Registro
