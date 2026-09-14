**ITAM (IT Asset Management)** e **CMDB (Configuration Management Database)** são conceitos totalmente diferentes, embora sejam profundamente interligados e frequentemente confundidos.

A forma mais simples de entender a diferença é pensar que o **ITAM cuida do ciclo de vida financeiro e contratual** do ativo (o bolso), enquanto o **CMDB cuida do ciclo de vida operacional e técnico** (o funcionamento).

Aqui está o detalhamento de como cada um funciona e onde eles se diferenciam:

* * *

### 1\. ITAM (Gerenciamento de Ativos de TI) – O Foco Financeiro

O ITAM trata os componentes de TI como **propriedades** da empresa. O objetivo principal é otimizar custos, mitigar riscos de auditoria e gerenciar o ciclo de vida comercial do ativo.

- **O que ele responde?**
    
- Quanto custou este servidor?
    
- De quem nós o compramos e quando expira a garantia?
    
- Quantas licenças de software nós compramos e quantas estão em uso para evitar multas de auditoria (*compliance*)?
    
- Qual é a depreciação financeira desse hardware?
    
- **Atributos comuns no ITAM:** Preço de compra, número da nota fiscal, número de série, contrato de leasing, proprietário do centro de custo, datas de expiração e status de amortização.
    

* * *

### 2\. CMDB (Banco de Dados do Gerenciamento de Configuração) – O Foco Operacional

O CMDB é o coração do gerenciamento de serviços (ITSM). Ele armazena os chamados **IC (Itens de Configuração)** e, mais importante, as **relações e dependências** entre eles para que a TI possa manter os serviços funcionando.

- **O que ele responde?**
    
- Em qual rack do datacenter este servidor físico está instalado?
    
- Quais sistemas operacionais e bancos de dados estão rodando nele?
    
- Se este servidor falhar hoje, **quais serviços de negócio (ex: sistema de vendas, ERP) vão cair?**
    
- Quais atualizações (*patches*) de segurança foram aplicadas a esta máquina?
    
- **Atributos comuns no CMDB:** Endereço IP, versão do firmware, relacionamentos de rede, dependências de software e histórico de incidentes/mudanças vinculados.
    

* * *

### Tabela Comparativa: ITAM vs. CMDB

| Critério | ITAM (Ativos) | CMDB (Configuração / IC) |
| --- | --- | --- |
| **Objetivo Principal** | Gestão de custos, contratos e conformidade legal. | Gestão de estabilidade, suporte e impacto operacional. |
| **Visão do Item** | Um bem de valor que deprecia ao longo do tempo. | Um componente de engenharia que entrega um serviço. |
| **Métrica de Sucesso** | ROI, economia em licenças, auditorias sem multas. | Menor Tempo Médio de Reparo (MTTR), controle de mudanças bem-sucedidas. |
| **Relações** | Vinculado a fornecedores, contratos e usuários. | Vinculado a outros servidores, redes, bancos de dados e serviços. |
| **Ciclo de Vida** | Da Requisição/Compra até o Descarte final. | Da Homologação/Instalação até a Desativação. |

* * *

### Como eles trabalham juntos na prática?

Eles não são excludentes; na verdade, as melhores ferramentas do mercado (como ServiceNow ou Jira Service Management) unificam os dois conceitos.

**Um exemplo prático:**  
Imagine que a sua empresa possui um **Notebook Dell**.

- Para o **ITAM**, esse notebook é o ativo *ID-9874*, que custou R\$ 5.000, foi comprado da distribuidora X, tem garantia de 3 anos e está atribuído ao funcionário André.
- Para o **CMDB**, esse mesmo notebook é um Item de Configuração (IC). O sistema registra que ele roda o Windows 11, tem 16GB de RAM, conecta-se à VPN da empresa e faz uso de um banco de dados hospedado em nuvem.

Se o notebook do André quebrar:

1.  O técnico olha o **CMDB** para entender o impacto técnico (quais acessos ele tinha).
2.  Se for necessário trocar a placa-mãe, o técnico consulta o **ITAM** para verificar se a máquina ainda está no período de garantia de fábrica para acionar o fornecedor sem custos extras.

Em resumo: o **ITAM gerencia o valor** e o **CMDB gerencia o funcionamento**.

[000 - Gestão Patrimonial x ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/000%20-%20Gestão%20Patrimonial%20x%20ITAM%20x%20CMDB.md)

[001 - ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/001%20-%20ITAM%20x%20CMDB.md)

[002 - ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM.md)

[002 - ITAM - Estação de Trabalho](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM%20-%20Estação%20de%20Trabalho.md)

[003 - ITAM - Exemplo](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/003%20-%20ITAM%20-%20Exemplo.md)

[004 - GEMINI](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/004%20-%20ITAM%20-%20Estrutura.md)

[005 - Como fica as contratações de IA](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/005%20-%20ITAM%20-%20Como%20fica%20as%20contratações%20de%20IA.md)

[006 - Proposta para o projeto](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/006%20-%20Proposta%20para%20o%20projeto.md)

[007 - Proposta para o Projeto ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/007%20-%20Proposta%20para%20o%20Projeto%20ITAM.md)