&nbsp;

# DIRETRIZES CORPORATIVAS PARA IMPLEMENTAÇÃO DA GESTÃO DE ATIVOS DE TI (ITAM)

## Informações do Documento

| Campo | Informação |
| --- | --- |
| Documento | Diretrizes Corporativas para Implementação da Gestão de Ativos de TI (ITAM) |
| Versão | 2.0 |
| Status | Proposta para Aprovação |
| Autor | André Luiz Bontempo |
| Área Responsável | Tecnologia da Informação / Governança de TI |
| Projeto | Implantação do IT Asset Management (ITAM) no TOPdesk |
| Ferramenta | TOPdesk Asset Management |
| Data de Emissão | 08/07/2026 |
| Última Revisão | 08/07/2026 |
| Próxima Revisão | Julho / 2027 |
| Classificação | Uso Interno |
| Aprovador | *(preencher)* |
| Base Conceitual | ITIL® 4, ISO/IEC 19770, ISO 55000, FinOps Foundation, boas práticas de ITAM e CMDB |

* * *

## Histórico de Revisões

| Versão | Data | Autor | Descrição |
| --- | --- | --- | --- |
| 1.0 | 08/07/2026 | André Luiz Bontempo | Criação inicial do documento. |
| 2.0 | 08/07/2026 | André Luiz Bontempo | Revisão estrutural, inclusão dos quatro pilares (HAM, SAM, Cloud/FinOps e ITCM), integração com CMDB e atualização das diretrizes conforme ITIL 4 e ISO/IEC 19770. |

* * *

## Distribuição
* * *
```

```

Este documento destina-se às seguintes áreas:

- Tecnologia da Informação e Governança de TI
- Service Desk e Infraestrutura
- Segurança da Informação
- Compras e Patrimônio
- Auditoria Interna e Controladoria
- Gestores das Unidades de Negócio

* * *

## Referências Normativas

- **ITIL® 4 Foundation / Intermediate** (Service Configuration & Asset Management)
- **ISO/IEC 19770-1** – IT Asset Management: ITAM framework
- **ISO 55000** – Asset Management: Overview, principles and terminology
- **ISO/IEC 20000** – IT Service Management
- **ISO/IEC 27001** – Information Security Management
- **FinOps Framework** (FinOps Foundation)
- **Documentação Técnica Oficial TOPdesk** (Asset Management API & Module)

* * *

# 1\. INTRODUÇÃO

A Gestão de Ativos de Tecnologia da Informação (*IT Asset Management* – ITAM) consiste no conjunto de processos, políticas, controles e ferramentas destinados a administrar os ativos de TI durante todo o seu ciclo de vida, desde o planejamento da aquisição até sua desativação e descarte final.

Mais do que um inventário patrimonial estático, o ITAM estabelece uma visão integrada dos recursos tecnológicos da organização, permitindo que ativos físicos, softwares, serviços em nuvem, contratos e relacionamentos entre componentes sejam gerenciados de forma estruturada, auditável e alinhada aos objetivos estratégicos da instituição.

Uma implementação eficiente de ITAM proporciona benefícios diretos para diversas áreas da organização, incluindo Tecnologia da Informação, Compras, Controladoria, Auditoria, Segurança da Informação e Governança Corporativa, oferecendo informações confiáveis para tomada de decisão, redução de custos, mitigação de riscos e melhoria contínua dos serviços de TI.

O presente documento estabelece as diretrizes para implantação do programa corporativo de Gestão de Ativos de TI, definindo sua arquitetura, princípios de governança, responsabilidades, categorias de ativos, estrutura mínima de dados, processos operacionais e modelo de evolução. Além disso, este documento servirá como referência para configuração do módulo de *Asset Management* do TOPdesk, definição dos processos organizacionais e integração com ferramentas de descoberta automática, monitoramento e gerenciamento de serviços.

* * *

# 2\. OBJETIVOS DO PROGRAMA ITAM

O Programa Corporativo de Gestão de Ativos de TI possui como objetivos principais:

- **Centralização:** Estabelecer um inventário corporativo único, centralizado e confiável (*Single Source of Truth*).
- **Rastreabilidade:** Garantir rastreabilidade completa dos ativos durante todo o seu ciclo de vida operacional e financeiro.
- **Otimização:** Melhorar a utilização dos recursos tecnológicos disponíveis, reduzindo perdas físicas e financeiras.
- **Conformidade:** Controlar o licenciamento de software e garantir conformidade com os contratos vigentes, mitigando riscos jurídicos.
- **Eficiência em Nuvem:** Reduzir desperdícios de assinaturas e serviços em nuvem por meio do controle contínuo de consumo (FinOps).
- **Apoio à Governança:** Fornecer dados auditáveis e confiáveis para planejamento orçamentário, auditorias internas, externas e conformidade regulatória.
- **Integração Operacional:** Fornecer dados consistentes para a construção da CMDB corporativa, apoiando diretamente os processos de Gerenciamento de Mudanças, Incidentes, Problemas e Continuidade dos Serviços de TI.

* * *

# 3\. ESCOPO

O programa contempla todos os ativos de tecnologia utilizados pela organização, independentemente de sua forma de aquisição, contratação ou consumo, divididos nas seguintes categorias:

### 3.1 Ativos Físicos (Hardware)

Equipamentos tangíveis utilizados pela organização:

- **User Endpoints:** Notebooks, desktops, tablets, smartphones, monitores.
- **Infraestrutura e Periféricos:** Servidores, storages, switches, roteadores, firewalls, access points, nobreaks, impressoras, scanners e equipamentos de telecomunicações.

### 3.2 Ativos de Software

Softwares instalados localmente (*On-Premise*) e licenças corporativas adquiridas:

- Sistemas operacionais, bancos de dados, suítes de escritório, ferramentas de desenvolvimento (Ex: Docker Desktop, JetBrains), middlewares, ferramentas de segurança (Ex: antivírus, EDR) e monitoramento.

### 3.3 Serviços em Nuvem

Serviços contratados em modelos de consumo, subscrição ou utilidade:

- Infraestrutura como Serviço (IaaS), Plataforma como Serviço (PaaS), Software como Serviço (SaaS) corporativos e consumo de APIs comerciais (Ex: OpenAI API, Google Gemini API, Anthropic API).

### 3.4 Contratos de TI

Instrumentos jurídicos e administrativos atrelados aos recursos tecnológicos:

- Garantias de fabricantes, contratos de manutenção, licenciamento de software, outsourcing, links de telecomunicações, acordos de suporte especializado e consultorias.

* * *

# 4\. ARQUITETURA DO PROGRAMA DE GESTÃO DE ATIVOS

A gestão corporativa de ativos será estruturada em quatro domínios complementares e interdependentes, denominados **Pilares do Programa ITAM**.

Cada pilar possui objetivos próprios, regras de categorização e indicadores específicos, mas todos consolidam e cruzam informações por meio do ecossistema do TOPdesk e da Base de Dados de Gerenciamento de Configuração (CMDB).

```
                      +---------------------------------------+
                      |       PROGRAMA CORPORATIVO ITAM       |
                      +---------------------------------------+
                                          |
        +--------------------+------------+------------+--------------------+
        |                    |                         |                    |
        ▼                    ▼                         ▼                    ▼
+---------------+    +---------------+         +---------------+    +---------------+
|   1. HAM      |    |   2. SAM      |         |  3. CLOUD /   |    |   4. ITCM     |
| (Hardware)    |    |  (Software)   |         |    FINOPS     |    |  (Contratos)  |
+---------------+    +---------------+         +---------------+    +---------------+
        |                    |                         |                    |
        +--------------------+------------+------------+--------------------+
                                          |
                                          ▼
                      +---------------------------------------+
                      |  CMDB (Itens de Configuração & Serv.)  |
                      +---------------------------------------+

```

* * *

# 5\. DETALHAMENTO DOS PILARES DO PROGRAMA ITAM

## 5.1 Hardware Asset Management (HAM)

**Objetivo:** Gerenciar o ciclo de vida completo dos ativos físicos. Garante controle patrimonial, localização geográfica, atribuição de responsabilidade e planejamento de ciclos de renovação tecnológica (*hardware refresh*).

### Exemplos de Registro no Sistema

- **Exemplo 1 – User Endpoints**
    
- **Patrimônio:** PAT-2026-0894 | **Ativo:** Notebook Dell Latitude 3440
    
- **Configuração:** Intel Core i5, 16 GB RAM, SSD 512 GB | **Status:** Em uso | **Responsável:** André Luiz Bontempo
    
- **Exemplo 2 – Infraestrutura**
    
- **Patrimônio:** SRV-0042 | **Ativo:** Servidor HPE ProLiant DL380 Gen10
    
- **Status:** Em Produção | **Localização:** Data Center Principal – Rack 04
    
- **Exemplo 3 – Periféricos / Reserva**
    
- **Patrimônio:** NOB-0115 | **Ativo:** Nobreak APC Smart-UPS BR 1500 VA
    
- **Status:** Reserva Técnica | **Localização:** Estoque Central TI
    

* * *

## 5.2 Software Asset Management (SAM)

**Objetivo:** Controlar e otimizar softwares baseados em licenças locais ou subscrições SaaS. Destina-se a mitigar os riscos de sublicenciamento (penalidades em auditorias) e evitar custos com superlicenciamento (licenças ociosas).

### Exemplos de Registro no Sistema

- **Exemplo 1 – Microsoft 365**
    
- **Serviço:** Microsoft 365 Business Premium | **Tipo:** SaaS
    
- **Métrica:** Mensal por usuário | **Contratadas:** 150 | **Em uso:** 132 | **Disponíveis:** 18
    
- **Exemplo 2 – GitHub Enterprise**
    
- **Serviço:** GitHub Enterprise Cloud | **Tipo:** SaaS (Assento de Desenvolvedor)
    
- **Métrica:** Anual | **Quantidade Contratada:** 25
    
- **Exemplo 3 – ChatGPT Enterprise**
    
- **Serviço:** ChatGPT Enterprise | **Tipo:** SaaS | **Métrica:** Mensal
    
- **Alocação:** Equipe de Produto e Inovação | **Quantidade Contratada:** 10
    

* * *

## 5.3 Cloud Asset Management (Cloud / FinOps)

**Objetivo:** Monitorar e governar ativos consumidos sob demanda em ambientes de nuvem pública (IaaS, PaaS e APIs). Devido à volatilidade e ao modelo de cobrança variável desse formato, este pilar atua sob a ótica da disciplina **FinOps** para garantir previsibilidade financeira e eliminação de desperdícios.

### Escopo e Modelos Contemplados

- **IaaS (Infraestrutura):** Instâncias de computação (AWS EC2, Azure VM, Google Compute Engine).
- **PaaS (Plataforma):** Bancos de dados gerenciados (MongoDB Atlas, Azure SQL, Amazon RDS) e clusters de containers (AKS, EKS).
- **APIs Comerciais / IA:** Tokens de processamento de inteligência artificial (OpenAI API, Google Gemini API, Anthropic API).
- **Storage:** Volumes de armazenamento em blocos e objetos (Amazon S3, Azure Blob, Google Cloud Storage).

### Métricas de Controle Operacional

Cada ativo em nuvem deve monitorar e registrar: horas de processamento, consumo de CPU/Memória, IOPS, tráfego de dados (egress), volume de tokens consumidos (IA), custo diário acumulado e o centro de custo associado via tags estruturadas.

### Regras de Governança Financeira (Alertas de Consumo)

> **Mecanismo de Alertas Automáticos baseados no Orçamento (Budgeting):**
> 
> - **Alerta Preventivo:** Disparado ao atingir **80%** do orçamento previsto para o mês.
> - **Alerta de Atenção:** Disparado ao atingir **90%** do orçamento previsto para o mês.
> - **Alerta Crítico:** Acionado imediatamente caso a projeção de consumo linear (*forecast*) aponte estouro do teto orçamentário ou anomalia de gastos (*spike*).
> - **Escalonamento:** Processo formalizado para revisão de arquitetura de nuvem, redimensionamento (*rightsizing*) ou solicitação de crédito suplementar.

### Exemplos de Registro no Sistema

- **Exemplo 1 — Infraestrutura em Nuvem (IaaS)**
    
- **Serviço:** AWS EC2 + Amazon RDS | **Tipo:** IaaS | **Cobrança:** Consumo por Hora
    
- **Métrica:** CPU, Memória e Armazenamento | **Ação:** Alerta preventivo ativo (80% do budget)
    
- **Exemplo 2 — Inteligência Artificial (APIs)**
    
- **Serviço:** OpenAI API | **Tipo:** API Comercial | **Cobrança:** Volume de Tokens (Input/Output)
    
- **Controle:** Consumo Diário com limite configurado via API Management | **Ação:** Bloqueio automático de segurança se estourar o teto diário
    
- **Exemplo 3 — Banco de Dados como Serviço (PaaS)**
    
- **Serviço:** MongoDB Atlas | **Tipo:** PaaS | **Métrica:** Armazenamento de Dados, IOPS e Rede
    
- **Controle:** Escalabilidade automática configurada com teto máximo de cluster (*tier limits*)
    

* * *

## 5.4 IT Contract Management (ITCM)

**Objetivo:** Gerenciar o ciclo de vida administrativo, financeiro e jurídico de todos os contratos que sustentam os ativos de TI. Esse pilar realiza o cruzamento de dependências no TOPdesk, vinculando o instrumento contratual diretamente aos Hardwares, Softwares ou Serviços em nuvem por ele amparados.

### Escopo Documental

Contratos de aquisição, termos de garantia de fabricantes, contratos de suporte e manutenção (*SLA*), contratos de outsourcing de impressão ou alocação de mão de obra, links de telecomunicações e termos de confidencialidade (*NDAs*).

### Informações Mínimas Obrigatórias para Cadastro

Número do contrato, Razão Social do fornecedor (CNPJ), Gestor Técnico do contrato, Objeto detalhado, Valor global e parcelado, Vigência, Índice de reajuste (Ex: IPCA, IGPM), Acordos de Nível de Serviço (SLA) acordados, Cláusula de Renovação Automática e Ativos vinculados.

### Cronograma de Alertas de Vencimento

Os alertas automáticos do TOPdesk para a equipe de Gestão de Contratos e Compras seguirão a régua de antecedência:

- **120 dias antes:** Avaliação de necessidade de renegociação ou abertura de novo processo de contratação.
- **90, 60 e 30 dias antes:** Avisos de acompanhamento e tramitação administrativa.
- **Data do Vencimento:** Alerta de encerramento de vigência.

### Exemplos de Registro no Sistema

- **Exemplo 1 — Garantia de Fabricante**
    
- **Contrato:** CT-DELL-2025-003 | **Objeto:** Dell ProSupport Plus
    
- **Ativos Relacionados:** Notebooks Corporativos (Lote 2025) | **Vencimento:** 15/12/2028
    
- **Exemplo 2 — Telecomunicações**
    
- **Contrato:** CT-CLARO-2026-A | **Objeto:** Link de Internet Dedicado 1 Gbps
    
- **Renovação:** Automática | **Reajuste:** IPCA Anual | **Vencimento:** 20/05/2028
    
- **Exemplo 3 — Outsourcing / Serviços Gerenciados**
    
- **Contrato:** CT-CONSULT-04 | **Objeto:** Serviço Avançado de Administração de Banco de Dados
    
- **SLA:** Atendimento a Incidentes Críticos em até 2 horas | **Vigência:** Até 31/01/2027
    

* * *

# 6\. PAPÉIS E RESPONSABILIDADES

A Gestão de Ativos de TI é um processo corporativo transversal e integrado, não se limitando a uma atividade exclusiva da área de TI. As responsabilidades estão distribuídas conforme descrito abaixo:

- **Tecnologia da Informação:** Responsável pela administração operacional do programa, gerenciamento da ferramenta TOPdesk, execução de inventários técnicos automáticos, validação e manutenção da integridade da CMDB e emissão de relatórios operacionais.
- **Compras:** Responsável pelo relacionamento comercial com fornecedores, condução de processos de aquisição de hardware e software, negociação de cláusulas de suporte e contratualizações, controle de reajustes e formalização de renovações de licenças.
- **Patrimônio / Controladoria:** Atua conjuntamente com a TI para garantir a conciliação físico-contábil, aplicação de etiquetas de patrimônio físico (regras de emplaquetamento corporativo), cálculo de depreciação de hardware e formalização de termos de baixa e descarte de bens.
- **Gestores das Unidades de Negócio:** Responsáveis por aprovar requisições de ativos para suas equipes, validar periodicamente a listagem de colaboradores sob sua gestão que possuem ativos atribuídos e notificar formalmente a TI sobre desligamentos ou transferências internas.
- **Usuários Finais:** Responsáveis diretos pela guarda, zelo e conservação dos ativos físicos fornecidos para o exercício de suas funções, devendo assinar o Termo de Responsabilidade e reportar imediatamente perdas, roubos ou incidentes operacionais.
- **Governança de TI:** Responsável por auditar os processos de ITAM, definir e revisar as políticas corporativas do programa, acompanhar os KPIs estratégicos e avaliar o avanço do nível de maturidade da organização frente ao mercado.

* * *

# 7\. CONFIGURATION MANAGEMENT DATABASE (CMDB)

## 7.1 Diferenciação Conceitual: ITAM vs. CMDB

Para evitar confusões operacionais comuns, o programa estabelece uma clara linha de corte conceitual baseada nas boas práticas do ITIL® 4:

| Atributo | ITAM (Gestão de Ativos) | CMDB (Gerenciamento de Configuração) |
| --- | --- | --- |
| **Foco Principal** | Ciclo de vida financeiro, contratual e patrimonial. | Estrutura operacional, dependências técnicas e serviços. |
| **Unidade de Controle** | Ativo (*Asset*) – Possui valor monetário e depreciação. | Item de Configuração (*CI*) – Componente de um serviço. |
| **Pergunta-Chave** | *"Quanto custou, quem é o dono e onde está?"* | *"Como está conectado e qual o impacto se falhar?"* |
| **Visão de Negócio** | Ênfase em Custos, Contratos, Auditoria e ROI. | Ênfase em Operação, Incidentes, Mudanças e SLA. |

* * *

## 7.2 O que é um Item de Configuração (CI)

Um Item de Configuração (*Configuration Item*) é qualquer componente que precise ser gerenciado para garantir a entrega de um Serviço de TI.

Nem todo ativo patrimonial é um CI (ex: um monitor individual de notebook normalmente é gerido apenas no ITAM), e nem todo CI é um ativo patrimonial (ex: uma Máquina Virtual, um banco de dados lógico ou um Certificado Digital não possuem etiqueta de patrimônio físico, mas são CIs críticos na CMDB).

* * *

## 7.3 Modelagem de Relacionamentos e Dependências na CMDB

O principal valor da CMDB reside no mapeamento das relações de dependência entre os elementos. Isso permite mapear visualmente cadeias de infraestrutura complexas, como ilustrado nos fluxos lógicos abaixo:

**Cenário de Aplicação On-Premise:**

```
[Notebook do Usuário] ──> [Acessa] ──> [Portal ERP] ──> [Executa em] ──> [Servidor de Aplicação Linux]
                                                                                      │
                                                                                      ▼
                                                                           [Banco de Dados PostgreSQL]
                                                                                      │
                                                                                      ▼
                                                                           [Volume no Storage SAN]

```

**Cenário de Aplicação Moderna em Nuvem / Microserviços:**

```
[Portal Corporativo Web] ──> [Balanceador NGINX] ──> [Container Docker] ──> [Cluster Kubernetes (PaaS)]
                                                                                      │
                                                                                      ▼
                                                                           [MongoDB Atlas (Cloud DB)]

```

### Tipos de Relacionamento Suportados no TOPdesk

Para manter a consistência da árvore de serviços, a CMDB utilizará exclusivamente os seguintes conectores padrões: *Depende de*, *Executa em*, *Conectado a*, *Hospedado em*, *Pertence a*, *Monitorado por* e *Contratado por*.

* * *

## 7.4 Benefícios da Integração Operacional

Ao sincronizar o ITAM com a CMDB no TOPdesk, os seguintes processos ganham automação e precisão:

- **Análise de Impacto em Mudanças (Change Management):** Antes de aprovar uma manutenção em um switch de rede, o sistema exibe quais servidores, bancos de dados e serviços de negócio serão afetados.
- **Agilidade no Atendimento de Incidentes (Troubleshooting):** Ao abrir um chamado para um usuário, o técnico visualiza imediatamente a configuração exata do computador dele, os softwares instalados e os chamados recorrentes daquele equipamento.
- **Mitigação de Riscos de Continuidade:** Mapeamento claro de caminhos de redundância de infraestrutura e vinculação de contatos de suporte de terceiros para acionamento de emergência.

* * *

# 8\. CICLO DE VIDA DOS ATIVOS DE TI

Todo ativo controlado pelo programa deve percorrer obrigatoriamente as fases estabelecidas abaixo, com atualização sistêmica de seus respectivos estados no TOPdesk:

```
[ Planejamento ] ──> [ Aquisição ] ──> [ Cadastro (ITAM) ] ──> [ Preparação ]
                                                                      │
                                                                      ▼
 [ Baixa/Descarte ] <── [ Encerramento ] <── [ Manutenção ] <── [ Operação ]

```

1.  **Planejamento:** Identificação da necessidade técnica do ativo e alinhamento orçamentário.

- *Estados:* Solicitado, Em Análise, Aprovado.

2.  **Aquisição:** Processamento da compra pela área de suprimentos.

- *Estados:* Em Aquisição, Pedido Emitido, Recebido (Nota Fiscal).

3.  **Cadastro:** Etapa crítica de entrada do bem no inventário corporativo. É realizado o emplaquetamento físico (HAM) ou registro de chaves/subscrições (SAM/Cloud), amarração ao fornecedor, centro de custo e contrato originário.
4.  **Preparação:** Homologação técnica e instalação de componentes básicos de conformidade antes da entrega. Inclui instalação de sistemas operacionais homologados, agentes de segurança (EDR), inventário automático e aplicação de baselines de conformidade.

- *Estados:* Em Preparação, Disponível.

5.  **Operação:** Período ativo de uso do equipamento.

- *Estados:* Em Uso, Em Produção, Reserva Técnica (Estoque TI), Em Empréstimo.

6.  **Manutenção:** Intervenções preventivas ou corretivas durantes a vida útil do bem.

- *Estados:* Em Garantia, Em Manutenção, Aguardando Peças de Reposição.

7.  **Renovação Tecnológica (*Refresh*):** Substituição programada do hardware por critérios técnicos objetivos: obsolescência severa, custo de manutenção corretiva superior ao valor residual, encerramento de suporte do fabricante (*End of Support - EOS*) ou degradação severa de performance.
8.  **Encerramento e Descarte:** Fim da vida útil corporativa do ativo. Realiza-se a formatação segura de dados (sanitização de discos conforme ISO 27001), desvinculação de licenças do SAM, baixa contábil e destinação para descarte ecologicamente correto com emissão de Certificado de Destruição Ambiental.

- *Estados:* Desativado, Baixado, Descartado.

* * *

# 9\. PROCESSOS OPERACIONAIS E INTEGRAÇÕES DE SISTEMAS

## 9.1 Processo de Movimentação de Ativos

Toda transferência de custódia de um equipamento (mudança de funcionário, alteração de filial física, envio para assistência) exige a imediata atualização no TOPdesk. O processo culminará na geração automática e assinatura digital de um novo **Termo de Responsabilidade** pelo usuário recebedor.

## 9.2 Frequência de Inventários e Auditorias Regulares

O programa não dependerá exclusivamente de processos manuais. Serão realizadas rotinas de conciliação com as seguintes periodicidades recomendadas:

- **Ativos em Nuvem (Cloud Assets):** Auditoria diária automatizada via APIs de billing dos provedores.
- **Ativos de Software (SAM):** Inventário e conciliação mensal via ferramentas de descoberta.
- **Equipamentos de Data Center / Críticos:** Auditoria e varredura de rede trimestral.
- **User Endpoints (Notebooks/Smartphones):** Inventário semestral por amostragem e conciliação de termos de guarda.

* * *

## 9.3 Arquitetura de Integrações do TOPdesk com Ferramentas de Descoberta

Para maximizar a precisão da base de dados e minimizar erros humanos, o módulo de Ativos do TOPdesk atuará de forma integrada com as ferramentas de infraestrutura existentes:

```
+--------------------------------------------------------+
|                  TOPdesk ASSET MANAGEMENT              |
|              (Source of Truth Administrativo)           |
+--------------------------------------------------------+
   ▲              ▲                  ▲              ▲
   │              │                  │              │ (APIs de Billing)
   │              │                  │              +── Provedores Cloud
   │              │                  │                  (AWS, Azure, GCP)
   │              │                  +── Ferramentas DevOps & Infra
   │              │                      (Docker, Kubernetes, Zabbix)
   │              +── Diretórios de Identidade
   │                  (Active Directory / Entra ID)
   +── Ferramentas de Descoberta Automática
       (OCS, GLPI Agent, Intune, SCCM, Lansweeper)

```

- **Ferramentas de Descoberta Automática (Ex: Microsoft Intune, SCCM, OCS, Lansweeper):** Capturam as informações técnicas reais em tempo de execução (especificações de CPU, memória utilizada, softwares efetivamente instalados nas máquinas, endereços IP e MAC).
- **Diretórios de Identidade (Microsoft Active Directory / Entra ID):** Sincronizam automaticamente os dados de usuários (Nome Completo, E-mail, Departamento, Centro de Custo, Status de Ativo/Desligado) evitando inconsistências cadastrais de pessoal.
- **Ferramentas de Monitoramento e DevOps (Ex: Zabbix, Kubernetes API):** Atualizam o status operacional do CI na CMDB (Online/Offline) e auxiliam no desenho automático da topologia de dependências de sistemas e containers.

* * *

# 10\. POLÍTICA DE QUALIDADE DOS DADOS, RISCOS E AUDITORIA

A integridade do programa ITAM reside na confiabilidade de suas informações. Dados desatualizados geram compras errôneas ou falhas críticas em auditorias de grandes fabricantes de software.

## 10.1 Princípios de Qualidade da Informação

- **Completude:** Proibição de cadastros sem o preenchimento de campos mandatórios (como número de série ou centro de custo).
- **Precisão:** Os dados de sistema devem obrigatoriamente refletir a realidade física e lógica do parque de TI.
- **Atualização:** Meta operacional de atualização de movimentações físicas no TOPdesk em até 24 horas úteis após o fato gerador.
- **Integridade:** Unicidade de chaves primárias. Um único número de patrimônio ou número de série não poderá possuir duplicidade de registro.

* * *

## 10.2 Matriz de Gestão de Riscos do Ambiente de Ativos

| Identificação do Risco | Impacto Estimado | Ação de Mitigação Proposta |
| --- | --- | --- |
| **Sublicenciamento de Software** | Multas financeiras elevadas e sanções legais em auditorias de fabricantes. | Cruzamento automatizado mensal entre licenças compradas (ITCM) e instaladas (SAM via Intune). |
| **Ativos Órfãos (Sem Responsável)** | Perda patrimonial por extravio, roubo ou uso indevido de equipamentos da empresa. | Bloqueio automatizado de login na rede para endpoints que não possuam usuário vinculado no TOPdesk por mais de 15 dias. |
| **Desperdício Financeiro em Nuvem** | Custos crescentes e estouro inesperado de orçamento operacional (*OPEX*). | Implantação de rotinas automáticas de FinOps no TOPdesk para identificar instâncias ociosas (*zombie assets*) e alertas baseados em orçamento. |
| **Contratos de Suporte Expirados** | Indisponibilidade prolongada de serviços de missão crítica por falta de suporte técnico do fabricante. | Régua de alertas contratuais agressiva disparada automaticamente a partir de 120 dias antes do vencimento do contrato. |

* * *

# 11\. INDICADORES DE DESEMPENHO (KPIs)

Para avaliação de eficiência do programa e reporte executivo para a Alta Administração, serão consolidados os seguintes painéis de indicadores:

### KPIs de Hardware (HAM)

- $\text{Taxa de Cobertura de Inventário} = \left( \frac{\text{Ativos detectados por varredura automática}}{\text{Total de ativos cadastrados no ITAM}} \right) \times 100$
- Percentual de equipamentos fora do prazo de garantia contratual.
- Idade média do parque tecnológico segregada por categoria de endpoint.
- Índice de ociosidade em estoque (Reserva Técnica mantida acima do *safety stock* acordado).

### KPIs de Software (SAM)

- $\text{Índice de Ociosidade de Licenças} = \left( \frac{\text{Licenças Adquiridas} - \text{Licenças Efetivamente Utilizadas}}{\text{Total de Licenças Adquiridas}} \right) \times 100$
- Volume financeiro economizado através de processos de colheita e reaproveitamento de licenças (*license harvesting*).
- Quantidade de ocorrências detectadas de softwares instalados não homologados ou sem contrato válido.

### KPIs de Cloud / FinOps

- Desvio orçamentário mensal ($\text{Gasto Real} \times \text{Gasto Previsto}$).
- Índice de recursos superdimensionados (*Overprovisioning*) em IaaS e PaaS.
- Redução de custos acumulada gerada por desligamento automático de ambientes de desenvolvimento/homologação fora do horário comercial.

### KPIs de Contratos (ITCM)

- Percentual de renovações contratuais processadas sem interrupção de cobertura de suporte.
- Índice de penalidades aplicadas a fornecedores por descumprimento de cláusulas de SLA acordadas.

* * *

# 12\. MODELO DE MATURIDADE DO PROGRAMA ITAM

O amadurecimento das práticas de gestão de ativos seguirá o seguinte escalonamento tático, visando atingir o **Nível 4** nos primeiros 18 meses de projeto:

```
[ Nível 1: Inicial ] ──> [ Nível 2: Gerenciado ] ──> [ Nível 3: Padronizado ] ──> [ Nível 4: Controlado ] ──> [ Nível 5: Otimizado ]

```

- **Nível 1 – Inicial:** Controle baseado em planilhas eletrônicas descentralizadas, informações incompletas, sem histórico estruturado de movimentações e processos puramente reativos.
- **Nível 2 – Gerenciado:** Inventário centralizado no TOPdesk, processos básicos de entrada e saída documentados, responsabilidades formais de guarda estabelecidas por termo de responsabilidade.
- **Nível 3 – Padronizado:** Processos institucionalizados na cultura organizacional, ferramentas de descoberta operando de forma integrada com o TOPdesk, catálogo corporativo de softwares homologados estabelecido.
- **Nível 4 – Controlado:** CMDB totalmente estruturada e integrada ao módulo de ITAM, governança orientada por indicadores e metas de qualidade de dados, conciliações e auditorias automáticas periódicas.
- **Nível 5 – Otimizado:** Práticas avançadas de FinOps integradas ao planejamento estratégico de expansão de negócios, automações completas de autoatendimento para provisionamento/desprovisionamento de licenças e hardware, melhoria contínua preditiva orientada a dados de consumo.

* * *

# 13\. FATORES CRÍTICOS DE SUCESSO E CONSIDERAÇÕES FINAIS

O sucesso da implementação do programa corporativo de ITAM e CMDB na organização depende fundamentalmente do cumprimento dos seguintes fatores:

1.  Apoio contínuo e visível da Alta Administração para a cobrança de conformidade dos processos por parte das demais gerências de negócio.
2.  Manutenção rigorosa da disciplina operacional de atualização dos cadastros no TOPdesk; ferramentas tecnológicas tornam-se obsoletas se os processos humanos falharem.
3.  Foco na capacitação continuada das equipes de TI, Compras e Controladoria nos conceitos de ITIL 4, ISO 19770 e práticas FinOps.

A consolidação deste programa utilizando o **TOPdesk** como plataforma integradora garantirá a eliminação de silos informacionais, gerando uma visão única, transparente e auditável sobre todo o patrimônio tecnológico corporativo. Este documento constitui a base normativa obrigatória para o direcionamento técnico do projeto de implantação.

* * *

# APÊNDICE A – GLOSSÁRIO

- **ITAM:** *IT Asset Management* (Gestão de Ativos de TI)
- **HAM:** *Hardware Asset Management* (Gestão de Ativos de Hardware)
- **SAM:** *Software Asset Management* (Gestão de Ativos de Software)
- **ITCM:** *IT Contract Management* (Gestão de Contratos de TI)
- **CMDB:** *Configuration Management Database* (Banco de Dados de Gerenciamento de Configuração)
- **CI:** *Configuration Item* (Item de Configuração)
- **ITSM:** *IT Service Management* (Gerenciamento de Serviços de TI)
- **FinOps:** *Financial Operations* (Modelo operacional de gerenciamento financeiro de computação em nuvem)
- **IaaS / PaaS / SaaS:** *Infrastructure / Platform / Software as a Service*
- **SLA:** *Service Level Agreement* (Acordo de Nível de Serviço)
- **EOL / EOS:** *End of Life* (Fim de Vida Comercial) / *End of Support* (Fim de Suporte do Fabricante)

* * *

# APÊNDICE B – MATRIZ RACI DO PROCESSO ITAM

A matriz abaixo define as responsabilidades funcionais para cada atividade crítica do ciclo de vida dos ativos corporativos.

- **R (Responsible):** Quem executa a atividade.
- **A (Accountable):** Quem responde pela atividade, aprova o resultado e possui autoridade final. (Apenas um por linha).
- **C (Consulted):** Quem deve ser consultado antes ou durante a execução (especialistas, assessores).
- **I (Informed):** Quem deve ser informado imediatamente após a conclusão da atividade.

| Atividade do Processo | Governança TI | Operação TI | Compras | Patrimônio | Gestores / Usuários |
| --- | --- | --- | --- | --- | --- |
| Definir Políticas e Diretrizes de ITAM | **A** | **R** | **C** | **C** | **I** |
| Aprovar Orçamento para Aquisição de Ativos | **C** | **I** | **C** | **I** | **A** |
| Executar Processo de Compra e Negociação | **I** | **C** | **A** / **R** | **I** | **I** |
| Recebimento Físico e Emplaquetamento | **I** | **R** | **I** | **A** | **I** |
| Cadastro Administrativo e Contratual no TOPdesk | **C** | **R** | **C** | **I** | **I** |
| Preparação Técnica e Homologação de Imagem | **I** | **A** / **R** | **I** | **I** | **I** |
| Transferência Física / Movimentação Interna | **I** | **R** | **I** | **I** | **A** |
| Executar Inventários e Auditorias de Campo | **A** | **R** | **I** | **C** | **C** |
| Conduzir Processo de Baixa Contábil e Descarte | **C** | **R** | **I** | **A** | **I** |

* * *

# APÊNDICE C – MODELO DE CLASSES DO TOPDESK ASSET MANAGEMENT

Para a parametrização inicial do módulo de novos ativos do TOPdesk, a estrutura lógica de objetos e heranças respeitará o seguinte desenho de taxonomia:

### 1\. Classe Principal: Ativos de Hardware (HAM)

- **Tipo de Ativo (Asset Type):** User Endpoints
    
- *Templates:* Notebook, Desktop, Tablet, Smartphone.
    
- **Tipo de Ativo (Asset Type):** Infraestrutura de Data Center
    
- *Templates:* Servidor Físico, Storage, Appliance, Switch Core, Firewall.
    
- **Tipo de Ativo (Asset Type):** Periféricos e Acessórios
    
- *Templates:* Monitor, Impressora Térmica, Nobreak, Dock Station.
    

### 2\. Classe Principal: Ativos de Software e Nuvem (SAM & Cloud)

- **Tipo de Ativo (Asset Type):** Licenciamento On-Premise
    
- *Templates:* Banco de Dados (Instância Local), Sistema Operacional Servidor.
    
- **Tipo de Ativo (Asset Type):** Subscrições SaaS
    
- *Templates:* Conta M365, Assento GitHub Enterprise, Licença Salesforce.
    
- **Tipo de Ativo (Asset Type):** Componentes de Nuvem (CIs Voláteis)
    
- *Templates:* Instância de Computação (IaaS), Cluster Kubernetes, Bucket de Armazenamento.
    

### 3\. Classe Principal: Contratos e Fornecedores (ITCM)

- **Tipo de Ativo (Asset Type):** Contratos de TI
- *Templates:* Contrato de Suporte Fabricante, Contrato de Link de Dados, NDA.

* * *

# APÊNDICE D – DICIONÁRIO DE DADOS MÍNIMO (TOPDESK INTERFACE)

Este dicionário serve como especificação funcional para a criação de campos obrigatórios dentro dos formulários de cadastro de ativos da plataforma TOPdesk.

| Nome do Campo | Tipo do Dado | Obrigatoriedade | Regra de Preenchimento / Origem | Responsável |
| --- | --- | --- | --- | --- |
| **Identificador Único (Nome)** | Texto Curto | **Mandatório** | Padrão de Nomenclatura: `[Sigla]-[Sequencial]` (Ex: NB-0894). | Operação TI |
| **Número de Patrimônio** | Alfanumérico | **Mandatório (HAM)** | Número gravado na etiqueta física de metal colada pela Controladoria. | Patrimônio |
| **Número de Série (S/N)** | Texto Curto | **Mandatório (HAM)** | Código de série exclusivo do fabricante extraído via BIOS ou etiqueta de fábrica. | Operação TI |
| **Estado do Ciclo de Vida** | Dropdown | **Mandatório** | Valores válidos fixos: `[Em Estoque, Em Uso, Manutenção, Desativado]`. | Operação TI |
| **Usuário Responsável** | Link Interno | Condicional | Obrigatório se o status for "Em Uso". Busca direta na tabela de Pessoas. | Operação TI |
| **Centro de Custo** | Dropdown | **Mandatório** | Código contábil da área de lotação financeira do ativo para rateio de despesas. | Compras / TI |
| **Código do Contrato Vinculado** | Link Interno | **Mandatório** | Relacionamento obrigatório com a classe de Contratos (ITCM) ativa no sistema. | Compras |
| **Criticidade do Ativo** | Dropdown | **Mandatório** | Classificação de Impacto: `[Baixa, Média, Alta, Crítica (Missão Crítica)]`. | Governança TI |
| **Endereço MAC Principal** | Texto (Regex) | Condicional | Obrigatório para ativos de rede e endpoints com placa de comunicação ativa. | Descoberta Aut. |