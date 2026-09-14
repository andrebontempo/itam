Segue uma versão completa e estruturada do documento, já preparada para servir como referência oficial do projeto de implantação do ITAM e futura configuração do TOPdesk.

# DIRETRIZES CORPORATIVAS PARA IMPLEMENTAÇÃO DA GESTÃO DE ATIVOS DE TI (ITAM)

## 1\. INTRODUÇÃO

A Gestão de Ativos de Tecnologia da Informação (IT Asset Management – ITAM) consiste no conjunto de processos, políticas, controles e ferramentas destinados a gerenciar todo o ciclo de vida dos ativos de TI, desde seu planejamento e aquisição até sua desativação e descarte.

A implantação do ITAM tem como finalidade estabelecer uma base única e confiável de informações sobre os recursos tecnológicos da organização, proporcionando maior controle operacional, redução de custos, conformidade legal e suporte à tomada de decisão.

Este documento define a estrutura conceitual, operacional e de governança que deverá ser utilizada como referência para implantação e evolução contínua da gestão de ativos de TI.

* * *

# 2\. OBJETIVOS DO PROGRAMA ITAM

O programa de Gestão de Ativos de TI possui os seguintes objetivos:

- Manter inventário corporativo centralizado e atualizado.
    
- Garantir rastreabilidade completa dos ativos durante todo o ciclo de vida.
    
- Reduzir perdas de equipamentos e licenças.
    
- Melhorar a utilização dos recursos tecnológicos.
    
- Apoiar auditorias internas e externas.
    
- Garantir conformidade contratual e regulatória.
    
- Fornecer informações confiáveis para planejamento orçamentário.
    
- Apoiar processos de governança de TI.
    
- Reduzir riscos operacionais relacionados à indisponibilidade de ativos.
    
- Estabelecer integração entre inventário, contratos, usuários e serviços.
    

* * *

# 3\. ESCOPO

O escopo do programa contempla:

## Ativos Físicos

- Notebooks
    
- Desktops
    
- Tablets
    
- Smartphones
    
- Monitores
    
- Impressoras
    
- Servidores
    
- Storages
    
- Switches
    
- Firewalls
    
- Nobreaks
    
- Equipamentos de telecomunicações
    

## Ativos Lógicos

- Sistemas operacionais
    
- Softwares corporativos
    
- Licenças
    
- Assinaturas SaaS
    
- Bancos de dados
    
- Ferramentas de desenvolvimento
    

## Serviços em Nuvem

- Infraestrutura como Serviço (IaaS)
    
- Plataforma como Serviço (PaaS)
    
- Software como Serviço (SaaS)
    
- APIs com cobrança por consumo
    

## Contratos

- Garantias
    
- Manutenção
    
- Telecomunicações
    
- Outsourcing
    
- Consultorias
    
- Licenciamento
    

* * *

# 4\. PAPÉIS E RESPONSABILIDADES

## Área de TI

Responsável pela administração operacional do programa ITAM.

Atividades:

- Cadastro e manutenção dos ativos.
    
- Controle de inventário.
    
- Gestão do ciclo de vida.
    
- Integração com ferramentas de descoberta.
    

## Área de Compras

Responsável por:

- Aquisição de ativos.
    
- Gestão de fornecedores.
    
- Formalização contratual.
    

## Gestores das Áreas

Responsáveis por:

- Aprovação de solicitações.
    
- Validação de atribuições.
    
- Controle do uso dos ativos sob sua responsabilidade.
    

## Usuários

Responsáveis por:

- Utilização adequada dos ativos.
    
- Comunicação de incidentes.
    
- Devolução dos ativos quando solicitado.
    

* * *

# 5\. HARDWARE ASSET MANAGEMENT (HAM)

## Objetivo

Controlar todos os ativos físicos de tecnologia ao longo de seu ciclo de vida.

* * *

## Categorias

### User Endpoints

- Notebooks
    
- Desktops
    
- Tablets
    
- Smartphones
    

### Infraestrutura

- Servidores
    
- Storages
    
- Appliances
    

### Rede

- Switches
    
- Firewalls
    
- Access Points
    
- Roteadores
    

### Periféricos

- Monitores
    
- Impressoras
    
- Scanners
    
- Nobreaks
    

* * *

## Campos Obrigatórios

### Identificação

- Nome do ativo
    
- Número de patrimônio
    
- Número de série
    
- Fabricante
    
- Modelo
    

### Responsabilidade

- Usuário responsável
    
- Gestor responsável
    
- Área responsável
    

### Localização

- Unidade
    
- Sala
    
- Rack
    
- Local físico
    

### Dados Financeiros

- Fornecedor
    
- Nota fiscal
    
- Data de aquisição
    
- Valor de aquisição
    
- Centro de custo
    

### Dados Técnicos

- Processador
    
- Memória
    
- Armazenamento
    
- Sistema operacional
    
- Endereço MAC
    

* * *

## Exemplo

Patrimônio: PAT-2026-0894

Ativo: Notebook Dell Latitude 3440

Fabricante: Dell

Processador: Intel Core i5

Memória: 16 GB

Armazenamento: SSD 512 GB

Usuário: Andre Luiz Bontempo

Status: Em Uso

Localização: Escritório Brasília

* * *

# 6\. SOFTWARE ASSET MANAGEMENT (SAM)

## Objetivo

Controlar ativos de software instalados localmente e garantir conformidade de licenciamento.

* * *

## Tipos de Licenciamento

### Por dispositivo

Exemplo:

- Windows Professional

### Por usuário

Exemplo:

- Microsoft 365

### Por servidor

Exemplo:

- SQL Server

### Por núcleo (Core)

Exemplo:

- Oracle Database

* * *

## Campos Obrigatórios

- Nome do software
    
- Fabricante
    
- Tipo de licença
    
- Quantidade adquirida
    
- Quantidade instalada
    
- Quantidade utilizada
    
- Data de renovação
    
- Contrato associado
    

* * *

## Indicadores

- Taxa de utilização de licenças
    
- Licenças ociosas
    
- Licenças excedidas
    
- Conformidade de licenciamento
    

* * *

# 7\. SAAS MANAGEMENT

## Objetivo

Controlar aplicações contratadas por assinatura.

* * *

## Exemplos

- Microsoft 365
    
- GitHub Enterprise
    
- Jira
    
- Confluence
    
- ChatGPT Enterprise
    
- Adobe Creative Cloud
    

* * *

## Campos Obrigatórios

- Nome do serviço
    
- Fornecedor
    
- Quantidade contratada
    
- Quantidade utilizada
    
- Quantidade disponível
    
- Valor mensal
    
- Valor anual
    
- Gestor do contrato
    

* * *

## Exemplo

Serviço: Microsoft 365 Business Premium

Licenças contratadas: 150

Licenças em uso: 132

Licenças disponíveis: 18

Status: Ativo

* * *

# 8\. CLOUD ASSET MANAGEMENT E FINOPS

## Objetivo

Gerenciar recursos tecnológicos consumidos sob demanda em ambientes de nuvem.

* * *

## Escopo

### IaaS

- AWS EC2
    
- Azure Virtual Machines
    

### PaaS

- MongoDB Atlas
    
- Azure SQL
    

### APIs

- OpenAI API
    
- Serviços Cognitivos
    

### Storage

- Amazon S3
    
- Azure Blob
    

* * *

## Campos Obrigatórios

- Serviço
    
- Provedor
    
- Conta associada
    
- Centro de custo
    
- Orçamento mensal
    
- Consumo atual
    
- Responsável técnico
    

* * *

## Regras de Controle

### Alerta Preventivo

80% do orçamento.

### Alerta Crítico

90% do orçamento.

### Escalonamento

100% do orçamento.

* * *

## Indicadores

- Consumo mensal
    
- Custo por sistema
    
- Custo por departamento
    
- Tendência de crescimento
    

* * *

# 9\. CONTRATOS E FORNECEDORES (ITCM)

## Objetivo

Gerenciar todos os contratos relacionados aos ativos de TI.

* * *

## Tipos

### Garantias

### Telecomunicações

### Licenciamento

### Suporte

### Consultoria

### Outsourcing

* * *

## Campos Obrigatórios

- Número do contrato
    
- Fornecedor
    
- Gestor do contrato
    
- Data de início
    
- Data de término
    
- SLA
    
- Valor mensal
    
- Valor anual
    
- Índice de reajuste
    
- Renovação automática
    

* * *

## Alertas

- 120 dias antes do vencimento
    
- 90 dias antes do vencimento
    
- 60 dias antes do vencimento
    
- 30 dias antes do vencimento
    

* * *

# 10\. CMDB E RELACIONAMENTOS

## Objetivo

Mapear relacionamentos entre ativos, usuários, serviços e sistemas.

* * *

## Exemplos de Relacionamentos

Notebook → Usuário

Servidor → Sistema

Sistema → Banco de Dados

Banco de Dados → Storage

Aplicação → Contrato

Serviço Cloud → Centro de Custo

* * *

## Benefícios

- Análise de impacto.
    
- Gestão de mudanças.
    
- Resolução de incidentes.
    
- Governança de serviços.
    

* * *

# 11\. CICLO DE VIDA DOS ATIVOS

## Planejamento

- Solicitado
    
- Em análise
    
- Aprovado
    

## Aquisição

- Comprado
    
- Recebido
    

## Implantação

- Em preparação
    
- Em homologação
    
- Disponível
    

## Operação

- Em uso
    
- Em produção
    
- Reserva técnica
    

## Manutenção

- Em garantia
    
- Em reparo
    
- Em empréstimo
    

## Encerramento

- Obsoleto
    
- Desativado
    
- Descartado
    
- Alienado
    

* * *

# 12\. PROCESSOS OPERACIONAIS

## Entrada de Ativos

Fluxo:

Solicitação → Aprovação → Compra → Recebimento → Cadastro → Disponibilização

* * *

## Movimentação

Fluxo:

Solicitação → Aprovação → Atualização cadastral → Termo de responsabilidade

* * *

## Devolução

Fluxo:

Solicitação → Recebimento → Inspeção → Estoque

* * *

## Baixa

Fluxo:

Avaliação → Aprovação → Descarte → Registro documental

* * *

# 13\. INTEGRAÇÕES E DESCOBERTA AUTOMÁTICA

## Inventário

- OCS Inventory
    
- GLPI Agent
    
- Microsoft Intune
    
- Microsoft SCCM
    
- Lansweeper
    

## Diretório Corporativo

- Active Directory
    
- Microsoft Entra ID
    

## Monitoramento

- Zabbix
    
- Grafana
    
- Prometheus
    

## Cloud

- AWS
    
- Azure
    
- Google Cloud Platform
    

* * *

# 14\. INDICADORES DE DESEMPENHO (KPIs)

## Hardware

- % ativos inventariados
    
- % ativos sem responsável
    
- % ativos fora de garantia
    

## Software

- Taxa de utilização de licenças
    
- Licenças ociosas
    
- Conformidade de licenciamento
    

## Cloud

- Consumo mensal
    
- Variação de custos
    
- Desvio orçamentário
    

## Contratos

- Contratos próximos ao vencimento
    
- Contratos sem gestor definido
    

* * *

# 15\. ESTRUTURA MÍNIMA DE DADOS PARA O TOPDESK

Todos os ativos cadastrados deverão possuir, no mínimo:

## Identificação

- Nome
    
- Tipo
    
- Fabricante
    
- Modelo
    
- Número de série
    
- Patrimônio
    

## Responsabilidade

- Usuário responsável
    
- Área responsável
    
- Gestor responsável
    

## Situação

- Status do ciclo de vida
    
- Criticidade
    
- Data de implantação
    

## Dados Técnicos

- Sistema operacional
    
- IP
    
- MAC Address
    
- Processador
    
- Memória
    
- Armazenamento
    

## Financeiro

- Centro de custo
    
- Fornecedor
    
- Valor de aquisição
    
- Data de aquisição
    

* * *

# 16\. ROADMAP DE IMPLEMENTAÇÃO

## Fase 1 – Estruturação

- Definição do modelo de dados.
    
- Configuração do TOPdesk.
    
- Definição de categorias.
    

## Fase 2 – Inventário Inicial

- Integração com OCS Inventory.
    
- Importação dos ativos existentes.
    
- Validação dos dados.
    

## Fase 3 – Governança

- Definição de responsáveis.
    
- Criação dos processos operacionais.
    
- Formalização dos termos de responsabilidade.
    

## Fase 4 – CMDB

- Mapeamento dos relacionamentos.
    
- Vinculação entre ativos e serviços.
    

## Fase 5 – Indicadores

- Construção de dashboards.
    
- Implantação dos KPIs.
    

## Fase 6 – Melhoria Contínua

- Auditorias periódicas.
    
- Revisões de inventário.
    
- Evolução dos processos.
    
- Avaliação de maturidade do ITAM.
    

* * *

# CONSIDERAÇÕES FINAIS

O ITAM deve ser tratado como um processo contínuo de governança e não apenas como uma atividade de inventário. A qualidade das informações cadastradas será determinante para o sucesso das operações de TI, da gestão financeira, do compliance e da tomada de decisão estratégica.

A ferramenta de ITAM deverá ser considerada a fonte oficial de informações dos ativos corporativos, mantendo integração com os demais sistemas de gestão, monitoramento, autenticação e suporte utilizados pela organização.

Esse documento já pode ser utilizado como base formal para aprovação do projeto e para iniciar a modelagem do Gerenciamento de Ativos do TOPdesk, incluindo os campos que serão importados do OCS Inventory e os que serão preenchidos manualmente pelas áreas responsáveis.

[000 - Gestão Patrimonial x ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/000%20-%20Gestão%20Patrimonial%20x%20ITAM%20x%20CMDB.md)

[001 - ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/001%20-%20ITAM%20x%20CMDB.md)

[002 - ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM.md)

[002 - ITAM - Estação de Trabalho](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM%20-%20Estação%20de%20Trabalho.md)

[003 - ITAM - Exemplo](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/003%20-%20ITAM%20-%20Exemplo.md)

[004 - GEMINI](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/004%20-%20ITAM%20-%20Estrutura.md)

[005 - Como fica as contratações de IA](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/005%20-%20ITAM%20-%20Como%20fica%20as%20contratações%20de%20IA.md)

[006 - Proposta para o projeto](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/006%20-%20Proposta%20para%20o%20projeto.md)

[007 - Proposta para o Projeto ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/007%20-%20Proposta%20para%20o%20Projeto%20ITAM.md)