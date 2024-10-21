# Diagrama de Casos de Uso - Sistema de Gerenciamento de Estoque para Padarias

## Atores

- **Administrador**: Gerencia o sistema, tem acesso a todas as funcionalidades.
- **Funcionário**: Registra entradas e saídas de ingredientes, sem acesso às configurações avançadas.
- **Sistema de Fornecedores**: Sistema externo que recebe pedidos de reabastecimento automatizados.

## Casos de Uso

### 1. Cadastrar Insumos
- **Ator Principal**: Administrador
- **Descrição**: O administrador cadastra novos ingredientes no sistema, incluindo nome, tipo, fornecedor e quantidades mínimas e máximas.

### 2. Registrar Entrada de Ingredientes
- **Ator Principal**: Funcionário
- **Descrição**: O funcionário registra a entrada de novos insumos no estoque quando eles são recebidos pela padaria.

### 3. Registrar Saída de Ingredientes
- **Ator Principal**: Funcionário
- **Descrição**: O funcionário registra a saída de ingredientes do estoque conforme são usados na produção de pães e outros produtos.

### 4. Gerar Relatórios de Consumo
- **Ator Principal**: Administrador
- **Descrição**: O administrador pode visualizar relatórios detalhados sobre o consumo de ingredientes, com gráficos de uso e tendências.

### 5. Configurar Alertas de Estoque Baixo
- **Ator Principal**: Administrador
- **Descrição**: O administrador define limites mínimos de estoque para cada ingrediente. O sistema emite alertas quando o nível de estoque atinge esse limite.

### 6. Emitir Alertas de Estoque Baixo
- **Ator Principal**: Sistema (Automático)
- **Descrição**: O sistema automaticamente gera alertas quando os níveis de estoque atingem o limite mínimo configurado.

### 7. Enviar Pedido de Reabastecimento
- **Ator Principal**: Sistema (Automático)
- **Atores Envolvidos**: Sistema de Fornecedores
- **Descrição**: Quando o estoque atinge um nível crítico, o sistema envia automaticamente um pedido de compra ao sistema de fornecedores externo.
