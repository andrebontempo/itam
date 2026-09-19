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

Os dois modelos principais de ativos criados no TOPdesk possuem a seguinte organização estrutural:

- **Modelo 1: Estação de Trabalho** (Hardware - HAM): 6 blocos (`Identificação & informações gerais`, `Especificações Técnicas & CMDB`, `Financeiro, Contratual & Suprimentos`, `Custódia, Segurança & Compliance`, `Grade de Relações`, `Documentos`).
- **Modelo 2: Licença de Software** (Software - SAM): 6 blocos (`Identificação de Software & Licença`, `Métricas de Licenciamento & Instalações`, `Financeiro, Contratual & Governança`, `Atribuição, Uso & Compliance`, `Grade de Relações`, `Documentos`).

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

## 4. FORMULÁRIO 2: MODELO "LICENÇA DE SOFTWARE" (SAM)

> [!NOTE]
> O modelo **Licença de Software** ampara a gestão de ativos de software On-Premise, subscrições SaaS (como o Microsoft 365) e softwares especialistas da Embrapa, mapeados no pilar **SAM (Software Asset Management)** no Designer de Modelo do TOPdesk.

| Seção no TOPdesk | Nome do Campo | Tipo de Dado no TOPdesk | Obrigatoriedade | Regra de Negócio / Exemplo | Origem / Responsável |
| --- | --- | --- | --- | --- | --- |
| **Identificação de Software & Licença** | **Nome do Software** | Texto Curto | **Mandatório** | Nome comercial do software (Ex: `Microsoft 365 Enterprise`, `Oracle Database`). | Governança TI |
| **Identificação de Software & Licença** | **Fabricante** | Dropdown / Texto | **Mandatório** | Desenvolvedor homologado (`Microsoft`, `Oracle`, `Red Hat`, `JetBrains`). | Governança TI / SAM |
| **Identificação de Software & Licença** | **Produto** | Texto Curto | **Mandatório** | Família do produto (`Office 365`, `Database Enterprise`, `IntelliJ IDEA`). | Governança TI |
| **Identificação de Software & Licença** | **Edição** | Dropdown / Texto | **Mandatório** | Edição contratada (`Business Premium`, `E3`, `E5`, `Standard`, `Enterprise`). | Compras / SAM |
| **Identificação de Software & Licença** | **Versão** | Texto Curto | **Mandatório** | Versão ou release oficial (`2024.1`, `21c`, `v11.0`). | Operação TI / SAM |
| **Identificação de Software & Licença** | **Tipo de Licença** | Dropdown | **Mandatório** | Modelo da licença (`Subscrição SaaS`, `Perpétua`, `Concorrente/Floating`, `OEM`, `Volume`). | SAM / Compras |
| **Identificação de Software & Licença** | **ID da Licença** | Texto Curto | **Mandatório** | Identificador da licença ou contrato no portal do fabricante. | Administrador SAM |
| **Identificação de Software & Licença** | **Identificador da Licença** | Texto Curto / Key | **Mandatório** | Padrão `SW-LIC-MS-OFFICE-M365` ou Tenant ID / Serial Key. | Administrador SAM |
| **Métricas de Licenciamento & Instalações** | **Métrica de Licenciamento** | Dropdown | **Mandatório** | Regra de medição (`Por Usuário/Assento`, `Por Dispositivo/Core`, `Concorrente`). | Gestão de Licenças / SAM |
| **Métricas de Licenciamento & Instalações** | **Quantidade Adquirida** | Número Inteiro | **Mandatório** | Total de licenças compradas constantes no contrato (Ex: `1.500`). | Compras / Contratos |
| **Métricas de Licenciamento & Instalações** | **Quantidade Licenciada** | Número Inteiro | **Mandatório** | Total de licenças efetivamente concedidas e aptas para uso. | SAM / Operação TI |
| **Métricas de Licenciamento & Instalações** | **Quantidade Instalada** | Número Inteiro | **Mandatório** | Total de instâncias/instalações detectadas via Discovery/Intune. | Discovery / Intune |
| **Métricas de Licenciamento & Instalações** | **Quantidade em Uso** | Número Inteiro | **Mandatório** | Assentos ou licenças em utilização ativa pelos colaboradores. | SAM / Discovery |
| **Métricas de Licenciamento & Instalações** | **Quantidade Disponível** | Número (Calculado) | **Mandatório** | Saldo em estoque: `[Qtd Adquirida] - [Qtd em Uso]` (Ex: `160`). Mede ociosidade. | Sistema (Fórmula TOPdesk) |
| **Métricas de Licenciamento & Instalações** | **Data da Primeira Instalação** | Data | Condicional | Timestamp da primeira ativação/instalação no acervo. | Discovery / SAM |
| **Métricas de Licenciamento & Instalações** | **Data da Última Instalação** | Data | Condicional | Timestamp do último provisionamento efetuado. | Discovery / SAM |
| **Métricas de Licenciamento & Instalações** | **Situação do Licenciamento** | Dropdown | **Mandatório** | Estado do licenciamento (`Ativo`, `Em Renovação`, `Expirado`, `Sublicenciado`). | Gestão de Licenças / SAM |
| **Financeiro, Contratual & Governança** | **Fornecedor** | Link Interno / Dropdown | **Mandatório** | Razão Social do parceiro comercial fornecedor / LSP / CSP (CNPJ). | Compras |
| **Financeiro, Contratual & Governança** | **Data de Aquisição** | Data | **Mandatório** | Data oficial da compra ou emissão da fatura. | Compras |
| **Financeiro, Contratual & Governança** | **Valor de Aquisição** | Moeda | **Mandatório** | Custo de aquisição do lote ou valor anuidade da subscrição. | Compras / Controladoria |
| **Financeiro, Contratual & Governança** | **Moeda** | Dropdown | **Mandatório** | Moeda do contrato (`BRL`, `USD`, `EUR`). | Compras |
| **Financeiro, Contratual & Governança** | **Nota Fiscal** | Texto Curto | **Mandatório** | Número do documento fiscal de compra. | Compras / Suprimentos |
| **Financeiro, Contratual & Governança** | **Contrato** | Link Interno | **Mandatório** | Associação ao registro do Contrato de Licenciamento (ITCM) no TOPdesk. | Compras |
| **Financeiro, Contratual & Governança** | **Pedido de Compra** | Texto Curto | **Mandatório** | Número do Pedido de Compra / Ordem de Serviço (PO). | Compras / Suprimentos |
| **Financeiro, Contratual & Governança** | **Centro de Custo** | Dropdown | **Mandatório** | Código contábil da unidade pagadora para rateio financeiro. | Governança TI |
| **Financeiro, Contratual & Governança** | **Início da Vigência** | Data | **Mandatório** | Data inicial de concessão do direito de uso ou contrato. | Compras / SAM |
| **Financeiro, Contratual & Governança** | **Fim da Vigência** | Data | **Mandatório** | Data limite do contrato SaaS / subscrição (dispara alerta aos 120 dias). | Compras / SAM |
| **Financeiro, Contratual & Governança** | **Renovação Automática** | Booleano (Sim/Não) | **Mandatório** | Indica se há renovação automática programada no contrato. | Compras / ITCM |
| **Financeiro, Contratual & Governança** | **Custo de Renovação** | Moeda | **Mandatório** | Valor estimativo recorrente da anuidade/renovação. | Compras / Financeiro |
| **Atribuição, Uso & Compliance** | **Responsável pela Licença** | Link Interno | **Mandatório** | Busca na tabela de Pessoas (Gestor do Software / Admin SAM). | Governança TI |
| **Atribuição, Uso & Compliance** | **Unidade** | Link Interno / Dropdown | **Mandatório** | Unidade Embrapa beneficiária do licenciamento. | Governança TI |
| **Atribuição, Uso & Compliance** | **Data da Atribuição** | Data | Condicional | Data de alocação da licença ao usuário ou servidor. | Service Desk / SAM |
| **Atribuição, Uso & Compliance** | **Ambiente de Aplicação** | Dropdown | **Mandatório** | Escopo de execução (`Produção`, `Homologação`, `Desenvolvimento`). | Operação TI |
| **Atribuição, Uso & Compliance** | **Uso Autorizado?** | Booleano (Sim/Não) | **Mandatório** | Confirmação de conformidade de uso institucional. | Segurança da Informação |
| **Atribuição, Uso & Compliance** | **Situação do Licenciamento** | Dropdown | **Mandatório** | Diagnóstico operacional (`Ativo`, `Em Renovação`, `Sublicenciado`). | SAM / Auditoria |
| **Atribuição, Uso & Compliance** | **Data da Última Auditoria** | Data | **Mandatório** | Timestamp do último batimento entre inventário e contratos. | Gestão de Licenças / SAM |
| **Atribuição, Uso & Compliance** | **Situação de Compliance** | Dropdown | **Mandatório** | Diagnóstico final (`Em Conformidade`, `Sublicenciado (Risco)`, `Superlicenciado (Desperdício)`). | Auditoria ITAM |
| **Atribuição, Uso & Compliance** | **Observações** | Área de Texto | Condicional | Notas técnicas, exceções de licenciamento ou ressalvas de audit. | SAM / Compliance |
| **Grade de Relações** | **Usuário** | Link de Entidade | **Mandatório** | Associação direta com a entidade de Pessoa/Usuário com licença atribuída. | Sistema TOPdesk |
| **Grade de Relações** | **Estação de Trabalho** | Link de Entidade | Condicional | Vinculação com estações de trabalho que possuem o software instalado. | Sistema TOPdesk |
| **Grade de Relações** | **Servidor** | Link de Entidade | Condicional | Vinculação com servidores de aplicação onde o software executa. | Sistema TOPdesk |
| **Grade de Relações** | **Pessoas** | Link de Entidade | Condicional | Vinculação com lista de colaboradores/grupos elegíveis. | Sistema TOPdesk |
| **Grade de Relações** | **Contrato** | Link de Entidade | **Mandatório** | Associação com os Contratos de TI amparadores. | ITCM / Compras |
| **Grade de Relações** | **Chamado** | Link de Entidade | Condicional | Histórico de chamados de suporte/requisições vinculados. | Service Desk |
| **Documentos** | **Estatuto** | Upload (PDF) | Condicional | Termos de uso, regulamento interno ou política do produto. | SAM / Governança |
| **Documentos** | **Proposta Comercial** | Upload (PDF) | **Mandatório** | Cópia da proposta comercial homologada da contratação. | Compras |
| **Documentos** | **Pedido de Compra** | Upload (PDF) | **Mandatório** | Cópia da ordem/pedido de compra emitido (PO). | Compras / Suprimentos |
| **Documentos** | **Nota Fiscal** | Upload (PDF/Imagem) | **Mandatório** | Cópia do documento fiscal de faturamento da licença. | Compras / Suprimentos |
| **Documentos** | **Certificado de Licença** | Upload (PDF) | **Mandatório** | Certificado oficial de licença (*License Certificate*). | SAM / Compras |
| **Documentos** | **Comprovante de Aquisição** | Upload (PDF) | Condicional | Comprovantes de faturamento ou quitação de liquidação. | Controladoria |
| **Documentos** | **Termo de Licenciamento** | Upload (PDF) | **Mandatório** | EULA / Contrato de Licença de Usuário Final do fabricante. | Governança TI |
| **Documentos** | **Evidência de Auditoria** | Upload (PDF) | Condicional | Relatório de conciliação ou laudo de auditoria de conformidade. | Auditoria / Compliance |
| **Documentos** | **Documentação do Fabricante** | Upload (PDF) | Condicional | Manual de métricas, datasheets ou guia de licenciamento. | Governança TI |
| **Documentos** | **Comprovante de Renovação** | Upload (PDF) | Condicional | Aditivo de renovação ou comprovante de vigência estendida. | Compras / ITCM |

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

### Passo 3: Criação do Modelo de Ativo "Licença de Software"
1. No menu lateral do Designer de Modelo, sob a classe **Ativo**, selecione a opção `Licença de Software` ou clique em **Criar modelo de ativo**.
2. No campo *Nome do Modelo*, insira `Licença de Software`.
3. Defina os **Ícones e Cores**: Ícone de Licença/Código em tom roxo/verde corporativo.
4. Crie os 6 Blocos/Seções Funcionais:
   - `Identificação de Software & Licença`
   - `Métricas de Licenciamento & Instalações`
   - `Financeiro, Contratual & Governança`
   - `Atribuição, Uso & Compliance`
   - `Grade de Relações`
   - `Documentos`
5. Arraste e insira os componentes de campo conforme a **Tabela do Formulário 2**.

### Passo 4: Configuração de Permissões de Acesso aos Campos (Permissions)
1. Vá em `Configurações > Perfis de Atendimento e Permissões`.
2. **Blocos Financeiros e Contratuais:** Restrinja a visualização e edição apenas para os grupos funcionais `Governança de TI`, `Compras/Contratos` e `Patrimônio/Controladoria`. Oculte para atendentes de Suporte N1.
3. **Chaves de Ativação / Tenant ID / Senhas:** Defina como *Campo Criptografado de Leitura Restrita*, visível apenas para os *Administradores de ITAM*.

### Passo 5: Automação via Action Sequences (Eventos)
1. Navegue para `Configurações > Módulos do Sistema > Eventos & Action Sequences`.
2. **Confirmação do Termo no SSP:** Crie uma regra acionada ao evento "Confirmação pelo Usuário no Portal SSP", configurada para:
   - Alterar `Termo de Responsabilidade` para `Aceito Digitalmente`.
   - Preencher `Data da Entrega` com a data/timestamp atual.
   - Alterar `Status` do ativo para `Em Uso`.
3. **Régua de Alertas Contratuais (120 dias):** Crie uma rotina agendada diária que busca ativos onde `Fim da Garantia` ou `Fim da Vigência` ocorra em menos de 120 dias e abra automaticamente uma Tarefa de Serviço para a fila de *Compras & Licenciamento*.


