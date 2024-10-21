# Expansão de Caso de Uso Crítico: Cadastrar Insumos

## 1. Caso de Uso: Cadastrar Insumos

### 1.1. Descrição:
O **Administrador** cadastra novos insumos no sistema, como farinha, fermento e outros ingredientes. Durante o cadastro, ele deve preencher informações detalhadas sobre o insumo, como nome, tipo, fornecedor, quantidade mínima e máxima. Essas informações são essenciais para o controle de estoque e disparo de alertas automáticos quando o nível de estoque estiver abaixo do limite.

### 1.2. Atores Envolvidos:
- **Administrador**: O único ator que pode realizar este caso de uso.

### 1.3. Pré-condições:
- O administrador deve estar autenticado no sistema.
- O sistema deve estar em funcionamento e o banco de dados deve estar acessível.

### 1.4. Fluxo Principal (Cenário de Sucesso):
1. O **Administrador** seleciona a opção "Cadastrar Insumos" no menu principal.
2. O sistema exibe um formulário para o cadastro de um novo insumo.
3. O **Administrador** preenche os seguintes campos obrigatórios:
   - Nome do insumo (ex: Farinha de Trigo).
   - Tipo do insumo (ex: Ingrediente Seco).
   - Fornecedor (selecionado de uma lista de fornecedores cadastrados).
   - Quantidade mínima para alertas de estoque baixo (ex: 20 kg).
   - Quantidade máxima (ex: 100 kg).
4. O **Administrador** confirma o cadastro.
5. O sistema valida as informações e salva o novo insumo no banco de dados.
6. O sistema exibe uma mensagem de confirmação de sucesso.
7. O fluxo termina.

### 1.5. Fluxo Alternativo (Dados Inválidos):
- **Passo 5A**: Se algum campo obrigatório não estiver preenchido ou contiver um valor inválido (ex: texto em campos numéricos):
   1. O sistema exibe uma mensagem de erro informando o problema.
   2. O **Administrador** corrige os dados e repete a ação de confirmação.
   3. O fluxo retorna ao Passo 5 do Fluxo Principal.

### 1.6. Fluxo Alternativo (Fornecedor Não Cadastrado):
- **Passo 3A**: Se o **Administrador** tenta cadastrar um insumo sem selecionar um fornecedor existente:
   1. O sistema exibe a opção para cadastrar um novo fornecedor.
   2. O **Administrador** pode cadastrar o fornecedor ou selecionar um existente.
   3. O fluxo retorna ao Passo 3 do Fluxo Principal.

### 1.7. Pós-condições:
- O novo insumo é salvo no banco de dados e pode ser utilizado nos processos de controle de estoque.
- O sistema pode gerar alertas automáticos com base nas quantidades mínimas e máximas definidas.

### 1.8. Exceções:
- Se houver falha na comunicação com o banco de dados, o sistema exibe uma mensagem de erro e interrompe o processo de cadastro.
- O sistema deve registrar uma tentativa de falha para auditoria.

### 1.9. Requisitos Não Funcionais:
- O cadastro de um insumo deve ser concluído em até 2 segundos após a confirmação.
- O sistema deve garantir que dois insumos com o mesmo nome não possam ser cadastrados (unicidade de nome).
