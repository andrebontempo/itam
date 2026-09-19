# DIRETRIZES CORPORATIVAS PARA IMPLEMENTAÇÃO DA GESTÃO DE ATIVOS DE TI (ITAM)

## Informações do Documento

| Campo | Informação |
| --- | --- |
| Documento | Diretrizes Corporativas para Implementação da Gestão de Ativos de TI (ITAM) |
| Versão | 8.0 |
| Status | Proposta para Aprovação |
| Autor | André Luiz Bontempo / Especialista ITIL v4 & Arquiteto TOPdesk |
| Área Responsável | Tecnologia da Informação / Governança de TI |
| Projeto | Implantação do IT Asset Management (ITAM) no TOPdesk |
| Ferramenta | TOPdesk Asset Management (Módulo Flexível de Ativos) |
| Data de Emissão | 08/07/2026 |
| Última Revisão | 18/09/2026 |
| Próxima Revisão | Setembro / 2027 |
| Classificação | Uso Interno |
| Aprovador | *(preencher)* |
| Base Conceitual | ITIL® 4, ISO/IEC 19770, ISO 55000, FinOps Foundation, boas práticas de ITAM e CMDB |

* * *

## Histórico de Revisões

| Versão | Data | Autor | Descrição |
| --- | --- | --- | --- |
| 1.0 | 08/07/2026 | André Luiz Bontempo | Criação inicial do documento. |
| 2.0 | 08/07/2026 | André Luiz Bontempo | Revisão estrutural, inclusão dos quatro pilares (HAM, SAM, Cloud/FinOps e ITCM), integração com CMDB e atualização das diretrizes conforme ITIL 4 e ISO/IEC 19770. |
| 3.0 | 29/07/2026 | André Luiz Bontempo / Antigravity | Revisão conceitual focada em ITIL v4: co-criação de valor e Quatro Dimensões; refinamento do pilar Cloud/FinOps; integração operacional de incidentes e requisições; automatização por Action Sequences; Termo no SSP e LGPD. |
| 4.0 | 14/09/2026 | André Luiz Bontempo / Antigravity | Revisão geral de governança e especificação funcional exaustiva dos Campos Obrigatórios no TOPdesk para Hardware (HAM) e Software (SAM), categorizados por abas. |
| 5.0 | 14/09/2026 | André Luiz Bontempo / Antigravity | Adequação estrita do escopo para Ativos de Tecnologia da Informação (TI), removendo visões e contextualizações de pesquisa agropecuária, biotecnologia e inovação no campo, focando exclusivamente na gestão corporativa de TI. |
| 6.0 | 18/09/2026 | André Luiz Bontempo / Antigravity | Alinhamento da taxonomia de classes (Apêndice C) e do Dicionário de Dados do modelo 'Estação de Trabalho' (Apêndice D.1) com a implementação no TOPdesk Designer de Modelo, incorporando as 6 seções funcionais (Identificação, Especificações Técnicas & CMDB, Financeiro/Contratual, Custódia/Compliance, Grade de Relações e Documentos). |
| 7.0 | 18/09/2026 | André Luiz Bontempo / Antigravity | Incorporação do modelo 'Dispositivo Móvel' (Smartphones, Tablets, Modems), expansão da taxonomia no Apêndice C e inclusão do Dicionário de Dados detalhado (Apêndice D.3) alinhado com o TOPdesk Designer de Modelo. |
| 8.0 | 18/09/2026 | André Luiz Bontempo / Antigravity | Incorporação do modelo 'Monitor' (Visores e Displays corporativos), especificação do Dicionário de Dados detalhado no Apêndice D.4 e renumeração de regras de validação para D.5. |

* * *

## Distribuição

Este documento destina-se às seguintes áreas:

- Tecnologia da Informação e Governança de TI
- Service Desk, Suporte e Infraestrutura
- Segurança da Informação e Compliance
- Compras, Suprimentos e Contratos
- Patrimônio, Controladoria e Auditoria Interna
- Gestores das Unidades de Negócio

* * *

## Referências Normativas

- **ITIL® 4 Foundation / Intermediate / Specialist** (Service Configuration Management & IT Asset Management Practices)
- **ISO/IEC 19770-1** – IT Asset Management: ITAM framework
- **ISO 55000** – Asset Management: Overview, principles and terminology
- **ISO/IEC 20000** – IT Service Management
- **ISO/IEC 27001** – Information Security Management
- **Lei Geral de Proteção de Dados (LGPD)** – Lei nº 13.709/2018
- **FinOps Framework** (FinOps Foundation)
- **Documentação Técnica Oficial TOPdesk** (Asset Management API & Module)

* * *

# 1. INTRODUÇÃO E GOVERNANÇA (ITIL® 4)

A Gestão de Ativos de Tecnologia da Informação (*IT Asset Management* – ITAM) consiste no conjunto de processos, políticas, controles e ferramentas destinados a administrar os ativos de TI durante todo o seu ciclo de vida, desde o planejamento da aquisição até sua desativação e descarte final.

Mais do que um inventário patrimonial estático, o ITAM estabelece uma visão integrada dos recursos tecnológicos da organização, permitindo que ativos físicos, softwares, serviços em nuvem, contratos e relacionamentos entre componentes sejam gerenciados de forma estruturada, auditável e alinhada aos objetivos estratégicos da instituição.

Uma implementação eficiente de ITAM proporciona benefícios diretos para diversas áreas da organização, incluindo Tecnologia da Informação, Compras, Controladoria, Auditoria, Segurança da Informação e Governança Corporativa, oferecendo informações confiáveis para tomada de decisão, redução de custos, mitigação de riscos e melhoria contínua dos serviços de TI.

O presente documento estabelece as diretrizes para implantação do programa corporativo de Gestão de Ativos de TI, definindo sua arquitetura, princípios de governança, responsabilidades, categorias de ativos, estrutura mínima de dados, processos operacionais e modelo de evolução. Além disso, este documento servirá como referência para configuração do módulo de *Asset Management* do TOPdesk, definição dos processos organizacionais e integração com ferramentas de descoberta automática, monitoramento e gerenciamento de serviços.

## 1.1 Co-criação de Valor na Embrapa
Em alinhamento com a **ITIL® 4**, o programa ITAM é concebido sob a ótica da **Co-criação de Valor**. Os ativos de TI não devem ser geridos meramente como bens contábeis ou itens isolados de infraestrutura, mas sim como habilitadores estratégicos que sustentam diretamente a produtividade, a eficiência operacional e a continuidade dos serviços corporativos de Tecnologia da Informação da Embrapa.

A exatidão da base de ativos garante que colaboradores e equipes técnicas tenham acesso a equipamentos funcionais, softwares devidamente licenciados e serviços de infraestrutura de alta disponibilidade. Paralelamente, a otimização de ativos reduz os desperdícios orçamentários, garantindo a governança financeira e a alocação eficiente dos recursos de TI.

## 1.2 As Quatro Dimensões da Gestão de Ativos de TI (ITAM)
Para assegurar uma abordagem holística e evitar falhas comuns de implementação baseadas puramente em software, o programa ITAM é modelado sob a estrutura das **Quatro Dimensões do Gerenciamento de Serviço da ITIL® 4**:

```
           +-------------------------------------------------------+
           |               AS QUATRO DIMENSÕES DO ITAM             |
           +-------------------------------------------------------+
           |                                                       |
           |   1. Organizações e Pessoas                           |
           |      - Definição de papéis de Governança, TI, Compras |
           |        e Patrimônio. Conscientização do usuário final |
           |        sobre a guarda de ativos.                      |
           |                                                       |
           |   2. Informação e Tecnologia                          |
           |      - Configuração do TOPdesk Asset Management como  |
           |        "Single Source of Truth", integrado a          |
           |        agentes de varredura automática (discovery).   |
           |                                                       |
           |   3. Parceiros e Fornecedores                         |
           |      - Gestão do ciclo de vida contratual (ITCM) para |
           |        garantir conformidade de SLAs, suporte técnico |
           |        vigente e renovações programadas.              |
           |                                                       |
           |   4. Fluxos de Valor e Processos                      |
           |      - Integração operacional do ciclo de vida dos    |
           |        ativos aos processos consolidados de           |
           |        Incidentes e Requisições no TOPdesk.           |
           |                                                       |
           +-------------------------------------------------------+
```

* * *

# 2. OBJETIVOS DO PROGRAMA ITAM

O Programa Corporativo de Gestão de Ativos de TI possui como objetivos principais:

- **Centralização:** Estabelecer um inventário corporativo único, centralizado e confiável (*Single Source of Truth*) por meio do TOPdesk Asset Management.
- **Rastreabilidade:** Garantir rastreabilidade completa dos ativos durante todo o seu ciclo de vida operacional, contratual e financeiro.
- **Otimização:** Melhorar a utilização dos recursos tecnológicos disponíveis, reduzindo perdas físicas, licenças obsoletas e ociosidades financeiras.
- **Conformidade:** Controlar o licenciamento de software e garantir conformidade com os contratos vigentes, mitigando riscos jurídicos perante fabricantes.
- **Eficiência em Nuvem (FinOps):** Reduzir desperdícios de assinaturas e serviços em nuvem pública por meio do controle contínuo de consumo estrutural.
- **Apoio à Governança e Auditoria:** Fornecer dados estruturados e auditáveis para planejamento orçamentário, auditorias internas, externas e compliance regulatório.
- **Integração Operacional:** Fornecer dados consistentes para a construção da CMDB corporativa, apoiando diretamente os processos existentes de Gerenciamento de Mudanças, Incidentes, Problemas e Continuidade dos Serviços de TI.
- **Sustentabilidade Tecnológica:** Monitorar a fase de descarte de hardware para assegurar a destinação ecológica correta e reciclagem de componentes eletrônicos obsoletos em conformidade com as diretrizes de responsabilidade ambiental da Embrapa.

* * *

# 3. ESCOPO

O programa contempla todos os ativos de tecnologia utilizados pela organização, independentemente de sua forma de aquisição, contratação ou consumo, divididos nas seguintes categorias:

### 3.1 Ativos Físicos (Hardware)
Equipamentos tangíveis utilizados pela organização:
- **User Endpoints:** Notebooks, desktops, tablets, smartphones, monitores.
- **Infraestrutura e Periféricos:** Servidores físicos, storages, switches, roteadores, firewalls, access points, nobreaks, impressoras, scanners e equipamentos de telecomunicações.

### 3.2 Ativos de Software
Softwares instalados localmente (*On-Premise*) e licenças corporativas adquiridas:
- Sistemas operacionais de servidores e estações, bancos de dados corporativos, suítes de escritório, ferramentas de desenvolvimento (Ex: Docker Desktop, JetBrains), middlewares, ferramentas de segurança (Ex: antivírus, EDR) e monitoramento.
- **Softwares Especialistas e Sistemas de TI:** Softwares corporativos de alto valor e alta especialidade voltados para engenharia de software, bancos de dados, infraestrutura e segurança (Ex: Oracle Database, Red Hat Enterprise Linux, VMware/Broadcom, JetBrains, ferramentas de BI e análise estatística), cuja gestão é crítica devido à diversidade de modelos de licenciamento (por core, concorrente, por volume ou subscrição).

### 3.3 Serviços em Nuvem
Serviços contratados em modelos de consumo, subscrição ou utilidade:
- Infraestrutura como Serviço (IaaS), Plataforma como Serviço (PaaS), Software como Serviço (SaaS) corporativos e consumo de APIs comerciais (Ex: OpenAI API, Google Gemini API, Anthropic API).

### 3.4 Contratos de TI
Instrumentos jurídicos e administrativos atrelados aos recursos tecnológicos:
- Garantias de fabricantes, contratos de suporte e manutenção (*SLA*), licenciamento de software, outsourcing, links de telecomunicações, acordos de suporte especializado e consultorias.

* * *

# 4. ARQUITETURA DO PROGRAMA DE GESTÃO DE ATIVOS

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

# 5. DETALHAMENTO DOS PILARES DO PROGRAMA ITAM

## 5.1 Hardware Asset Management (HAM)
**Objetivo:** Gerenciar o ciclo de vida completo dos ativos físicos. Garante controle patrimonial, localização geográfica, atribuição de responsabilidade e planejamento de ciclos de renovação tecnológica (*hardware refresh*).

> [!IMPORTANT]
> **Requisito Cadastral no TOPdesk (HAM):**
> Todo ativo físico deve ter seu **Cartão de Ativo** cadastrado no modelo **Estação de Trabalho** (ou demais modelos de Hardware) preenchido obrigatoriamente conforme o **Dicionário de Campos de Hardware (Apêndice D.1)**. A ausência de preenchimento dos campos obrigatórios (como Número de Série, Patrimônio e Centro de Custo) bloqueará a disponibilização do equipamento no catálogo de serviços do Service Desk.

### Exemplos de Registro no Sistema
- **Exemplo 1 – User Endpoints (Estação de Trabalho)**
  - **Patrimônio:** PAT-2026-0894 | **Modelo:** Estação de Trabalho (Notebook Dell Latitude 3440)
  - **Configuração:** Intel Core i5, 16 GB RAM, SSD 512 GB | **Status:** Em Uso | **Responsável:** André Luiz Bontempo
- **Exemplo 2 – Infraestrutura (Servidor)**
  - **Patrimônio:** SRV-0042 | **Modelo:** Servidor (HPE ProLiant DL380 Gen10)
  - **Status:** Em Produção | **Localização:** Data Center Principal – Rack 04
- **Exemplo 3 – Periféricos / Reserva**
  - **Patrimônio:** NOB-0115 | **Modelo:** Periférico (Nobreak APC Smart-UPS BR 1500 VA)
  - **Status:** Em Estoque | **Localização:** Estoque Central TI

* * *

## 5.2 Software Asset Management (SAM)
**Objetivo:** Controlar e otimizar softwares baseados em licenças locais ou subscrições SaaS. Destina-se a mitigar os riscos de sublicenciamento (penalidades em auditorias) e evitar custos com superlicenciamento (licenças ociosas).

> [!IMPORTANT]
> **Requisito Cadastral no TOPdesk (SAM):**
> As licenças corporativas, subscrições SaaS e softwares especialistas de TI da Embrapa devem ter seus registros efetuados rigorosamente com base no **Dicionário de Campos de Software (Apêndice D.2)**. O controle de conformidade entre licenças adquiridas e instâncias ativas coletadas via varredura automatizada depende da precisão destes atributos.

### Exemplos de Registro no Sistema
- **Exemplo 1 – Microsoft 365**
  - **Serviço:** Microsoft 365 Business Premium | **Tipo:** SaaS
  - **Métrica:** Mensal por usuário | **Contratadas:** 150 | **Em uso:** 132 | **Disponíveis:** 18
- **Exemplo 2 – Softwares Especialistas de TI (Ex: JetBrains / Oracle DB)**
  - **Serviço:** JetBrains All Products Pack | **Tipo:** Licença Corporativa / Concorrente (*Floating*)
  - **Métrica:** Anual por assento/servidor de licença | **Servidor:** LICSVR-DEV-01 | **Módulos:** IntelliJ, PyCharm, WebStorm
- **Exemplo 3 – GitHub Enterprise**
  - **Serviço:** GitHub Enterprise Cloud | **Tipo:** SaaS (Assento de Desenvolvedor)
  - **Métrica:** Anual | **Quantidade Contratada:** 25

* * *

## 5.3 Cloud Asset Management (Cloud / FinOps)
**Objetivo:** Monitorar e governar ativos consumidos sob demanda em ambientes de nuvem pública (IaaS, PaaS e APIs). Devido à volatilidade e ao modelo de cobrança variável desse formato, este pilar atua sob a ótica da disciplina **FinOps** para garantir previsibilidade financeira e eliminação de desperdícios.

### Escopo e Delimitação Conceitual no TOPdesk
> [!IMPORTANT]
> **Alinhamento Arquitetural de Dados:**
> Para garantir a estabilidade e a performance do banco de dados do TOPdesk, a ferramenta **NÃO** registrará dados voláteis de telemetria fina em tempo real (como consumo instantâneo de CPU, tráfego de dados (egress), IOPS ou contagem bruta de chamadas de API). O monitoramento de desempenho e o faturamento granular diário permanecerão nas ferramentas e plataformas nativas de nuvem (AWS Cost Explorer, Azure Cost Management, GCP Billing, Vantage, etc.).
> 
> O TOPdesk será a fonte de verdade para a **Governança e Metadados Estruturais** do recurso em nuvem, registrando: ID único do recurso na nuvem, Provedor Cloud, Tipo de Instância/Recurso, Centro de Custo associado, Dono do Ativo, Ambiente (Produção/Homologação/Desenvolvimento) e links diretos para os respectivos consoles ou dashboards de monitoramento técnico.

### Métricas de Controle de Governança
Cada ativo em nuvem deve registrar no TOPdesk: data de criação, ciclo de faturamento recorrente, centro de custo associado via tags estruturadas de governança e custo acumulado consolidado no fechamento mensal.

### Regras de Governança Financeira (Alertas de Consumo)
As ferramentas nativas de gerenciamento de custos de nuvem serão configuradas para disparar alertas com base no Orçamento (*Budgeting*):
- **Alerta Preventivo:** Disparado ao atingir **80%** do orçamento previsto para o mês.
- **Alerta de Atenção:** Disparado ao atingir **90%** do orçamento previsto para o mês.
- **Alerta Crítico (Anomalia/Estouro):** Disparado se houver projeção de estouro ou um pico repentino de consumo (*spend spike*).
- **Integração com o TOPdesk via Webhook:** Ao atingir o status **Crítico (Estouro)** nas ferramentas de nuvem, um Webhook enviará um alerta automático para o TOPdesk, abrindo imediatamente um **Chamado de Incidente** de prioridade adequada na fila de suporte de infraestrutura para que o fluxo de incidentes nativo seja ativado para análise de arquitetura ou redimensionamento (*rightsizing*).

### Exemplos de Registro no Sistema
- **Exemplo 1 — Infraestrutura em Nuvem (IaaS)**
  - **Serviço:** AWS EC2 + Amazon RDS | **Tipo:** IaaS | **Cobrança:** Consumo por Hora
  - **Governança:** Vinculado ao Centro de Custo da Infraestrutura de TI | **Ação:** Webhook integrado para abertura de incidente se houver desvio orçamentário.
- **Exemplo 2 — Inteligência Artificial (APIs)**
  - **Serviço:** OpenAI API | **Tipo:** API Comercial | **Cobrança:** Volume de Tokens
  - **Controle:** Teto diário configurado via API Management.
- **Exemplo 3 — Banco de Dados como Serviço (PaaS)**
  - **Serviço:** MongoDB Atlas | **Tipo:** PaaS | **Governança:** Centro de Custo Desenvolvimento de Softwares.

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
- **90, 60 e 30 dias antes:** Avisos de acompanhamento e tramitação administrativa no Service Desk.
- **Data do Vencimento:** Alerta de encerramento de vigência e potencial interrupção de serviço.

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

# 6. PAPÉIS E RESPONSABILIDADES

A Gestão de Ativos de TI é um processo corporativo transversal e integrado. As responsabilidades estão distribuídas conforme descrito abaixo:

- **Tecnologia da Informação (Operação de TI):** Responsável pela administração operacional do programa ITAM, gerenciamento da ferramenta TOPdesk, execução de inventários técnicos automáticos, validação e manutenção da integridade da CMDB, atualização do ciclo de vida técnico e emissão de relatórios operacionais.
- **Compras (Suprimentos e Contratos):** Responsável pelo relacionamento comercial com fornecedores, condução de processos de aquisição de hardware e software, negociação de cláusulas de suporte e contratualizações, controle de reajustes e formalização de renovações de licenças.
- **Patrimônio / Controladoria:** Atua conjuntamente com a TI para garantir a conciliação físico-contábil, aplicação de etiquetas de patrimônio físico (regras de emplaquetamento corporativo), cálculo de depreciação de hardware e formalização de termos de baixa e descarte de bens.
- **Gestores das Unidades de Negócio:** Responsáveis por aprovar requisições de ativos para suas equipes, validar periodicamente a listagem de colaboradores sob sua gestão que possuem ativos atribuídos e notificar formalmente a TI sobre desligamentos ou transferências internas.
- **Usuários Finais:** Responsáveis diretos pela guarda, zelo e conservação dos ativos físicos fornecidos para o exercício de suas funções, devendo efetuar o aceite digital do Termo de Responsabilidade no Portal de Autoatendimento (SSP) e reportar imediatamente perdas, roubos ou incidentes operacionais.
- **Governança de TI / Compliance:** Responsável por auditar os processos de ITAM, definir e revisar as políticas corporativas do programa, acompanhar os KPIs estratégicos e avaliar o avanço do nível de maturidade da organização frente ao mercado.

* * *

# 7. CONFIGURATION MANAGEMENT DATABASE (CMDB)

## 7.1 Diferenciação Conceitual: ITAM vs. CMDB

Para evitar confusões operacionais comuns, o programa estabelece uma clara linha de corte conceitual baseada nas boas práticas do ITIL® 4:

| Atributo | ITAM (Gestão de Ativos) | CMDB (Gerenciamento de Configuração) |
| --- | --- | --- |
| **Foco Principal** | Ciclo de vida financeiro, contratual e patrimonial. | Estrutura operacional, dependências técnicas e serviços. |
| **Unidade de Controle** | Ativo (*Asset*) – Possui valor monetário e depreciação. | Item de Configuração (*CI*) – Componente de um serviço. |
| **Pergunta-Chave** | *"Quanto custou, quem é o dono e onde está?"* | *"Como está conectado e qual o impacto se falhar?"* |
| **Visão de Negócio** | Ênfase em Custos, Contratos, Auditoria e ROI. | Ênfase em Operação, Incidentes, Mudanças e SLA. |

### 7.1.1 Consolidação Prática no TOPdesk: Abas e Controle de Acesso
Apesar das divisões conceituais, os universos de ITAM e CMDB consolidam-se no mesmo **Cartão de Ativo** dentro do TOPdesk. Esta arquitetura evita duplicidade de dados e silos de informação. A separação dos perfis se dá por meio de **Blocos de Cadastro** com controle rígido de acesso:
- **Bloco Operacional / Especificações Técnicas & CMDB:** Visível e editável para as equipes de Suporte, Service Desk e Infraestrutura. Registra informações como número de série, endereço IP, MAC, sistema operacional, versão do software e dependências técnicas na topologia do serviço.
- **Bloco Financeiro, Contratual & Suprimentos:** Visível apenas para perfis de Governança de TI, Compras e Controladoria/Patrimônio. Contém dados de Nota Fiscal, valor de aquisição, depreciação acumulada, fornecedor e contrato de suporte amarrado.

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

> [!IMPORTANT]
> **Regra de Ouro da CMDB:**
> Deve-se evitar o mapeamento exaustivo de cabos, periféricos simples ou switches de borda não gerenciados. Mapeie apenas itens de configuração que agreguem valor à análise de impacto técnico e tomada de decisão no Service Desk.

* * *

## 7.4 Benefícios da Integração Operacional com Módulos Operantes (Incidentes e Requisições)

Considerando que a Embrapa já tem consolidado o uso do TOPdesk para a **Gestão de Incidentes** e **Requisição de Serviços**, a ativação da CMDB e ITAM potencializará a operação da seguinte forma:

- **Vinculação Obrigatória em Incidentes:** Todos os chamados de incidentes abertos, tanto na interface dos analistas de Service Desk quanto na abertura pelo Portal de Autoatendimento (SSP) do usuário final, deverão obrigatoriamente ter o Ativo/CI impactado selecionado.
- **Identificação de Ativos Problemáticos ("Limões"):** O TOPdesk consolidará no Cartão de Ativo todo o histórico de chamados abertos vinculados a ele. Isso possibilita à TI a visualização rápida e geração de relatórios de equipamentos com recorrência crítica de falhas, acelerando a tomada de decisão para manutenção corretiva especializada ou aceleração de sua substituição programada (*Hardware Refresh*).
- **Integração com a Base de Conhecimento:** Ao selecionar um Ativo/CI afetado na tela do chamado, o TOPdesk associará e sugerirá de forma proativa itens da Base de Conhecimento correlatos, agilizando o *troubleshooting* pelo técnico.
- **Análise de Impacto em Mudanças (Change Management):** Antes de aprovar uma manutenção preventiva ou corretiva de infraestrutura, a árvore de CMDB exibirá de forma gráfica e automatizada quais aplicações corporativas, servidores lógicos e serviços de TI do negócio serão paralisados ou afetados.

* * *

# 8. CICLO DE VIDA DOS ATIVOS DE TI

Todo ativo controlado pelo programa deve percorrer obrigatoriamente as fases estabelecidas abaixo, com atualização sistêmica de seus respectivos estados no TOPdesk:

```
[ Planejamento ] ──> [ Aquisição ] ──> [ Cadastro (ITAM) ] ──> [ Preparação ]
                                                                      │
                                                                      ▼
 [ Baixa/Descarte ] <── [ Encerramento ] <── [ Manutenção ] <── [ Operação ]
```

1. **Planejamento:** Identificação da necessidade técnica do ativo e alinhamento orçamentário.
   - *Estados:* Solicitado, Em Análise, Aprovado.
2. **Aquisição:** Processamento da compra pela área de suprimentos/compras.
   - *Estados:* Em Aquisição, Pedido Emitido, Recebido (Nota Fiscal).
3. **Cadastro:** Etapa crítica de entrada do bem no inventário corporativo. É realizado o emplaquetamento físico (HAM) ou registro de chaves/subscrições (SAM/Cloud), amarração ao fornecedor, centro de custo e contrato originário.
4. **Preparação:** Homologação técnica e instalação de componentes básicos de conformidade antes da entrega. Inclui instalação de sistemas operacionais homologados, agentes de segurança (EDR), inventário automático e aplicação de baselines de conformidade.
   - *Estados:* Em Preparação, Disponível.
5. **Operação:** Período ativo de uso do equipamento.
   - *Estados:* Em Uso, Em Produção, Reserva Técnica (Estoque TI), Em Empréstimo.
6. **Manutenção:** Intervenções preventivas ou corretivas durante a vida útil do bem.
   - *Estados:* Em Garantia, Em Manutenção, Aguardando Peças de Reposição.
7. **Renovação Tecnológica (*Refresh*):** Substituição programada do hardware por critérios técnicos objetivos: obsolescência severa, custo de manutenção corretiva superior ao valor residual, encerramento de suporte do fabricante (*End of Support - EOS*) ou degradação severa de performance que prejudique a produtividade.
8. **Encerramento e Descarte:** Fim da vida útil corporativa do ativo. Realiza-se a formatação segura de dados (sanitização física/apagamento seguro de discos conforme normas ISO 27001), desvinculação de licenças do SAM, baixa contábil e destinação para descarte ecologicamente correto com emissão obrigatória do Certificado de Destruição Ambiental pelo parceiro homologado.
   - *Estados:* Desativado, Baixado, Descartado.

## 8.1 Transições Automatizadas via Action Sequences
Para mitigar falhas humanas nos registros manuais, a atualização dos status dos ativos no TOPdesk será automatizada via **Action Sequences** (APIs internas de eventos):
- **Automação de Entrega:** O encerramento do fluxo de uma tarefa de "Entrega de Equipamento ao Usuário" altera automaticamente o status do ativo no *Asset Management* de "Disponível" para "Em Uso" e atualiza o campo de "Usuário Responsável" com os dados do solicitante.
- **Automação de Manutenção:** A abertura de um chamado categorizado como "Falha de Hardware - Manutenção Corretiva" transiciona o status do ativo referenciado para "Em Manutenção", bloqueando a sua disponibilidade lógica nas buscas de novos atendimentos.

* * *

# 9. PROCESSOS OPERACIONAIS E INTEGRAÇÕES DE SISTEMAS

## 9.1 Processo de Movimentação e Termo de Responsabilidade Digital no SSP
Toda transferência de custódia de um equipamento exige a imediata atualização cadastral no TOPdesk. Em substituição às assinaturas em papel ou integrações com sistemas externos de assinatura eletrônica, o processo ocorrerá nativamente pelo **Portal de Autoatendimento (SSP) do TOPdesk**:

```
      TI prepara o Notebook e altera status para "Disponível para Entrega"
                                       │
                                       ▼
       TOPdesk cria uma tarefa de confirmação no SSP do Colaborador
                                       │
                                       ▼
    Usuário acessa o SSP, lê as diretrizes e clica em "Confirmar Aceite"
                                       │
                                       ▼
       Log gravado no Cartão do Ativo (IP, Data/Hora, E-mail do Usuário)
    e status do ativo no TOPdesk é atualizado automaticamente para "Em Uso"
```

* * *

## 9.2 Frequência de Inventários e Auditorias Regulares
O programa não dependerá exclusivamente de processos manuais. Serão realizadas rotinas de conciliação com as seguintes periodicidades recomendadas:
- **Ativos em Nuvem (Cloud Assets):** Auditoria de conciliação mensal automatizada por script integrando o billing com o TOPdesk.
- **Ativos de Software (SAM):** Inventário e conciliação mensal via ferramentas de descoberta técnica.
- **Equipamentos de Data Center / Críticos:** Auditoria e varredura de rede física/lógica trimestral.
- **User Endpoints (Notebooks/Smartphones):** Inventário semestral por amostragem e conciliação de termos de guarda aceitos no SSP.

* * *

## 9.3 Arquitetura de Integrações do TOPdesk com Ferramentas de Descoberta

Para garantir a acurácia dos dados cadastrados e agilizar o input operacional, as APIs de Ativos do TOPdesk serão integradas ao ecossistema existente na Embrapa:

```
+--------------------------------------------------------+
|                  TOPdesk ASSET MANAGEMENT              |
|              (Source of Truth Administrativo)          |
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

- **Ferramentas de Descoberta Automática (Ex: Microsoft Intune, SCCM, Lansweeper):** Atualizam periodicamente especificações de hardware (processador, memória instalada, capacidade de disco, endereços IP e MAC ativos) e capturam a lista de softwares instalados para o SAM.
- **Diretórios de Identidade (Microsoft Active Directory / Entra ID):** Sincronizam a base de usuários do TOPdesk (tabela Pessoas), atualizando nomes, e-mails, departamentos e centros de custos, prevenindo divergências cadastrais.
- **Ferramentas de Monitoramento e DevOps (Ex: Zabbix, Kubernetes API):** Informam status operacionais e topologias dinâmicas dos CIs na CMDB.

### 9.3.1 Regras de Conciliação de Dados (Reconciliation Rules)
Para evitar que as ferramentas automáticas de descoberta técnica sobreponham dados de governança e de controle financeiro do ITAM de forma equivocada, aplicam-se as seguintes regras de conciliação:

| Categoria do Dado | Fonte / Proprietária do Dado | Regra de Negócio na Divergência |
| --- | --- | --- |
| **Especificações Técnicas** (RAM, CPU, IP, MAC, Softwares instalados) | **Ferramenta de Discovery** (Intune, Lansweeper) | Atualização automática e substituição pelo dado mais recente coletado. |
| **Metadados de Negócio** (Centro de Custo, Status Operacional, Criticidade, Dono) | **TI / Compras (Manual ou Workflow)** | Bloqueado para gravação por Discovery. Apenas formulários ou Action Sequences do TOPdesk podem alterar. |
| **Dados Pessoais / Identidade** (Departamento, Centro de Custo da Pessoa, E-mail) | **Diretório de Identidades** (Entra ID / AD) | Sobrescreve diariamente as tabelas internas de Pessoas no TOPdesk. |

* * *

# 10. POLÍTICA DE QUALIDADE DOS DADOS, RISCOS E AUDITORIA

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

## 10.3 Adequação à Lei Geral de Proteção de Dados (LGPD)
Dado que os Cartões de Ativos registram a custódia física e de uso de dispositivos associando-os a colaboradores (Nome, E-mail, Matrícula), estabelecem-se as seguintes regras de proteção de dados pessoais:
- **Retenção de Histórico de Custódia:** O histórico de quem usou cada ativo de hardware é considerado de interesse legítimo e segurança da informação da empresa, devendo ser mantido para rastreabilidade de acessos à rede corporativa por períodos legais.
- **Restrição de Acesso:** As abas e blocos que armazenam o histórico de custódia e proprietários antigos dos ativos serão de visibilidade restrita, acessíveis exclusivamente aos perfis de "Administrador de ITAM" e "Segurança da Informação", sendo ocultadas para analistas de nível 1 do Service Desk comum.
- **Anonimização no Descarte:** No momento em que o ativo for desativado e encaminhado para descarte físico ambiental definitivo, o processo de baixa desvinculará e anonimizará a associação direta de dados pessoais dos cartões históricos, mantendo os logs operacionais limpos de identificadores pessoais diretos.

* * *

# 11. INDICADORES DE DESEMPENHO (KPIs)

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
- Desvio orçamentário mensal ($\text{Gasto Real} - \text{Gasto Previsto}$).
- Índice de recursos superdimensionados (*Overprovisioning*) em IaaS e PaaS.
- Redução de custos acumulada gerada por desligamento automático de ambientes de desenvolvimento/homologação fora do horário comercial.

### KPIs de Contratos (ITCM)
- Percentual de renovações contratuais processadas sem interrupção de cobertura de suporte técnico.
- Índice de penalidades aplicadas a fornecedores por descumprimento de cláusulas de SLA acordadas.

* * *

# 12. MODELO DE MATURIDADE DO PROGRAMA ITAM

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

# 13. FATORES CRÍTICOS DE SUCESSO E CONSIDERAÇÕES FINAIS

O sucesso da implementação do programa corporativo de ITAM e CMDB na organização depende fundamentalmente do cumprimento dos seguintes fatores:

1. Apoio contínuo e visível da Alta Administração para a cobrança de conformidade dos processos por parte das demais gerências de negócio.
2. Manutenção rigorosa da disciplina operacional de atualização dos cadastros no TOPdesk; ferramentas tecnológicas tornam-se obsoletas se os processos humanos falharem.
3. Foco na capacitação continuada das equipes de TI, Compras e Controladoria nos conceitos de ITIL 4, ISO 19770 e práticas FinOps.

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
- **SSP:** *Self-Service Portal* (Portal de Autoatendimento TOPdesk)

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

Para a parametrização no Designer de Modelo do TOPdesk Asset Management, a estrutura lógica de objetos respeita a seguinte taxonomia cadastrada no sistema:

### 1. Modelos sob a Classe "Ativo"
- **Dispositivo Móvel:** Smartphones, Tablets, Modems corporativos e SIM Cards / eSIM (HAM - Mobile Endpoints).
- **Equipamento de Rede:** Switches, Roteadores, Firewalls, Access Points, Appliances de Rede.
- **Estação de Trabalho:** Desktops e Notebooks corporativos (HAM - User Endpoints).
- **Licença de Software:** Licenciamento On-Premise, subscrições SaaS, licenças corporativas (SAM).
- **Monitor:** Monitores individuais acoplados, displays ultrawide e visores corporativos (HAM - Displays).
- **Periférico:** Nobreaks, Impressoras, Scanners, Dock Stations, Acessórios.
- **Servidor:** Servidores físicos, Storages e chassis de Data Center.

### 2. Modelos sob a Classe "Bem em massa"
- **Criar modelo de ativo em massa:** Cadastros e importações parametrizadas de itens de lote/massa.

### 3. Classe Principal: Contratos e Fornecedores (ITCM)
- **Contratos de TI:** Contratos de Suporte do Fabricante, Garantias, Links de Dados, Licenciamento de Software, NDAs.

* * *

# APÊNDICE D – DICIONÁRIO DE DADOS E ESPECIFICAÇÃO DE CAMPOS OBRIGATÓRIOS NO TOPDESK

Este dicionário serve como especificação funcional e normativa para a parametrização dos formulários cadastrais no módulo de **Asset Management** do TOPdesk. 


## D.1 – Dicionário de Campos Obrigatórios para Ativos de Hardware (Modelo "Estação de Trabalho")

Os ativos de hardware do modelo **Estação de Trabalho** (Desktops e Notebooks) são cadastrados no TOPdesk contemplando a seguinte estrutura de seções, campos, relações e documentos:

### Seção 1: Identificação & informações gerais

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Hostname** | Texto Curto | **Mandatório** | Nome do dispositivo na rede (Ex: `DESKTOP-EMB01`, `NB-ANDRE`). | Operação TI / Discovery |
| **Tipo de Equipamento** | Dropdown | **Mandatório** | Tipo de ativo: `[Desktop, Notebook]`. | Operação TI |
| **Marca** | Dropdown | **Mandatório** | Catálogo homologado: `[Dell, Lenovo, HP, Apple, Positivo]`. | Operação TI |
| **Modelo Comercial** | Texto Curto | **Mandatório** | Modelo exato do equipamento (Ex: `Latitude 3440`, `OptiPlex 7010`). | Operação TI |
| **Número de Série** | Texto Curto | **Mandatório** | Código de série exclusivo da BIOS do fabricante (Ex: `5CD2348XYZ`). | Discovery / TI |
| **Patrimônio** | Alfanumérico | **Mandatório** | Número gravado na etiqueta física de metal (Ex: `PAT-2026-0894`). | Controladoria / Patrimônio |
| **Status** | Dropdown | **Mandatório** | Ciclo de vida: `[Planejado, Em Estoque, Em Uso, Em Manutenção, Em Descarte, Desativado]`. | Operação TI / Service Desk |

### Seção 2: Especificações Técnicas & CMDB

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Memória RAM** | Texto Curto / Número | **Mandatório** | Capacidade total de RAM em GB (Ex: `8 GB`, `16 GB`, `32 GB`). | Discovery / TI |
| **Processador** | Texto Curto | **Mandatório** | Modelo da CPU (Ex: `Intel Core i5-1345U`, `AMD Ryzen 5 PRO`). | Discovery / TI |
| **Armazenamento** | Texto Curto | **Mandatório** | Capacidade e tipo de disco (Ex: `512 GB SSD NVMe`). | Discovery / TI |
| **Sistema Operacional** | Dropdown | **Mandatório** | Sistema ativo: `[Windows 11 Pro, Linux RHEL, macOS]`. | Discovery / TI |
| **Versão do SO** | Texto Curto | **Mandatório** | Versão ou build do SO (Ex: `23H2`, `22.04 LTS`). | Discovery / TI |
| **IP** | Texto (Regex) | Condicional | Endereço IP IPv4/v6 atribuído (Ex: `10.20.4.15`). | Discovery / Infra |
| **MAC** | Texto (Regex) | **Mandatório** | Formato `XX:XX:XX:XX:XX:XX`. Requerido para controle 802.1X / DHCP. | Discovery / TI |
| **OU - Unidade Organizacional** | Texto Curto / Dropdown | **Mandatório** | Caminho da OU no AD / Entra ID (Ex: `OU=Desktops,OU=Sede,DC=embrapa,DC=br`). | Diretório ID / TI |

### Seção 3: Financeiro, Contratual & Suprimentos

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Fornecedor** | Link Interno / Dropdown | **Mandatório** | Razão Social do fornecedor cadastrado (CNPJ). | Compras |
| **Data de Aquisição** | Data | **Mandatório** | Data oficial de entrada/faturamento do ativo. | Compras |
| **Valor de Aquisição** | Moeda (BRL) | **Mandatório** | Valor unitário de compra constante na Nota Fiscal. | Compras / Controladoria |
| **Nota Fiscal** | Texto Curto | **Mandatório** | Número do documento fiscal de entrada. | Compras / Suprimentos |
| **Contrato** | Link Interno | **Mandatório** | Relacionamento com o contrato de aquisição/garantia (ITCM). | Compras |
| **Início da Garantia** | Data | **Mandatório** | Data inicial da garantia do fabricante. | Compras / TI |
| **Fim da Garantia** | Data | **Mandatório** | Data de término do suporte/garantia do fabricante (Ex: Dell ProSupport). | Compras / TI |
| **Centro de Custo** | Dropdown | **Mandatório** | Código contábil pagador para rateio corporativo. | Compras / Governança |
| **Data Prevista de Descarte** | Data | Condicional | Data planejada para desativação e substituição tecnológica (*Hardware Refresh*). | Governança TI |

### Seção 4: Custódia, Segurança & Compliance

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Responsável pelo Ativo** | Link Interno | Condicional | Busca direta na tabela de Pessoas (Mandatório se Status = `Em Uso`). | Service Desk / TI |
| **Unidade** | Link Interno / Dropdown | **Mandatório** | Unidade da Embrapa (Ex: `Embrapa Sede`, `Embrapa Agrobiologia`). | Operação TI |
| **Localização** | Texto Curto / Dropdown | **Mandatório** | Detalhamento físico da alocação (Ex: `Prédio Central - Sala 102`). | Operação TI |
| **Data da Entrega** | Data | Condicional | Data de entrega efetiva do ativo ao colaborador. | Service Desk / TI |
| **Termo de Responsabilidade** | Dropdown | **Mandatório** | Status do termo: `[Aguardando Aceite no SSP, Aceito Digitalmente, Isento/Infra]`. | Action Sequence / SSP |
| **Situação da Custódia** | Dropdown | **Mandatório** | Diagnóstico de posse: `[Regular, Pendente de Aceite, Extraviado, Em Devolução]`. | Governança TI |
| **Classificação da Informação** | Dropdown | **Mandatório** | Grau de sigilo dos dados manipulados: `[Pública, Interna, Confidencial, Restrita]`. | Segurança da Informação |
| **Dados Pessoais Tratados?** | Booleano (Sim/Não) | **Mandatório** | Indica tratamento de dados pessoais conforme LGPD. | Segurança / Compliance |
| **Situação de Compliance** | Dropdown | **Mandatório** | Diagnóstico de conformidade: `[Em Conformidade, Não Conforme, Em Auditoria]`. | Segurança / Compliance |
| **Data da Última Avaliação** | Data | Condicional | Data da última verificação ou auditoria de conformidade de segurança. | Segurança / Audit |

### Seção 5: Grade de Relações

| Entidade Relacionada | Tipo de Vínculo | Obrigatoriedade | Regra de Negócio / Descrição |
| --- | --- | --- | --- |
| **Usuário** | Link de Entidade | **Mandatório** | Vínculo direto com o colaborador (Pessoa) custodiante. |
| **Localização** | Link de Entidade | **Mandatório** | Vínculo com a estrutura de localização física. |
| **Software** | Link de Entidade | Condicional | Vínculo com licenças e softwares instalados/alocados. |
| **Chamado** | Link de Entidade | Condicional | Histórico de Incidentes e Requisições vinculados ao equipamento. |
| **Contrato** | Link de Entidade | **Mandatório** | Vínculo com Contratos de TI amparadores. |
| **Monitor** | Link de Entidade | Condicional | Vínculo com monitores individuais acoplados à estação. |
| **Impressora** | Link de Entidade | Condicional | Vínculo com impressoras alocadas ou mapeadas. |

### Seção 6: Documentos (Anexos Comprobatórios)

| Tipo de Documento | Formato de Arquivo | Obrigatoriedade | Descrição / Finalidade |
| --- | --- | --- | --- |
| **Nota Fiscal** | Upload (PDF/Imagem) | **Mandatório** | Documento fiscal de faturamento de aquisição. |
| **Termo de Responsabilidade** | Upload (PDF/Doc) | Condicional | Termo assinado fisicamente (caso não seja via SSP). |
| **Comprovante de Garantia** | Upload (PDF) | Condicional | Certificado de garantia ou apólice de suporte do fabricante. |
| **Documentação Técnica** | Upload (PDF) | Condicional | Datasheet, manual ou laudo técnico de homologação. |
| **Evidência de Auditoria** | Upload (PDF) | Condicional | Laudo de auditoria interna/externa ou checklist de segurança. |
| **Contrato** | Upload (PDF) | **Mandatório** | Cópia do contrato de compra ou prestação de serviços. |


---

## D.2 – Dicionário de Campos Obrigatórios para Ativos de Software & Licenciamento (Modelo "Licença de Software")

Os ativos de software do modelo **Licença de Software** (subscrições SaaS, licenças On-Premise e softwares especialistas) são cadastrados no TOPdesk contemplando a seguinte estrutura de seções, campos, relações e documentos:

### Seção 1: Identificação de Software & Licença

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Nome do Software** | Texto Curto | **Mandatório** | Nome comercial do software (Ex: `Microsoft 365 Enterprise`, `Oracle Database`). | Governança TI |
| **Fabricante** | Dropdown / Texto | **Mandatório** | Desenvolvedor homologado (`Microsoft`, `Oracle`, `Red Hat`, `JetBrains`). | Governança TI / SAM |
| **Produto** | Texto Curto | **Mandatório** | Família do produto (`Office 365`, `Database Enterprise`, `IntelliJ`). | Governança TI |
| **Edição** | Dropdown / Texto | **Mandatório** | Edição contratada (`Business Premium`, `E3`, `E5`, `Standard`, `Enterprise`). | Compras / SAM |
| **Versão** | Texto Curto | **Mandatório** | Versão ou release oficial (`2024.1`, `21c`, `v11.0`). | Operação TI / SAM |
| **Tipo de Licença** | Dropdown | **Mandatório** | Modelo da licença (`Subscrição SaaS`, `Perpétua`, `Concorrente/Floating`, `OEM`, `Volume`). | SAM / Compras |
| **ID da Licença** | Texto Curto | **Mandatório** | Identificador da licença ou contrato no portal do fabricante. | Administrador SAM |
| **Identificador da Licença** | Texto Curto / Key | **Mandatório** | Padrão `SW-LIC-MS-OFFICE-M365` ou Tenant ID / Serial Key. | Administrador SAM |

### Seção 2: Métricas de Licenciamento & Instalações

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Métrica de Licenciamento** | Dropdown | **Mandatório** | Regra de medição (`Por Usuário/Assento`, `Por Dispositivo/Core`, `Concorrente`). | Gestão de Licenças / SAM |
| **Quantidade Adquirida** | Número Inteiro | **Mandatório** | Total de licenças compradas constantes no contrato (Ex: `1.500`). | Compras / Contratos |
| **Quantidade Licenciada** | Número Inteiro | **Mandatório** | Total de licenças efetivamente concedidas e aptas para uso. | SAM / Operação TI |
| **Quantidade Instalada** | Número Inteiro | **Mandatório** | Total de instâncias/instalações detectadas via Discovery/Intune. | Discovery / Intune |
| **Quantidade em Uso** | Número Inteiro | **Mandatório** | Assentos ou licenças em utilização ativa pelos colaboradores. | SAM / Discovery |
| **Quantidade Disponível** | Número (Calculado) | **Mandatório** | Saldo em estoque: `[Qtd Adquirida] - [Qtd em Uso]` (Ex: `160`). Mede ociosidade. | Sistema (Fórmula TOPdesk) |
| **Data da Primeira Instalação** | Data | Condicional | Timestamp da primeira ativação/instalação no acervo. | Discovery / SAM |
| **Data da Última Instalação** | Data | Condicional | Timestamp do último provisionamento efetuado. | Discovery / SAM |
| **Situação do Licenciamento** | Dropdown | **Mandatório** | Estado do licenciamento (`Ativo`, `Em Renovação`, `Expirado`, `Sublicenciado`). | Gestão de Licenças / SAM |

### Seção 3: Financeiro, Contratual & Governança

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Fornecedor** | Link Interno / Dropdown | **Mandatório** | Razão Social do parceiro comercial fornecedor / LSP / CSP (CNPJ). | Compras |
| **Data de Aquisição** | Data | **Mandatório** | Data oficial da compra ou emissão da fatura. | Compras |
| **Valor de Aquisição** | Moeda | **Mandatório** | Custo de aquisição do lote ou valor anuidade da subscrição. | Compras / Controladoria |
| **Moeda** | Dropdown | **Mandatório** | Moeda do contrato (`BRL`, `USD`, `EUR`). | Compras |
| **Nota Fiscal** | Texto Curto | **Mandatório** | Número do documento fiscal de compra. | Compras / Suprimentos |
| **Contrato** | Link Interno | **Mandatório** | Associação ao registro do Contrato de Licenciamento (ITCM) no TOPdesk. | Compras |
| **Pedido de Compra** | Texto Curto | **Mandatório** | Número do Pedido de Compra / Ordem de Serviço (PO). | Compras / Suprimentos |
| **Centro de Custo** | Dropdown | **Mandatório** | Código contábil da unidade pagadora para rateio financeiro. | Governança TI |
| **Início da Vigência** | Data | **Mandatório** | Data inicial de concessão do direito de uso ou contrato. | Compras / SAM |
| **Fim da Vigência** | Data | **Mandatório** | Data limite do contrato SaaS / subscrição (dispara alerta aos 120 dias). | Compras / SAM |
| **Renovação Automática** | Booleano (Sim/Não) | **Mandatório** | Indica se há renovação automática programada no contrato. | Compras / ITCM |
| **Custo de Renovação** | Moeda | **Mandatório** | Valor estimativo recorrente da anuidade/renovação. | Compras / Financeiro |

### Seção 4: Atribuição, Uso & Compliance

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Responsável pela Licença** | Link Interno | **Mandatório** | Busca na tabela de Pessoas (Gestor do Software / Admin SAM). | Governança TI |
| **Unidade** | Link Interno / Dropdown | **Mandatório** | Unidade Embrapa beneficiária do licenciamento. | Governança TI |
| **Data da Atribuição** | Data | Condicional | Data de alocação da licença ao usuário ou servidor. | Service Desk / SAM |
| **Ambiente de Aplicação** | Dropdown | **Mandatório** | Escopo de execução (`Produção`, `Homologação`, `Desenvolvimento`). | Operação TI |
| **Uso Autorizado?** | Booleano (Sim/Não) | **Mandatório** | Confirmação de conformidade de uso institucional. | Segurança da Informação |
| **Situação do Licenciamento** | Dropdown | **Mandatório** | Diagnóstico operacional (`Ativo`, `Em Renovação`, `Sublicenciado`). | SAM / Auditoria |
| **Data da Última Auditoria** | Data | **Mandatório** | Timestamp do último batimento entre inventário e contratos. | Gestão de Licenças / SAM |
| **Situação de Compliance** | Dropdown | **Mandatório** | Diagnóstico final (`Em Conformidade`, `Sublicenciado (Risco)`, `Superlicenciado (Desperdício)`). | Auditoria ITAM |
| **Observações** | Área de Texto | Condicional | Notas técnicas, exceções de licenciamento ou ressalvas de audit. | SAM / Compliance |

### Seção 5: Grade de Relações

| Entidade Relacionada | Tipo de Vínculo | Obrigatoriedade | Regra de Negócio / Descrição |
| --- | --- | --- | --- |
| **Usuário** | Link de Entidade | **Mandatório** | Vínculo com a entidade Pessoa/Usuário com licença atribuída. |
| **Estação de Trabalho** | Link de Entidade | Condicional | Vínculo com estações de trabalho que possuem o software instalado. |
| **Servidor** | Link de Entidade | Condicional | Vínculo com servidores de aplicação onde o software executa. |
| **Pessoas** | Link de Entidade | Condicional | Vínculo com lista de colaboradores/grupos elegíveis. |
| **Contrato** | Link de Entidade | **Mandatório** | Associação com os Contratos de TI amparadores. |
| **Chamado** | Link de Entidade | Condicional | Histórico de chamados de suporte/requisições vinculados. |

### Seção 6: Documentos (Anexos Comprobatórios)

| Tipo de Documento | Formato de Arquivo | Obrigatoriedade | Descrição / Finalidade |
| --- | --- | --- | --- |
| **Estatuto** | Upload (PDF) | Condicional | Termos de uso, regulamento interno ou política do produto. |
| **Proposta Comercial** | Upload (PDF) | **Mandatório** | Cópia da proposta comercial homologada da contratação. |
| **Pedido de Compra** | Upload (PDF) | **Mandatório** | Cópia da ordem/pedido de compra emitido (PO). |
| **Nota Fiscal** | Upload (PDF/Imagem) | **Mandatório** | Cópia do documento fiscal de faturamento da licença. |
| **Certificado de Licença** | Upload (PDF) | **Mandatório** | Certificado oficial de licença (*License Certificate*). |
| **Comprovante de Aquisição** | Upload (PDF) | Condicional | Comprovantes de faturamento ou quitação de liquidação. |
| **Termo de Licenciamento** | Upload (PDF) | **Mandatório** | EULA / Contrato de Licença de Usuário Final do fabricante. |
| **Evidência de Auditoria** | Upload (PDF) | Condicional | Relatório de conciliação ou laudo de auditoria de conformidade. |
| **Documentação do Fabricante** | Upload (PDF) | Condicional | Manual de métricas, datasheets ou guia de licenciamento. |
| **Comprovante de Renovação** | Upload (PDF) | Condicional | Aditivo de renovação ou comprovante de vigência estendida. |


---

## D.3 – Dicionário de Campos Obrigatórios para Ativos de Hardware (Modelo "Dispositivo Móvel")

Os ativos de hardware do modelo **Dispositivo Móvel** (Smartphones, Tablets, Modems e SIM Cards) são cadastrados no TOPdesk contemplando a seguinte estrutura de seções, campos, relações e documentos:

### Seção 1: Identificação & Informações Gerais

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Nome do dispositivo** | Texto Curto | **Mandatório** | Identificação do dispositivo mobile (Ex: `TEL-ANDRE`, `SMART-0012`). | Operação TI / Discovery |
| **Tipo de Dispositivo** | Dropdown | **Mandatório** | Tipo de ativo: `[Smartphone, Tablet, Modem / MiFi, Chip GSM / eSIM]`. | Operação TI |
| **Marca** | Dropdown / Texto | **Mandatório** | Fabricante homologado: `[Samsung, Apple, Motorola, Xiaomi, Huawei]`. | Operação TI |
| **Modelo Comercial** | Texto Curto | **Mandatório** | Modelo comercial exato (Ex: `Galaxy S23`, `iPhone 15 Pro`, `Tab S9`). | Operação TI |
| **Número de série** | Texto Curto | **Mandatório** | Código de série exclusivo do fabricante (Ex: `R58M10XXXXX`). | Operação TI / Discovery |
| **IMEI 1** | Texto Curto (15 dígs) | **Mandatório** | Primeiro identificador internacional de equipamento móvel. | Operação TI / MDM |
| **IMEI 2** | Texto Curto (15 dígs) | Condicional | Segundo IMEI (suporte a Dual SIM / eSIM). | Operação TI / MDM |
| **Patrimônio** | Alfanumérico | **Mandatório** | Número gravado na etiqueta física de tombo/patrimônio. | Controladoria / Patrimônio |
| **Status** | Dropdown | **Mandatório** | Ciclo de vida: `[Planejado, Em Estoque, Em Uso, Em Manutenção, Em Descarte, Desativado]`. | Operação TI / Service Desk |

### Seção 2: Especificações Técnicas & CMDB

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Sistema Operacional** | Dropdown | **Mandatório** | Sistema do dispositivo: `[Android, iOS, iPadOS, Outro]`. | Operação TI / MDM |
| **Versão do SO** | Texto Curto | **Mandatório** | Versão do SO mobile (Ex: `Android 14`, `iOS 17.4`). | MDM / TI |
| **Armazenamento** | Texto Curto | **Mandatório** | Capacidade de armazenamento interno (Ex: `128 GB`, `256 GB`). | Operação TI |
| **Memória RAM** | Texto Curto | **Mandatório** | Capacidade de memória RAM (Ex: `6 GB`, `8 GB`, `12 GB`). | Operação TI |
| **Número da Linha** | Texto Curto | Condicional | Número telefônico / linha associada (Ex: `+55 (61) 99999-8888`). | Operação TI / Telecom |
| **Operadora** | Dropdown | Condicional | Operadora de telefonia móvel: `[Vivo, Claro, TIM, Outra]`. | Operação TI / Telecom |
| **ICCID** | Texto Curto (20 dígs) | Condicional | Identificador do SIM Card físico / eSIM (Ex: `89551012345678901234`). | Operação TI / Telecom |
| **MAC** | Texto (Regex) | **Mandatório** | Endereço MAC da placa Wi-Fi. Requerido para controle de rede. | MDM / TI |
| **IP** | Texto (Regex) | Condicional | Endereço IP na rede corporativa ou VPN. | MDM / Infra |
| **IMEI 1** | Texto Curto | **Mandatório** | Reiteração do IMEI 1 registrado para batimento CMDB/MDM. | MDM / TI |

### Seção 3: Financeiro, Contratual & Suprimentos

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Fornecedor** | Link Interno / Dropdown | **Mandatório** | Razão Social do fornecedor / revenda (CNPJ). | Compras |
| **Data de Aquisição** | Data | **Mandatório** | Data oficial de faturamento/compra do dispositivo. | Compras |
| **Valor de Aquisição** | Moeda (BRL) | **Mandatório** | Valor unitário de compra constante na Nota Fiscal. | Compras / Controladoria |
| **Nota Fiscal** | Texto Curto | **Mandatório** | Número do documento fiscal de faturamento. | Compras / Suprimentos |
| **Contrato** | Link Interno | **Mandatório** | Vínculo com o contrato de aquisição ou comodato telecom (ITCM). | Compras |
| **Início da Garantia** | Data | **Mandatório** | Data inicial da garantia do fabricante. | Compras / TI |
| **Fim da Garantia** | Data | **Mandatório** | Data de término da garantia do fabricante. | Compras / TI |
| **Centro de Custo** | Dropdown | **Mandatório** | Código contábil da unidade pagadora para rateio financeiro. | Governança TI |
| **Data Prevista de Descarte** | Data | Condicional | Data planejada para substituição tecnológica (*Mobile Refresh*). | Governança TI |

### Seção 4: Custódia, Segurança & Compliance

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Responsável pelo Ativo** | Link Interno | Condicional | Busca direta na tabela de Pessoas (Mandatório se Status = `Em Uso`). | Service Desk / TI |
| **Unidade** | Link Interno / Dropdown | **Mandatório** | Unidade Embrapa de alocação do dispositivo. | Operação TI |
| **Localização** | Texto Curto / Dropdown | **Mandatório** | Alocação física ou departamento do usuário. | Operação TI |
| **Data da Entrega** | Data | Condicional | Data de entrega do dispositivo móvel ao usuário. | Service Desk / TI |
| **Termo de Responsabilidade** | Dropdown | **Mandatório** | Status do termo: `[Aguardando Aceite no SSP, Aceito Digitalmente, Isento]`. | Action Sequence / SSP |
| **Situação da Custódia** | Dropdown | **Mandatório** | Diagnóstico de posse: `[Regular, Pendente de Aceite, Extraviado, Em Devolução]`. | Governança TI |
| **Classificação da Informação** | Dropdown | **Mandatório** | Sigilo dos dados: `[Pública, Interna, Confidencial, Restrita]`. | Segurança da Informação |
| **Dados Pessoais Tratados?** | Booleano (Sim/Não) | **Mandatório** | Indica se o dispositivo trata/acessa dados pessoais (LGPD). | Segurança / Compliance |
| **Situação de Compliance** | Dropdown | **Mandatório** | Diagnóstico MDM e segurança: `[Em Conformidade, Não Conforme, Em Auditoria]`. | Segurança / Compliance |
| **Data da Última Avaliação** | Data | Condicional | Timestamp da última verificação MDM / auditoria. | Segurança / Audit |

### Seção 5: Grade de Relações

| Entidade Relacionada | Tipo de Vínculo | Obrigatoriedade | Regra de Negócio / Descrição |
| --- | --- | --- | --- |
| **Usuário** | Link de Entidade | **Mandatório** | Vínculo direto com a pessoa custodiante do dispositivo. |
| **Linha / Serviço** | Link de Entidade | Condicional | Vínculo com a linha telefônica / plano corporativo de dados. |
| **Chamado** | Link de Entidade | Condicional | Histórico de chamados e suporte vinculados. |
| **Contrato** | Link de Entidade | **Mandatório** | Vínculo com contrato de aquisição ou operadora de telefonia. |

### Seção 6: Documentos (Anexos Comprobatórios)

| Tipo de Documento | Formato de Arquivo | Obrigatoriedade | Descrição / Finalidade |
| --- | --- | --- | --- |
| **Nota Fiscal** | Upload (PDF/Imagem) | **Mandatório** | Documento fiscal de faturamento do dispositivo. |
| **Termo de Responsabilidade** | Upload (PDF/Doc) | Condicional | Termo assinado fisicamente (se não for via SSP). |
| **Comprovante de Garantia** | Upload (PDF) | Condicional | Certificado de garantia do fabricante. |
| **Documentação Técnica** | Upload (PDF) | Condicional | Datasheet ou especificações homologadas do modelo. |
| **Evidência de Auditoria** | Upload (PDF) | Condicional | Relatório de conformidade de MDM ou segurança. |
| **Contrato** | Upload (PDF) | **Mandatório** | Cópia do contrato de compra ou comodato com operadora. |


---

## D.4 – Dicionário de Campos Obrigatórios para Ativos de Hardware (Modelo "Monitor")

Os ativos de hardware do modelo **Monitor** (Displays, Visores e Monitores Corporativos) são cadastrados no TOPdesk contemplando a seguinte estrutura de seções, campos, relações e documentos:

### Seção 1: Identificação & Informações Gerais

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Tipo de Monitor** | Dropdown | **Mandatório** | Tipo de tela: `[LED, LCD, OLED, Ultrawide, Touchscreen, Curvo]`. | Operação TI |
| **Marca** | Dropdown / Texto | **Mandatório** | Fabricante homologado: `[Dell, Samsung, LG, HP, AOC, Lenovo]`. | Operação TI |
| **Modelo Comercial** | Texto Curto | **Mandatório** | Modelo exato do fabricante (Ex: `P2422H`, `UltraSharp U2723QE`). | Operação TI |
| **Número de Série** | Texto Curto | **Mandatório** | Código exclusivo (S/N) do fabricante (Ex: `CN-0V1234-74261-34A-1234`). | Operação TI |
| **Patrimônio** | Alfanumérico | **Mandatório** | Número gravado na etiqueta física de tombo/patrimônio. | Controladoria / Patrimônio |
| **Status** | Dropdown | **Mandatório** | Ciclo de vida: `[Planejado, Em Estoque, Em Uso, Em Manutenção, Em Descarte, Desativado]`. | Operação TI / Service Desk |

### Seção 2: Especificações Técnicas & CMDB

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Tamanho da Tela** | Texto Curto / Número | **Mandatório** | Tamanho da tela em polegadas (Ex: `21.5"`, `23.8"`, `27"`, `34"`). | Operação TI |
| **Resolução** | Dropdown / Texto | **Mandatório** | Resolução nativa: `[Full HD (1920x1080), 4K UHD (3840x2160), 2K QHD (2560x1440)]`. | Operação TI |
| **Proporção de Tela** | Dropdown | **Mandatório** | Formato de exibição: `[16:9, 16:10, 21:9, 32:9]`. | Operação TI |
| **Tecnologia do Painel** | Dropdown | **Mandatório** | Tipo de painel: `[IPS, VA, TN, OLED, QD-OLED]`. | Operação TI |
| **Taxa de Atualização** | Texto Curto / Dropdown | **Mandatório** | Frequência de atualização em Hz (Ex: `60 Hz`, `75 Hz`, `144 Hz`). | Operação TI |
| **Tempo de Resposta** | Texto Curto | **Mandatório** | Tempo de resposta de píxel (Ex: `5 ms`, `1 ms`). | Operação TI |
| **Conexões de Vídeo** | Texto Curto / Dropdown | **Mandatório** | Portas de entrada suportadas (Ex: `HDMI, DisplayPort, USB-C, VGA`). | Operação TI |
| **USB Hub** | Dropdown / Booleano | **Mandatório** | Presença de hub USB integrado: `[Sim (4 portas USB-A/C), Não]`. | Operação TI |
| **Alto-falantes** | Booleano (Sim/Não) | **Mandatório** | Presença de alto-falantes embutidos no monitor. | Operação TI |
| **Ajuste de Posição** | Dropdown / Texto | **Mandatório** | Capacidade ergonômica: `[PIVOT (Giratória), Altura, Inclinação, Suporte VESA]`. | Operação TI |
| **Energia / Voltagem** | Dropdown | **Mandatório** | Alimentação elétrica: `[Bivolt 110V/220V, Fonte Externa 19V]`. | Operação TI |
| **MAC** | Texto (Regex) | Condicional | Endereço MAC da placa de rede (Monitores com Dock Station / RJ45 embutida). | Discovery / TI |
| **IP** | Texto (Regex) | Condicional | Endereço IP atribuído (Monitores inteligentes / Smart Display de rede). | Discovery / Infra |

### Seção 3: Financeiro, Contratual & Suprimentos

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Fornecedor** | Link Interno / Dropdown | **Mandatório** | Razão Social do fornecedor / revenda (CNPJ). | Compras |
| **Data de Aquisição** | Data | **Mandatório** | Data oficial de faturamento/compra do monitor. | Compras |
| **Valor de Aquisição** | Moeda (BRL) | **Mandatório** | Valor unitário de compra constante na Nota Fiscal. | Compras / Controladoria |
| **Nota Fiscal** | Texto Curto | **Mandatório** | Número do documento fiscal de faturamento. | Compras / Suprimentos |
| **Contrato** | Link Interno | **Mandatório** | Vínculo com o contrato de aquisição ou fornecimento (ITCM). | Compras |
| **Início da Garantia** | Data | **Mandatório** | Data inicial da garantia do fabricante. | Compras / TI |
| **Fim da Garantia** | Data | **Mandatório** | Data de término da garantia/suporte do fabricante. | Compras / TI |
| **Centro de Custo** | Dropdown | **Mandatório** | Código contábil da unidade pagadora para rateio financeiro. | Governança TI |
| **Data Prevista de Descarte** | Data | Condicional | Data planejada para substituição tecnológica (*Hardware Refresh*). | Governança TI |

### Seção 4: Custódia, Segurança & Compliance

| Nome do Campo no TOPdesk | Tipo do Dado | Obrigatoriedade | Regra de Negócio / Origem | Perfil Responsável |
| --- | --- | --- | --- | --- |
| **Responsável pelo Ativo** | Link Interno | Condicional | Busca direta na tabela de Pessoas (Mandatório se Status = `Em Uso`). | Service Desk / TI |
| **Unidade** | Link Interno / Dropdown | **Mandatório** | Unidade Embrapa de alocação do monitor. | Operação TI |
| **Localização** | Texto Curto / Dropdown | **Mandatório** | Detalhamento físico da alocação (Ex: `Prédio Central - Sala 102`). | Operação TI |
| **Data da Entrega** | Data | Condicional | Data de entrega do monitor ao usuário custodiante. | Service Desk / TI |
| **Termo de Responsabilidade** | Dropdown | **Mandatório** | Status do termo: `[Aguardando Aceite no SSP, Aceito Digitalmente, Isento]`. | Action Sequence / SSP |
| **Situação da Custódia** | Dropdown | **Mandatório** | Diagnóstico de posse: `[Regular, Pendente de Aceite, Extraviado, Em Devolução]`. | Governança TI |
| **Classificação da Informação** | Dropdown | **Mandatório** | Grau de sigilo: `[Pública, Interna, Confidencial, Restrita]`. | Segurança da Informação |
| **Situação de Compliance** | Dropdown | **Mandatório** | Diagnóstico de conformidade: `[Em Conformidade, Não Conforme, Em Auditoria]`. | Segurança / Compliance |
| **Data da Última Avaliação** | Data | Condicional | Timestamp da última verificação ou auditoria patrimonial. | Segurança / Audit |

### Seção 5: Grade de Relações

| Entidade Relacionada | Tipo de Vínculo | Obrigatoriedade | Regra de Negócio / Descrição |
| --- | --- | --- | --- |
| **Usuário** | Link de Entidade | **Mandatório** | Vínculo direto com a pessoa custodiante do monitor. |
| **Estação de Trabalho Relacionada** | Link de Entidade | Condicional | Vínculo direto com o Desktop ou Notebook ao qual o monitor está conectado. |
| **Localização** | Link de Entidade | **Mandatório** | Vínculo com a estrutura de localização física. |

### Seção 6: Documentos (Anexos Comprobatórios)

| Tipo de Documento | Formato de Arquivo | Obrigatoriedade | Descrição / Finalidade |
| --- | --- | --- | --- |
| **Nota Fiscal** | Upload (PDF/Imagem) | **Mandatório** | Cópia da Nota Fiscal de faturamento do equipamento. |
| **Termo de Responsabilidade** | Upload (PDF/Doc) | Condicional | Termo de Guarda assinado fisicamente (quando fora do SSP). |
| **Documento de Aquisição** | Upload (PDF) | Condicional | Cópia do pedido de compra / ordem de fornecimento. |
| **Comprovante de Garantia** | Upload (PDF) | Condicional | Certificado de garantia ou apólice de suporte do fabricante. |
| **Documentação Técnica** | Upload (PDF) | Condicional | Datasheet ou manual do fabricante. |


---

## D.5 – Regras de Validação, Nomenclatura e Triggers de Automação no TOPdesk

Para evitar dados inconsistentes e garantir automação eficiente nos fluxos operacionais do TOPdesk, aplicam-se as seguintes regras de validação e automações nativas (*Action Sequences*):

### 1. Padrões Obrigatórios de Nomenclatura (Asset Tags / Primary Keys)
- **User Endpoints:** `NB-[SEQUENCIAL_5_DIGITOS]` para Notebooks (Ex: `NB-04821`); `DT-[SEQUENCIAL_5_DIGITOS]` para Desktops (Ex: `DT-01293`).
- **Dispositivos Móveis:** `MOB-[SEQUENCIAL_5_DIGITOS]` para Smartphones/Tablets (Ex: `MOB-00142`); `MOD-[SEQUENCIAL_5_DIGITOS]` para Modems 4G/5G (Ex: `MOD-00034`).
- **Monitores e Visores:** `MON-[SEQUENCIAL_5_DIGITOS]` para Monitores (Ex: `MON-00812`).
- **Servidores e Data Center:** `SRV-[SLA/SIGLA]-[SEQ]` (Ex: `SRV-DB-0012`); `STG-[SEQ]` para Storages; `SW-[SEQ]` para Switches.
- **Licenças de Software:** `SW-LIC-[FABRICANTE]-[SIGLA_PROD]` (Ex: `SW-LIC-MS-M365-PREM`, `SW-LIC-MATH-MATLAB24`).

### 2. Validações por Expressões Regulares (Regex) no TOPdesk
- **Endereço MAC:** `^([0-9A-Fa-f]{2}[:-]){5}([0-9A-Fa-f]{2})$` (Impede o cadastro de endereços MAC inválidos ou sem formatadores padrão).
- **Endereço IP IPv4:** `^((25[0-5]|(2[0-4]|1\d|[1-9]|)\d)\.){3}(25[0-5]|(2[0-4]|1\d|[1-9]|)\d)$`
- **Número de Série (S/N):** `^[A-Za-z0-9\-\_]{5,30}$` (Garante entre 5 e 30 caracteres alfanuméricos sem espaços).
- **IMEI (1 e 2):** `^[0-9]{15}$` (Exatamente 15 dígitos numéricos).
- **ICCID:** `^[0-9]{18,20}$` (Entre 18 e 20 dígitos numéricos).

### 3. Automações de Eventos via Action Sequences
- **Trigger de Confirmação no SSP:** Quando o usuário clica em "Confirmar Aceite" no Termo de Guarda no Portal SSP:
  - O **Status do Termo** altera para `Aceito Digitalmente`.
  - A **Data/Hora do Aceite** é preenchida com o timestamp atual.
  - O **Estado do Ciclo de Vida** do ativo transiciona automaticamente de `Disponível` para `Em Uso`.
- **Trigger de Manutenção de Ativo:** Quando um chamado de incidente da categoria *Hardware - Defeito Físico* é aberto e associado a um ativo:
  - O **Estado do Ciclo de Vida** do ativo altera para `Em Manutenção`.
- **Trigger de Régua de Alertas Contratuais (SAM/ITCM):** Executado diariamente às 06:00:
  - Dispara notificação à equipe de Compras aos **120, 90, 60 e 30 dias** antes da *Data de Expiração / Renovação* de qualquer licença de software ou garantia de hardware.


