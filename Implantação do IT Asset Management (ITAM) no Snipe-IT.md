# DIRETRIZES CORPORATIVAS PARA IMPLEMENTAÇÃO DA GESTÃO DE ATIVOS DE TI (ITAM) COM SNIPE-IT

## Informações do Documento

| Campo | Informação |
| --- | --- |
| Documento | Diretrizes Corporativas e Projeto de Implantação de Gestão de Ativos de TI (ITAM) |
| Versão | 1.0 |
| Status | Proposta Técnica para Aprovação Executiva |
| Autor | Especialista em ITIL v4 & Gestão de Ativos de TI (ITAM) |
| Área Responsável | Secretaria de Tecnologia da Informação / Governança de TI |
| Instituição | Embrapa (Empresa Brasileira de Pesquisa Agropecuária) |
| Abrangência | Sede (Brasília/DF) e 43 Unidades Descentralizadas (UDs) |
| Ferramenta | Snipe-IT (Open Source IT Asset Management Platform) |
| Data de Emissão | 30/07/2026 |
| Classificação | Uso Interno |
| Base Conceitual | ITIL® 4, ISO/IEC 19770, ISO 55000, FinOps Foundation, Boas Práticas Snipe-IT |

---

## Histórico de Revisões

| Versão | Data | Autor | Descrição |
| --- | --- | --- | --- |
| 1.0 | 30/07/2026 | Especialista ITAM & ITIL | Criação da proposta técnica completa de implantação do ITAM do zero utilizando a ferramenta Snipe-IT para a Embrapa (Sede + 43 Unidades Descentralizadas). |

---

## Distribuição

Este documento destina-se às seguintes instâncias da Embrapa:

- Diretoria Executiva e Secretaria de TI (Sede)
- Comitê de Governança de TI e Segurança da Informação
- Chefias de Administração e Pontos Focais de TI das 43 Unidades Descentralizadas (UDs)
- Equipes de Infraestrutura, Suporte, Compras, Contratos e Patrimônio
- Auditoria Interna e Controladoria Corporativa

---

## Referências Normativas e Tecnológicas

- **ITIL® 4 Practice Guides** – IT Asset Management & Service Configuration Management
- **ISO/IEC 19770-1** – IT Asset Management Systems: Requirements
- **ISO 55000 / 55001** – Asset Management Overview and Requirements
- **Lei Geral de Proteção de Dados (LGPD)** – Lei nº 13.709/2018
- **Documentação Oficial Snipe-IT v6.x / v7.x** (REST API, Multi-Company Support, LDAP/AD Integration, EULA Signatures)

---

# 1. INTRODUÇÃO E GOVERNANÇA (ITIL® 4)

A Gestão de Ativos de Tecnologia da Informação (*IT Asset Management* – ITAM) na Embrapa é um imperativo estratégico para a sustentabilidade da pesquisa agropecuária nacional. Dada a presença geográfica da instituição — constituída pela Sede em Brasília/DF e **43 Unidades Descentralizadas (UDs)** distribuídas por todos os biomas e regiões do Brasil —, o gerenciamento descentralizado e sem padronização resulta em riscos de conformidade, ociosidade de recursos e opacidade orçamentária.

Esta proposta estabelece um projeto estruturado para a implantação do ITAM **do zero**, utilizando como plataforma centralizadora a ferramenta **Snipe-IT** (plataforma *open-source* líder de mercado em ITAM). A solução permitirá centralizar a visibilidade corporativa enquanto preserva a autonomia operacional necessária às 43 UDs.

## 1.1 Co-criação de Valor na Embrapa

Sob a ótica da **ITIL® 4**, o ITAM não é um processo burocrático de controle físico, mas um habilitador de **Co-criação de Valor**. Na Embrapa:
- **Pesquisa Agropecuária e Inovação:** Garantir que cientistas e pesquisadores em qualquer UD (ex: Embrapa Soja, Embrapa Amazônia Oriental, Embrapa Gado de Corte) disponham de hardware homologado, estações de trabalho de alto desempenho e softwares científicos (ArcGIS, MATLAB, SAS, ferramentas de sequenciamento genômico) devidamente licenciados e operacionais.
- **Eficiência Orçamentária e Reinvestimento:** O controle rigoroso do ciclo de vida dos ativos evita compras duplicadas e subscrições ociosas, liberando recursos orçamentários diretamente para projetos finalísticos de PD&I (Pesquisa, Desenvolvimento e Inovação).

## 1.2 As Quatro Dimensões da Gestão de Ativos de TI (ITAM)

```
           +-------------------------------------------------------+
           |           AS QUATRO DIMENSÕES DO ITAM / SNIPE-IT      |
           +-------------------------------------------------------+
           |                                                       |
           |   1. Organizações e Pessoas                           |
           |      - Estrutura de Governança Centralizada (Sede) +  |
           |        Pontos Focais de TI nas 43 UDs.                |
           |        Cultura de zelo patrimonial e aceite digital.  |
           |                                                       |
           |   2. Informação e Tecnologia                          |
           |      - Cluster Snipe-IT de alta disponibilidade.      |
           |        Sincronização nativa AD/LDAP, leitura de       |
           |        Barcodes/QR Codes e APIs REST de descoberta.    |
           |                                                       |
           |   3. Parceiros e Fornecedores                         |
           |      - Mapeamento de contratos de garantia, licenças, |
           |        suporte de fabricantes (Dell, HPE, Cisco, etc.)|
           |        e revendas de softwares científicos.           |
           |                                                       |
           |   4. Fluxos de Valor e Processos                      |
           |      - Fluxos padronizados de Entrada, Checkout,      |
           |        Auditoria Periódica, Manutenção e Descarte     |
           |        integrados aos Service Desks locais/centrais.  |
           |                                                       |
           +-------------------------------------------------------+
```

---

# 2. OBJETIVOS DO PROGRAMA ITAM COM SNIPE-IT

1. **Repositório Único e Consolidado (Single Source of Truth):** Implantar o Snipe-IT como fonte única da verdade para todos os ativos de TI da Embrapa (Sede + 43 UDs).
2. **Arquitetura Multi-Unidade (Multi-Company/Location):** Estruturar o Snipe-IT de modo a permitir visão consolidada para a Sede e visibilidade segregada/gestão local para cada uma das 43 UDs.
3. **Rastreabilidade e Aceite Digital Automático:** Utilizar o recurso nativo de **EULA / Digital Signature** do Snipe-IT para emissão e aceite eletrônico imediato de Termos de Responsabilidade por e-mail no momento do envio do equipamento ao usuário.
4. **Agilidade em Inventários com QR Code:** Padronizar a etiquetagem com QR Codes gerados pelo Snipe-IT, permitindo auditorias físicas ágeis por leitores móveis e smartphones nas 43 UDs.
5. **Mitigação de Riscos Legais e Fiscais (SAM):** Controlar licenças corporativas e científicas, prevenindo multas por sublicenciamento e eliminando pagamentos por licenças não utilizadas.
6. **Automação de Entrada via AD/LDAP e Discovery:** Integrar o Snipe-IT ao Active Directory corporativo para sincronização em tempo real de usuários, departamentos e lotações nas UDs, além de scripts e agentes de descoberta de hardware/software.

---

# 3. ESCOPO CORPORATIVO

O escopo do ITAM abrange todos os recursos tecnológicos da Embrapa, categorizados no Snipe-IT como:

### 3.1 Hardware (Assets / Ativos Patrimoniais)
- **User Endpoints:** Notebooks, Desktops, Workstations de Pesquisa, Tablets, Smartphones corporativos.
- **Infraestrutura de Rede e Data Center:** Servidores físicos, Storages, Appliances, Switches, Firewalls, Roteadores, Nobreaks, Access Points.
- **Equipamentos Científicos de TI:** Clusters de computação gráfica/genômica, receptores GNSS/RTK de precisão agrícola, servidores de campo.

### 3.2 Componentes e Acessórios (Components & Accessories)
- **Componentes:** RAM, SSDs/HDDs, Placas de Vídeo/GPU alocados ou substituídos em servidores e estações.
- **Acessórios:** Monitores, Dock stations, Téclados, Mouses, Nobreaks individuais, Periféricos de campo.

### 3.3 Licenças de Software (Licenses - SAM)
- **Softwares Corporativos:** Sistemas Operacionais, Suítes de Escritório (Microsoft 365 / Google Workspace), Antivírus/EDR.
- **Softwares de Pesquisa Agropecuária (Especializados):** ArcGIS/ArcMap, MATLAB, SAS, SPSS, software de modelagem climatológica e biométrica, cujas licenças possuem alto valor monetário.

### 3.4 Insumos e Consumíveis (Consumables)
- Toners, cartuchos de impressão, mídias de backup, cabos de rede, adaptadores de campo.

### 3.5 Nuvem & Contratos (Cloud / FinOps & Suppliers)
- Metadados de instâncias Cloud (AWS, Azure, GCP), contas de API e mapeamento de contratos de garantia e manutenção vinculados aos fornecedores cadastrados no Snipe-IT.

---

# 4. ARQUITETURA ORGANIZACIONAL (SEDE + 43 UNIDADES DESCENTRALIZADAS)

Para atender à complexidade da Embrapa, o Snipe-IT será configurado utilizando o conceito de **Multi-Company Support** (`full_multiple_companies_support = true`) combinado com a estrutura hierárquica de **Locations** (Localizações).

```
========================================================================================
                          SNIPE-IT EMBRAPA CORPORATIVO (CLUSTER)
========================================================================================
                                           │
       +-----------------------------------+-----------------------------------+
       │                                   │                                   │
       ▼                                   ▼                                   ▼
+-----------------------+       +-----------------------+       +-----------------------+
|  EMBRAPA SEDE (DF)    |       | EMBRAPA SOJA (PR)     |       | EMBRAPA AMAZÔNIA (PA) | ... (43 UDs)
+-----------------------+       +-----------------------+       +-----------------------+
| - Depto TI Sede       |       | - Laboratórios        |       | - Estações de Campo   |
| - Data Center Central |       | - Campo Experimental  |       | - Prédio Central UD   |
| - Estoque Central TI  |       | - Almoxarifado UD     |       | - Almoxarifado UD     |
+-----------------------+       +-----------------------+       +-----------------------+
```

## 4.1 Modelo de Scoping e Permissões por Unidade

1. **Empresas/Unidades (Companies):**
   - Cada UD será cadastrada como uma entidade ("Company") no Snipe-IT (ex: `Embrapa Sede`, `Embrapa Soja`, `Embrapa Gado de Corte`, `Embrapa Amazônia Oriental`).
   - Isso permite que administradores locais de TI visualizem e gerenciem apenas os ativos pertencentes à sua própria UD.
2. **Localizações Físicas (Locations & Child Locations):**
   - Dentro de cada UD, serão estruturadas localizações filhas (ex: `Embrapa Soja -> Bloco de Laboratórios -> Lab Biotecnologia 02` ou `Embrapa Sede -> Data Center -> Rack A04`).
3. **Perfis de Acesso (User Groups & Roles):**
   - **Super Admin (Sede):** Equipe de Governança de TI central. Acesso total a todas as 44 unidades, relatórios consolidados e auditorias globais.
   - **Admin de TI da UD:** Responsável técnico da Unidade Descentralizada. Gerencia check-in/check-out, inventários locais e cadastros da sua UD.
   - **Técnico de Suporte UD:** Realiza movimentações operacionais, atribuição a usuários e leitura de QR Codes.
   - **Auditores Internos:** Acesso somente leitura para relatórios patrimoniais e de conformidade.
   - **Usuários Finais (Self-Service View):** Colaboradores de qualquer UD visualizam apenas os ativos sob sua responsabilidade e realizam o aceite digital dos Termos.

---

# 5. DETALHAMENTO DOS PILARES ITAM NO SNIPE-IT

## 5.1 Hardware Asset Management (HAM)

No Snipe-IT, o HAM é estruturado através da tríade: **Categoria + Modelo + Ativo (Asset Tag/Patrimônio)**.

### Mapeamento de Status Labels (Estados do Ciclo de Vida)
O Snipe-IT utiliza *Status Labels* customizados divididos em quatro meta-status nativos:

| Status Label no Snipe-IT | Meta-Status Nativo | Significado Operacional na Embrapa |
| --- | --- | --- |
| **Pronto para Uso (Estoque)** | `Deployable` | Equipamento formatado, homologado e disponível na Reserva Técnica da UD/Sede. |
| **Em Uso (Alocado)** | `Deployable` | Equipamento em posse de um colaborador ou associado a uma sala/laboratório. |
| **Em Aquisição / Trânsito** | `Pending` | Comprado ou em transferência entre UDs; aguardando tombamento e emplaquetamento. |
| **Em Preparação (Staging)** | `Pending` | Recebido na TI; instalando imagem homologada e agentes de segurança. |
| **Em Assistência / Manutenção** | `Undeployable` | Em reparo técnico (garantia do fabricante ou manutenção local). |
| **Aguardando Descarte (Baixa)** | `Undeployable` | Equipamento obsoleto/danificado; desativado aguardando laudo patrimonial. |
| **Descartado / Sanitizado** | `Archived` | Fim do ciclo de vida; baixado contabilmente e enviado para descarte ecológico com certificado. |

### Etiquetagem e Barcode / QR Code
- Todos os ativos recebem **QR Codes** padronizados impressos diretamente via Snipe-IT em impressoras térmicas (ex: Zebra/Dymo) nas 43 UDs.
- O QR Code contém a URL direta do ativo no Snipe-IT, permitindo que técnicos escaneiem a etiqueta com leitores corporativos ou aplicativos móveis para abrir a ficha do equipamento em segundos.

---

## 5.2 Software Asset Management (SAM)

O Snipe-IT possui um módulo dedicado para a gestão de **Licenças (Licenses)**:

### Funcionalidades do SAM no Snipe-IT
- **Controle de Assentos (Seats):** Registro da quantidade total de licenças adquiridas e distribuição individualizada para usuários ou ativos.
- **Licenciamento por Unidade (UD):** Licenças adquiridas por uma UD específica ficam restritas à sua alocação local; licenças corporativas compradas pela Sede são compartilhadas entre UDs.
- **Softwares Científicos de Alto Valor:** Monitoramento estrito de licenças de softwares como ArcGIS, MATLAB, SAS e SPSS. Identificação de assentos alocados a usuários inativos para imediata **recolheita (*License Harvesting*)**.
- **Alertas de Expiração:** Notificações automáticas por e-mail enviadas 90, 60 e 30 dias antes do vencimento de licenças temporárias ou subscrições SaaS.

---

## 5.3 Cloud Asset Management (Cloud / FinOps)

Embora o Snipe-IT seja focado no inventário de ativos físicos e lógicos, o gerenciamento de ativos Cloud no Snipe-IT será modelado da seguinte forma:
- **Categorias Especializadas:** `Serviço Cloud (IaaS/PaaS)` e `API Comercial / SaaS`.
- **Campos Customizados (Custom Fields):** ID do Tenant/Conta Cloud, Provedor (AWS/Azure/GCP), Centro de Custo da UD/Projeto de Pesquisa, Budget Mensal Alocado e URL da Console de Gestão Financeira.
- **Integração via Webhook / API:** Scripts automatizados atualizam o custo acumulado mensal e alertam se o gasto ultrapassar o orçamento aprovado para o projeto de pesquisa da UD.

---

## 5.4 IT Contract Management (ITCM)

No Snipe-IT, o pilar contratual é sustentado através do módulo de **Suppliers (Fornecedores)** e da associação de dados financeiros/contratuais nos formulários de ativos:
- **Gestão de Fornecedores:** Cadastro unificado de fabricantes e revendas com contatos, e-mails de suporte e número de contratos SEI.
- **Controle de Garantias:** O Snipe-IT calcula automaticamente a data de término da garantia com base na data de compra e meses de garantia cadastrados, gerando alertas de iminente expiração.
- **Vinculação de Arquivos Contratuais:** Upload de Notas Fiscais, Termos de Garantia e Contratos em PDF diretamente na ficha do ativo no Snipe-IT.

---

# 6. FLUXO DE ACEITE DIGITAL DO TERMO DE RESPONSABILIDADE (EULA NATIVO)

Um dos maiores diferenciais do Snipe-IT para a Embrapa é o fluxo **nativo de aceite eletrônico**, eliminando o papel e integrações complexas de assinatura:

```
[1. TI da UD realiza o Checkout do Ativo para o Colaborador no Snipe-IT]
                                   │
                                   ▼
[2. Snipe-IT envia e-mail automático com o Termo de Responsabilidade (EULA)]
                                   │
                                   ▼
[3. Colaborador clica no link seguro, lê as cláusulas e assina digitalmente]
                                   │
                                   ▼
[4. Snipe-IT registra o Aceite com Timestamp, IP e Assinatura Visual]
                                   │
                                   ▼
[5. Status do Ativo muda para "Em Uso" com Audit Log inalterável]
```

- **Validade Jurídica e Rastreabilidade:** O registro grava a data/hora exata, endereço IP do dispositivo e a confirmação do usuário autenticado no Active Directory.
- **Régua de Cobrança Automática:** Caso o colaborador não aceite o termo em até 48 horas, o Snipe-IT envia lembretes automáticos por e-mail e alerta o gestor de TI da UD.

---

# 7. PAPÉIS E RESPONSABILIDADES (MATRIZ RACI)

A governança do ITAM com o Snipe-IT divide responsabilidades entre a Sede (Governança Central) e as 43 Unidades Descentralizadas (Operação Local):

- **R (Responsible):** Quem executa a atividade.
- **A (Accountable):** Quem responde pela autoridade final da atividade.
- **C (Consulted):** Quem é consultado.
- **I (Informed):** Quem é informado.

| Atividade do Processo ITAM | Governança TI (Sede) | Admin TI (UD) | Compras / Contratos | Patrimônio / Controladoria | Usuário Final |
| --- | --- | --- | --- | --- | --- |
| Definir Diretrizes e Taxonomia no Snipe-IT | **A** / **R** | **C** | **C** | **C** | **I** |
| Manutenção do Cluster Snipe-IT e Integrações | **A** / **R** | **I** | **I** | **I** | **I** |
| Tombamento e Emplaquetamento (QR Code) na UD | **I** | **R** | **I** | **A** | **I** |
| Cadastro de Ativos e Notas Fiscais no Snipe-IT | **I** | **R** | **C** | **A** | **I** |
| Checkout de Ativos e Coleta do Aceite Digital | **I** | **R** | **I** | **I** | **A** / **Accept** |
| Executar Inventários Periódicos por QR Code na UD | **A** | **R** | **I** | **C** | **C** |
| Recolheita de Licenças de Software Ociosas (SAM) | **A** | **R** | **C** | **I** | **I** |
| Emissão de Laudo e Processo de Descarte de Bens | **C** | **R** | **I** | **A** | **I** |

---

# 8. DICIONÁRIO DE DADOS E CUSTOM FIELDS NO SNIPE-IT

Para garantir a padronização das 43 UDs, a Sede definirá **Custom Fieldsets** (Conjuntos de Campos Customizados) obrigatórios no Snipe-IT:

### Fieldset 1: Endpoints (Notebooks / Desktops / Workstations)
- **Número do Processo SEI:** Texto Curto (Mandatório)
- **Número do Pedido / Nota Fiscal:** Texto Curto (Mandatório)
- **Centro de Custo / Projeto:** Dropdown Unidades/Projetos Embrapa (Mandatório)
- **Endereço MAC da Placa Principal:** Regex MAC (Mandatório)
- **HostName / Nome na Rede:** Texto Curto (Mandatório)
- **Criticidade do Equipamento:** Dropdown `[Baixa, Média, Alta, Crítica]` (Mandatório)

### Fieldset 2: Servidores e Infraestrutura de Data Center
- **Endereço IP Gerenciamento / Out-of-Band (iDRAC/iLO):** IP Address (Mandatório)
- **Unidade de Rack / Posição:** Texto Curto (Mandatório)
- **Ambiente:** Dropdown `[Produção, Homologação, Desenvolvimento, Testes]` (Mandatório)
- **Grupo Técnico Responsável:** Dropdown `[Redes, Servidores, DBA, Segurança]` (Mandatório)

### Fieldset 3: Softwares Científicos & Licenças
- **Modalidade de Licenciamento:** Dropdown `[Por Usuário, Por Máquina, Concorrente, Projeto]` (Mandatório)
- **Código do Contrato de Licenciamento:** Texto Curto (Mandatório)
- **Projeto de Pesquisa Vinculado:** Texto Curto (Condicional)

---

# 9. ARQUITETURA DE INTEGRAÇÕES DO SNIPE-IT

O Snipe-IT será o coração da gestão de ativos, comunicando-se com a infraestrutura corporativa da Embrapa via APIs REST e protocolos nativos:

```
+-------------------------------------------------------------------+
|                     SNIPE-IT ENTERPRISE ITAM                      |
|                  (Source of Truth Administrativo)                 |
+-------------------------------------------------------------------+
   ▲                 ▲                   ▲                 ▲
   │                 │                   │                 │
   │ (LDAP Sync)     │ (REST API)        │ (API Token)     │ (Webhooks/API)
   │                 │                   │                 │
+--+----------+   +--+---------------+ +-+---------------+ +-+---------------+
| Active      |   | Agentes de       | | ITSM / Service  | | Provedores Cloud|
| Directory / |   | Descoberta       | | Desk (TOPdesk/  | | (AWS, Azure,    |
| Entra ID    |   | (OCS/Lansweeper/ | | GLPI/Jira)    | | GCP Cost APIs)  |
| Embrapa     |   | Intune/Script)   | |               | |                 |
+-------------+   +------------------+ +-----------------+ +-----------------+
```

1. **Sincronização Nativa AD/LDAP:**
   - Sincroniza periodicamente todos os colaboradores das 43 UDs com o Snipe-IT.
   - Sincroniza campos de E-mail, Matrícula, Departamento e Lotação (UD).
   - Usuários inativados no AD têm seus ativos sinalizados automaticamente para recolhimento.
2. **Integração com Ferramentas de Descoberta (Discovery):**
   - Agentes leves ou scripts (PowerShell/Bash) alimentam o Snipe-IT via **REST API** com dados atualizados de hardware (RAM real, CPU, HD, versão de SO e softwares instalados).
3. **Integração com Sistema de ITSM / Chamados (TOPdesk / GLPI / Jira Service Management):**
   - Ao abrir um chamado de suporte ou incidente na ferramenta de ITSM, o analista consulta a API do Snipe-IT pelo Asset Tag/Patrimônio ou e-mail do usuário para associar o ativo ao ticket.
   - Facilita a identificação de equipamentos problemáticos ("limões") em qualquer UD.

---

# 10. PLANO DE PROJETO E ROLLOUT EM ONDAS REGIONAIS

Considerando a extensão territorial da Embrapa (Sede + 43 UDs), a implantação será executada em **4 Fases ao longo de 12 Meses**:

```
[ Fase 1: Infra & Pilotagem ] ──> [ Fase 2: Onda 1 - Sul/Sudeste ] ──> [ Fase 3: Onda 2 - Centro-Oeste/NE ] ──> [ Fase 4: Onda 3 - Norte & SAM ]
      (Meses 1 a 2)                    (Meses 3 a 5)                       (Meses 6 a 8)                         (Meses 9 a 12)
```

### Fase 1: Fundação, Infraestrutura e Piloto (Meses 1 - 2)
- **Instalação da Infraestrutura:** Implantação do cluster Snipe-IT em alta disponibilidade (Docker/Kubernetes + MySQL HA + Backup).
- **Configuração de Governança:** Cadastro das 44 "Companies" (Sede + 43 UDs), custom fieldsets, status labels e permissões.
- **Integração AD/LDAP:** Sincronização inicial da base corporativa de pessoas.
- **Projeto Piloto:** Homologação na **Sede (DF)** e em **3 UDs Piloto** (ex: Embrapa Cerrados/DF, Embrapa Soja/PR e Embrapa Informática Agropecuária/SP).

### Fase 2: Rollout Regional - Onda 1 (Meses 3 - 5)
- Capacitação dos Pontos Focais de TI das UDs das regiões **Sul e Sudeste** (14 UDs).
- Carga de dados legados do patrimônio (SIAFI/SEI) e emplaquetamento QR Code nas UDs da Onda 1.
- Ativação do aceite digital EULA para novos checkouts.

### Fase 3: Rollout Regional - Onda 2 (Meses 6 - 8)
- Capacitação dos Pontos Focais de TI das UDs das regiões **Centro-Oeste e Nordeste** (16 UDs).
- Execução de inventários por amostragem via leitores móveis/QR Code.
- Integração da API do Snipe-IT com a ferramenta de Chamados/ITSM.

### Fase 4: Rollout Regional - Onda 3 & Consolidação SAM/Cloud (Meses 9 - 12)
- Capacitação dos Pontos Focais de TI das UDs da região **Norte** (13 UDs).
- Consolidação do pilar **SAM (Licenciamento Científico e Corporativo)** em todas as 44 unidades.
- Implantação dos painéis executivos de FinOps e KPIs corporativos no PowerBI/Metabase conectados ao Snipe-IT.

---

# 11. AUDITORIAS PERIÓDICAS E QUALIDADE DOS DADOS

O Snipe-IT possui uma funcionalidade nativa de **Audit Scheduling** (Agendamento de Auditorias):
- **Auditoria semestral obrigatória:** Cada UD receberá notificações automáticas pelo Snipe-IT para realizar a varredura física de amostras de ativos (10% a 20% do parque local a cada trimestre).
- **Relatório de Divergências:** Ativos não encontrados durante a varredura de auditoria têm seu status alterado para "Aguardando Localização" e disparam alerta imediato para a Chefia de Administração da UD.

---

# 12. INDICADORES DE DESEMPENHO (KPIS)

Para reporte à Diretoria Executiva da Embrapa, serão acompanhados os seguintes KPIs extraídos do Snipe-IT:

1. **Taxa de Cobertura de Inventário:**
   $$\text{TCI} = \left( \frac{\text{Ativos auditados/detectados com QR Code}}{\text{Total de ativos cadastrados patrimonialmente}} \right) \times 100$$
   *Meta:* $> 98\%$ em todas as 43 UDs.

2. **Índice de Aceite Digital do Termo (EULA):**
   $$\text{IAD} = \left( \frac{\text{Termos de Responsabilidade Assinados Digitalmente}}{\text{Total de Ativos em Posse de Colaboradores}} \right) \times 100$$
   *Meta:* $100\%$ em até 5 dias úteis após o checkout.

3. **Taxa de Reaproveitamento de Licenças (SAM - License Harvesting):**
   - Quantidade de licenças científicas/corporativas recuperadas de usuários inativos ou ociosos e alocadas para novas demandas de pesquisa.

4. **Índice de Equipamentos em Reserva Técnica (Ociosidade):**
   - Percentual de ativos no status "Pronto para Uso" parados por mais de 30 dias nas UDs (alerta para redistribuição entre UDs necessitadas).

---

# 13. CONSIDERAÇÕES FINAIS E PRÓXIMOS PASSOS

A implantação do programa de **Gestão de Ativos de TI (ITAM) na Embrapa utilizando o Snipe-IT** resolverá historicamente o desafio da gestão descentralizada entre a Sede e as 43 Unidades Descentralizadas.

Por ser uma solução dedicada, moderna, flexível e sem custos de licenciamento por ser *open-source*, o Snipe-IT proporcionará:
- Autonomia operacional para a TI de cada UD;
- Visibilidade executiva e auditabilidade centralizada para a Sede;
- Processo 100% digital com QR Codes e assinatura eletrônica de termos;
- Conformidade estrita com ITIL v4, ISO 19770 e LGPD.

**Aprovação Solicitada:** Aprovação desta Proposta Técnica para início imediato da Fase 1 (Infraestrutura do Cluster Snipe-IT, Integração AD/LDAP e Piloto na Sede + 3 UDs).
