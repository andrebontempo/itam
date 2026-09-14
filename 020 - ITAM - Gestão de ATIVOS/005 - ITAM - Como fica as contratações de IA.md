As contratações de Inteligência Artificial se tornaram um excelente desafio para o gerenciamento de ativos, justamente porque elas quebram o modelo tradicional de TI.

Seguindo a estrutura dos 4 pilares, você deve dividi-las em **dois lugares diferentes**, dependendo do modelo de cobrança. Isso é fundamental para que a equipe de Finanças e a equipe de Compliance tenham os indicadores corretos.

Veja onde encaixar cada uma:

### 1\. No Pilar: **Software Asset Management (SAM / SaaS)**

**Onde ficam:** As assinaturas de preço fixo por usuário/mês.

- **Exemplos:** OpenAI ChatGPT Plus/Enterprise, Microsoft 365 Copilot, GitHub Copilot, Adobe Firefly, Cursor, etc.
    
- **Por que aqui?** Porque elas se comportam exatamente como um **SaaS tradicional**. O foco da gestão de ativos aqui é controlar o **desperdício de licenças**: monitorar se o funcionário que ganhou uma licença de R\$ 150/mês de um assistente de IA realmente a utilizou nos últimos 30 dias. Se não usou, a licença é revogada e repassada para outro.
    

### 2\. No Pilar: **Serviços em Nuvem (Cloud / FinOps)**

**Onde ficam:** As contratações por demanda de consumo (cobrança por volume de tokens, requisições ou horas de processamento de GPU).

- **Exemplos:** Uso de APIs da OpenAI (GPT-4o), Anthropic (Claude), Google Vertex AI, instâncias de GPU na AWS/Azure para treinar modelos próprios.
    
- **Por que aqui?** Porque o comportamento desse gasto é idêntico ao de infraestrutura em nuvem (*IaaS/PaaS*). Não dá para gerenciar por "número de usuários", e sim por **teto de orçamento (Budgets) e telemetria de consumo**. Se um desenvolvedor errar um loop em um script integrado à API da OpenAI, ele pode gerar uma fatura de milhares de dólares em poucas horas. A gestão de ativos aqui precisa de alertas automatizados de consumo diário.
    

### A Camada de Governança (Pilar 4: Contratos)

Lembrando que os pilares se conversam: as duas modalidades acima terão seus contratos jurídicos, termos de uso, políticas de privacidade de dados (LGPD) e faturas gerenciados no pilar de **Contratos**.

### Resumo prático para o seu sistema:

- **IA por Assinatura (Preço Fixo):** Gerencie no módulo de **SaaS/Software** (foco em quantidade de assentos/licenças).
    
- **IA por Tokens/API (Consumo):** Gerencie no módulo de **Cloud/FinOps** (foco em custo financeiro e limites de tráfego/uso).
    
- [000 - Gestão Patrimonial x ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/000%20-%20Gestão%20Patrimonial%20x%20ITAM%20x%20CMDB.md)
    
    [001 - ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/001%20-%20ITAM%20x%20CMDB.md)
    
    [002 - ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM.md)
    
    [002 - ITAM - Estação de Trabalho](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM%20-%20Estação%20de%20Trabalho.md)
    
    [003 - ITAM - Exemplo](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/003%20-%20ITAM%20-%20Exemplo.md)
    
    [004 - GEMINI](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/004%20-%20ITAM%20-%20Estrutura.md)
    
    [005 - Como fica as contratações de IA](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/005%20-%20ITAM%20-%20Como%20fica%20as%20contratações%20de%20IA.md)
    
    [006 - Proposta para o projeto](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/006%20-%20Proposta%20para%20o%20projeto.md)
    
    [007 - Proposta para o Projeto ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/007%20-%20Proposta%20para%20o%20Projeto%20ITAM.md)