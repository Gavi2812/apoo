# Documento de Requisitos (v1)

## 1. Introdução

### 1.1. Propósito
Este documento tem como objetivo detalhar os requisitos do sistema de gerenciamento de estoque destinado a pequenas e médias padarias que utilizam insumos como farinha, fermento e outros ingredientes na produção artesanal. O sistema visa automatizar e otimizar o controle de estoque, fornecendo funcionalidades que garantem maior eficiência na gestão dos insumos utilizados diariamente.

### 1.2. Escopo
O sistema permitirá às padarias controlar o estoque de insumos, registrar entradas e saídas, gerar relatórios e emitir alertas quando o nível de um ingrediente estiver baixo. Ele também oferecerá sugestões automáticas para novas compras com base no histórico de consumo.

### 1.3. Definições, Acrônimos e Abreviações
- **Estoque**: Quantidade disponível de ingredientes.
- **Entrada**: Registro de novos insumos no estoque.
- **Saída**: Consumo de ingredientes durante a produção.
- **Ingrediente**: Insumo necessário para a produção de pães e outros produtos.
  
### 1.4. Referências
- Livro: "Gestão de Estoque em Pequenas Empresas", 2022.
- Documentação oficial de Django e Flask para o backend.
- GitHub para controle de versão e desenvolvimento colaborativo.

---

## 2. Descrição Geral

### 2.1. Perspectiva do Produto
O **Sistema de Gerenciamento de Estoque para Padarias** é um sistema de software desenvolvido para facilitar a gestão de ingredientes. Ele proporcionará à padaria uma interface amigável para registrar entradas e saídas de insumos, automatizar alertas de reabastecimento e gerar relatórios sobre o uso de ingredientes.

### 2.2. Funções do Sistema
- Controle de entrada e saída de ingredientes.
- Relatórios automáticos de níveis de estoque.
- Alertas para insumos com nível baixo.
- Sugestão automática de pedidos de compra com base no histórico.
- Dashboard com gráficos de consumo e estoque.

### 2.3. Usuários
- **Administrador**: Usuário com acesso total ao sistema, capaz de visualizar relatórios, configurar alertas e gerenciar o estoque.
- **Funcionário**: Usuário responsável por registrar entradas e saídas de ingredientes.

### 2.4. Restrições
- O sistema será acessado via navegador web e precisará de uma conexão à internet para funcionar.
- O sistema deve ser fácil de usar em dispositivos móveis e desktops.

---

## 3. Requisitos Funcionais

### RF01 - Cadastro de Ingredientes
O sistema deve permitir o cadastro de ingredientes contendo os seguintes campos: nome, tipo (farinha, fermento, etc.), quantidade mínima, quantidade máxima e fornecedor.

### RF02 - Registro de Entrada de Ingredientes
O sistema deve permitir o registro de novas entradas de ingredientes no estoque.

### RF03 - Registro de Saída de Ingredientes
O sistema deve permitir o registro de saídas de ingredientes durante a produção de pães e outros produtos.

### RF04 - Relatórios de Consumo
O sistema deve gerar relatórios que detalham o consumo de ingredientes em períodos diários, semanais e mensais.

### RF05 - Alertas de Estoque Baixo
O sistema deve emitir alertas automáticos quando o nível de um ingrediente atingir o limite mínimo cadastrado.

### RF06 - Sugestão de Pedidos de Compra
O sistema deve sugerir automaticamente pedidos de compra com base no consumo médio dos últimos 30 dias.

### RF07 - Dashboard de Visualização
O sistema deve apresentar um painel de controle com gráficos de consumo e estoque atualizado.

---

## 4. Requisitos Não Funcionais

### RNF01 - Compatibilidade de Dispositivos
O sistema deve ser compatível com desktops, tablets e smartphones.

### RNF02 - Performance
O sistema deve ser capaz de processar e exibir relatórios de estoque em menos de 2 segundos.

### RNF03 - Segurança
O sistema deve utilizar criptografia para proteger os dados sensíveis, como informações de fornecedores e quantidades de estoque.

### RNF04 - Escalabilidade
O banco de dados deve suportar até 100.000 registros de insumos e transações.

### RNF05 - Disponibilidade
O sistema deve estar disponível 99% do tempo, garantindo mínimo de inatividade para que as padarias não sejam afetadas em suas operações diárias.

---

## 5. Interface de Usuário

### IU01 - Tela de Cadastro de Ingredientes
A tela de cadastro deve permitir a inserção rápida de novos ingredientes com preenchimento automático de campos, como fornecedor e tipo de ingrediente.

### IU02 - Tela de Dashboard
A tela de dashboard deve exibir gráficos interativos para uma melhor visualização do consumo de insumos e níveis de estoque.

---

## 6. Regras de Negócio

### RN01 - Estoque Mínimo
Se o estoque de um ingrediente atingir o nível mínimo configurado, um alerta deve ser emitido imediatamente para o administrador.

### RN02 - Consumo por Produção
Cada tipo de pão cadastrado deve consumir uma quantidade específica de ingredientes, afetando diretamente o nível de estoque.

### RN03 - Sugestão de Compras
A sugestão de compras deve ser feita com base no consumo médio de cada ingrediente nos últimos 30 dias, evitando desperdício e falta de insumos.

