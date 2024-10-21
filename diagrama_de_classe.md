### Estrutura do Diagrama de Classes

1. **Classes**:
   - **Funcionario**: Representa o funcionário que registra a entrada de insumos e consulta o estoque.
   - **Sistema**: Representa o sistema que gerencia insumos e realiza as operações.
   - **Insumo**: Representa os insumos que estão sendo registrados e gerenciados.

2. **Atributos**:
   - Cada classe tem atributos que armazenam informações relevantes.
   - Por exemplo, `Funcionario` tem atributos como `nome` e `cargo`.

3. **Métodos**:
   - Cada classe também possui métodos que definem o comportamento da classe.
   - Por exemplo, `Sistema` tem um método para `registrarEntrada` e outro para `consultarEstoque`.

4. **Relacionamentos**:
   - As setas indicam como as classes se relacionam.
   - No exemplo, um `Funcionario` utiliza um `Sistema`, e o `Sistema` gerencia um `Insumo`.

# Diagrama de Classes

```mermaid
classDiagram
    class Funcionario {
        +String nome
        +String cargo
        +void registrarEntrada(Insumo insumo)
        +void consultarEstoque()
    }

    class Sistema {
        +void registrarEntrada(Insumo insumo)
        +void consultarEstoque()
        +List<Insumo> buscarInsumos()
    }

    class Insumo {
        +String nome
        +int quantidade
        +void validar()
        +void atualizarQuantidade(int novaQuantidade)
    }

    Funcionario --> Sistema : utiliza
    Sistema --> Insumo : gerencia









