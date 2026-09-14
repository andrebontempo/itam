Segue um exemplo completo de um registro de ativo utilizando apenas o conjunto mínimo recomendado.

## Registro de Ativo

### Identificação

| Campo | Valor |
| --- | --- |
| Nome do Ativo | NOTE-0123 |
| Hostname | FIN-PC-045 |
| Número de Série | PF4X9ABC12345 |
| Fabricante | Lenovo |
| Modelo | ThinkPad E14 Gen 5 |
| Tipo do Ativo | Notebook |

* * *

### Responsabilidade

| Campo | Valor |
| --- | --- |
| Usuário Principal | João da Silva |
| Departamento | Financeiro |
| Unidade | Sede Brasília |

* * *

### Situação do Ativo

| Campo | Valor |
| --- | --- |
| Status | Em uso |
| Data da Última Sincronização | 19/06/2026 08:35 |

* * *

### Dados Técnicos

| Campo | Valor |
| --- | --- |
| Sistema Operacional | Windows 11 Pro |
| Versão do Sistema Operacional | 24H2 |
| Processador | Intel Core i5-13420H |
| Memória RAM | 16 GB |
| Armazenamento Total | SSD NVMe 512 GB |
| Endereço IP | 10.10.20.45 |
| Endereço MAC | 00:1A:2B:3C:4D:5E |

* * *

## Como esse registro ajuda na prática

Imagine que um chamado chega ao Service Desk:

> "Meu computador está lento."

O analista consegue consultar rapidamente:

- Quem é o usuário responsável → João da Silva
    
- Qual equipamento está sendo utilizado → NOTE-0123
    
- Modelo do equipamento → ThinkPad E14 Gen 5
    
- Especificações → i5 + 16 GB RAM + SSD 512 GB
    
- Sistema operacional → Windows 11 Pro 24H2
    
- Última comunicação com o inventário → hoje às 08:35
    
- Endereço IP → 10.10.20.45
    

Sem precisar acessar o computador do usuário inicialmente.

* * *

## Outro exemplo (Desktop)

### Identificação

| Campo | Valor |
| --- | --- |
| Nome do Ativo | DESK-0087 |
| Hostname | RH-PC-012 |
| Número de Série | MXL456987123 |
| Fabricante | Dell |
| Modelo | OptiPlex 7010 |
| Tipo do Ativo | Desktop |

### Responsabilidade

| Campo | Valor |
| --- | --- |
| Usuário Principal | Maria Oliveira |
| Departamento | Recursos Humanos |
| Unidade | Filial Goiânia |

### Situação do Ativo

| Campo | Valor |
| --- | --- |
| Status | Em uso |
| Data da Última Sincronização | 19/06/2026 07:58 |

### Dados Técnicos

| Campo | Valor |
| --- | --- |
| Sistema Operacional | Windows 10 Pro |
| Versão do Sistema Operacional | 22H2 |
| Processador | Intel Core i3-10100 |
| Memória RAM | 8 GB |
| Armazenamento Total | SSD SATA 240 GB |
| Endereço IP | 10.20.15.87 |
| Endereço MAC | 54:BF:64:91:2A:10 |

* * *

## Relatórios que você já consegue gerar com esse conjunto mínimo

- Quantidade de notebooks por departamento.
    
- Quantidade de computadores por unidade.
    
- Máquinas com Windows 10 e Windows 11.
    
- Computadores com menos de 8 GB de RAM.
    
- Equipamentos sem sincronização há mais de 30 dias.
    
- Ativos por usuário.
    
- Inventário completo por fabricante (Dell, Lenovo, HP).
    
- Relação de IPs e hostnames.
    
- Equipamentos em estoque ou manutenção.
    

Para uma primeira implementação de ITAM no TOPdesk integrada ao OCS Inventory, esse conjunto é simples, sustentável e cobre a maioria das necessidades operacionais e de auditoria.

&nbsp;

[000 - Gestão Patrimonial x ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/000%20-%20Gestão%20Patrimonial%20x%20ITAM%20x%20CMDB.md)

[001 - ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/001%20-%20ITAM%20x%20CMDB.md)

[002 - ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM.md)

[002 - ITAM - Estação de Trabalho](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM%20-%20Estação%20de%20Trabalho.md)

[003 - ITAM - Exemplo](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/003%20-%20ITAM%20-%20Exemplo.md)

[004 - GEMINI](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/004%20-%20ITAM%20-%20Estrutura.md)

[005 - Como fica as contratações de IA](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/005%20-%20ITAM%20-%20Como%20fica%20as%20contratações%20de%20IA.md)

[006 - Proposta para o projeto](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/006%20-%20Proposta%20para%20o%20projeto.md)

[007 - Proposta para o Projeto ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/007%20-%20Proposta%20para%20o%20Projeto%20ITAM.md)