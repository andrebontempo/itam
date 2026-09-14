# DIRETRIZES CORPORATIVAS PARA IMPLEMENTAÇÃO DA GESTÃO DE ATIVOS DE TI (ITAM)

## Informações do Documento

| Campo | Informação |
| --- | --- |
| Documento | Diretrizes Corporativas para Implementação da Gestão de Ativos de TI (ITAM) |
| Versão | 2.0 |
| Status | Proposta para Aprovação |
| Autor | André Luiz Bontempo |
| Área Responsável | Tecnologia da Informação |
| Projeto | Implantação do IT Asset Management (ITAM) no TOPdesk |
| Ferramenta | TOPdesk Asset Management |
| Data de Emissão | 08/07/2026 |
| Última Revisão | 08/07/2026 |
| Próxima Revisão | Julho/2027 |
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

Este documento destina-se às seguintes áreas:

- Tecnologia da Informação
- Governança de TI
- Service Desk
- Infraestrutura
- Segurança da Informação
- Compras
- Patrimônio
- Auditoria Interna
- Gestores das Unidades

* * *

## Referências Normativas

- ITIL® 4 Foundation
- ISO/IEC 19770-1 – IT Asset Management
- ISO 55000 – Asset Management
- ISO/IEC 20000 – IT Service Management
- ISO/IEC 27001 – Information Security Management
- FinOps Framework
- Documentação oficial do TOPdesk

&nbsp;

* * *

# 1\. INTRODUÇÃO

A Gestão de Ativos de Tecnologia da Informação (IT Asset Management – ITAM) consiste no conjunto de processos, políticas, controles e ferramentas destinados a administrar os ativos de TI durante todo o seu ciclo de vida, desde o planejamento da aquisição até sua desativação e descarte.

Mais do que um inventário patrimonial, o ITAM estabelece uma visão integrada dos recursos tecnológicos da organização, permitindo que ativos físicos, softwares, serviços em nuvem, contratos e relacionamentos entre componentes sejam gerenciados de forma estruturada, auditável e alinhada aos objetivos estratégicos da instituição.

Uma implementação eficiente de ITAM proporciona benefícios diretos para diversas áreas da organização, incluindo Tecnologia da Informação, Compras, Controladoria, Auditoria, Segurança da Informação e Governança Corporativa, oferecendo informações confiáveis para tomada de decisão, redução de custos, mitigação de riscos e melhoria contínua dos serviços de TI.

O presente documento estabelece as diretrizes para implantação do programa corporativo de Gestão de Ativos de TI, definindo sua arquitetura, princípios de governança, responsabilidades, categorias de ativos, estrutura mínima de dados, processos operacionais e modelo de evolução.

Além disso, este documento servirá como referência para configuração do módulo de Asset Management do TOPdesk, definição dos processos organizacionais e integração com ferramentas de descoberta automática, monitoramento e gerenciamento de serviços.

* * *

# 2\. OBJETIVOS DO PROGRAMA ITAM

O Programa Corporativo de Gestão de Ativos de TI possui como objetivos principais:

- estabelecer um inventário corporativo único, centralizado e confiável;
    
- garantir rastreabilidade completa dos ativos durante todo o seu ciclo de vida;
    
- melhorar a utilização dos recursos tecnológicos disponíveis;
    
- reduzir perdas físicas e financeiras relacionadas aos ativos de TI;
    
- controlar licenciamento de software e conformidade contratual;
    
- reduzir desperdícios de assinaturas e serviços em nuvem;
    
- apoiar auditorias internas e externas;
    
- fornecer informações confiáveis para planejamento orçamentário;
    
- fortalecer a governança dos ativos tecnológicos;
    
- integrar ativos, usuários, contratos, serviços e infraestrutura em uma visão única;
    
- apoiar processos de Gerenciamento de Mudanças, Incidentes, Problemas e Continuidade dos Serviços;
    
- fornecer dados consistentes para construção da CMDB corporativa.
    

* * *

# 3\. ESCOPO

O programa contempla todos os ativos de tecnologia utilizados pela organização, independentemente de sua forma de aquisição, contratação ou consumo.

O escopo está dividido nas seguintes categorias.

## 3.1 Ativos Físicos

Incluem todos os equipamentos tangíveis utilizados pela organização.

Exemplos:

- notebooks;
    
- desktops;
    
- tablets;
    
- smartphones;
    
- monitores;
    
- impressoras;
    
- scanners;
    
- servidores;
    
- storages;
    
- switches;
    
- roteadores;
    
- firewalls;
    
- access points;
    
- nobreaks;
    
- equipamentos de telecomunicações.
    

* * *

## 3.2 Ativos de Software

Compreendem softwares instalados localmente e licenças adquiridas pela organização.

Exemplos:

- sistemas operacionais;
    
- bancos de dados;
    
- suítes de escritório;
    
- ferramentas de desenvolvimento;
    
- softwares especializados;
    
- middleware;
    
- softwares de monitoramento;
    
- softwares de segurança.
    

* * *

## 3.3 Serviços em Nuvem

Incluem serviços contratados em modelos de consumo ou assinatura.

Exemplos:

- Infraestrutura como Serviço (IaaS);
    
- Plataforma como Serviço (PaaS);
    
- Software como Serviço (SaaS);
    
- APIs comerciais;
    
- armazenamento em nuvem;
    
- inteligência artificial sob demanda.
    

* * *

## 3.4 Contratos

Abrangem todos os instrumentos jurídicos relacionados aos ativos tecnológicos.

Exemplos:

- garantias;
    
- manutenção;
    
- licenciamento;
    
- outsourcing;
    
- telecomunicações;
    
- suporte especializado;
    
- consultorias;
    
- contratos de serviços gerenciados.
    

* * *

# 4\. ARQUITETURA DO PROGRAMA DE GESTÃO DE ATIVOS

A gestão corporativa de ativos será organizada em quatro domínios complementares, denominados **pilares do programa ITAM**.

Cada pilar possui objetivos próprios, regras de categorização, indicadores específicos e processos operacionais distintos, mas todos compartilham informações por meio da Base de Dados de Gerenciamento de Configuração (CMDB), permitindo uma visão integrada do ambiente tecnológico.

Essa arquitetura proporciona:

- especialização dos processos de gestão;
    
- padronização dos cadastros;
    
- redução de redundâncias;
    
- rastreabilidade completa do ciclo de vida;
    
- integração entre ativos físicos, softwares, contratos e serviços;
    
- suporte à tomada de decisão baseada em dados.
    

Os quatro pilares são:

1.  Hardware Asset Management (HAM);
    
2.  Software Asset Management (SAM);
    
3.  Cloud Asset Management (Cloud / FinOps);
    
4.  IT Contract Management (ITCM).
    

Cada um desses pilares é apresentado nas seções seguintes.

* * *

# 5\. PILARES DO PROGRAMA ITAM

## 5.1 Hardware Asset Management (HAM)

### Objetivo

Gerenciar todos os ativos físicos de tecnologia durante seu ciclo de vida completo, desde a aquisição até o descarte ambientalmente adequado.

O foco deste pilar é garantir rastreabilidade patrimonial, controle operacional, gestão financeira dos equipamentos e correta atribuição aos usuários ou serviços.

Entre seus principais objetivos destacam-se:

- reduzir perdas patrimoniais;
    
- controlar movimentações;
    
- planejar renovações tecnológicas (*refresh*);
    
- administrar garantias;
    
- controlar localização física dos equipamentos;
    
- apoiar auditorias patrimoniais.
    

### Exemplos de Registro

**Exemplo 1 – User Endpoints**

| Campo | Valor |
| --- | --- |
| Patrimônio | PAT-2026-0894 |
| Ativo | Notebook Dell Latitude 3440 |
| Configuração | Intel Core i5 • 16 GB RAM • SSD 512 GB |
| Status | Em uso |
| Responsável | Andre Luiz Bontempo |

* * *

**Exemplo 2 – Infraestrutura**

| Campo | Valor |
| --- | --- |
| Patrimônio | SRV-0042 |
| Ativo | Servidor HPE ProLiant DL380 Gen10 |
| Status | Em Produção |
| Localização | Rack 04 – Data Center Principal |

* * *

**Exemplo 3 – Periféricos**

| Campo | Valor |
| --- | --- |
| Patrimônio | NOB-0115 |
| Ativo | Nobreak APC Smart-UPS BR 1500 VA |
| Status | Reserva Técnica |

* * *

## 5.2 Software Asset Management (SAM)

### Objetivo

Gerenciar ativos de software licenciados pela organização, sejam eles instalados localmente (*On-Premise*) ou disponibilizados por assinatura (*Software as a Service – SaaS*).

Este pilar tem como finalidade garantir conformidade contratual, otimizar o uso das licenças adquiridas e reduzir custos decorrentes de licenciamento inadequado.

Os principais objetivos incluem:

- controle de conformidade;
    
- prevenção de riscos em auditorias de fabricantes;
    
- eliminação de licenças ociosas;
    
- otimização financeira;
    
- controle de renovações;
    
- gestão centralizada de assinaturas.
    

### Exemplos de Registro

**Exemplo 1 – Microsoft 365**

| Campo | Valor |
| --- | --- |
| Serviço | Microsoft 365 Business Premium |
| Tipo | SaaS |
| Licenciamento | Mensal por usuário |
| Contratadas | 150 |
| Em uso | 132 |
| Disponíveis | 18  |

* * *

**Exemplo 2 – GitHub Enterprise**

| Campo | Valor |
| --- | --- |
| Serviço | GitHub Enterprise Cloud |
| Licenciamento | Anual |
| Tipo | Assentos de Desenvolvedor |
| Quantidade | 25  |

* * *

**Exemplo 3 – ChatGPT Enterprise**

| Campo | Valor |
| --- | --- |
| Serviço | ChatGPT Enterprise |
| Tipo | SaaS |
| Licenciamento | Mensal |
| Usuários | Equipe de Produto e Inovação |
| Quantidade | 10  |

&nbsp;

* * *

# 5.3 Cloud Asset Management (Cloud / FinOps)

## Objetivo

O **Cloud Asset Management**, apoiado pelas práticas de **FinOps**, é responsável pelo gerenciamento dos ativos tecnológicos consumidos sob demanda em ambientes de computação em nuvem.

Diferentemente do licenciamento tradicional de software, os recursos em nuvem possuem cobrança variável, baseada no consumo efetivo de processamento, armazenamento, largura de banda, número de requisições ou utilização de APIs. Dessa forma, sua gestão exige monitoramento contínuo, controle orçamentário e mecanismos automáticos de alerta.

Este pilar tem como principais objetivos:

- controlar custos dos serviços em nuvem;
    
- estabelecer previsibilidade orçamentária;
    
- evitar desperdícios de recursos;
    
- monitorar crescimento do consumo;
    
- otimizar utilização da infraestrutura;
    
- apoiar decisões de escalabilidade;
    
- garantir governança financeira dos ambientes cloud.
    

* * *

## Escopo

Este domínio contempla recursos dos seguintes modelos de serviço:

### Infraestrutura como Serviço (IaaS)

Exemplos:

- Amazon EC2
    
- Azure Virtual Machines
    
- Google Compute Engine
    

### Plataforma como Serviço (PaaS)

Exemplos:

- MongoDB Atlas
    
- Azure SQL Database
    
- Amazon RDS
    
- Azure Kubernetes Service
    

### APIs Comerciais

Exemplos:

- OpenAI API
    
- Anthropic API
    
- Google Gemini API
    
- Azure OpenAI Service
    

### Serviços de Armazenamento

Exemplos:

- Amazon S3
    
- Azure Blob Storage
    
- Google Cloud Storage
    

* * *

## Métricas de Controle

Cada ativo deverá possuir indicadores específicos de consumo.

Exemplos:

- horas de processamento;
    
- consumo de CPU;
    
- memória utilizada;
    
- armazenamento;
    
- IOPS;
    
- transferência de dados;
    
- número de requisições;
    
- volume de tokens consumidos;
    
- custo diário;
    
- custo mensal;
    
- centro de custo associado.
    

* * *

## Regras de Governança

O gerenciamento financeiro deverá considerar, no mínimo:

### Alerta Preventivo

Acionado quando o consumo atingir **80% do orçamento previsto**.

### Alerta de Atenção

Acionado quando o consumo atingir **90% do orçamento**.

### Alerta Crítico

Acionado quando houver previsão de ultrapassagem do orçamento ou crescimento anormal do consumo.

### Escalonamento

Quando necessário, deverá existir processo formal para:

- aprovação de aumento de orçamento;
    
- bloqueio de recursos não críticos;
    
- revisão da arquitetura;
    
- identificação de desperdícios.
    

* * *

## Exemplos de Registro

### Exemplo 1 — Infraestrutura em Nuvem

| Campo | Valor |
| --- | --- |
| Serviço | AWS EC2 + Amazon RDS |
| Tipo | IaaS |
| Cobrança | Consumo |
| Métrica | CPU, Memória e Armazenamento |
| Alerta | 80% do orçamento |

* * *

### Exemplo 2 — Inteligência Artificial

| Campo | Valor |
| --- | --- |
| Serviço | OpenAI API |
| Tipo | API Comercial |
| Cobrança | Milhões de Tokens |
| Controle | Consumo Diário |
| Ação | Alerta ou bloqueio automático |

* * *

### Exemplo 3 — Banco de Dados

| Campo | Valor |
| --- | --- |
| Serviço | MongoDB Atlas |
| Tipo | PaaS |
| Métrica | Armazenamento, IOPS e Rede |
| Controle | Escalabilidade automática |

* * *

# 5.4 IT Contract Management (ITCM)

## Objetivo

O **IT Contract Management (ITCM)** representa a camada administrativa, financeira e jurídica do programa de Gestão de Ativos.

Seu objetivo é controlar todos os contratos relacionados aos ativos de tecnologia, garantindo conformidade, rastreabilidade e gestão dos compromissos assumidos pela organização.

Os contratos cadastrados deverão possuir relacionamento com ativos físicos, softwares, serviços em nuvem e fornecedores, permitindo identificar rapidamente quais recursos serão impactados por vencimentos ou alterações contratuais.

* * *

## Escopo

Este domínio contempla:

- contratos de aquisição;
    
- garantias de fabricantes;
    
- contratos de manutenção;
    
- contratos de outsourcing;
    
- contratos de suporte especializado;
    
- contratos de telecomunicações;
    
- contratos de licenciamento;
    
- acordos de nível de serviço (SLA);
    
- termos de confidencialidade (NDA);
    
- contratos de consultoria.
    

* * *

## Informações Mínimas

Cada contrato deverá possuir, no mínimo:

- número do contrato;
    
- fornecedor;
    
- gestor responsável;
    
- objeto contratual;
    
- valor contratado;
    
- vigência;
    
- índice de reajuste;
    
- SLA;
    
- renovação automática;
    
- ativos vinculados.
    

* * *

## Alertas

Recomenda-se a configuração automática de alertas para:

- 120 dias antes do vencimento;
    
- 90 dias antes;
    
- 60 dias antes;
    
- 30 dias antes;
    
- vencimento.
    

* * *

## Exemplos de Registro

### Exemplo 1 — Garantia

| Campo | Valor |
| --- | --- |
| Contrato | CT-DELL-2025-003 |
| Objeto | Dell ProSupport |
| Ativos Relacionados | Notebooks Corporativos |
| Vencimento | 15/12/2028 |

* * *

### Exemplo 2 — Telecomunicações

| Campo | Valor |
| --- | --- |
| Contrato | CT-CLARO-2026-A |
| Objeto | Link Internet 1 Gbps |
| Renovação | Automática |
| Reajuste | IGPM |

* * *

### Exemplo 3 — Outsourcing

| Campo | Valor |
| --- | --- |
| Contrato | CT-CONSULT-04 |
| Serviço | Administração de Banco de Dados |
| SLA | Atendimento em até 2 horas |
| Vigência | Até 31/01/2027 |

* * *

# 6\. PAPÉIS E RESPONSABILIDADES

O sucesso do programa de Gestão de Ativos depende da definição clara das responsabilidades entre as áreas envolvidas.

O ITAM é um processo corporativo e não exclusivamente da área de Tecnologia da Informação.

* * *

## 6.1 Tecnologia da Informação

Responsável pela administração operacional do programa.

Principais responsabilidades:

- administrar o TOPdesk;
    
- cadastrar ativos;
    
- manter informações atualizadas;
    
- controlar movimentações;
    
- administrar integrações;
    
- executar inventários periódicos;
    
- manter a CMDB;
    
- acompanhar indicadores;
    
- produzir relatórios gerenciais.
    

* * *

## 6.2 Compras

Responsável pelo relacionamento com fornecedores.

Atividades:

- aquisição de ativos;
    
- negociação contratual;
    
- cadastro de fornecedores;
    
- controle de contratos;
    
- renovação de licenças.
    

* * *

## 6.3 Patrimônio

Quando existir área patrimonial, deverá atuar conjuntamente com a TI.

Responsabilidades:

- patrimônio físico;
    
- inventário patrimonial;
    
- baixas patrimoniais;
    
- conciliações.
    

* * *

## 6.4 Gestores das Áreas

Compete aos gestores:

- aprovar solicitações;
    
- validar usuários responsáveis;
    
- comunicar movimentações;
    
- acompanhar utilização dos ativos.
    

* * *

## 6.5 Usuários

Cada colaborador será responsável pelos ativos sob sua guarda.

Deverá:

- utilizar adequadamente os equipamentos;
    
- comunicar incidentes;
    
- preservar o patrimônio;
    
- devolver equipamentos quando solicitado.
    

* * *

## 6.6 Governança de TI

Compete à Governança:

- definir políticas;
    
- acompanhar indicadores;
    
- realizar auditorias;
    
- revisar processos;
    
- avaliar maturidade do programa.
    

* * *

# 7\. HARDWARE ASSET MANAGEMENT (HAM)

## Objetivo

O Hardware Asset Management (HAM) é responsável pelo gerenciamento completo dos ativos físicos da organização.

Seu propósito é assegurar que cada equipamento possa ser identificado, localizado, auditado e acompanhado durante todo o seu ciclo de vida.

* * *

## Categorias

### User Endpoints

- notebooks;
    
- desktops;
    
- tablets;
    
- smartphones.
    

* * *

### Data Center

- servidores;
    
- storages;
    
- appliances;
    
- racks.
    

* * *

### Rede

- switches;
    
- roteadores;
    
- firewalls;
    
- access points;
    
- controladoras.
    

* * *

### Periféricos

- monitores;
    
- impressoras;
    
- scanners;
    
- webcams;
    
- nobreaks.
    

* * *

### Telecomunicações

- rádios;
    
- gateways;
    
- equipamentos de voz;
    
- equipamentos WAN.
    

* * *

## Informações Obrigatórias

Cada ativo deverá possuir, no mínimo:

### Identificação

- patrimônio;
    
- número de série;
    
- fabricante;
    
- modelo;
    
- categoria.
    

### Responsabilidade

- usuário;
    
- gestor;
    
- área.
    

### Localização

- unidade;
    
- prédio;
    
- sala;
    
- rack;
    
- posição física.
    

### Dados Financeiros

- fornecedor;
    
- nota fiscal;
    
- valor;
    
- centro de custo;
    
- data de aquisição.
    

### Dados Técnicos

- processador;
    
- memória;
    
- armazenamento;
    
- sistema operacional;
    
- endereço MAC;
    
- endereço IP (quando aplicável).
    

* * *

## Estados do Ciclo de Vida

O hardware poderá assumir os seguintes estados:

- solicitado;
    
- adquirido;
    
- recebido;
    
- homologação;
    
- disponível;
    
- em uso;
    
- em produção;
    
- manutenção;
    
- empréstimo;
    
- reserva técnica;
    
- obsoleto;
    
- descarte.
    

* * *

## Boas Práticas

Todos os ativos deverão:

- possuir identificação única;
    
- estar vinculados a um responsável;
    
- possuir localização conhecida;
    
- possuir histórico de movimentações;
    
- possuir histórico de manutenção;
    
- estar vinculados aos contratos correspondentes;
    
- estar relacionados aos Configuration Items (CI) quando fizerem parte da infraestrutura de serviços.
    

* * *

* * *

# 8\. SOFTWARE ASSET MANAGEMENT (SAM)

## 8.1 Objetivo

O **Software Asset Management (SAM)** é responsável pela governança de todos os ativos de software utilizados pela organização, independentemente de sua forma de licenciamento.

Este domínio contempla aplicações instaladas localmente (*On-Premise*), soluções fornecidas como serviço (*Software as a Service – SaaS*) e demais modelos de licenciamento comercial.

Seu objetivo é assegurar que os softwares utilizados estejam em conformidade com os contratos de licenciamento, reduzindo riscos jurídicos, financeiros e operacionais, além de otimizar os investimentos realizados pela organização.

* * *

## 8.2 Objetivos Específicos

O programa de SAM deverá:

- controlar todo o inventário de software;
    
- manter rastreabilidade das licenças;
    
- reduzir desperdícios;
    
- identificar softwares não autorizados;
    
- apoiar auditorias de fabricantes;
    
- controlar versões homologadas;
    
- gerenciar renovações;
    
- apoiar planejamento financeiro.
    

* * *

## 8.3 Categorias de Software

### Sistemas Operacionais

Exemplos:

- Windows
    
- Linux
    
- macOS
    

* * *

### Bancos de Dados

Exemplos:

- PostgreSQL
    
- Oracle Database
    
- Microsoft SQL Server
    
- MongoDB Enterprise
    

* * *

### Ferramentas Corporativas

Exemplos:

- Microsoft Office
    
- LibreOffice
    
- Adobe Acrobat
    

* * *

### Desenvolvimento

Exemplos:

- GitHub Enterprise
    
- JetBrains
    
- Visual Studio
    
- Docker Desktop
    

* * *

### Segurança

Exemplos:

- Microsoft Defender
    
- CrowdStrike
    
- ESET
    
- Trend Micro
    

* * *

### SaaS

Exemplos:

- Microsoft 365
    
- Jira
    
- Confluence
    
- ChatGPT Enterprise
    
- Adobe Creative Cloud
    

* * *

## 8.4 Modelos de Licenciamento

Cada software deverá possuir seu modelo de licenciamento identificado.

Exemplos:

- por usuário;
    
- por dispositivo;
    
- por servidor;
    
- por núcleo (Core);
    
- por processador;
    
- por máquina virtual;
    
- por assinatura mensal;
    
- por assinatura anual;
    
- por consumo.
    

* * *

## 8.5 Informações Obrigatórias

Cada ativo de software deverá possuir:

### Identificação

- nome;
    
- fabricante;
    
- versão;
    
- edição.
    

### Licenciamento

- tipo de licença;
    
- quantidade adquirida;
    
- quantidade instalada;
    
- quantidade utilizada;
    
- quantidade disponível.
    

### Contrato

- fornecedor;
    
- contrato associado;
    
- data de renovação;
    
- custo.
    

### Governança

- gestor responsável;
    
- proprietário do sistema;
    
- criticidade;
    
- classificação.
    

* * *

## 8.6 Indicadores

O programa deverá monitorar, entre outros:

- taxa de utilização;
    
- licenças disponíveis;
    
- licenças excedidas;
    
- softwares sem contrato;
    
- softwares descontinuados;
    
- softwares não homologados.
    

* * *

## 8.7 Boas Práticas

- centralização do catálogo de software;
    
- padronização de versões;
    
- revisão periódica das licenças;
    
- remoção de softwares não utilizados;
    
- integração com inventário automático;
    
- integração com processos de mudança.
    

* * *

# 9\. CONFIGURATION MANAGEMENT DATABASE (CMDB)

## 9.1 Objetivo

A **Configuration Management Database (CMDB)** é a base de dados responsável por armazenar os **Configuration Items (CIs)** e seus relacionamentos.

Enquanto o ITAM administra o ciclo de vida dos ativos, a CMDB descreve **como esses ativos compõem e suportam os serviços de TI**.

Essa distinção é fundamental:

| ITAM | CMDB |
| --- | --- |
| Gerencia ativos | Gerencia itens de configuração |
| Ênfase financeira | Ênfase operacional |
| Controle patrimonial | Relacionamentos |
| Ciclo de vida | Prestação de serviços |
| Custos | Impactos |

Embora possuam finalidades diferentes, ambos os processos compartilham informações e devem permanecer sincronizados.

* * *

## 9.2 O que é um Configuration Item (CI)

Um **Configuration Item (CI)** é qualquer componente que necessite ser gerenciado para garantir a entrega de um serviço de TI.

Nem todo ativo é um CI.

Da mesma forma, nem todo CI representa um ativo patrimonial.

Exemplos de CIs:

- servidores;
    
- máquinas virtuais;
    
- aplicações;
    
- bancos de dados;
    
- switches;
    
- firewalls;
    
- APIs;
    
- serviços cloud;
    
- certificados digitais;
    
- clusters Kubernetes;
    
- balanceadores;
    
- filas de mensageria.
    

* * *

## 9.3 Relacionamentos

O principal objetivo da CMDB é representar as dependências existentes entre os componentes do ambiente.

Exemplo:

```
Notebook
      │
      ▼
Usuário
      │
      ▼
Sistema Corporativo
      │
      ▼
Servidor de Aplicação
      │
      ▼
Banco PostgreSQL
      │
      ▼
Storage
      │
      ▼
Infraestrutura Cloud
```

* * *

Outro exemplo:

```
Portal Corporativo
        │
        ▼
NGINX
        │
        ▼
Container Docker
        │
        ▼
Banco MongoDB
        │
        ▼
Storage
```

* * *

## 9.4 Tipos de Relacionamentos

A CMDB deverá suportar relacionamentos como:

- depende de;
    
- executa em;
    
- conectado a;
    
- utiliza;
    
- hospedado em;
    
- protegido por;
    
- monitorado por;
    
- contratado por;
    
- pertence a;
    
- mantido por.
    

* * *

## 9.5 Benefícios

Uma CMDB bem estruturada permite:

- análise de impacto;
    
- gerenciamento de mudanças;
    
- gerenciamento de incidentes;
    
- gerenciamento de problemas;
    
- continuidade de serviços;
    
- gestão de riscos;
    
- planejamento de capacidade.
    

* * *

## 9.6 Integração entre ITAM e CMDB

Embora distintos, ambos deverão compartilhar informações.

### O ITAM fornece

- patrimônio;
    
- fabricante;
    
- fornecedor;
    
- garantia;
    
- contratos;
    
- localização;
    
- custo;
    
- responsável.
    

* * *

### A CMDB fornece

- dependências;
    
- impacto;
    
- serviços relacionados;
    
- aplicações suportadas;
    
- infraestrutura associada.
    

* * *

## Exemplo Integrado

```
Notebook Dell

↓

Usuário

↓

Sistema Financeiro

↓

Servidor Linux

↓

Banco PostgreSQL

↓

Storage SAN

↓

Contrato de Suporte

↓

Fornecedor
```

* * *

# 10\. MODELO DE DADOS DA CMDB

Todos os Configuration Items deverão possuir, sempre que aplicável:

## Identificação

- Nome
    
- Categoria
    
- Tipo
    
- Classe
    
- Fabricante
    
- Modelo
    

* * *

## Operação

- Ambiente (Produção, Homologação, Desenvolvimento)
    
- Criticidade
    
- Disponibilidade
    
- SLA
    

* * *

## Localização

- Unidade
    
- Rack
    
- Região Cloud
    
- Zona de Disponibilidade
    

* * *

## Responsabilidade

- Dono do serviço
    
- Gestor técnico
    
- Equipe responsável
    

* * *

## Relacionamentos

- Serviço associado
    
- Aplicações
    
- Banco de dados
    
- Equipamentos
    
- Contratos
    
- Monitoramento
    

* * *

## Histórico

Todo CI deverá manter histórico de:

- mudanças;
    
- substituições;
    
- atualizações;
    
- incidentes relevantes;
    
- alterações de relacionamento.
    

* * *

# 11\. RELACIONAMENTO COM OUTROS PROCESSOS ITIL

O ITAM e a CMDB são processos transversais e deverão apoiar diversos processos de gerenciamento de serviços.

## Gerenciamento de Incidentes

Permite identificar rapidamente:

- ativos afetados;
    
- usuários impactados;
    
- serviços indisponíveis.
    

* * *

## Gerenciamento de Problemas

Permite identificar:

- ativos com maior incidência de falhas;
    
- componentes recorrentes;
    
- tendências de indisponibilidade.
    

* * *

## Gerenciamento de Mudanças

Antes da aprovação de uma mudança será possível identificar:

- dependências;
    
- impacto;
    
- riscos;
    
- ativos envolvidos.
    

* * *

## Gerenciamento de Liberação

Permite controlar:

- versões implantadas;
    
- ambientes afetados;
    
- softwares relacionados.
    

* * *

## Gerenciamento de Continuidade

Permite identificar:

- ativos críticos;
    
- dependências;
    
- infraestrutura de contingência;
    
- requisitos de recuperação.
    

* * *

## Benefícios Esperados

Ao integrar ITAM, CMDB e ITSM, a organização obtém:

- maior confiabilidade das informações;
    
- redução do tempo de diagnóstico de incidentes;
    
- melhor planejamento de mudanças;
    
- maior previsibilidade de impactos;
    
- redução de riscos operacionais;
    
- melhoria da governança de TI;
    
- aumento da maturidade dos processos.
    

* * *

* * *

# 12\. CICLO DE VIDA DOS ATIVOS

## 12.1 Objetivo

Todo ativo de Tecnologia da Informação deverá possuir um ciclo de vida claramente definido, permitindo sua rastreabilidade desde a identificação da necessidade de aquisição até sua desativação e descarte.

A padronização do ciclo de vida assegura consistência das informações, facilita auditorias, apoia a gestão financeira e melhora o planejamento da renovação tecnológica.

* * *

## 12.2 Etapas do Ciclo de Vida

O ciclo de vida corporativo dos ativos será composto pelas seguintes fases:

### Planejamento

Nesta fase ocorre a identificação da necessidade do ativo.

Estados possíveis:

- Solicitado
    
- Em análise
    
- Aguardando aprovação
    
- Aprovado
    

* * *

### Aquisição

Após a aprovação da demanda inicia-se o processo de compra.

Estados possíveis:

- Em aquisição
    
- Pedido emitido
    
- Recebido
    
- Conferido
    

* * *

### Cadastro

Após o recebimento, o ativo deverá ser registrado na ferramenta de ITAM.

Atividades:

- cadastro patrimonial;
    
- registro técnico;
    
- vinculação contratual;
    
- associação ao fornecedor;
    
- associação ao centro de custo.
    

* * *

### Preparação

Antes da disponibilização ao usuário ou ambiente produtivo deverão ser realizadas atividades como:

- instalação do sistema operacional;
    
- atualização de firmware;
    
- instalação de softwares homologados;
    
- aplicação de políticas de segurança;
    
- inventário automático;
    
- testes funcionais.
    

Estados:

- Em preparação
    
- Em homologação
    
- Disponível
    

* * *

### Operação

Representa o período de utilização do ativo.

Estados possíveis:

- Em uso
    
- Em produção
    
- Reserva técnica
    
- Disponível
    
- Em empréstimo
    

* * *

### Manutenção

Durante sua vida útil o ativo poderá passar por manutenção preventiva ou corretiva.

Estados:

- Em garantia
    
- Em manutenção
    
- Aguardando peças
    
- Em reparo
    
- Em análise técnica
    

* * *

### Renovação Tecnológica (Refresh)

Sempre que necessário deverá ser avaliada a substituição do ativo.

Critérios recomendados:

- obsolescência tecnológica;
    
- aumento do custo de manutenção;
    
- indisponibilidade de peças;
    
- encerramento do suporte do fabricante;
    
- baixa performance.
    

* * *

### Encerramento

O encerramento do ciclo de vida poderá ocorrer por:

- obsolescência;
    
- substituição;
    
- perda;
    
- roubo;
    
- descarte ambientalmente adequado;
    
- alienação;
    
- doação.
    

Estados finais:

- Desativado
    
- Baixado
    
- Descartado
    
- Alienado
    

* * *

# 13\. PROCESSOS OPERACIONAIS

## 13.1 Entrada de Ativos

Fluxo recomendado:

```text
Solicitação
        │
        ▼
Aprovação
        │
        ▼
Aquisição
        │
        ▼
Recebimento
        │
        ▼
Cadastro no ITAM
        │
        ▼
Preparação
        │
        ▼
Entrega ao usuário
```

* * *

## 13.2 Movimentação

Toda movimentação deverá ser registrada.

Exemplos:

- troca de usuário;
    
- mudança de unidade;
    
- alteração de departamento;
    
- movimentação entre racks;
    
- mudança de ambiente;
    
- substituição temporária.
    

Fluxo:

```text
Solicitação

↓

Aprovação

↓

Atualização cadastral

↓

Registro do histórico

↓

Novo termo de responsabilidade
```

* * *

## 13.3 Empréstimo

Ativos emprestados deverão possuir:

- responsável temporário;
    
- período do empréstimo;
    
- motivo;
    
- data prevista para devolução.
    

* * *

## 13.4 Devolução

Fluxo recomendado:

```text
Recebimento

↓

Inspeção

↓

Atualização cadastral

↓

Formatação (quando aplicável)

↓

Retorno ao estoque
```

* * *

## 13.5 Inventário

Inventários deverão ocorrer periodicamente.

Recomenda-se:

| Tipo | Frequência |
| --- | --- |
| User Endpoints | Semestral |
| Data Center | Trimestral |
| Equipamentos críticos | Mensal |
| Softwares | Mensal |
| Cloud | Diário (automatizado) |

* * *

## 13.6 Baixa Patrimonial

A baixa deverá possuir documentação comprobatória.

Motivos:

- obsolescência;
    
- perda;
    
- roubo;
    
- descarte;
    
- venda;
    
- doação.
    

Todos os documentos deverão permanecer vinculados ao ativo.

* * *

# 14\. INTEGRAÇÕES E DESCOBERTA AUTOMÁTICA

## Objetivo

O processo de ITAM deverá integrar-se às principais ferramentas corporativas, reduzindo atividades manuais e aumentando a confiabilidade das informações.

O inventário automático deverá complementar o cadastro manual, preservando informações administrativas que normalmente não são descobertas pelas ferramentas de inventário.

* * *

## 14.1 Ferramentas de Inventário

Ferramentas recomendadas:

- OCS Inventory;
    
- GLPI Agent;
    
- Microsoft Intune;
    
- Microsoft Configuration Manager (SCCM);
    
- Lansweeper.
    

Essas ferramentas deverão fornecer informações como:

- hardware instalado;
    
- softwares instalados;
    
- sistema operacional;
    
- endereço IP;
    
- endereço MAC;
    
- número de série;
    
- versão de BIOS;
    
- espaço em disco;
    
- memória;
    
- processador.
    

* * *

## 14.2 Diretório Corporativo

Integração recomendada com:

- Microsoft Active Directory;
    
- Microsoft Entra ID;
    
- LDAP corporativo.
    

Objetivos:

- sincronização de usuários;
    
- departamentos;
    
- unidades;
    
- gestores;
    
- grupos organizacionais.
    

* * *

## 14.3 Monitoramento

Integração recomendada com:

- Zabbix;
    
- Grafana;
    
- Prometheus.
    

Benefícios:

- associação entre ativos e monitoramento;
    
- identificação de ativos indisponíveis;
    
- atualização automática de status;
    
- apoio à análise de impacto.
    

* * *

## 14.4 Service Desk

Integração com o TOPdesk deverá permitir:

- abertura de chamados diretamente pelo ativo;
    
- visualização do histórico;
    
- associação entre incidentes e equipamentos;
    
- relacionamento com mudanças;
    
- relacionamento com problemas.
    

* * *

## 14.5 Ambientes Cloud

Integração recomendada com:

- Amazon Web Services (AWS);
    
- Microsoft Azure;
    
- Google Cloud Platform (GCP);
    
- Oracle Cloud Infrastructure (OCI).
    

Informações sincronizadas:

- instâncias;
    
- bancos de dados;
    
- redes;
    
- volumes;
    
- custos;
    
- regiões;
    
- tags;
    
- contas.
    

* * *

## 14.6 Ferramentas DevOps

Quando aplicável, recomenda-se integração com:

- GitHub Enterprise;
    
- GitLab;
    
- Azure DevOps;
    
- Jenkins;
    
- Kubernetes.
    

Objetivos:

- relacionamento entre aplicações e infraestrutura;
    
- rastreabilidade das implantações;
    
- apoio à CMDB.
    

* * *

# 15\. POLÍTICA DE QUALIDADE DOS DADOS

A qualidade das informações cadastradas é um dos principais fatores de sucesso do programa de ITAM.

Todo ativo deverá atender aos seguintes princípios:

## Completude

Todos os campos obrigatórios deverão estar preenchidos.

* * *

## Precisão

As informações deverão refletir fielmente o estado atual do ativo.

* * *

## Atualização

Sempre que ocorrer movimentação, alteração técnica ou mudança de responsabilidade, o cadastro deverá ser atualizado.

* * *

## Integridade

Não deverão existir registros duplicados.

Cada ativo deverá possuir um identificador único.

* * *

## Consistência

As informações compartilhadas entre ITAM, CMDB, inventário automático e Service Desk deverão permanecer sincronizadas.

* * *

# 16\. AUDITORIA E CONFORMIDADE

O programa deverá estabelecer auditorias periódicas para validar:

- existência física dos ativos;
    
- conformidade do inventário;
    
- utilização de softwares;
    
- contratos vigentes;
    
- responsáveis cadastrados;
    
- ativos órfãos;
    
- ativos duplicados;
    
- ativos sem localização definida.
    

* * *

## Indicadores de Auditoria

Sugere-se acompanhar, entre outros:

- percentual de ativos auditados;
    
- percentual de inconsistências encontradas;
    
- tempo médio para correção;
    
- ativos sem responsável;
    
- ativos sem contrato;
    
- ativos sem localização;
    
- softwares não homologados.
    

* * *

# 17\. GESTÃO DE RISCOS

O programa de ITAM deverá contribuir para a identificação e mitigação de riscos relacionados aos ativos de TI.

Exemplos de riscos:

| Risco | Impacto | Mitigação |
| --- | --- | --- |
| Equipamento sem responsável | Extravio ou uso indevido | Termo de responsabilidade e auditorias periódicas |
| Licenças insuficientes | Não conformidade em auditorias | Revisão periódica do inventário de software |
| Contratos vencidos | Interrupção de suporte | Alertas automáticos de renovação |
| Crescimento descontrolado dos custos em nuvem | Extrapolação orçamentária | Monitoramento contínuo com práticas de FinOps |
| Ativos sem registro na CMDB | Dificuldade na análise de impacto | Integração entre ITAM e CMDB |

* * *

Na **Parte 5** concluiremos o documento com:

- **KPIs e Indicadores de Desempenho**;
    
- **Estrutura mínima de dados para o TOPdesk**;
    
- **Roadmap de Implantação**;
    
- **Modelo de Maturidade do ITAM**;
    
- **Recomendações para evolução contínua**;
    
- **Considerações finais**, consolidando o documento em um guia corporativo para implantação e governança do ITAM.
    

&nbsp;

# DIRETRIZES CORPORATIVAS PARA IMPLEMENTAÇÃO DA GESTÃO DE ATIVOS DE TI (ITAM)

# PARTE 5

* * *

# 18\. INDICADORES DE DESEMPENHO (KPIs)

## 18.1 Objetivo

A mensuração dos resultados do Programa de Gestão de Ativos de TI é fundamental para avaliar sua eficiência, apoiar a tomada de decisão e promover a melhoria contínua.

Os indicadores deverão ser acompanhados periodicamente por meio de painéis gerenciais (*dashboards*), permitindo o monitoramento da evolução do programa e a identificação de oportunidades de melhoria.

Recomenda-se que os indicadores sejam classificados em quatro grandes grupos, correspondentes aos pilares do programa: Hardware, Software, Cloud/FinOps e Contratos.

* * *

## 18.2 Indicadores de Hardware (HAM)

### Inventário

- Percentual de ativos inventariados.
    
- Percentual de ativos auditados.
    
- Percentual de ativos sem patrimônio.
    
- Percentual de ativos sem número de série.
    

### Responsabilidade

- Percentual de ativos sem usuário responsável.
    
- Percentual de ativos sem gestor definido.
    
- Percentual de ativos sem localização cadastrada.
    

### Ciclo de Vida

- Ativos em produção.
    
- Ativos em manutenção.
    
- Ativos em garantia.
    
- Ativos em fim de vida (*End of Life – EOL*).
    
- Ativos em fim de suporte (*End of Support – EOS*).
    
- Tempo médio de permanência em estoque.
    
- Idade média do parque tecnológico.
    

### Financeiro

- Valor total dos ativos.
    
- Valor por unidade.
    
- Valor por centro de custo.
    
- Valor depreciado (quando aplicável).
    

* * *

## 18.3 Indicadores de Software (SAM)

### Licenciamento

- Taxa de utilização das licenças.
    
- Licenças disponíveis.
    
- Licenças ociosas.
    
- Licenças excedidas.
    
- Licenças próximas ao vencimento.
    

### Conformidade

- Softwares homologados.
    
- Softwares não homologados.
    
- Softwares sem contrato.
    
- Softwares instalados sem autorização.
    

### Financeiro

- Investimento anual em software.
    
- Economia obtida com reaproveitamento de licenças.
    
- Custo por usuário.
    
- Custo por departamento.
    

* * *

## 18.4 Indicadores de Cloud (FinOps)

### Consumo

- Consumo mensal.
    
- Consumo diário.
    
- Crescimento mensal.
    
- Recursos ociosos.
    

### Financeiro

- Custo por ambiente.
    
- Custo por sistema.
    
- Custo por centro de custo.
    
- Custo por projeto.
    
- Desvio orçamentário.
    

### Eficiência

- Recursos subutilizados.
    
- Recursos superdimensionados.
    
- Percentual de otimização.
    
- Economia obtida por ações de FinOps.
    

* * *

## 18.5 Indicadores de Contratos (ITCM)

- Contratos vigentes.
    
- Contratos próximos ao vencimento.
    
- Contratos renovados.
    
- Contratos encerrados.
    
- SLA atendido.
    
- SLA descumprido.
    
- Fornecedores homologados.
    
- Valor anual contratado.
    

* * *

## 18.6 Indicadores Estratégicos

A alta administração poderá acompanhar indicadores consolidados, tais como:

- maturidade do ITAM;
    
- percentual de ativos corretamente classificados;
    
- percentual de ativos relacionados à CMDB;
    
- percentual de ativos auditados;
    
- conformidade geral do ambiente;
    
- índice de qualidade dos dados.
    

* * *

# 19\. ESTRUTURA MÍNIMA DE DADOS PARA O TOPDESK

O TOPdesk será a ferramenta corporativa responsável pelo gerenciamento dos ativos de TI e pela integração com os demais processos de gerenciamento de serviços.

Para garantir padronização e qualidade das informações, todos os ativos deverão possuir um conjunto mínimo de atributos.

* * *

## 19.1 Identificação

- Nome do ativo
    
- Categoria
    
- Classe
    
- Tipo
    
- Fabricante
    
- Modelo
    
- Número de patrimônio
    
- Número de série
    
- Código interno
    

* * *

## 19.2 Responsabilidade

- Usuário responsável
    
- Gestor responsável
    
- Área responsável
    
- Unidade organizacional
    

* * *

## 19.3 Localização

- Unidade
    
- Prédio
    
- Andar
    
- Sala
    
- Rack (quando aplicável)
    
- Região Cloud (quando aplicável)
    

* * *

## 19.4 Situação

- Estado do ciclo de vida
    
- Criticidade
    
- Ambiente (Produção, Homologação ou Desenvolvimento)
    
- Disponibilidade
    

* * *

## 19.5 Dados Técnicos

- Sistema operacional
    
- Processador
    
- Memória
    
- Armazenamento
    
- Endereço IP
    
- Endereço MAC
    
- Hostname
    
- Domínio
    

* * *

## 19.6 Dados Financeiros

- Centro de custo
    
- Fornecedor
    
- Data de aquisição
    
- Valor de aquisição
    
- Contrato associado
    
- Garantia
    
- Data de término da garantia
    

* * *

## 19.7 Relacionamentos

Cada ativo deverá possuir relacionamentos, quando aplicável, com:

- usuário;
    
- departamento;
    
- contrato;
    
- fornecedor;
    
- serviço de TI;
    
- Configuration Item (CI);
    
- software;
    
- banco de dados;
    
- equipamento de rede;
    
- monitoramento;
    
- chamados;
    
- mudanças;
    
- problemas.
    

* * *

# 20\. ROADMAP DE IMPLEMENTAÇÃO

A implantação do programa deverá ocorrer de forma gradual, permitindo ganhos progressivos de maturidade.

* * *

## Fase 1 – Planejamento

Objetivos:

- definição do escopo;
    
- definição da governança;
    
- definição das categorias;
    
- definição do modelo de dados;
    
- configuração inicial do TOPdesk.
    

**Entregáveis:**

- política de ITAM;
    
- catálogo de ativos;
    
- estrutura de classes;
    
- modelo de dados.
    

* * *

## Fase 2 – Inventário Inicial

Objetivos:

- integração com ferramentas de descoberta;
    
- importação do inventário existente;
    
- saneamento dos dados;
    
- eliminação de duplicidades.
    

**Entregáveis:**

- inventário consolidado;
    
- base inicial do ITAM.
    

* * *

## Fase 3 – Estruturação da Governança

Objetivos:

- definição de responsáveis;
    
- definição de fluxos;
    
- implantação dos processos operacionais;
    
- formalização dos termos de responsabilidade.
    

* * *

## Fase 4 – Integração com a CMDB

Objetivos:

- criação dos Configuration Items;
    
- modelagem dos relacionamentos;
    
- integração com o Service Desk;
    
- integração com monitoramento.
    

* * *

## Fase 5 – Indicadores e Dashboards

Objetivos:

- implantação dos KPIs;
    
- construção dos painéis gerenciais;
    
- definição das rotinas de acompanhamento.
    

* * *

## Fase 6 – Melhoria Contínua

Objetivos:

- auditorias periódicas;
    
- revisão dos processos;
    
- evolução da CMDB;
    
- ampliação das integrações;
    
- avaliação periódica da maturidade do programa.
    

* * *

# 21\. MODELO DE MATURIDADE DO PROGRAMA ITAM

A evolução do programa deverá ser acompanhada por níveis de maturidade.

| Nível | Descrição |
| --- | --- |
| **1 – Inicial** | Inventário descentralizado, informações incompletas e processos informais. |
| **2 – Gerenciado** | Inventário consolidado, processos documentados e responsabilidades definidas. |
| **3 – Padronizado** | Processos institucionalizados, integração com ferramentas de descoberta e indicadores consolidados. |
| **4 – Controlado** | Automação, integração com CMDB, governança baseada em indicadores e auditorias periódicas. |
| **5 – Otimizado** | ITAM integrado ao planejamento estratégico, FinOps, automações avançadas e melhoria contínua baseada em métricas. |

* * *

# 22\. FATORES CRÍTICOS DE SUCESSO

A implantação do programa dependerá, entre outros, dos seguintes fatores:

- apoio da alta administração;
    
- definição clara de papéis e responsabilidades;
    
- qualidade das informações cadastradas;
    
- integração entre processos de ITAM, CMDB e ITSM;
    
- atualização contínua dos dados;
    
- capacitação das equipes;
    
- utilização consistente da ferramenta corporativa;
    
- auditorias periódicas;
    
- acompanhamento por indicadores;
    
- comprometimento das áreas de negócio.
    

* * *

# 23\. CONSIDERAÇÕES FINAIS

A Gestão de Ativos de Tecnologia da Informação deve ser entendida como um processo permanente de governança, e não apenas como um inventário de equipamentos.

Sua efetividade depende da integração entre pessoas, processos, tecnologias e informações, garantindo que os ativos sejam administrados de forma eficiente durante todo o seu ciclo de vida e que contribuam para a entrega de valor ao negócio.

A utilização do **TOPdesk** como plataforma corporativa para ITAM permitirá consolidar informações provenientes de ferramentas de descoberta automática, monitoramento, diretório corporativo e gerenciamento de serviços, estabelecendo uma **fonte única e confiável de informações** (*Single Source of Truth*) para os ativos de TI.

A integração entre **ITAM**, **CMDB** e os processos de **ITSM** proporcionará maior capacidade de análise de impacto, melhoria na gestão de mudanças, redução do tempo de resolução de incidentes, otimização dos investimentos em tecnologia e fortalecimento da governança corporativa.

Este documento deverá servir como referência para a implantação, operação e evolução contínua do Programa de Gestão de Ativos de TI, sendo revisado periodicamente para acompanhar a evolução tecnológica, as necessidades da organização e as melhores práticas internacionais.

* * *

# APÊNDICE A – GLOSSÁRIO

| Sigla | Descrição |
| --- | --- |
| **ITAM** | IT Asset Management (Gestão de Ativos de TI) |
| **HAM** | Hardware Asset Management |
| **SAM** | Software Asset Management |
| **Cloud/FinOps** | Gestão Financeira e Operacional de Recursos em Nuvem |
| **ITCM** | IT Contract Management |
| **CMDB** | Configuration Management Database |
| **CI** | Configuration Item |
| **ITSM** | IT Service Management |
| **IaaS** | Infrastructure as a Service |
| **PaaS** | Platform as a Service |
| **SaaS** | Software as a Service |
| **SLA** | Service Level Agreement |
| **EOL** | End of Life |
| **EOS** | End of Support |

* * *

## Minha recomendação técnica

Depois de revisar todo o documento, eu faria ainda **uma última evolução** antes de considerá-lo final.

Hoje ele está excelente como **diretriz corporativa** (aproximadamente 30 páginas). Porém, para implantação do TOPdesk, eu acrescentaria três apêndices que normalmente fazem muita diferença na execução do projeto:

1.  **Modelo de Classes do TOPdesk** (Assets, Asset Types, Templates e relacionamentos).
    
2.  **Dicionário de Dados**, definindo cada campo do cadastro (nome, tipo, obrigatoriedade, origem do dado e responsável pela atualização).
    
3.  **Matriz RACI**, indicando quem é Responsável (Responsible), Aprovador (Accountable), Consultado (Consulted) e Informado (Informed) em cada processo do ciclo de vida do ativo.
    

Esses anexos transformariam este documento de uma diretriz de governança em um **manual completo de implementação do ITAM no TOPdesk**, reduzindo dúvidas durante a configuração da ferramenta e a operacionalização dos processos.