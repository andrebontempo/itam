O ITAM (IT Asset Management) não é apenas um inventário; ele é o processo de controlar todo o ciclo de vida dos ativos de TI: aquisição, uso, movimentação, manutenção, renovação e descarte.

O objetivo principal é responder perguntas como:

- Quais ativos de TI a empresa possui?
    
- Quem está usando cada ativo?
    
- Onde ele está?
    
- Quanto custou?
    
- Quando vence a garantia?
    
- Quando deve ser substituído?
    
- Quais licenças estão em uso?
    
- Quais ativos estão parados ou em estoque?
    

### Quais ativos entram no ITAM?

### 1\. Hardware

| Entra | Normalmente não entra |
| --- | --- |
| Notebooks | Mouse |
| Desktops | Teclado |
| Servidores | Cabos |
| Switches | Adaptadores |
| Roteadores | Carregadores comuns |
| Firewalls | Webcam barata |
| Access Points | —   |
| Smartphones corporativos | —   |
| Tablets | —   |
| Storages | —   |
| Monitores (opcional) | —   |

### 2\. Software

- Windows
    
- Microsoft 365
    
- Adobe
    
- AutoCAD
    
- Antivírus
    
- ERP
    
- CRM
    
- Ferramentas SaaS
    

### 3\. Serviços e contratos

- VPS Hostinger
    
- AWS
    
- Azure
    
- Google Workspace
    
- Domínios
    
- Certificados SSL
    
- Links de internet
    
- Contratos de suporte
    

### Estrutura de um registro ITAM

### Exemplo 1 — Notebook de usuário

Hardware

Campos recomendados

| Campo | Exemplo |
| --- | --- |
| ID do ativo | NB-00231 |
| Tipo | Notebook |
| Fabricante | Lenovo |
| Modelo | ThinkPad E14 Gen 5 |
| Número de série | PF4X9ABC |
| Patrimônio | TI-4587 |
| Usuário | João Silva |
| Departamento | Financeiro |
| Localização | Brasília - Matriz |
| Data de compra | 10/03/2025 |
| Valor | R\$ 4.800,00 |
| Garantia | 10/03/2028 |
| Status | Em uso |
| Sistema operacional | Windows 11 Pro |
| Observações | SSD 512 GB / 16 GB RAM |

### Exemplo 2 — Servidor

Infraestrutura

Registro

| Campo | Exemplo |
| --- | --- |
| ID  | SRV-0007 |
| Nome | srv-glpi |
| Fabricante | Dell |
| Modelo | PowerEdge R450 |
| Serial | 8H3K92 |
| CPU | Xeon Silver |
| RAM | 64 GB |
| Armazenamento | 2x SSD 960 GB RAID1 |
| SO  | Ubuntu Server 24.04 |
| Localização | CPD Matriz |
| Garantia | 15/09/2027 |
| Status | Produção |

### Exemplo 3 — Switch

Rede

Registro

| Campo | Exemplo |
| --- | --- |
| ID  | SW-0012 |
| Modelo | TP-Link SG3428 |
| IP de gerenciamento | 10.0.0.10 |
| Firmware | 1.0.8 |
| Localização | Rack 01 |
| Status | Ativo |

### Exemplo 4 — Licença Microsoft 365

Software

Registro

| Campo | Exemplo |
| --- | --- |
| ID  | LIC-0365-001 |
| Produto | Microsoft 365 Business Standard |
| Quantidade comprada | 50  |
| Quantidade em uso | 42  |
| Fornecedor | Microsoft |
| Vencimento | 01/02/2027 |
| Custo mensal | R\$ 1.850,00 |

### Exemplo 5 — VPS / Cloud

Serviço

Registro

| Campo | Exemplo |
| --- | --- |
| ID  | VPS-0003 |
| Fornecedor | Hostinger |
| Plano | VPS 4 vCPU / 16 GB |
| IP  | xxx.xxx.xxx.xxx |
| Custo mensal | R\$ 129,90 |
| Renovação | 12/06/2027 |
| Serviços hospedados | GLPI, n8n, Vaultwarden |

### Ciclo de vida do ativo

O grande diferencial do ITAM é acompanhar o ativo do começo ao fim.

Compra | Recebimento | Implantação | Manutenção | Transferência | Estoque | Descarte

### Quais campos são realmente essenciais?

### Mínimo viável para começar

- ID do ativo
    
- Tipo
    
- Fabricante e modelo
    
- Número de série
    
- Usuário responsável
    
- Localização
    
- Data de compra
    
- Garantia
    
- Status
    
- Valor
    

### Minha recomendação para sua implantação

### Comece registrando apenas

- Notebooks e desktops
    
- Servidores
    
- Equipamentos de rede
    
- Licenças Microsoft
    
- Domínios
    
- Certificados
    
- VPS e serviços cloud
    

### Não registre inicialmente

- Mouse
    
- Teclado
    
- Cabos
    
- Headsets baratos
    
- Periféricos de baixo valor
    

### Resultado prático

Com isso você terá um ITAM enxuto e útil, capaz de responder rapidamente:

- Quantos notebooks temos?
    
- Quem está com cada equipamento?
    
- Quais garantias vencem este ano?
    
- Quais licenças estão sobrando?
    
- Quanto custa a infraestrutura de TI?
    
- Quais ativos precisam ser substituídos?
    

Se quiser, no próximo passo posso te mostrar como modelar isso no GLPI (entidades, tipos de ativos, campos obrigatórios e automações) para você já começar a implantação da forma correta.

[000 - Gestão Patrimonial x ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/000%20-%20Gestão%20Patrimonial%20x%20ITAM%20x%20CMDB.md)

[001 - ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/001%20-%20ITAM%20x%20CMDB.md)

[002 - ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM.md)

[002 - ITAM - Estação de Trabalho](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM%20-%20Estação%20de%20Trabalho.md)

[003 - ITAM - Exemplo](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/003%20-%20ITAM%20-%20Exemplo.md)

[004 - GEMINI](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/004%20-%20ITAM%20-%20Estrutura.md)

[005 - Como fica as contratações de IA](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/005%20-%20ITAM%20-%20Como%20fica%20as%20contratações%20de%20IA.md)

[006 - Proposta para o projeto](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/006%20-%20Proposta%20para%20o%20projeto.md)

[007 - Proposta para o Projeto ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/007%20-%20Proposta%20para%20o%20Projeto%20ITAM.md)