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
