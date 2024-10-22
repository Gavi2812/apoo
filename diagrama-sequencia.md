# Diagrama de sequência 



```mermaid
sequenceDiagram
    participant Admin as Administrador
    participant UI as Interface de Usuário
    participant System as Sistema
    participant DB as Banco de Dados

    Admin->>UI: Seleciona "Cadastrar Insumo"
    UI->>System: Solicita o formulário de cadastro
    System-->>UI: Retorna o formulário

    Admin->>UI: Preenche o formulário e envia
    UI->>System: Envia dados do insumo para validação
    System->>DB: Verifica fornecedor no banco de dados
    DB-->>System: Fornecedor encontrado

    System->>DB: Insere novo insumo no banco de dados
    DB-->>System: Confirmação de cadastro

    System-->>UI: Exibe mensagem de sucesso
    UI-->>Admin: Confirmação do cadastro concluído
