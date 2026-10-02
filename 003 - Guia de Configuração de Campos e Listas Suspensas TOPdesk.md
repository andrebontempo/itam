# GUIA DE CONFIGURAÇÃO DE CAMPOS E LISTAS SUSPENSAS NO TOPDESK

## Informações do Documento

| Campo | Informação |
| --- | --- |
| Documento | Guia de Configuração dos Campos e Opções das Listas Suspensas |
| Versão | 1.0 |
| Data | 01/10/2026 |
| Modelo TOPdesk | Estação de Trabalho (Desktops e Notebooks - HAM) |
| Autor | André Luiz Bontempo / Especialista ITIL v4 & Arquiteto TOPdesk |
| Projeto | Implantação do IT Asset Management (ITAM) no TOPdesk |
| Instituição | Embrapa |

---

## 1. OBJETIVO E DIRETRIZES DE PADRONIZAÇÃO

Este guia especifica a **parametrização exata** a ser executada no **Designer de Modelo do TOPdesk Asset Management** para o modelo `Estação de Trabalho`.

### Regras Gerais de Governança de Dados:
1. **Campos do Tipo "Lista Suspensa" (Dropdown)**: Devem ser utilizados sempre que o atributo possuir um conjunto finito e homologado de valores. A caixa *"Os usuários podem adicionar opções"* deve permanecer **desmarcada** para evitar poluição cadastral.
2. **Campos do Tipo "Texto Curto"**: Reservados estritamente para identificadores únicos (Hostname, S/N, Patrimônio, Nota Fiscal).
3. **Campos do Tipo "Texto com Regex"**: Utilizados para formatar com máscara obrigatória dados técnicos como Endereço IP e Endereço MAC.
4. **Campos do Tipo "Link de Entidade"**: Utilizados para relacionamento direto com tabelas nativas do TOPdesk (Pessoas, Empresas, Contratos, Localização).

---

## 2. ESPECIFICAÇÃO DETALHADA DOS CAMPOS POR SEÇÃO

---

### SEÇÃO 1: Identificação & Informações Gerais

| Rótulo do Campo | ID do Campo (TOPdesk) | Tipo no TOPdesk | Opções Selecionáveis da Lista Suspensa / Regra | Obrigatoriedade |
| --- | --- | --- | --- | --- |
| **Nome do host** | `name` / `computador` | Texto Curto | Identificador único de rede. Padrão `NB-XXXXX` ou `DT-XXXXX`. | **Mandatório** |
| **Tipo de Equipamento** | `tipo-de-equipamento` | **Lista Suspensa** | - `Desktop`<br>- `Notebook` | **Mandatório** |
| **Marca** | `marca` | **Lista Suspensa** | - `Apple`<br>- `Daten`<br>- `Dell`<br>- `HP`<br>- `Lenovo`<br>- `Positivo` | **Mandatório** |
| **Modelo Comercial** | `modelo` | **Lista Suspensa** | - `EliteBook 840 G10`<br>- `EliteDesk 800 G9`<br>- `Latitude 3440`<br>- `Latitude 5440`<br>- `MacBook Pro 14"`<br>- `Master D620`<br>- `OptiPlex 7010`<br>- `Precision 3660`<br>- `ThinkPad E14 Gen 5`<br>- `ThinkPad L14 Gen 4`<br>- `ThinkPad T14 Gen 4` | **Mandatório** |
| **Número de Série** | `numero-de-serie` | Texto Curto | Serial exclusivo da BIOS / Fabricante (Ex: `5CD2348XYZ`). | **Mandatório** |
| **Patrimônio** | `patrimonio` | Texto Curto | Etiqueta física de tombamento patrimonial (Ex: `PAT-2026-0894`). | **Mandatório** |
| **Status** | `status` | **Lista Suspensa** | - `Planejado`<br>- `Em Estoque`<br>- `Em Uso`<br>- `Em Manutenção`<br>- `Em Descarte`<br>- `Desativado` | **Mandatório** |

---

### SEÇÃO 2: Especificações Técnicas & CMDB

| Rótulo do Campo | ID do Campo (TOPdesk) | Tipo no TOPdesk | Opções Selecionáveis da Lista Suspensa / Regra | Obrigatoriedade |
| --- | --- | --- | --- | --- |
| **Memória RAM** | `ram` | **Lista Suspensa** | - `8 GB`<br>- `16 GB`<br>- `32 GB`<br>- `64 GB` | **Mandatório** |
| **Processador** | `processador` | **Lista Suspensa** | - `AMD Ryzen 5 PRO 7530U`<br>- `AMD Ryzen 7 PRO 7730U`<br>- `Apple M3 Pro`<br>- `Intel Core i3-10100`<br>- `Intel Core i5-1335U`<br>- `Intel Core i5-1340P`<br>- `Intel Core i5-1345U`<br>- `Intel Core i5-13500`<br>- `Intel Core i7-1355U`<br>- `Intel Core i7-1365U`<br>- `Intel Core i7-13700`<br>- `Intel Core i7-13700K` | **Mandatório** |
| **Armazenamento** | `armazenamento` | **Lista Suspensa** | - `256 GB SSD SATA`<br>- `256 GB SSD NVMe`<br>- `512 GB SSD NVMe`<br>- `1 TB SSD NVMe`<br>- `2 TB SSD NVMe` | **Mandatório** |
| **Sistema Operacional** | `sistema-operacional` | **Lista Suspensa** | - `Windows 11 Pro`<br>- `Windows 10 Pro`<br>- `Linux RHEL`<br>- `macOS` | **Mandatório** |
| **Versão do SO** | `versao-do-so` | **Lista Suspensa** | - `23H2`<br>- `22H2`<br>- `22.04 LTS`<br>- `9.3`<br>- `14.4 Sonoma` | **Mandatório** |
| **IP** | `ip` | Texto (Regex) | Expressão Regular (IPv4):<br>`^((25[0-5]\|(2[0-4]\|1\d\|[1-9]\|)\d)\.){3}(25[0-5]\|(2[0-4]\|1\d\|[1-9]\|)\d)$` | Condicional |
| **MAC** | `mac` | Texto (Regex) | Expressão Regular (MAC Address):<br>`^([0-9A-Fa-f]{2}[:-]){5}([0-9A-Fa-f]{2})$` | **Mandatório** |
| **OU - Unidade Organizacional** | `ou-unidade-organizacional` | **Lista Suspensa** | - `OU=Desktops,OU=Sede,DC=embrapa,DC=br`<br>- `OU=Notebooks,OU=Sede,DC=embrapa,DC=br`<br>- `OU=Workstations,OU=Sede,DC=embrapa,DC=br`<br>- `OU=EstoqueTI,OU=Sede,DC=embrapa,DC=br`<br>- `OU=Descarte,OU=Sede,DC=embrapa,DC=br`<br>- `OU=Macs,OU=Sede,DC=embrapa,DC=br`<br>- `OU=Notebooks,OU=Agrobiologia,DC=embrapa,DC=br`<br>- `OU=Desktops,OU=MilhoESorgo,DC=embrapa,DC=br`<br>- `OU=Notebooks,OU=MilhoESorgo,DC=embrapa,DC=br`<br>- `OU=Notebooks,OU=Agroenergia,DC=embrapa,DC=br` | **Mandatório** |

---

### SEÇÃO 3: Financeiro, Contratual & Suprimentos

| Rótulo do Campo | ID do Campo (TOPdesk) | Tipo no TOPdesk | Opções Selecionáveis da Lista Suspensa / Regra | Obrigatoriedade |
| --- | --- | --- | --- | --- |
| **Fornecedor** | `fornecedor` | **Link de Entidade** *(ou Lista)* | Busca na tabela de Pessoas/Empresas do TOPdesk:<br>- `Apple Computer Brasil Ltda (00.623.904/0001-73)`<br>- `Dell Computadores do Brasil Ltda (02.321.444/0001-03)`<br>- `Hewlett Packard Brasil Ltda (04.975.667/0001-40)`<br>- `Lenovo Tecnologia Brasil Ltda (07.275.920/0001-61)`<br>- `Positivo Tecnologia S.A. (81.243.735/0001-48)` | **Mandatório** |
| **Data de Aquisição** | `data-de-compra` | Data | Data oficial da compra (Formato `YYYY-MM-DD`). | **Mandatório** |
| **Valor de Aquisição** | `valor-de-compra` | Moeda (BRL) | Custo unitário constante na Nota Fiscal. | **Mandatório** |
| **Nota Fiscal** | `nota` | Texto Curto | Número do documento fiscal. | **Mandatório** |
| **Contrato** | `contrato` | **Link de Entidade** *(ou Lista)* | Associação com a tabela de Contratos de TI (ITCM):<br>- `CT-APPLE-2025-002`<br>- `CT-DELL-2025-003`<br>- `CT-HP-2024-009`<br>- `CT-LENOVO-2025-001`<br>- `CT-POSITIVO-2023-005` | **Mandatório** |
| **Início da Garantia** | `inicio-da-garantia` | Data | Data inicial da garantia do fabricante. | **Mandatório** |
| **Fim da Garantia** | `vencimento-da-garantia` | Data | Data final da garantia do fabricante (dispara alerta). | **Mandatório** |
| **Centro de Custo** | `centro-de-custo` | **Lista Suspensa** | - `CC-10201 - Comunicação & Design`<br>- `CC-10203 - TI Governança`<br>- `CC-10204 - Suporte Operacional`<br>- `CC-10501 - Pesquisa & Desenvolvimento`<br>- `CC-10502 - Pesquisa Agronômica`<br>- `CC-10503 - Biocombustíveis` | **Mandatório** |
| **Data Prevista de Descarte** | `data-prevista-de-descarte` | Data | Data planejada para substituição tecnológica (*Hardware Refresh*). | Condicional |

---

### SEÇÃO 4: Custódia, Segurança & Compliance

| Rótulo do Campo | ID do Campo (TOPdesk) | Tipo no TOPdesk | Opções Selecionáveis da Lista Suspensa / Regra | Obrigatoriedade |
| --- | --- | --- | --- | --- |
| **Responsável pelo Ativo** | `responsavel-pelo-ativo` / `usuario` | **Link de Entidade** | Busca direta na tabela de **Pessoas** do TOPdesk. | Condicional |
| **Unidade** | `unidade` | **Lista Suspensa** | - `Embrapa Sede`<br>- `Embrapa Agrobiologia`<br>- `Embrapa Milho e Sorgo`<br>- `Embrapa Agroenergia` | **Mandatório** |
| **Localização** | `localizacao` | **Lista Suspensa** | - `Prédio Central - Sala 102`<br>- `Prédio Central - Sala 205`<br>- `Prédio Anexo - Sala 401`<br>- `Prédio Principal - Sala 108`<br>- `Prédio Administrativo - Sala 12`<br>- `Prédio de Laboratórios - Sala 110`<br>- `Prédio de Engenharia - Sala 204`<br>- `Lab Biotecnologia - Sala 03`<br>- `Estação Experimental - Campo 02`<br>- `Laboratório de Manutenção TI`<br>- `Estoque Central TI - Prateleira B2`<br>- `Depósito de Descarte TI` | **Mandatório** |
| **Data da Entrega** | `data-da-entrega` | Data | Data efetiva de entrega ao colaborador. | Condicional |
| **Termo de Responsabilidade** | `termo-de-responsabilidade` | **Lista Suspensa** | - `Aceito Digitalmente`<br>- `Aguardando Aceite no SSP`<br>- `Isento/Infra` | **Mandatório** |
| **Situação da Custódia** | `situacao-da-custodia` | **Lista Suspensa** | - `Regular`<br>- `Pendente de Aceite`<br>- `Em Devolução`<br>- `Extraviado` | **Mandatório** |
| **Classificação da Informação** | `classificacao-da-informacao` | **Lista Suspensa** | - `Pública`<br>- `Interna`<br>- `Confidencial`<br>- `Restrita` | **Mandatório** |
| **Dados Pessoais Tratados?** | `dados-pessoais-tratados` | **Lista Suspensa** | - `Sim`<br>- `Não` | **Mandatório** |
| **Situação de Compliance** | `situacao-de-compliance` | **Lista Suspensa** | - `Em Conformidade`<br>- `Não Conforme`<br>- `Em Auditoria` | **Mandatório** |
| **Data da Última Avaliação** | `data-da-ultima-avaliacao` | Data | Timestamp da última auditoria patrimonial/segurança. | Condicional |

---

### SEÇÕES 5 & 6: Grade de Relações e Documentos

| Rótulo do Campo | Tipo no TOPdesk | Descrição |
| --- | --- | --- |
| **Usuário** | Link de Entidade | Vínculo relacional com a tabela de Pessoas do TOPdesk. |
| **Localização** | Link de Entidade | Vínculo relacional com a tabela de Localização física. |
| **Software** | Link de Entidade | Vínculo relacional com a tabela de Licenças de Software (SAM). |
| **Chamado** | Link de Entidade | Vínculo com histórico de Incidentes e Requisições. |
| **Contrato** | Link de Entidade | Vínculo com o cadastro de Contratos de TI. |
| **Monitor** | Link de Entidade | Vínculo com monitores/displays acoplados. |
| **Impressora** | Link de Entidade | Vínculo com impressoras alocadas. |
| **Documentos Anexos** | Upload de Arquivos | PDF/Imagem da Nota Fiscal, Termo de Guarda, Garantia, Datasheet e Auditoria. |

---

## 3. PASSO A PASSO PARA CONFIGURAR NO TOPDESK DESIGNER DE MODELO

1. Acesse o TOPdesk como Administrador: `Configurações > Gerenciamento de Ativos > Designer de Modelo`.
2. Abra o modelo **Estação de Trabalho**.
3. Para cada campo listado como **Lista Suspensa**:
   - Clique em **Editar** no campo.
   - Em *Tipo*, selecione `Lista suspensa`.
   - Em *Opções selecionáveis*, escolha `Opções Próprias`.
   - Clique em **Adicionar opção** e insira exatamente cada valor da tabela acima.
   - Certifique-se de manter desmarcada a caixa *"Os usuários podem adicionar opções"*.
4. Clique em **Salvar Mudanças** e **Publicar**.
