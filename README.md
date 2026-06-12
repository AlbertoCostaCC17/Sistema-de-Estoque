# Sistema de Gerenciamento de Estoque

Este é um sistema web responsivo para controle e gerenciamento de estoque, desenvolvido como projeto acadêmico para o curso de Engenharia de Software (5º Período). O sistema foi construído utilizando tecnologias web padrão (HTML5, CSS3 avançado e JavaScript Vanilla) concentradas em um único arquivo, facilitando a execução e distribuição do protótipo funcional.

## Funcionalidades Executadas no Sistema

O sistema entrega uma experiência interativa completa no modelo de *Single Page Application* (SPA) com controle de estado local:

1. **Dashboard Dinâmico**:
   * Indicadores em tempo real: Total de produtos cadastrados, quantidade total de itens físicos em estoque, alertas de estoque baixo e estoque zerado.
   * Lista visual rápida dos alertas ativos mais importantes e das últimas movimentações registradas.
   * Tabela consolidada de produtos por status e localização.

2. **Gerenciamento de Produtos (CRUD completo)**:
   * Cadastro de novos produtos com campos obrigatórios (SKU, Nome), além de Unidade de medida, Estoque inicial, Estoque mínimo, Categoria e vínculo com um Depósito específico.
   * Filtro de busca instantânea por nome, SKU ou categoria.
   * Edição e exclusão de produtos em tempo real com atualização imediata de todos os indicadores da aplicação.

3. **Movimentações de Estoque**:
   * Registro histórico de **Entradas**, **Saídas** e **Ajustes** (para avarias ou inventário).
   * Validação rígida de integridade que impede saídas maiores do que a quantidade disponível (prevenção de estoque negativo).
   * Histórico detalhado registrando data/hora automática, tipo de movimentação, quantidade alterada, observações e o nome do responsável pela ação.

4. **Controle Dinâmico de Alertas**:
   * Aba dedicada que filtra automaticamente os produtos com estoque crítico (baixo ou zerado), integrando um atalho rápido para registrar a entrada de reposição.
   * Badge de notificação no menu lateral que atualiza dinamicamente o número de alertas pendentes.

5. **Gestão de Depósitos (Múltiplos Locais)**:
   * Cadastro e edição de locais de armazenamento (Depósitos) contendo localização e colaborador responsável.
   * Monitoramento inteligente de volumetria que calcula quantos produtos diferentes estão armazenados em cada depósito e impede a exclusão de depósitos que ainda possuem itens vinculados.

## 🛠️ Tecnologias Utilizadas

* **Estruturação**: HTML5 Semântico.
* **Estilização**: CSS3 customizado utilizando Variáveis CSS (`:root`), layouts estruturados em Grid/Flexbox nativos e design inteiramente responsivo para dispositivos móveis e desktops.
* **Componentes de UI**: Modais nativos interativos, sistema de notificações temporizadas (*Toasts*) e badges dinâmicas de status.
* **Lógica e Persistência**: JavaScript ES6 puro, gerenciando arrays de estado locais para simular perfeitamente o comportamento de uma aplicação conectada a um banco de dados relacional.
