# INSTRUÇÃO PRÁTICA PARA CRIAÇÃO DOS FORMULÁRIOS NO TOPDESK

## Informações do Documento

| Campo | Informação |
| --- | --- |
| Documento | Instrução Prática para Criação dos Formulários de Ativos no TOPdesk |
| Versão | 2.0 |
| Data | 18/09/2026 |
| Autor | André Luiz Bontempo / Especialista ITIL v4 & Arquiteto TOPdesk |
| Projeto | Implantação do IT Asset Management (ITAM) no TOPdesk |
| Ferramenta | TOPdesk Asset Management (Módulo Flexível de Ativos) |
| Instituição | Embrapa (Empresa Brasileira de Pesquisa Agropecuária) |

---

## 1. INTRODUÇÃO E OBJETIVO

Este documento estabelece o guia prático de parametrização dos formulários cadastrais dentro do módulo de **Asset Management (Módulo Flexível de Ativos)** do TOPdesk. 

A estrutura foi concebida para atender rigorosamente às diretrizes corporativas de governança de TI, ITIL® 4, ISO/IEC 19770 e LGPD, garantindo a padronização no cadastro de equipamentos de **Hardware (Estação de Trabalho - Desktop e Notebook)** e licenças de **Software (Pacote MS Office / Microsoft 365)**.

---

## 2. ESTRUTURA DE SEÇÕES E ESTRUTURAÇÃO DO FORMULÁRIO NO TOPDESK

No Designer de Modelo do TOPdesk Asset Management, os formulários são divididos em **Blocos/Seções Funcionais**, suplementados por uma **Grade de Relações** e uma área de **Documentos Anexos**. 

Para o modelo **Estação de Trabalho**, o formulário é composto por 6 blocos estruturados:

1. **Identificação & informações gerais** (Visível a todos os atendentes do Service Desk)
2. **Especificações Técnicas & CMDB** (Editável por Suporte N1, N2, Infraestrutura e ferramentas de Discovery)
3. **Financeiro, Contratual & Suprimentos** (Restrita a Governança, Compras, Contratos e Controladoria)
4. **Custódia, Segurança & Compliance** (Restrita a Administradores ITAM, Segurança da Informação e Compliance LGPD)
5. **Grade de Relações** (Associações dinâmicas de entidades no TOPdesk: Usuário, Localização, Software, Chamado, Contrato, Monitor, Impressora)
6. **Documentos** (Anexos comprobatórios: Nota Fiscal, Termo de Responsabilidade, Comprovante de Garantia, Documentação Técnica, Evidência de Auditoria, Contrato)

---

## 3. FORMULÁRIO 1: MODELO "ESTAÇÃO DE TRABALHO" (DESKTOP E NOTEBOOK - HAM)

> [!NOTE]
> No TOPdesk Asset Management, Desktops e Notebooks compartilham o mesmo modelo principal (**Estação de Trabalho**), diferenciando-se pelo campo **Tipo de Equipamento**. 

| Seção no TOPdesk | Nome do Campo | Tipo de Dado no TOPdesk | Obrigatoriedade | Regra de Negócio / Exemplo | Origem / Responsável |
| --- | --- | --- | --- | --- | --- |
| **Identificação & informações gerais** | **Hostname** | Texto Curto | **Mandatório** | Nome do computador na rede (Ex: `DESKTOP-EMB01`, `NB-ANDRE`). Chave de rede. | Operação TI / Discovery |
| **Identificação & informações gerais** | **Tipo de Equipamento** | Dropdown | **Mandatório** | Seleção de tipo: `[Desktop, Notebook]`. | Operação TI |
| **Identificação & informações gerais** | **Marca** | Dropdown | **Mandatório** | Catálogo de fabricantes homologados: `[Dell, Lenovo, HP, Apple, Positivo]`. | Operação TI |
| **Identificação & informações gerais** | **Modelo Comercial** | Texto Curto | **Mandatório** | Modelo exato (Ex: `Latitude 3440` para Notebook ou `OptiPlex 7010` para Desktop). | Operação TI |
| **Identificação & informações gerais** | **Número de Série** | Texto Curto | **Mandatório** | Código exclusivo da BIOS do fabricante (Ex: `5CD2348XYZ`). Regex alfanumérico. | Discovery (Intune) / TI |
| **Identificação & informações gerais** | **Patrimônio** | Alfanumérico | **Mandatório** | Etiqueta física de metal colada no gabinete/carcaça (Ex: `PAT-2026-0894`). | Controladoria / Patrimônio |
| **Identificação & informações gerais** | **Status** | Dropdown | **Mandatório** | Ciclo de vida: `[Planejado, Em Estoque, Em Uso, Em Manutenção, Em Descarte, Desativado]`. | Operação TI / Service Desk |
| **Especificações Técnicas & CMDB** | **Memória RAM** | Texto Curto / Número | **Mandatório** | Capacidade total de memória RAM (Ex: `8 GB`, `16 GB`, `32 GB`). | Discovery / TI |
| **Especificações Técnicas & CMDB** | **Processador** | Texto Curto | **Mandatório** | Modelo da CPU (Ex: `Intel Core i5-1345U`, `AMD Ryzen 5 PRO`). | Discovery / TI |
| **Especificações Técnicas & CMDB** | **Armazenamento** | Texto Curto | **Mandatório** | Tipo e capacidade de disco (Ex: `512 GB SSD NVMe`). | Discovery / TI |
| **Especificações Técnicas & CMDB** | **Sistema Operacional** | Dropdown | **Mandatório** | Sistema operacional: `[Windows 11 Pro, Windows 10 Pro, Linux RHEL, macOS]`. | Discovery / TI |
| **Especificações Técnicas & CMDB** | **Versão do SO** | Texto Curto | **Mandatório** | Build ou edição do sistema operacional (Ex: `23H2`, `22.04 LTS`). | Discovery / TI |
| **Especificações Técnicas & CMDB** | **IP** | Texto (Regex) | Condicional | Endereço IP IPv4/v6 atribuído (Ex: `10.20.4.15`). | Discovery / Infra |
| **Especificações Técnicas & CMDB** | **MAC** | Texto (Regex) | **Mandatório** | Endereço físico MAC (Ex: `XX:XX:XX:XX:XX:XX`). Requerido para controle 802.1X/DHCP. | Discovery / TI |
| **Especificações Técnicas & CMDB** | **OU - Unidade Organizacional** | Texto Curto / Dropdown | **Mandatório** | Caminho da OU no Active Directory / Entra ID (Ex: `OU=Desktops,OU=Sede,DC=embrapa,DC=br`). | Diretório ID / TI |
| **Financeiro, Contratual & Suprimentos** | **Fornecedor** | Link Interno / Dropdown | **Mandatório** | Razão Social do parceiro comercial fornecedor (CNPJ). | Compras |
| **Financeiro, Contratual & Suprimentos** | **Data de Aquisição** | Data | **Mandatório** | Data oficial de recebimento/entrada do ativo. | Compras |
| **Financeiro, Contratual & Suprimentos** | **Valor de Aquisição** | Moeda (BRL) | **Mandatório** | Valor unitário constante na Nota Fiscal. | Compras / Controladoria |
| **Financeiro, Contratual & Suprimentos** | **Nota Fiscal** | Texto Curto | **Mandatório** | Número do documento fiscal de faturamento da compra. | Compras / Suprimentos |
| **Financeiro, Contratual & Suprimentos** | **Contrato** | Link Interno | **Mandatório** | Associação direta ao registro do Contrato de Aquisição/Garantia (ITCM) no TOPdesk. | Compras |
| **Financeiro, Contratual & Suprimentos** | **Início da Garantia** | Data | **Mandatório** | Data inicial de vigência da garantia do fabricante. | Compras / TI |
| **Financeiro, Contratual & Suprimentos** | **Fim da Garantia** | Data | **Mandatório** | Data de término da cobertura de suporte do fabricante (Ex: Dell ProSupport). | Compras / TI |
| **Financeiro, Contratual & Suprimentos** | **Centro de Custo** | Dropdown | **Mandatório** | Código contábil da área de lotação financeira para rateio corporativo. | Compras / Governança |
| **Financeiro, Contratual & Suprimentos** | **Data Prevista de Descarte** | Data | Condicional | Data planejada para fim da vida útil operacional do equipamento. | Governança TI |
| **Custódia, Segurança & Compliance** | **Responsável pelo Ativo** | Link Interno | Condicional | Busca direta na tabela de **Pessoas** do TOPdesk (Obrigatório se Status = `Em Uso`). | Service Desk / TI |
| **Custódia, Segurança & Compliance** | **Unidade** | Link Interno / Dropdown | **Mandatório** | Unidade da Embrapa (Ex: `Embrapa Sede`, `Embrapa Agrobiologia`). | Operação TI |
| **Custódia, Segurança & Compliance** | **Localização** | Texto Curto / Dropdown | **Mandatório** | Detalhamento físico da alocação (Ex: `Prédio Central - Sala 102`). | Operação TI |
| **Custódia, Segurança & Compliance** | **Data da Entrega** | Data | Condicional | Data de entrega efetiva do ativo ao usuário custodiante. | Service Desk / TI |
| **Custódia, Segurança & Compliance** | **Termo de Responsabilidade** | Dropdown | **Mandatório** | Status do termo: `[Aguardando Aceite no SSP, Aceito Digitalmente, Isento/Infra]`. | Action Sequence / SSP |
| **Custódia, Segurança & Compliance** | **Situação da Custódia** | Dropdown | **Mandatório** | Diagnóstico da posse: `[Regular, Pendente de Aceite, Extraviado, Em Devolução]`. | Governança TI |
| **Custódia, Segurança & Compliance** | **Classificação da Informação** | Dropdown | **Mandatório** | Nível de sigilo dos dados manipulados: `[Pública, Interna, Confidencial, Restrita]`. | Segurança da Informação |
| **Custódia, Segurança & Compliance** | **Dados Pessoais Tratados?** | Booleano (Sim/Não) | **Mandatório** | Indica se o equipamento processa dados pessoais sob amparo da LGPD. | Segurança / Compliance |
| **Custódia, Segurança & Compliance** | **Situação de Compliance** | Dropdown | **Mandatório** | Diagnóstico de conformidade: `[Em Conformidade, Não Conforme, Em Auditoria]`. | Segurança / Compliance |
| **Custódia, Segurança & Compliance** | **Data da Última Avaliação** | Data | Condicional | Data da última verificação ou auditoria de conformidade de segurança. | Segurança / Audit |
| **Grade de Relações** | **Usuário** | Link de Entidade | **Mandatório** | Associação direta com a entidade de Pessoa/Usuário no TOPdesk. | Sistema TOPdesk |
| **Grade de Relações** | **Localização** | Link de Entidade | **Mandatório** | Associação direta com o cadastro de Localização física. | Sistema TOPdesk |
| **Grade de Relações** | **Software** | Link de Entidade | Condicional | Licenças e softwares instalados/alocados à estação de trabalho. | SAM / Discovery |
| **Grade de Relações** | **Chamado** | Link de Entidade | Condicional | Histórico de Incidentes e Requisições vinculados à estação de trabalho. | Service Desk |
| **Grade de Relações** | **Contrato** | Link de Entidade | **Mandatório** | Contratos de garantia e manutenção associados ao ativo. | ITCM / Compras |
| **Grade de Relações** | **Monitor** | Link de Entidade | Condicional | Vinculação com o ativo periférico Monitor conectado à estação. | HAM / TI |
| **Grade de Relações** | **Impressora** | Link de Entidade | Condicional | Vinculação com a impressora alocada/mapeada para o usuário. | HAM / TI |
| **Documentos** | **Nota Fiscal** | Upload (PDF/Imagem) | **Mandatório** | Cópia digital da Nota Fiscal de aquisição do bem. | Compras / Suprimentos |
| **Documentos** | **Termo de Responsabilidade** | Upload (PDF/Doc) | Condicional | Cópia física do Termo de Responsabilidade assinado (quando não for digital). | Service Desk / TI |
| **Documentos** | **Comprovante de Garantia** | Upload (PDF) | Condicional | Certificado de garantia ou apólice de suporte estendido do fabricante. | Compras / TI |
| **Documentos** | **Documentação Técnica** | Upload (PDF) | Condicional | Datasheet, manual técnico ou laudos de homologação do equipamento. | TI / Infraestrutura |
| **Documentos** | **Evidência de Auditoria** | Upload (PDF) | Condicional | Laudos de auditoria interna ou relatórios de verificação de compliance. | Auditoria / Compliance |
| **Documentos** | **Contrato** | Upload (PDF) | **Mandatório** | Cópia do instrumento contratual amparador da aquisição/garantia. | Compras / ITCM |

---

## 4. FORMULÁRIO 2: LICENCIAMENTO DE SOFTWARE (PACOTE MS OFFICE / MICROSOFT 365 - SAM)

> [!NOTE]
> Suítes de escritório como o **Microsoft Office / M365** são geridas no pilar **SAM (Software Asset Management)** no TOPdesk, amparando licenças baseadas em assentos SaaS ou licenças perpétuas On-Premise.

| Aba / Bloco no TOPdesk | Nome do Campo | Tipo de Dado no TOPdesk | Obrigatoriedade | Regra de Negócio / Exemplo | Origem / Responsável |
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
3. Selecione a opção **Designer de Modelo**.

### Passo 2: Criação do Modelo de Ativo "Estação de Trabalho"
1. No menu lateral do Designer de Modelo, sob a classe **Ativo**, clique em **Criar modelo de ativo**.
2. No campo *Nome do Modelo*, insira `Estação de Trabalho`.
3. Defina os **Ícones e Cores**: Ícone de Computador/Estação em tom azul corporativo.
4. Crie os 6 Blocos/Seções Funcionais:
   - `Identificação & informações gerais`
   - `Especificações Técnicas & CMDB`
   - `Financeiro, Contratual & Suprimentos`
   - `Custódia, Segurança & Compliance`
   - `Grade de Relações`
   - `Documentos`
5. Arraste e insira os componentes de campo conforme a **Tabela do Formulário 1**.

### Passo 3: Criação do Modelo de Licença de Software (MS Office / M365)
1. No menu lateral do Designer de Modelo, sob a classe **Ativo**, selecione a opção `Licença de Software` ou clique em **Criar modelo de ativo**.
2. No campo *Nome do Modelo*, insira `Licença de Software (SAM)`.
3. Defina os **Ícones e Cores**: Ícone de Licença/Código em tom verde/roxo corporativo.
4. Organize os blocos funcionais conforme especificado na **Tabela do Formulário 2**.

### Passo 4: Configuração de Permissões de Acesso aos Campos (Permissions)
1. Vá em `Configurações > Perfis de Atendimento e Permissões`.
2. **Bloco Financeiro, Contratual & Suprimentos:** Restrinja a visualização e edição apenas para os grupos funcionais `Governança de TI`, `Compras/Contratos` e `Patrimônio/Controladoria`. Oculte para atendentes de Suporte N1.
3. **Chaves de Ativação / Tenant ID / Senhas:** Defina como *Campo Criptografado de Leitura Restrita*, visível apenas para os *Administradores de ITAM*.

### Passo 5: Automação via Action Sequences (Eventos)
1. Navegue para `Configurações > Módulos do Sistema > Eventos & Action Sequences`.
2. **Confirmação do Termo no SSP:** Crie uma regra acionada ao evento "Confirmação pelo Usuário no Portal SSP", configurada para:
   - Alterar `Termo de Responsabilidade` para `Aceito Digitalmente`.
   - Preencher `Data da Entrega` com a data/timestamp atual.
   - Alterar `Status` do ativo para `Em Uso`.
3. **Régua de Alertas Contratuais (120 dias):** Crie uma rotina agendada diária que busca ativos onde `Fim da Garantia` ou `Data de Renovação / Expiração` ocorra em menos de 120 dias e abra automaticamente uma Tarefa de Serviço para a fila de *Compras & Licenciamento*.

