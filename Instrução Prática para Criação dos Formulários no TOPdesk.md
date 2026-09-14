# INSTRUÇÃO PRÁTICA PARA CRIAÇÃO DOS FORMULÁRIOS NO TOPDESK

## Informações do Documento

| Campo | Informação |
| --- | --- |
| Documento | Instrução Prática para Criação dos Formulários de Ativos no TOPdesk |
| Versão | 1.0 |
| Data | 14/09/2026 |
| Autor | André Luiz Bontempo / Especialista ITIL v4 & Arquiteto TOPdesk |
| Projeto | Implantação do IT Asset Management (ITAM) no TOPdesk |
| Ferramenta | TOPdesk Asset Management (Módulo Flexível de Ativos) |
| Instituição | Embrapa (Empresa Brasileira de Pesquisa Agropecuária) |

---

## 1. INTRODUÇÃO E OBJETIVO

Este documento estabelece o guia prático de parametrização dos formulários cadastrais dentro do módulo de **Asset Management (Módulo Flexível de Ativos)** do TOPdesk. 

A estrutura foi concebida para atender rigorosamente às diretrizes corporativas de governança de TI, ITIL® 4, ISO/IEC 19770 e LGPD, garantindo a padronização no cadastro de equipamentos de **Hardware (Desktop e Notebook)** e licenças de **Software (Pacote MS Office / Microsoft 365)**.

---

## 2. ESTRUTURA DE ABAS DE CADASTRO NO TOPDESK

Para garantir governança de dados e restrição de acesso por perfil, os formulários no TOPdesk devem ser organizados em **4 Abas de Cadastro**:

1. **Aba 1: Informações Gerais** (Visível a todos os atendentes do Service Desk)
2. **Aba 2: Especificações Técnicas & CMDB** (Editável por Suporte N1, N2 e Infraestrutura)
3. **Aba 3: Financeira & ITCM** (Restrita a Governança, Compras e Controladoria)
4. **Aba 4: Custódia & Compliance LGPD / Audit** (Restrita a Administradores ITAM e Segurança da Informação)

---

## 3. FORMULÁRIO 1: ATIVOS DE HARDWARE (DESKTOP E NOTEBOOK - HAM)

> [!NOTE]
> No TOPdesk Asset Management, Desktops e Notebooks compartilham a mesma classe (`User Endpoints`), diferenciando-se pelo **Subtipo / Template**. Campos de mobilidade aplicam-se exclusivamente aos Notebooks.

| Aba no TOPdesk | Nome do Campo | Tipo de Dado no TOPdesk | Obrigatoriedade | Regra de Negócio / Exemplo | Origem / Responsável |
| --- | --- | --- | --- | --- | --- |
| **Informações Gerais** | **Identificador Único (Asset Tag)** | Texto Curto | **Mandatório** | Padrão `DT-XXXXX` (Desktop) ou `NB-XXXXX` (Notebook). Chave primária. | Operação TI / Inventário |
| **Informações Gerais** | **Subtipo de Ativo (Template)** | Dropdown | **Mandatório** | Seleção fixa: `[Desktop, Notebook]`. | Operação TI |
| **Informações Gerais** | **Número de Patrimônio** | Alfanumérico | **Mandatório** | Etiqueta física de metal colada no gabinete/carcaça (Ex: `PAT-2026-0894`). | Controladoria / Patrimônio |
| **Informações Gerais** | **Estado do Ciclo de Vida** | Dropdown | **Mandatório** | Valores: `[Planejado, Em Estoque, Em Uso, Em Manutenção, Em Descarte, Desativado]`. | Operação TI / Service Desk |
| **Informações Gerais** | **Unidade / Lotação Geográfica** | Link Interno / Dropdown | **Mandatório** | Unidade da Embrapa (Ex: `Embrapa Sede - Prédio Central`). | Operação TI |
| **Informações Gerais** | **Criticidade** | Dropdown | **Mandatório** | Impacto operacional: `[Baixa, Média, Alta]`. | Governança TI |
| **Técnica & CMDB** | **Número de Série (S/N)** | Texto Curto | **Mandatório** | Código exclusivo da BIOS do fabricante (Ex: `5CD2348XYZ`). Regex alfanumérico. | Discovery (Intune) / TI |
| **Técnica & CMDB** | **Fabricante / Marca** | Dropdown | **Mandatório** | Catálogo: `[Dell, Lenovo, HP, Apple, Positivo]`. | Operação TI |
| **Técnica & CMDB** | **Modelo Comercial** | Texto Curto | **Mandatório** | Modelo exato (Ex: `OptiPlex 7010` para Desktop ou `Latitude 3440` para Notebook). | Operação TI |
| **Técnica & CMDB** | **Processador (CPU)** | Texto Curto | **Mandatório** | Modelo da CPU (Ex: `Intel Core i5-1345U`, `AMD Ryzen 5 PRO`). | Discovery / TI |
| **Técnica & CMDB** | **Memória RAM (GB)** | Número Inteiro | **Mandatório** | Capacidade total em Gigabytes: `[8, 16, 32]`. | Discovery / TI |
| **Técnica & CMDB** | **Armazenamento Principal** | Texto Curto | **Mandatório** | Tipo e capacidade (Ex: `512 GB SSD NVMe`). | Discovery / TI |
| **Técnica & CMDB** | **Sistema Operacional** | Dropdown | **Mandatório** | `[Windows 11 Pro, Windows 10 Pro, Linux RHEL, macOS]`. | Discovery / TI |
| **Técnica & CMDB** | **Endereço MAC Ethernet** | Texto (Regex) | **Mandatório** | Formato `XX:XX:XX:XX:XX:XX`. Placa de rede cabeada. | Discovery / TI |
| **Técnica & CMDB** | **Endereço MAC Wi-Fi** | Texto (Regex) | Exclusivo Notebook | Formato `XX:XX:XX:XX:XX:XX`. Placa de rede sem fio (obrigatório em Notebooks). | Discovery / TI |
| **Técnica & CMDB** | **Possui Dock Station / Fonte Extra?** | Booleano (Sim/Não) | Exclusivo Notebook | Indica se acompanha acessórios de mobilidade na entrega. | Operação TI |
| **Financeira & ITCM** | **Número da Nota Fiscal (NF)** | Texto Curto | **Mandatório** | Número do documento fiscal de faturamento da compra. | Compras / Suprimentos |
| **Financeira & ITCM** | **Data da Nota Fiscal** | Data | **Mandatório** | Data oficial de entrada do ativo no acervo. | Compras |
| **Financeira & ITCM** | **Valor de Aquisição (R$)** | Moeda (BRL) | **Mandatório** | Valor unitário constante na NF. | Compras / Controladoria |
| **Financeira & ITCM** | **Contrato Vinculado (ITCM)** | Link Interno | **Mandatório** | Associação direta ao registro do Contrato de Aquisição/Garantia no TOPdesk. | Compras |
| **Financeira & ITCM** | **Vencimento da Garantia** | Data | **Mandatório** | Data de término da cobertura de suporte do fabricante (Ex: Dell ProSupport). | Compras / TI |
| **Financeira & ITCM** | **Centro de Custo Pagador** | Dropdown | **Mandatório** | Código contábil da área de lotação financeira para rateio. | Compras / Governança |
| **Custódia & LGPD** | **Usuário Responsável (Custodiante)**| Link Interno | Condicional | Busca direta na tabela de **Pessoas** do TOPdesk (Obrigatório se Estado = `Em Uso`). | Service Desk / TI |
| **Custódia & LGPD** | **Status do Termo de Guarda** | Dropdown | **Mandatório** | Valores: `[Aguardando Aceite no SSP, Aceito Digitalmente, Isento/Infra]`. | Action Sequence / SSP |
| **Custódia & LGPD** | **Data/Hora do Aceite Digital** | Data/Hora | Condicional | Registrado automaticamente no clique de aceite do usuário no Portal SSP. | Action Sequence (Automático) |
| **Custódia & LGPD** | **IP do Aceite Digital** | Texto (IP) | Condicional | Log do IP da estação do usuário no aceite (Auditabilidade LGPD). | Action Sequence (Automático) |

---

## 4. FORMULÁRIO 2: LICENCIAMENTO DE SOFTWARE (PACOTE MS OFFICE / MICROSOFT 365 - SAM)

> [!NOTE]
> Suítes de escritório como o **Microsoft Office / M365** são geridas no pilar **SAM (Software Asset Management)** no TOPdesk, amparando licenças baseadas em assentos SaaS ou licenças perpétuas On-Premise.

| Aba no TOPdesk | Nome do Campo | Tipo de Dado no TOPdesk | Obrigatoriedade | Regra de Negócio / Exemplo | Origem / Responsável |
| --- | --- | --- | --- | --- | --- |
| **Informações Gerais** | **Identificador Único do Licenciamento**| Texto Curto | **Mandatório** | Padrão `SW-LIC-MS-OFFICE-M365` ou `SW-LIC-MS-OFF-PROPLUS`. | Gestão de Licenças / SAM |
| **Informações Gerais** | **Nome Oficial do Software** | Texto Curto | **Mandatório** | Nome comercial (Ex: `Microsoft 365 Apps for Enterprise`, `Office 2021 ProPlus`). | Governança TI |
| **Informações Gerais** | **Categoria de Software** | Dropdown | **Mandatório** | Seleção fixa: `[Suíte de Escritório / Produtividade]`. | Governança TI |
| **Informações Gerais** | **Fabricante / Publisher** | Dropdown | **Mandatório** | Valor fixo: `[Microsoft]`. | Governança TI |
| **Informações Gerais** | **Edição / Plano Contratado** | Dropdown | **Mandatório** | Seleção: `[M365 Business Premium, M365 E3, M365 E5, Office Home & Business]`. | Compras / SAM |
| **Informações Gerais** | **Estado do Licenciamento** | Dropdown | **Mandatório** | Valores: `[Ativo, Em Renovação, Expirado, Sublicenciado]`. | Gestão de Licenças / SAM |
| **Métricas & Instalações**| **Modelo de Licenciamento** | Dropdown | **Mandatório** | Valores: `[Assento SaaS / Nomeado por Usuário, Perpétua por Dispositivo]`. | Gestão de Licenças / SAM |
| **Métricas & Instalações**| **Métrica de Cobrança** | Dropdown | **Mandatório** | `[Mensal (Subscrição), Anual (Subscrição), Perpétua com Software Assurance]`. | Compras / SAM |
| **Métricas & Instalações**| **Quantidade de Licenças Adquiridas**| Número Inteiro | **Mandatório** | Total exato de licenças/assentos contratados (Ex: `1.500`). | Compras / Contratos |
| **Métricas & Instalações**| **Instalações / Alocações Ativas** | Número Inteiro | **Mandatório** | Total de assentos atribuídos no Admin Center / Intune (Ex: `1.340`). | Admin Center / Discovery |
| **Métricas & Instalações**| **Licenças Disponíveis em Estoque**| Número (Calculado) | **Mandatório** | Campo de fórmula nativa: `[Qtd Adquirida] - [Qtd Ativa]` (Ex: `160`). Mede ociosidade. | Sistema (Fórmula TOPdesk) |
| **Métricas & Instalações**| **ID do Tenant / Conta SaaS** | Texto (Criptografado) | **Mandatório** | Tenant ID da Embrapa no Microsoft Entra ID / M365 Admin Center. | Administrador SAM |
| **Métricas & Instalações**| **Chave de Produto / KMS Key** | Texto (Criptografado) | Condicional | Obrigatório apenas se a versão for On-Premise / Volume Licensing (MAK/KMS). | Administrador SAM |
| **Financeira & ITCM** | **Contrato Vinculado (ITCM)** | Link Interno | **Mandatório** | Associação obrigatória ao Contrato de Licenciamento Microsoft ativo no TOPdesk. | Compras / Suprimentos |
| **Financeira & ITCM** | **Fornecedor / Revenda Homologada** | Link Interno / Dropdown | **Mandatório** | Razão Social do parceiro Microsoft (LSP / CSP) vencedor da licitação (CNPJ). | Compras |
| **Financeira & ITCM** | **Data de Início da Vigência** | Data | **Mandatório** | Data de ativação do contrato de subscrição no portal Microsoft. | Compras / SAM |
| **Financeira & ITCM** | **Data de Renovação / Expiração** | Data | **Mandatório** | Data limite do contrato SaaS. Dispara alerta automático de renovação aos 120 dias. | Compras / Action Sequence |
| **Financeira & ITCM** | **Valor Anual Total (R$)** | Moeda (BRL) | **Mandatório** | Valor total do contrato recorrente de licenças MS Office. | Compras |
| **Financeira & ITCM** | **Centro de Custo Pagador** | Dropdown | **Mandatório** | Centro de custo institucional da TI para rateio corporativo. | Governança TI |
| **Atribuição & Audit** | **Lista de Usuários / Computadores** | Tabela Relacionada | **Mandatório** | Lista de colaboradores (Pessoas) ou computadores com licença atribuída. | Admin Center / Discovery |
| **Atribuição & Audit** | **Status de Conformidade** | Dropdown | **Mandatório** | Diagnóstico: `[Em Conformidade, Sublicenciado (Risco), Superlicenciado (Ocioso)]`. | Auditoria ITAM |

---

## 5. PASSO A PASSO TÉCNICO PARA CONFIGURAÇÃO NO TOPDESK

Siga o roteiro abaixo para realizar a criação física dos templates e campos no ambiente de administração do TOPdesk:

### Passo 1: Navegação no Painel de Administração
1. Acesse o TOPdesk com perfil de **Administrador do Sistema**.
2. Navegue até o menu de navegação lateral: `Configurações do TOPdesk > Gerenciamento de Ativos (Asset Management)`.
3. Selecione a opção **Templates de Ativos (Asset Templates)**.

### Passo 2: Criação do Template de Hardware (Desktop / Notebook)
1. Clique em **Novo Template de Ativo**.
2. No campo *Nome do Template*, insira `User Endpoints (Desktop & Notebook)`.
3. Selecione a *Classe de Ativo* pai como `Hardware (HAM)`.
4. Defina os **Ícones e Cores**: Ícone de Computador/Notebook em tom azul corporativo.
5. Crie as 4 Abas:
   - `Informações Gerais`
   - `Especificações Técnicas & CMDB`
   - `Financeira & ITCM`
   - `Custódia & LGPD`
6. Arraste e insira os componentes de campo conforme a **Tabela 1**.

### Passo 3: Criação do Template de Software (MS Office / M365)
1. Clique em **Novo Template de Ativo**.
2. No campo *Nome do Template*, insira `Licenciamento de Software (SAM)`.
3. Selecione a *Classe de Ativo* pai como `Software (SAM)`.
4. Defina os **Ícones e Cores**: Ícone de Licença/Código em tom verde/roxo corporativo.
5. Crie as 4 Abas:
   - `Informações Gerais`
   - `Métricas & Instalações`
   - `Financeira & ITCM`
   - `Atribuição & Audit`
6. Arraste e insira os componentes de campo conforme a **Tabela 2**.

### Passo 4: Configuração de Permissões de Acesso aos Campos (Permissions)
1. Vá em `Configurações > Perfis de Atendimento e Permissões`.
2. **Aba Financeira & ITCM:** Restrinja a visualização e edição apenas para os grupos funcionais `Governança de TI`, `Compras/Contratos` e `Patrimônio/Controladoria`. Oculte para atendentes de Suporte N1.
3. **Chaves de Ativação / Tenant ID:** Defina como *Campo Criptografado de Leitura Restrita*, visível apenas para os *Administradores de ITAM*.

### Passo 5: Automação via Action Sequences (Eventos)
1. Navegue para `Configurações > Módulos do Sistema > Eventos & Action Sequences`.
2. **Confirmação do Termo no SSP:** Crie uma regra acionada ao evento "Confirmação pelo Usuário no Portal SSP", configurada para:
   - Alterar `Status do Termo de Guarda` para `Aceito Digitalmente`.
   - Preencher `Data/Hora do Aceite Digital` com `{now}`.
   - Alterar `Estado do Ciclo de Vida` do ativo para `Em Uso`.
3. **Régua de Alertas Contratuais (120 dias):** Crie uma rotina agendada diária que busca ativos onde `Data de Renovação / Expiração` ocorra em menos de 120 dias e abra automaticamente uma Tarefa de Serviço para a fila de *Compras & Licenciamento*.
