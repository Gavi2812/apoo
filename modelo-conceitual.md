# Descrição das Entidades

## Insumo

**Descrição**: Representa os ingredientes e materiais utilizados na padaria.

**Atributos**:
- **id**: Identificador único do índice.
- **nome**: Nome do insumo (ex: "Farinha de Trigo").
- **tipo**: Classificação do insumo (ex: "Ingrediente", "Embalagem").
- **fornecedor_id**: Relaciona o consumo ao seu fornecedor.
- **quantidade**: Estoque atual do insumo.
- **quantidade_min**: Quantidade mínima permitida antes de gerar um alerta.
- **quantidade_max**: Quantidade máxima permitida para evitar excessos.
- **unidade_medida**: Unidade de medida utilizada (ex: "kg", "g").
- **validade**: Dados de validade do insumo, importantes para controle de estoque.
- **preço_unitario**: Preço por unidade, útil para controle financeiro.

## Fornecedor

**Descrição**: Representa os fornecedores de insumos.

**Atributos**:
- **id**: Identificador único do fornecedor.
- **nome**: Nome do fornecedor.
- **contato**: Informações de contato do fornecedor (telefone, email).
- **endereco**: Endereço do fornecedor.
- **cnpj**: Número de CNPJ do fornecedor para questões fiscais.
- **rating**: Avaliação do fornecedor, ajudando a escolher o melhor para o negócio.

## Funcionário 

**Descrição**: Representa os funcionários que gerenciam o estoque.

**Atributos**:
- **id**: Identificador único do funcionário.
- **nome**: Nome do funcionário.
- **cargo**: Cargo ou função do funcionário (ex: "Gerente", "Estoquista").
- **email**: Email do funcionário.
- **senha**: Senha para acesso ao sistema de gerenciamento.
- **data_admissao**: Data em que o funcionário foi admitido.
- **status**: Status atual do funcionário (ex: "Ativo", "Inativo").

## Entrada

**Descrição**: Registrar como entradas de insumos no estoque.

**Atributos**:
- **id**: Identificador único de entrada.
- **data**: Data em que a entrada foi registrada.
- **quantidade**: Quantidade de insumos recebidos.
- **insumo_id**: Relaciona a entrada ao insumo correspondente.
- **funcionario_id**: ID do funcionário que registrou a entrada.
- **lote**: Número do lote do insumo, importante para rastreabilidade.

## Saída

**Descrição**: Registrar as saídas de insumos do estoque.

**Atributos**:
- **id**: Identificador único da saída.
- **data**: Data em que a saída foi registrada.
- **quantidade**: Quantidade de insumos retirados.
- **insumo_id**: Relaciona a saída ao insumo correspondente.
- **funcionario_id**: ID do funcionário que registrou a saída.
- **motivo**: Motivo da saída, ajudando no controle de uso (ex: "Venda", "Perda").

## Relatório

**Descrição**: Representa relatórios gerados sobre o estoque.

**Atributos**:
- **id**: Identificador único do relatório.
- **data**: Data em que o relatório foi gerado.
- **total_insumos**: Total de insumos registrados no relatório.
- **funcionario_id**: ID do funcionário que gerou o relatório.
- **detalhes**: Informações adicionais ou observações sobre o relatório.





```mermaid
classDiagram
    class Insumo {
        +id: int
        +nome: string
        +tipo: string
        +fornecedor_id: int
        +quantidade: float
        +quantidade_min: float
        +quantidade_max: float
        +unidade_medida: string
        +validade: date
        +preco_unitario: float
    }

    class Fornecedor {
        +id: int
        +nome: string
        +contato: string
        +endereco: string
        +cnpj: string
        +rating: float
    }

    class Funcionario {
        +id: int
        +nome: string
        +cargo: string
        +email: string
        +senha: string
        +data_admissao: date
        +status: string
    }

    class Entrada {
        +id: int
        +data: date
        +quantidade: float
        +insumo_id: int
        +funcionario_id: int
        +lote: string
    }

    class Saida {
        +id: int
        +data: date
        +quantidade: float
        +insumo_id: int
        +funcionario_id: int
        +motivo: string
    }

    class Relatorio {
        +id: int
        +data: date
        +total_insumos: float
        +funcionario_id: int
        +detalhes: string
    }

    Insumo "1" --> "N" Fornecedor
    Funcionario "1" --> "N" Entrada
    Funcionario "1" --> "N" Saida
    Funcionario "1" --> "N" Relatorio
    Entrada "N" --> "1" Insumo
    Saida "N" --> "1" Insumo
