# DIRETRIZES CORPORATIVAS E PROJETO DE IMPLANTAÇÃO DA GESTÃO DE ATIVOS DE TI (ITAM) COM SNIPE-IT

## Informações do Documento

| Campo | Informação |
| --- | --- |
| Documento | Diretrizes Corporativas e Projeto de Implantação de Gestão de Ativos de TI (ITAM) |
| Versão | 3.0 |
| Status | Proposta Técnica para Aprovação Executiva |
| Autor | André Luiz Bontempo / Especialista ITIL® 4 & Arquiteto ITAM |
| Área Responsável | Secretaria de Tecnologia da Informação / Governança de TI |
| Instituição | Embrapa (Empresa Brasileira de Pesquisa Agropecuária) |
| Abrangência | Sede (Brasília/DF) e 43 Unidades Descentralizadas (UDs) |
| Ferramenta | Snipe-IT (Open Source IT Asset Management Platform) |
| Data de Emissão | 08/07/2026 |
| Última Revisão | 30/07/2026 |
| Próxima Revisão | Julho / 2027 |
| Classificação | Uso Interno |
| Base Conceitual | ITIL® 4, ISO/IEC 19770, ISO 55000, ISO 27001, FinOps Foundation, LGPD, Documentação Oficial Snipe-IT |

---

## Histórico de Revisões

| Versão | Data | Autor | Descrição |
| --- | --- | --- | --- |
| 1.0 | 08/07/2026 | André Luiz Bontempo | Criação inicial do documento de diretrizes de ITAM. |
| 2.0 | 29/07/2026 | André Luiz Bontempo | Revisão conceitual dos pilares HAM, SAM, Cloud/FinOps e ITCM. |
| 3.0 | 30/07/2026 | André Luiz Bontempo / Antigravity | Reestruturação completa do projeto orientada à plataforma **Snipe-IT** e restrição estrita a **Ativos de TI**. Inclusão da arquitetura *Multi-Company* para Sede + 43 UDs, fluxo de aceite digital EULA, conciliação patrimonial (SIAFI/SEI), sanitização LGPD/Wiping, integração ITSM/CMDB, dicionário de dados expandido (nativos e customizados) e plano de rollout em ondas regionais. |

---

## Distribuição

Este documento destina-se às seguintes instâncias da Embrapa:

- Diretoria Executiva e Secretaria de TI (Sede)
- Comitê de Governança de TI, Segurança da Informação e Compliance
- Chefias de Administração e Pontos Focais de TI das 43 Unidades Descentralizadas (UDs)
- Equipes de Suporte, Infraestrutura, Compras, Contratos e Patrimônio
- Auditoria Interna e Controladoria Corporativa

---

## Referências Normativas e Tecnológicas

- **ITIL® 4 Practice Guides** – IT Asset Management & Service Configuration Management
- **ISO/IEC 19770-1** – IT Asset Management Systems: Requirements
- **ISO 55000 / 55001** – Asset Management: Overview, principles and terminology
- **ISO/IEC 27001** – Information Security Management Systems
- **NIST SP 800-88 Rev. 1** – Guidelines for Media Sanitization
- **Lei Geral de Proteção de Dados (LGPD)** – Lei nº 13.709/2018
- **FinOps Framework** – FinOps Foundation
- **Documentação Técnica Oficial Snipe-IT v6.x / v7.x** (REST API, Multi-Company Support, LDAP/AD Integration, EULA Signatures, Custom Fields)

---

# 1. INTRODUÇÃO E GOVERNANÇA (ITIL® 4)

A Gestão de Ativos de Tecnologia da Informação (*IT Asset Management* – ITAM) consiste no conjunto de processos, políticas, controles e automações destinados a gerenciar o ciclo de vida completo dos ativos tecnológicos da organização — desde o planejamento da aquisição até sua desativação, sanitização de dados e descarte ecológico final.

Na Embrapa, caracterizada por uma estrutura geográfica altamente distribuída constituída pela Sede em Brasília/DF e **43 Unidades Descentralizadas (UDs)** presentes em todos os biomas brasileiros, o gerenciamento de TI sem padronização centralizada gera riscos severos de conformidade legal, desbalanço patrimonial entre unidades e ineficiência orçamentária.

Esta diretriz estabelece a reestruturação corporativa do ITAM com foco exclusivo em **Ativos de Tecnologia da Informação**, utilizando a plataforma **Snipe-IT** como repositório único centralizador (*Single Source of Truth*). A solução permite garantir rastreabilidade, auditabilidade e governança nacional, preservando a agilidade operacional necessária ao cotidiano das 43 UDs.

## 1.1 Co-criação de Valor na Embrapa

Em alinhamento com a **ITIL® 4**, o programa ITAM é concebido sob a ótica da **Co-criação de Valor**. Os ativos de TI não são geridos meramente como bens patrimoniais estáticos, mas como habilitadores estratégicos diretamente associados às atividades finalísticas da Embrapa:

- **Pesquisa Agropecuária e Inovação:** Garantir que cientistas e pesquisadores em qualquer UD (ex: Embrapa Soja, Embrapa Amazônia Oriental, Embrapa Gado de Corte) disponham de notebooks de alta performance, estações de trabalho de processamento gráfico/genômico e softwares científicos (ArcGIS, MATLAB, SAS, SPSS) devidamente licenciados, atualizados e prontos para uso.
- **Eficiência Orçamentária e Reinvestimento em PD&I:** O controle rigoroso do ciclo de vida dos ativos evita compras duplicadas, equipamentos ociosos em estoque e subscrições de software/nuvem desnecessárias, liberando recursos orçamentários para investimento direto em projetos de Pesquisa, Desenvolvimento e Inovação.

## 1.2 As Quatro Dimensões da Gestão de Ativos de TI (ITAM)

Para assegurar uma abordagem holística e evitar falhas de implantação baseadas unicamente em software, o programa ITAM é estruturado sob as **Quatro Dimensões do Gerenciamento de Serviço da ITIL® 4**:

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
           |      - Cluster Snipe-IT em alta disponibilidade.      |
           |        Sincronização nativa AD/LDAP, leitura de       |
           |        QR Codes e APIs REST de descoberta automática. |
           |                                                       |
           |   3. Parceiros e Fornecedores                         |
           |      - Mapeamento de contratos de garantia, licenças, |
           |        suporte de fabricantes (Dell, HPE, Cisco)      |
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

O Programa Corporativo de Gestão de Ativos de TI possui como objetivos estratégicos:

1. **Repositório Único e Consolidado (*Single Source of Truth*):** Implantar o Snipe-IT como fonte única da verdade para todos os ativos de TI da Embrapa (Sede + 43 UDs).
2. **Arquitetura Multi-Unidade (*Multi-Company / Location*):** Configurar o Snipe-IT para oferecer visão executiva consolidada para a Sede e gestão segregada para cada uma das 43 UDs.
3. **Rastreabilidade e Aceite Digital Automático:** Utilizar o recurso nativo de **EULA / Digital Signature** do Snipe-IT para emissão e aceite eletrônico imediato do Termo de Responsabilidade por e-mail no momento da entrega do bem ao colaborador.
4. **Agilidade em Inventários com QR Code:** Padronizar a etiquetagem com QR Codes gerados pelo Snipe-IT, permitindo auditorias físicas ágeis por leitores móveis e smartphones.
5. **Mitigação de Riscos Legais e Fiscais (SAM):** Gerenciar licenças corporativas e científicas, prevenindo penalidades por sublicenciamento e eliminando custos com licenças ociosas (*License Harvesting*).
6. **Governança de Custos em Nuvem (FinOps):** Mapear ativos e recursos consumidos em nuvem pública (IaaS, PaaS e APIs), controlando orçamentos e emitindo alertas automatizados em caso de desvios orçamentários.
7. **Integração com Ferramentas de ITSM e Descoberta:** Conectar o Snipe-IT ao Active Directory corporativo, agentes de inventário automático e plataformas de chamados/ITSM via APIs REST.
8. **Sustentabilidade Tecnológica e Sanitização LGPD:** Assegurar a sanitização segura de mídias de dados (NIST SP 800-88) e o descarte ecologicamente correto com certificação ambiental.

---

# 3. ESCOPO CORPORATIVO EXCLUSIVO DE TI

O escopo do programa contempla **exclusivamente ativos de Tecnologia da Informação**, independentemente de sua forma de aquisição, contratação ou modelo de alocação. Ativos patrimoniais não-TI (mobiliário, veículos, ferramentas agrícolas ou infraestrutura predial geral) ficam expressamente fora deste escopo.

Os ativos de TI dividem-se nas seguintes categorias dentro do Snipe-IT:

### 3.1 Hardware de TI (Assets / Ativos Patrimoniais)
Equipamentos físicos tangíveis de computação e conectividade:
- **User Endpoints:** Notebooks, Desktops, Workstations de Pesquisa, Tablets, Smartphones corporativos.
- **Infraestrutura de Rede e Data Center:** Servidores físicos, Storages, Appliances de Segurança, Switches Core/Acesso, Roteadores, Firewalls, Access Points, Nobreaks de Rack/Data Center.
- **Equipamentos Científicos Tecnológicos de TI:** Clusters de alta performance (HPC), receptores GNSS/RTK de precisão agrícola, servidores de campo e estações de sensoriamento remoto.

### 3.2 Componentes e Acessórios de TI (Components & Accessories)
Itens lógicos e físicos integrados a equipamentos ou distribuídos como periféricos:
- **Componentes:** Pentes de memória RAM, SSDs/HDDs internos, Placas de Vídeo/GPU, Placas de Rede alocadas ou substituídas em servidores e workstations.
- **Acessórios:** Monitores adicionais, Docking Stations, Teclados, Mouses, Nobreaks individuais de bancada, Adaptadores e Leitores de campo.

### 3.3 Licenças de Software (Licenses - SAM)
Licenças de software locais (*On-Premise*) e subscrições SaaS:
- **Softwares Corporativos:** Sistemas Operacionais de servidores e estações, Suítes de Produtividade (Microsoft 365, Google Workspace), Antivírus/EDR, Bancos de Dados.
- **Softwares de Pesquisa Agropecuária (Especializados):** Softwares de alto valor monetário e especialidade técnica voltados para biotecnologia, genética, estatística e geomapeamento (ArcGIS/ArcMap, MATLAB, SAS, SPSS, softwares de sequenciamento genômico).

### 3.4 Serviços em Nuvem & FinOps (Cloud Assets)
Serviços contratados em modelos de consumo ou utilidade:
- Infraestrutura como Serviço (IaaS), Plataforma como Serviço (PaaS), Bancos de Dados gerenciados e consumo de APIs comerciais de Inteligência Artificial (OpenAI, Gemini, Anthropic).

### 3.5 Contratos e Garantias de TI (ITCM & Suppliers)
Instrumentos contratuais e garantias vinculados aos ativos tecnológicos:
- Termos de garantia estendida de fabricantes (Dell ProSupport, HPE Care Pack, Cisco SMARTnet), contratos de manutenção de hardware/software, acordos de nível de serviço (SLA) e contratos de suporte especializado.

---

# 4. ARQUITETURA ORGANIZACIONAL (SEDE + 43 UNIDADES DESCENTRALIZADAS)

Para atender à amplitude geográfica da Embrapa, o Snipe-IT será configurado utilizando a funcionalidade de **Multi-Company Support** (`full_multiple_companies_support = true`) combinada com a estrutura hierárquica de **Locations** (Localizações).

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

1. **Empresas/Unidades (*Companies*):**
   - Cada UD é cadastrada como uma entidade ("Company") no Snipe-IT (ex: `Embrapa Sede`, `Embrapa Soja`, `Embrapa Gado de Corte`, `Embrapa Amazônia Oriental`).
   - A configuração garante que os administradores de TI de uma UD visualizem e gerenciem exclusivamente os ativos pertencentes à sua própria unidade.
2. **Localizações Físicas (*Locations & Child Locations*):**
   - Dentro de cada UD, são estruturadas localizações filhas (ex: `Embrapa Soja -> Bloco de Laboratórios -> Lab Biotecnologia 02` ou `Embrapa Sede -> Data Center -> Rack A04`).
3. **Perfis de Acesso (*User Groups & Roles*):**
   - **Super Admin (Sede):** Equipe de Governança de TI Central. Acesso global a todas as 44 entidades, relatórios consolidados e auditorias nacionais.
   - **Admin de TI da UD:** Responsável técnico da Unidade Descentralizada. Gerencia cadastros, check-in/check-out e inventários locais da sua UD.
   - **Técnico de Suporte UD:** Realiza movimentações operacionais, atribuição a colaboradores e leitura de QR Codes.
   - **Auditores Internos / Patrimônio:** Acesso somente leitura para emissão de relatórios patrimoniais e de conformidade fiscal.
   - **Usuários Finais (Visão Self-Service):** Colaboradores de qualquer UD visualizam apenas os ativos atribuídos à sua guarda e efetuam o aceite digital dos Termos de Responsabilidade.

## 4.2 Protocolo de Transferência de Ativos entre Unidades Descentralizadas (Multi-Company Transfer)

A movimentação física ou lógica de um ativo de TI entre UDs (ex: transferência de uma workstation de alta performance da `Embrapa Soja` para a `Embrapa Amazônia Oriental`) obedece ao seguinte protocolo padronizado:

```
[1. Aprovação SEI] ──> [2. Checkout para Trânsito] ──> [3. Alteração da Company] ──> [4. Aceite e Recebimento]
```

1. **Formalização no SEI:** A transferência patrimonial é formalmente aprovada no Sistema Eletrônico de Informações (SEI) pelas Chefias de Administração das UDs envolvidas.
2. **Checkout de Trânsito no Snipe-IT:** A TI da UD de origem altera o status do ativo no Snipe-IT para `Em Aquisição / Trânsito` e atribui a localização temporária `Em Trânsito Inter-UDs`.
3. **Alteração da Entidade (*Company*):** O Admin de TI da UD de origem (ou Super Admin da Sede) altera o campo *Company* do ativo no Snipe-IT para a UD de destino.
4. **Aceite e Recebimento Técnico:** Ao receber o equipamento, a TI da UD de destino valida o estado físico, altera o status para `Pronto para Uso (Estoque)` ou `Em Uso`, atualiza a localização física local (*Location*) e aciona o fluxo de Aceite Digital (EULA) para o novo responsável final.

---

# 5. DETALHAMENTO DOS PILARES ITAM NO SNIPE-IT

O programa corporativo de ITAM é sustentado por quatro pilares operacionais complementares, todos consolidados na plataforma Snipe-IT.

```
                      +---------------------------------------+
                      |       PROGRAMA CORPORATIVO ITAM       |
                      +---------------------------------------+
                                          │
        +--------------------+------------+------------+--------------------+
        |                    |                         |                    |
        ▼                    ▼                         ▼                    ▼
+---------------+    +---------------+         +---------------+    +---------------+
|   1. HAM      |    |   2. SAM      |         |  3. CLOUD /   |    |   4. ITCM     |
|  (Hardware)   |    |  (Software)   |         |    FINOPS     |    |  (Contratos)  |
+---------------+    +---------------+         +---------------+    +---------------+
        |                    |                         |                    |
        +--------------------+------------+------------+--------------------+
                                          │
                                          ▼
                      +---------------------------------------+
                      |  SNIPE-IT ENTERPRISE ASSET DATABASE   |
                      +---------------------------------------+
```

---

## 5.1 Hardware Asset Management (HAM)

**Objetivo:** Gerenciar o ciclo de vida completo dos equipamentos físicos de TI, garantindo controle patrimonial, rastreabilidade de custódia, localização precisa e planejamento de renovação tecnológica (*Hardware Refresh*).

### Mapeamento de Status Labels (Estados do Ciclo de Vida no Snipe-IT)
O Snipe-IT utiliza *Status Labels* customizados vinculados a quatro meta-status nativos:

| Status Label no Snipe-IT | Meta-Status Nativo | Significado Operacional na Embrapa |
| --- | --- | --- |
| **Pronto para Uso (Estoque)** | `Deployable` | Equipamento formatado, homologado e disponível na Reserva Técnica da UD/Sede. |
| **Em Uso (Alocado)** | `Deployable` | Equipamento em posse de um colaborador ou associado a um laboratório/sala. |
| **Em Aquisição / Trânsito** | `Pending` | Comprado ou em transferência inter-UDs; aguardando tombamento e recebimento. |
| **Em Preparação (Staging)** | `Pending` | Recebido na TI; instalando imagem homologada e agentes de segurança. |
| **Em Assistência / Manutenção** | `Undeployable` | Em reparo técnico (garantia do fabricante ou manutenção local). |
| **Aguardando Descarte (Baixa)** | `Undeployable` | Equipamento obsoleto/danificado; desativado aguardando laudo e sanitização. |
| **Descartado / Sanitizado** | `Archived` | Fim da vida útil; sanitizado (wiping), baixado contabilmente e enviado a descarte ecológico. |

### Etiquetagem e Barcode / QR Code
- Todos os ativos recebem **QR Codes** padronizados impressos via Snipe-IT em impressoras térmicas (ex: Zebra/Dymo) nas 43 UDs.
- O QR Code armazena a URL direta do ativo no Snipe-IT. Técnicos de TI e auditores realizam a leitura utilizando aplicativos móveis ou leitores corporativos, abrindo a ficha do equipamento em segundos.

### Sanitização de Dados (LGPD) e Descarte Ecológico (Wiping & Logística Reversa)
Para garantir conformidade estrita com a **LGPD (Lei nº 13.709/2018)** e a ISO/IEC 27001:
- **Sanitização de Mídias (*Wiping*):** Nenhuma mídia de armazenamento (HDD, SSD, NVMe, Fita) pode ser descartada ou baixada sem sanitização prévia padronizada pelas normas **NIST SP 800-88 Rev. 1** ou **DoD 5220.22-M**.
- **Laudo Técnico de Sanitização:** É obrigatório realizar o upload do laudo em PDF (gerado pela ferramenta de *wiping*) na aba de anexos do ativo no Snipe-IT antes da alteração para o status `Aguardando Descarte`.
- **Certificado de Destruição Ecológica:** Equipamentos destinados a descarte final exigem o anexo do Certificado de Destruição/Reciclagem emitido por empresa homologada em logística reversa ambiental para a efetiva transição do ativo para o meta-status `Descartado / Sanitizado (Archived)`.

---

## 5.2 Software Asset Management (SAM)

**Objetivo:** Controlar e otimizar softwares baseados em licenças locais ou subscrições SaaS. Destina-se a mitigar os riscos de sublicenciamento (penalidades em auditorias) e evitar custos com superlicenciamento (licenças ociosas).

### Funcionalidades do Módulo *Licenses* no Snipe-IT
- **Controle de Assentos (*Seats*):** Registro exato do total de licenças adquiridas e distribuição individualizada para colaboradores ou ativos.
- **Licenciamento por Unidade (UD):** Licenças adquiridas por uma UD específica ficam restritas à alocação local; licenças corporativas compradas pela Sede são compartilhadas entre UDs.
- **Softwares Científicos de Alto Valor:** Monitoramento rigoroso de softwares como ArcGIS, MATLAB, SAS e SPSS. Identificação automática de assentos alocados a colaboradores inativos ou desligados para imediata **recolheita (*License Harvesting*)**.
- **Alertas de Expiração:** Notificações automáticas por e-mail enviadas 90, 60 e 30 dias antes do vencimento de licenças temporárias ou subscrições SaaS.

---

## 5.3 Cloud Asset Management (Cloud / FinOps)

**Objetivo:** Monitorar e governar ativos e recursos consumidos sob demanda em ambientes de nuvem pública (IaaS, PaaS e APIs comerciais). Atua sob a disciplina **FinOps** para garantir previsibilidade financeira e eliminação de desperdícios.

### Modelagem no Snipe-IT
- **Categorias Especializadas:** `Serviço Cloud (IaaS/PaaS)` e `API Comercial / SaaS`.
- **Campos Customizados (*Custom Fields*):** ID do Tenant/Conta Cloud, Provedor (AWS/Azure/GCP), Centro de Custo da UD/Projeto de Pesquisa, Orçamento Mensal Alocado (Budget) e URL da Console Financeira.
- **Integração via Webhook / API:** Scripts automatizados atualizam mensalmente o custo consolidado no Snipe-IT. Se o gasto ultrapassar o orçamento aprovado para o projeto, um Webhook dispara um alerta automático para a fila de suporte de infraestrutura para análise de arquitetura ou redimensionamento (*rightsizing*).

---

## 5.4 IT Contract Management (ITCM & Suppliers)

**Objetivo:** Gerenciar o ciclo de vida administrativo e financeiro dos contratos de garantia, suporte e manutenção de TI, vinculando o instrumento contratual diretamente aos ativos amparados.

### Modelagem no Snipe-IT
- **Módulo *Suppliers* (Fornecedores):** Cadastro unificado de fabricantes e revendas com CNPJ, contatos técnicos, e-mails de suporte e número do processo SEI originário.
- **Controle de Garantias:** O Snipe-IT calcula automaticamente a data de expiração da garantia com base na data de compra e meses de garantia informados, emitindo alertas preventivos.
- **Vinculação de Documentos:** Upload de Notas Fiscais, Termos de Garantia e Contratos em PDF diretamente na ficha do ativo no Snipe-IT.
- **Régua de Alertas Contratuais:** Notificações automáticas para Compras e TI disparadas com **120, 90, 60 e 30 dias** de antecedência do vencimento de contratos ou termos de manutenção.

---

# 6. FLUXO DE ACEITE DIGITAL DO TERMO DE RESPONSABILIDADE (EULA NATIVO)

Um dos principais diferenciais do Snipe-IT é o seu **fluxo nativo de aceite eletrônico**, que elimina a necessidade de impressões em papel e integrações com sistemas externos de assinatura:

```
[1. TI realiza o Checkout do Ativo para o Colaborador no Snipe-IT]
                                   │
                                   ▼
[2. Snipe-IT envia e-mail automático com o Termo de Responsabilidade (EULA)]
                                   │
                                   ▼
[3. Colaborador clica no link seguro, lê as cláusulas e assina digitalmente]
                                   │
                                   ▼
[4. Snipe-IT grava o Aceite com Timestamp, IP e Assinatura Visual]
                                   │
                                   ▼
[5. Status do Ativo muda para "Em Uso" com Audit Log inalterável]
```

### Regras do Processo de Aceite Digital:
- **Validade Jurídica e Auditabilidade:** O Snipe-IT registra no banco de dados a data/hora exata, o endereço IP do dispositivo do colaborador e a assinatura desenhada/confirmada.
- **Régua de Cobrança Automática:** Caso o colaborador não efetue o aceite em até **48 horas**, o Snipe-IT reenvia lembretes automáticos diários por e-mail e notifica o gestor imediato após 5 dias úteis.

---

# 7. INTEGRAÇÃO COM GERENCIAMENTO DE CONFIGURAÇÃO (CMDB VS. ITAM)

## 7.1 Diferenciação Conceitual: ITAM vs. CMDB

Para evitar duplicações e inconsistências operacionais, o programa estabelece uma clara linha de corte conceitual:

| Atributo | ITAM (Snipe-IT) | CMDB (Plataforma ITSM Corporativa) |
| --- | --- | --- |
| **Foco Principal** | Ciclo de vida administrativo, financeiro, contratual e patrimonial. | Estrutura operacional, dependências técnicas e serviços de TI. |
| **Unidade de Controle** | Ativo de TI (*Asset*) – Possui etiqueta, valor financeiro e responsável. | Item de Configuração (*CI*) – Componente de um serviço de TI. |
| **Pergunta-Chave** | *"Quanto custou, quem é o dono, onde está e qual a garantia?"* | *"Como está conectado e qual o impacto se falhar?"* |
| **Visão de Negócio** | Ênfase em Custos, Contratos, Auditoria, EULA e Licenciamento. | Ênfase em Operação, Incidentes, Mudanças e SLAs de Serviço. |

## 7.2 Integração Snipe-IT <-> CMDB / ITSM via API REST

O **Snipe-IT** atua como a **Fonte Única da Verdade para ITAM**. A topologia de serviços e dependências operacionais (CMDB) permanece na ferramenta de ITSM corporativa (ex: TOPdesk, GLPI ou Jira Service Management), integrada ao Snipe-IT via **API REST**:

```
+------------------------------------+             +------------------------------------+
|         SNIPE-IT ENTERPRISE        |  REST API   |      PLATAFORMA ITSM / CMDB        |
|  (Source of Truth Administrativo)  | ◄─────────► |   (Gestão de Chamados e Serviços)  |
+------------------------------------+             +------------------------------------+
| - Patrimônio / Asset Tag (QR Code) |             | - Vinculação em Ticket Incidente   |
| - Custódia / Aceite Digital EULA   |             | - Árvore de Dependência de Serviço |
| - Nota Fiscal, Garantia e Contrato |             | - Análise de Impacto de Mudanças   |
| - Assentos de Licenças (SAM)       |             | - Base de Conhecimento Sugerida    |
+------------------------------------+             +------------------------------------+
```

### Benefícios Operacionais da Integração:
- **Vinculação Obrigatória em Incidentes:** Ao abrir um chamado de suporte, a ferramenta de ITSM consulta o Snipe-IT via API pelo Asset Tag ou e-mail do usuário para associar o ativo exato ao ticket.
- **Identificação de Equipamentos Problemáticos ("Limões"):** O histórico de incidentes associado ao Asset Tag do Snipe-IT permite identificar equipamentos com alta taxa de falhas, acelerando a decisão de manutenção corretiva ou substituição antecipada (*Hardware Refresh*).
- **Análise de Impacto em Mudanças (Change Management):** Antes de aprovar uma manutenção em infraestrutura, a árvore da CMDB exibe quais aplicações corporativas e serviços de pesquisa serão afetados, utilizando as especificações sincronizadas do Snipe-IT.

---

# 8. CICLO DE VIDA DOS ATIVOS DE TI

Todo ativo de TI controlado pelo programa deve percorrer obrigatoriamente as fases estabelecidas abaixo, com transição de status registrada no Snipe-IT:

```
[ Planejamento ] ──> [ Aquisição ] ──> [ Cadastro/Snipe-IT ] ──> [ Staging/Preparação ]
                                                                       │
                                                                       ▼
  [ Descarte/Wiping ] <── [ Encerramento ] <── [ Manutenção ] <── [ Operação (Em Uso) ]
```

1. **Planejamento:** Identificação da necessidade tecnológica e aprovação orçamentária.
2. **Aquisição:** Processamento da compra pela área de Compras/Suprimentos. Emissão da Nota Fiscal e Empenho.
3. **Cadastro no Snipe-IT:** Entrada do bem no inventário. Emplaquetamento com QR Code, amarração ao fornecedor, Nota Fiscal, garantia e `Company` (UD proprietária). Status inicial: `Em Aquisição / Trânsito (Pending)`.
4. **Staging / Preparação:** Homologação técnica pela equipe de TI. Instalação de imagem corporativa, agentes de segurança (EDR), inventário automático e ingressão no AD. Status: `Em Preparação (Pending)`.
5. **Operação:** Entrega ao colaborador com envio do e-mail de Aceite Digital (EULA). Após a assinatura, o status é alterado automaticamente para `Em Uso (Deployable)`.
6. **Manutenção:** Intervenções em garantia ou reparos locais. Status alterado para `Em Assistência / Manutenção (Undeployable)`.
7. **Renovação Tecnológica (*Refresh*):** Substituição programada baseada em obsolescência, fim de suporte do fabricante (*EOS*) ou degradação de performance.
8. **Encerramento e Descarte:** Sanitização obrigatória de mídias de dados (*wiping* NIST SP 800-88), upload do laudo técnico no Snipe-IT, baixa contábil no SIAFI e destinação para logística reversa ecológica com Certificado de Destruição. Status final: `Descartado / Sanitizado (Archived)`.

---

# 9. PROCESSOS OPERACIONAIS E ARQUITETURA DE INTEGRAÇÕES

O Snipe-IT operará como o núcleo do ecossistema de gestão de ativos da Embrapa, integrando-se via APIs e conectores nativos aos sistemas corporativos:

```
+-------------------------------------------------------------------+
|                     SNIPE-IT ENTERPRISE ITAM                      |
|                  (Source of Truth Administrativo)                 |
+-------------------------------------------------------------------+
   ▲                 ▲                   ▲                 ▲
   │                 │                   │                 │
   │ (LDAP Sync)     │ (REST API)        │ (API REST)      │ (Webhooks/API)
   │                 │                   │                 │
+--+----------+   +--+---------------+ +-+---------------+ +-+---------------+
| Active      |   | Agentes de       | | ITSM / Service  | | Provedores Cloud|
| Directory / |   | Descoberta       | | Desk (TOPdesk/  | | (AWS, Azure,    |
| Entra ID    |   | (Intune/OCS/     | | GLPI/Jira)    | | GCP Cost APIs)  |
| Embrapa     |   | Lansweeper)      | |               | |                 |
+-------------+   +------------------+ +-----------------+ +-----------------+
```

## 9.1 Sincronização Nativa AD/LDAP
- Sincroniza diariamente os colaboradores das 43 UDs e Sede com a base de pessoas do Snipe-IT.
- Atualiza campos de E-mail, Matrícula, Departamento e Lotação (UD).
- Colaboradores inativados no AD sinalizam automaticamente alerta para recolhimento dos ativos sob sua custódia.

## 9.2 Agentes de Descoberta Automática (*Discovery*)
- Agentes (Microsoft Intune, Lansweeper, OCS Inventory) atualizam dados técnicos via REST API no Snipe-IT (RAM real, processador, capacidade de disco, IP/MAC ativos e lista de softwares instalados).

## 9.3 Conciliação Físico-Contábil (SIAFI / SEI)
- O campo `Asset Tag` no Snipe-IT é obrigatoriamente espelhado como o **Número de Tombamento Patrimonial oficial**.
- Relatórios periódicos comparam a base do Snipe-IT com a contabilidade corporativa (SIAFI), identificando divergências ou baixas pendentes.

## 9.4 Regras de Conciliação de Dados (*Reconciliation Rules*)
Para impedir que ferramentas automáticas de descoberta sobrescrevam dados administrativos de governança, aplicam-se as seguintes regras:

| Categoria do Dado | Fonte Proprietária | Regra de Negócio na Divergência |
| --- | --- | --- |
| **Especificações Técnicas** (RAM, CPU, IP, MAC, Softwares instalados) | **Ferramenta de Discovery** (Intune/Lansweeper) | Atualização automática e substituição pelo dado técnico mais recente. |
| **Metadados de Governança** (Company, Location, Status, Nota Fiscal, Valor) | **TI / Compras (Manual no Snipe-IT)** | Bloqueado para gravação por Discovery. Alterável apenas por admins do Snipe-IT. |
| **Dados do Colaborador** (Nome, E-mail, Lotação, Cargo) | **Active Directory / Entra ID** | Sincronização diária sobrescrevendo dados cadastrais de pessoas. |

## 9.5 Diretriz de Segurança para Credenciais de Ativos
> [!CAUTION]
> **Proibição de Senhas no Snipe-IT:**
> É expressamente proibido armazenar senhas, chaves privadas ou segredos de acesso (senhas de iDRAC, iLO, root de switches ou BIOS) em qualquer campo do Snipe-IT.
> Os formulários de infraestrutura registrarão exclusivamente a URL/ID da credencial cadastrada no **Cofre de Senhas Corporativo** da Embrapa (ex: HashiCorp Vault / LAPS).

---

# 10. POLÍTICA DE QUALIDADE DOS DADOS, GESTÃO DE RISCOS E LGPD

## 10.1 Princípios de Qualidade da Informação
- **Completude:** Bloqueio de cadastros sem o preenchimento de campos obrigatórios nativos e customizados.
- **Precisão:** Os dados do Snipe-IT devem corresponder exatamente ao estado físico e lógico do equipamento.
- **Atualização:** Meta operacional de registrar movimentações físicas no Snipe-IT em até **24 horas úteis**.
- **Unicidade:** Garantia de chaves primárias únicas. Proibição de duplicidade de *Asset Tag* ou *Serial Number*.

---

## 10.2 Matriz de Gestão de Riscos

| Identificação do Risco | Impacto Estimado | Ação de Mitigação Proposta |
| --- | --- | --- |
| **Sublicenciamento de Software** | Penalidades financeiras elevadas em auditorias de fabricantes. | Conciliação mensal automatizada no módulo *Licenses* entre assentos comprados e instalados. |
| **Ativos Órfãos (Sem Custódia)** | Perda patrimonial e uso indevido de equipamentos corporativos. | Bloqueio de login na rede para endpoints sem usuário vinculado no Snipe-IT por mais de 15 dias. |
| **Desperdício Financeiro Cloud** | Estouro de orçamento operacional (*OPEX*) em nuvem. | Webhooks de alerta no Snipe-IT ao atingir 80% e 90% do budget alocado por projeto. |
| **Garantia Expirada em Servidores** | Indisponibilidade por falta de peças de reposição do fabricante. | Alertas contratuais automáticos disparados a partir de 120 dias antes do fim da garantia. |

---

## 10.3 Adequação à Lei Geral de Proteção de Dados (LGPD)
- **Retenção de Custódia:** O histórico de uso dos equipamentos é mantido por legítimo interesse e segurança da informação corporativa.
- **Restrição de Acesso:** O histórico de custódia anterior de um ativo é acessível apenas a perfil de Administrador e Segurança da Informação.
- **Anonimização no Descarte:** Ao enviar o ativo para o status `Descartado / Sanitizado (Archived)`, o processo desvincula a identificação do colaborador, mantendo apenas o log de auditoria técnica.

---

# 11. INDICADORES DE DESEMPENHO (KPIS)

Para avaliação executiva do programa, os seguintes KPIs serão monitorados continuamente via dashboards conectados ao Snipe-IT:

### 1. Taxa de Cobertura de Inventário (TCI)
$$\text{TCI} = \left( \frac{\text{Ativos auditados / detectados com QR Code}}{\text{Total de ativos cadastrados no ITAM}} \right) \times 100$$
- *Meta:* $> 98\%$ em todas as 43 UDs e Sede.

### 2. Taxa de Aceite Digital do Termo EULA (TAD)
$$\text{TAD} = \left( \frac{\text{Termos EULA Assinados Digitalmente}}{\text{Total de Ativos Atribuídos a Colaboradores}} \right) \times 100$$
- *Meta:* $100\%$ em até 5 dias úteis após o checkout.

### 3. Taxa de Ociosidade de Licenças (TOL - SAM)
$$\text{TOL} = \left( \frac{\text{Licenças Adquiridas} - \text{Licenças Efetivamente Utilizadas}}{\text{Total de Licenças Adquiridas}} \right) \times 100$$
- *Meta:* $< 5\%$ com rotinas de *License Harvesting*.

### 4. Desvio Orçamentário Cloud ($\Delta_{\text{Budget}}$)
$$\Delta_{\text{Budget}} = \text{Gasto Real Acumulado} - \text{Gasto Previsto (Budget)}$$
- *Meta:* $\Delta_{\text{Budget}} \le 0$ (sem estouro orçamentário).

---

# 12. MODELO DE MATURIDADE DO PROGRAMA ITAM

O amadurecimento das práticas de ITAM na Embrapa seguirá o escalonamento tático visando atingir o **Nível 4** em 18 meses:

```
[ Nível 1: Inicial ] ──> [ Nível 2: Gerenciado ] ──> [ Nível 3: Padronizado ] ──> [ Nível 4: Controlado ] ──> [ Nível 5: Otimizado ]
```

- **Nível 1 – Inicial:** Planilhas descentralizadas nas UDs, dados incompletos, sem rastreabilidade.
- **Nível 2 – Gerenciado:** Snipe-IT implantado, arquitetura Multi-Company ativa, aceite EULA obrigatório.
- **Nível 3 – Padronizado:** AD/LDAP integrado, etiquetagem QR Code padronizada nas 43 UDs, catálogo de softwares homologados.
- **Nível 4 – Controlado:** Agentes de descoberta integrados via API, conciliação SIAFI automática, governança FinOps e SAM consolidados.
- **Nível 5 – Otimizado:** Automação total de provisionamento, preditividade de *Hardware Refresh* e otimização contínua orientada a dados.

---

# 13. PLANO DE PROJETO E ROLLOUT EM ONDAS REGIONAIS

A implantação na Sede e nas 43 UDs será realizada em **4 Fases ao longo de 12 Meses**:

```
[ Fase 1: Infra & Pilotagem ] ──> [ Fase 2: Onda 1 - Sul/Sudeste ] ──> [ Fase 3: Onda 2 - CO/Nordeste ] ──> [ Fase 4: Onda 3 - Norte & SAM ]
      (Meses 1 a 2)                    (Meses 3 a 5)                      (Meses 6 a 8)                        (Meses 9 a 12)
```

- **Fase 1: Infraestrutura & Piloto (Meses 1-2):** Implantação do cluster Snipe-IT (Docker HA + MySQL), integração AD/LDAP e projeto piloto na Sede e 3 UDs Piloto (Embrapa Cerrados, Embrapa Soja e Embrapa Informática Agropecuária).
- **Fase 2: Onda 1 – Regiões Sul e Sudeste (Meses 3-5):** Capacitação dos Pontos Focais de TI e carga inicial de dados em 14 UDs.
- **Fase 3: Onda 2 – Regiões Centro-Oeste e Nordeste (Meses 6-8):** Rollout em 16 UDs e integração com a plataforma de Chamados/ITSM.
- **Fase 4: Onda 3 – Região Norte & Consolidação SAM/Cloud (Meses 9-12):** Rollout nas 13 UDs da Região Norte, consolidação das licenças científicas (SAM) e dashboards executivos.

---

# 14. FATORES CRÍTICOS DE SUCESSO E CONSIDERAÇÕES FINAIS

O sucesso da implantação do ITAM com o Snipe-IT na Embrapa depende de:
1. Compromisso da Alta Administração na cobrança da disciplina operacional do cadastro em todas as UDs;
2. Cumprimento rigoroso do fluxo de Aceite Digital EULA por 100% dos colaboradores;
3. Capacitação continuada dos Pontos Focais de TI nas 43 UDs.

A adoção do **Snipe-IT** como plataforma dedicada proporcionará à Embrapa governança centralizada na Sede, autonomia operacional nas 43 UDs e auditabilidade plena.

---

# APÊNDICE A – GLOSSÁRIO TÉCNICO

- **ITAM:** *IT Asset Management* (Gestão de Ativos de TI)
- **HAM:** *Hardware Asset Management* (Gestão de Ativos de Hardware)
- **SAM:** *Software Asset Management* (Gestão de Ativos de Software)
- **ITCM:** *IT Contract Management* (Gestão de Contratos de TI)
- **Snipe-IT:** Plataforma open-source dedicada à gestão de ativos de TI
- **EULA:** *End User License Agreement* (Termo de Responsabilidade e Aceite Digital)
- **Multi-Company:** Recursos do Snipe-IT para segregação de visibilidade e gestão por entidade/UD
- **CI:** *Configuration Item* (Item de Configuração em CMDB)
- **FinOps:** *Financial Operations* (Governança financeira de consumo em Nuvem)
- **Wiping:** Processo de sanitização lógica irreversível de mídias de dados (NIST SP 800-88)
- **UD:** Unidade Descentralizada da Embrapa

---

# APÊNDICE B – MATRIZ RACI DO PROCESSO ITAM

- **R (Responsible):** Quem executa a atividade.
- **A (Accountable):** Quem possui a autoridade e aprovação final.
- **C (Consulted):** Quem é consultado.
- **I (Informed):** Quem é informado.

| Atividade do Processo | Governança TI (Sede) | Admin TI (UD) | Compras / Contratos | Patrimônio / Controladoria | Colaborador / Usuário |
| --- | --- | --- | --- | --- | --- |
| Definir Diretrizes e Taxonomia no Snipe-IT | **A** / **R** | **C** | **C** | **C** | **I** |
| Manutenção da Infraestrutura do Snipe-IT | **A** / **R** | **I** | **I** | **I** | **I** |
| Tombamento e Emplaquetamento QR Code na UD | **I** | **R** | **I** | **A** | **I** |
| Cadastro de Ativos e Notas Fiscais no Snipe-IT | **I** | **R** | **C** | **A** | **I** |
| Checkout de Ativos e Coleta do Aceite Digital | **I** | **R** | **I** | **I** | **A** / **Accept** |
| Executar Inventários Periódicos por QR Code | **A** | **R** | **I** | **C** | **C** |
| Recolheita de Licenças Ociosas (SAM Harvesting) | **A** | **R** | **C** | **I** | **I** |
| Sanitização de Mídias (Wiping) e Descarte | **C** | **R** | **I** | **A** | **I** |

---

# APÊNDICE C – DICIONÁRIO DE DADOS E CAMPOS OBRIGATÓRIOS NO SNIPE-IT

Para garantir a auditabilidade nacional, o cadastro no Snipe-IT obedece à parametrização obrigatória descrita a seguir.

## C.1 Campos Nativos Globais Obrigatórios (Hardware Assets)

Estes campos são nativos do Snipe-IT e **obrigatórios para qualquer ativo de hardware**:

| Campo Native no Snipe-IT | Tipo de Dado / Formato | Regra de Preenchimento / Validação | Obrigatoriedade |
| --- | --- | --- | --- |
| **Asset Tag** | Texto Único | Número da Etiqueta / Tombamento Patrimonial Embrapa (QR Code). | **Obrigatório** |
| **Model (Modelo)** | Seleção / Objeto | Associa o fabricante, categoria, especificações e o *Custom Fieldset*. | **Obrigatório** |
| **Status Label** | Seleção / Status | Estado do Ciclo de Vida (`Em Uso`, `Pronto para Uso`, `Em Manutenção`, etc.). | **Obrigatório** |
| **Serial Number (Número de Série)** | Texto Curto | Número de série oficial do fabricante (Dell Service Tag, Lenovo S/N, Cisco S/N). | **Obrigatório** |
| **Company (Unidade Embrapa)** | Seleção / Multi-Company | Identifica a UD proprietária (`Embrapa Sede` ou uma das 43 UDs). | **Obrigatório** |
| **Location (Localização Física)** | Seleção Hierárquica | Edifício, Bloco, Sala ou Laboratório onde o bem está alocado. | **Obrigatório** |
| **Purchase Date (Data de Compra)** | Data (`YYYY-MM-DD`) | Data de emissão da Nota Fiscal de aquisição. | **Obrigatório** |
| **Purchase Cost (Valor de Aquisição)** | Monetário (`BRL R$`) | Valor nominal de compra constante na Nota Fiscal. | **Obrigatório** |
| **Supplier (Fornecedor)** | Seleção / Cadastro | Razão Social e CNPJ da empresa fornecedora contratada. | **Obrigatório** |
| **Order Number (Empenho / NF)** | Texto Curto | Número da Nota Fiscal e/ou Nota de Empenho vinculada. | **Obrigatório** |
| **Warranty (Garantia em Meses)** | Numérico Inteiro | Período de garantia em meses (ex: `36` ou `60` meses). | **Obrigatório** |
| **Assignee (Atribuído a)** | Seleção (Usuário/Local) | Usuário (Matrícula AD) ou Localização. **Obrigatório quando Status = "Em Uso"**. | **Condicional** |

---

## C.2 Campos Customizados Obrigatórios por Categoria (Custom Fieldsets)

### C.2.1 Fieldset 1: Endpoints (Notebooks, Desktops, Workstations)

| Campo Customizado | Tipo de Campo no Snipe-IT | Regra / Máscara de Validação | Obrigatoriedade |
| --- | --- | --- | --- |
| **Número do Processo SEI** | `Textbox` | Formato Padrão SEI (`00000.000000/0000-00`) | **Obrigatório** |
| **Número da Nota Fiscal (NF)** | `Textbox` | Numérico / Alfanumérico da NF | **Obrigatório** |
| **Centro de Custo / Projeto SEI** | `Dropdown` | Lista de Projetos e Centros de Custos Embrapa | **Obrigatório** |
| **HostName / Nome na Rede** | `Textbox` | Formato FQDN (`[HOSTNAME].embrapa.br`) | **Obrigatório** |
| **Endereço MAC Ethernet** | `Textbox` | Regex MAC Address (`^([0-9A-Fa-f]{2}[:-]){5}([0-9A-Fa-f]{2})$`) | **Obrigatório** |
| **Endereço MAC Wi-Fi** | `Textbox` | Regex MAC Address | **Obrigatório (se notebook/tablet)** |
| **Criticidade do Equipamento** | `Dropdown` | Valores: `[Baixa, Média, Alta, Crítica]` | **Obrigatório** |
| **Status Criptografia de Disco** | `Dropdown` | Valores: `[BitLocker Ativo, FileVault Ativo, Inativo, Não Suportado]` | **Obrigatório** |

### C.2.2 Fieldset 2: Dispositivos Móveis Corporativos (Smartphones e Tablets)

| Campo Customizado | Tipo de Campo no Snipe-IT | Regra / Máscara de Validação | Obrigatoriedade |
| --- | --- | --- | --- |
| **Número do Processo SEI** | `Textbox` | Formato Padrão SEI | **Obrigatório** |
| **IMEI 1 Principal** | `Textbox` | Regex IMEI (15 dígitos numéricos) | **Obrigatório** |
| **IMEI 2 Secundário** | `Textbox` | Regex IMEI (15 dígitos numéricos) | **Obrigatório (se Dual SIM)** |
| **Número da Linha Corporativa** | `Textbox` | Formato `+55 (XX) 9XXXX-XXXX` | **Obrigatório** |
| **Código do Chip SIM (ICCID)** | `Textbox` | Numérico (19-20 dígitos do chip) | **Obrigatório** |
| **MDM Enrollment Status** | `Dropdown` | Valores: `[Matriculado/Ativo, Inativo, Não Encontrado]` | **Obrigatório** |

### C.2.3 Fieldset 3: Servidores e Infraestrutura de Data Center

| Campo Customizado | Tipo de Campo no Snipe-IT | Regra / Máscara de Validação | Obrigatoriedade |
| --- | --- | --- | --- |
| **Número do Processo SEI** | `Textbox` | Formato Padrão SEI | **Obrigatório** |
| **IP Out-of-Band (iDRAC / iLO)** | `Textbox` | Formato IPv4 Validador | **Obrigatório** |
| **IP Principal de Produção** | `Textbox` | Formato IPv4 / IPv6 Validador | **Obrigatório** |
| **Localização em Rack & Elevação (U)** | `Textbox` | Exemplo: `Rack R-04 / Pos U12-U14` | **Obrigatório** |
| **Ambiente de Execução** | `Dropdown` | Valores: `[Produção, Homologação, Desenvolvimento, Treinamento]` | **Obrigatório** |
| **Grupo Técnico Responsável** | `Dropdown` | Valores: `[Suporte N3, Redes, DBAs, SysAdmins, Segurança, Cloud]` | **Obrigatório** |
| **ID no Cofre de Senhas Corporativo** | `Textbox / URL` | Referência/ID no Cofre Corporativo (Sem expor senhas) | **Obrigatório** |
| **Número do Contrato de Suporte 24/7** | `Textbox` | Código do Contrato de Suporte/SLA do Fabricante | **Obrigatório** |

### C.2.4 Fieldset 4: Equipamentos Científicos & Tecnológicos de Campo

| Campo Customizado | Tipo de Campo no Snipe-IT | Regra / Máscara de Validação | Obrigatoriedade |
| --- | --- | --- | --- |
| **Código do Projeto de Pesquisa (SEG)** | `Textbox` | Código de Projeto no Sistema SEG/Embrapa | **Obrigatório** |
| **Pesquisador Responsável Técnico** | `Textbox` | Nome e Matrícula do Pesquisador Líder | **Obrigatório** |
| **Ambiente de Operação Principal** | `Dropdown` | Valores: `[Laboratório Biossegurança, Campo Aberto, Casa de Vegetação, Embarcado]` | **Obrigatório** |
| **Registro Anatel / ANAC** | `Textbox` | Homologação para Drones, Rádios RTK e Sensores | **Obrigatório (se drone/rádio)** |
| **Código Fomento Externo (Finep/FAP)** | `Textbox` | Código do projeto de agência financiadora externa | **Condicional** |

### C.2.5 Módulo de Licenças de Software (SAM - Software Asset Management)

| Campo no Módulo Licenses | Tipo de Dado | Regra / Descrição do Preenchimento | Obrigatoriedade |
| --- | --- | --- | --- |
| **Software Name (Nome e Versão)** | Texto Curto | Nome oficial da aplicação e versão (ex: `ArcGIS Pro 3.2`, `MATLAB R2024a`). | **Obrigatório** |
| **Manufacturer (Fabricante)** | Seleção | Esri, MathWorks, Microsoft, SAS Institute, IBM, etc. | **Obrigatório** |
| **Seats (Quantidade de Assentos)** | Numérico | Número total de licenças/assentos contratados. | **Obrigatório** |
| **License Category (Categoria)** | Seleção | `Softwares Científicos`, `Sistemas Operacionais`, `Produtividade`, `Segurança`. | **Obrigatório** |
| **Product Key / Ativação** | Texto Protegido | Chave de licença corporativa ou método de ativação (KMS / Servidor FlexLM). | **Obrigatório** |
| **Modalidade de Licenciamento** | Custom Field | Valores: `[Perpétua, SaaS Anual, Por Core/CPU, Por Usuário, Concorrente]`. | **Obrigatório** |
| **Expiration Date (Vencimento)** | Data | Data de término da subscrição ou contrato de suporte (gera alertas automáticos). | **Obrigatório** |
| **Processo SEI / Contrato** | Custom Field | Número do Processo SEI de Contratação da Licença. | **Obrigatório** |
| **Escopo de Licenciamento** | Custom Field | Valores: `[Corporativo Sede, UD Específica, Projeto Científico Restrito]`. | **Obrigatório** |
