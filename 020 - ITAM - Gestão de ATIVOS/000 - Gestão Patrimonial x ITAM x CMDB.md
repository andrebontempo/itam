Essa é uma dúvida muito importante. Se você registrar **todos os bens da empresa**, realmente estará fazendo apenas um controle patrimonial.

A gestão de ativos de TI (IT Asset Management - ITAM) e a gestão de configuração (Configuration Management - CMDB) têm objetivos diferentes.

### 1\. Gestão Patrimonial

Pergunta principal:

> "O que a empresa possui e quanto vale?"

Exemplos:

- Mesa
    
- Cadeira
    
- Ar-condicionado
    
- Impressora
    
- Notebook
    
- Monitor
    

Foco:

- Valor contábil
    
- Depreciação
    
- Localização física
    
- Responsável
    

* * *

### 2\. Gestão de Ativos de TI (ITAM)

Pergunta principal:

> "Quais recursos de TI a empresa possui, quem utiliza e qual o seu ciclo de vida?"

Você registra apenas ativos relevantes para a área de TI.

#### Hardware

- Notebooks
    
- Desktops
    
- Servidores
    
- Storages
    
- Switches
    
- Roteadores
    
- Firewalls
    
- Access Points
    
- Smartphones corporativos
    
- Tablets
    
- Monitores (opcional)
    
- Impressoras de rede (opcional)
    

#### Software

- Licenças do Windows
    
- Licenças Office/Microsoft 365
    
- Adobe
    
- AutoCAD
    
- Antivírus
    
- Sistemas corporativos
    

#### Serviços

- VPS
    
- Servidores cloud
    
- Links de internet
    
- Certificados SSL
    
- Domínios
    
- Assinaturas SaaS
    

#### Informações importantes

- Número de série
    
- Fabricante
    
- Modelo
    
- Responsável
    
- Centro de custo
    
- Data de compra
    
- Garantia
    
- Status (ativo, estoque, manutenção, descarte)
    
- Contrato associado
    

* * *

### 3\. Gestão de Configuração (CMDB)

Pergunta principal:

> "Como os componentes de TI se relacionam entre si?"

Aqui você registra os chamados **Itens de Configuração (Configuration Items - CI)**.

Exemplo:

Servidor:

- srv-glpi

Aplicação:

- GLPI

Banco:

- MariaDB

Infraestrutura:

- VPS Hostinger

Relacionamentos:

```
GLPI
 ↓
MariaDB
 ↓
Servidor Linux
 ↓
VPS Hostinger
```

Se a VPS cair, você sabe imediatamente quais serviços serão impactados.

* * *

## O que normalmente entra em uma CMDB

### Infraestrutura

- Servidores físicos
    
- Máquinas virtuais
    
- Containers Docker
    
- Storages
    
- Switches
    
- Firewalls
    
- Links de internet
    

### Sistemas

- GLPI
    
- n8n
    
- Zabbix
    
- Vaultwarden
    
- Joplin Server
    
- ERP
    
- CRM
    

### Serviços

- DNS
    
- E-mail
    
- VPN
    
- Active Directory
    
- Banco de dados
    

### Cloud

- VPS
    
- Instâncias cloud
    
- Buckets de armazenamento
    
- Balanceadores
    

### Documentação

- Certificados digitais
    
- Domínios
    
- Contratos de suporte
    

* * *

## O que normalmente NÃO entra

Normalmente não vale a pena registrar:

- Mouse
    
- Teclado
    
- Webcam
    
- Headset
    
- Cabos
    
- Adaptadores
    
- Carregadores
    
- Cadeiras
    
- Mesas
    

A menos que sejam itens de alto valor ou sujeitos a controle rigoroso.

* * *

## Regra prática

Uma boa pergunta é:

> "Se este item falhar, ele pode causar indisponibilidade de um serviço de TI?"

Se a resposta for sim, provavelmente deve estar na CMDB.

Exemplos:

| Item | ITAM | CMDB |
| --- | --- | --- |
| Notebook de usuário | Sim | Geralmente não |
| Servidor Linux | Sim | Sim |
| Switch Core | Sim | Sim |
| Licença Microsoft 365 | Sim | Não |
| Domínio da empresa | Sim | Sim |
| VPS Hostinger | Sim | Sim |
| Mouse USB | Não | Não |
| GLPI | Não | Sim |
| Banco de dados MariaDB | Não | Sim |
| Certificado SSL | Sim | Sim |

* * *

Para uma empresa de porte médio, especialmente se você estiver usando o GLPI, uma abordagem eficiente é:

1.  **ITAM** para controlar:
    
    - Computadores
        
    - Servidores
        
    - Equipamentos de rede
        
    - Licenças
        
    - Contratos
        
    - Domínios
        
    - Certificados
        
2.  **CMDB** para mapear:
    
    - Serviços de negócio
        
    - Aplicações
        
    - Bancos de dados
        
    - Servidores
        
    - Infraestrutura cloud
        
    - Dependências entre componentes
        

Assim você evita transformar o projeto em um simples inventário patrimonial e passa a ter uma visão operacional da infraestrutura e dos serviços de TI.

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