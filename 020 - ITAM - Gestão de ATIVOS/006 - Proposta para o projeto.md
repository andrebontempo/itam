# DOCUMENTO BASE: DIRETRIZES DE IMPLEMENTAÇÃO DO ITAM (GESTÃO DE ATIVOS DE TI)

Este documento estabelece a estrutura conceitual e operacional para o projeto de implantação da Gestão de Ativos de TI (**ITAM**). A estrutura foi desenhada para garantir o controle total sobre o ciclo de vida, a conformidade legal (compliance), a eficiência financeira e a governança de todos os recursos tecnológicos.

O projeto será regido por **4 pilares fundamentais**, detalhados a seguir com suas respectivas regras de categorização e exemplos práticos de registro.

## 1\. Hardware Asset Management (HAM)

**Descrição:** Responsável pelo controle físico, financeiro e contratual de todos os ativos tangíveis de tecnologia, desde o momento do recebimento até o descarte ecológico e homologado. O foco principal é evitar perdas físicas, otimizar o ciclo de renovação tecnológica (refresh) e gerenciar a atribuição de equipamentos aos colaboradores.

### Exemplos de Registro:

- **Exemplo 1 (User Endpoints):**
    
    - **Identificador/Patrimônio:** PAT-2026-0894
        
    - **Ativo:** Notebook Dell Latitude 3440 (Intel i5, 16GB RAM, 512GB SSD)
        
    - **Status/Atribuição:** Em uso (Atribuído ao colaborador Andre Luiz Bontempo)
        
- **Exemplo 2 (Infraestrutura/Data Center):**
    
    - **Identificador/Patrimônio:** SRV-0042
        
    - **Ativo:** Servidor Físico HPE ProLiant DL380 Gen10
        
    - **Status/Atribuição:** Em produção (Rack 04 - Data Center Principal)
        
- **Exemplo 3 (Periféricos/Redundância):**
    
    - **Identificador/Patrimônio:** NOB-0115
        
    - **Ativo:** Nobreak APC Smart-UPS BR 1500VA
        
    - **Status/Atribuição:** Em estoque / Reserva Técnica
        

## 2\. Software Asset Management (SAM / SaaS)

**Descrição:** Focado na governança de propriedade intelectual, conformidade de licenças instaladas localmente (On-Premise) e gerenciamento de assinaturas em nuvem de preço fixo por usuário (SaaS). O objetivo principal deste pilar é mitigar riscos em auditorias de fabricantes e eliminar o desperdício de licenças pagas que não estão sendo utilizadas.

### Exemplos de Registro:

- **Exemplo 1 (SaaS / Licenciamento Fixo):**
    
    - **Nome do Ativo:** Microsoft 365 Business Premium
        
    - **Tipo/Métricas:** Assinatura Mensal (Preço Fixo por Usuário)
        
    - **Volume/Alocação:** 150 Licenças Contratadas (132 Ativas / 18 Disponíveis)
        
- **Exemplo 2 (Ferramentas de Desenvolvimento / SaaS):**
    
    - **Nome do Ativo:** GitHub Enterprise Cloud
        
    - **Tipo/Métricas:** Assinatura Anual (Preço Fixo por Assento de Desenvolvedor)
        
    - **Volume/Alocação:** 25 Assentos Ativos
        
- **Exemplo 3 (IA por Assinatura / Preço Fixo):**
    
    - **Nome do Ativo:** OpenAI ChatGPT Enterprise
        
    - **Tipo/Métricas:** Assinatura Mensal Corporativa (Licença Fixa)
        
    - **Volume/Alocação:** 10 Licenças Atribuídas à equipe de Produto/Inovação
        

## 3\. Serviços em Nuvem (Cloud / FinOps)

**Descrição:** Destinado ao monitoramento e controle de recursos intangíveis baseados em consumo elástico, sob demanda ou por telemetria (IaaS, PaaS e APIs). Diferente do pilar de Software, os ativos aqui não são contabilizados por "assentos de usuários", mas sim por volume de tráfego, processamento de dados e requisições, exigindo políticas rígidas de orçamento para evitar estouros orçamentários dinâmicos.

### Exemplos de Registro:

- **Exemplo 1 (Infraestrutura em Nuvem Pública):**
    
    - **Nome do Ativo:** AWS EC2 & RDS (Instâncias de Produção)
        
    - **Métrica de Consumo:** Horas de computação de CPU/Memória e GB de armazenamento por mês
        
    - **Regra de Alerta:** Notificação automática ao atingir 80% do orçamento mensal projetado
        
- **Exemplo 2 (IA por Demanda / Consumo de Tokens):**
    
    - **Nome do Ativo:** OpenAI API (Integração de Sistemas Corporativos)
        
    - **Métrica de Consumo:** Volume de requisições / Cobrança dinâmica por Milhões de Tokens (Input/Output)
        
    - **Regra de Alerta:** Bloqueio de requisições ou Alerta Crítico se o gasto diário ultrapassar a meta estabelecida
        
- **Exemplo 3 (Plataforma como Serviço / PaaS):**
    
    - **Nome do Ativo:** MongoDB Atlas (Banco de Dados em Nuvem)
        
    - **Métrica de Consumo:** Armazenamento, IOPS e transferência de dados na rede
        
    - **Regra de Alerta:** Monitoramento de picos de tráfego e escalonamento automático de nível
        

## 4\. Contratos e Ciclo de Vida (ITCM)

**Descrição:** Funciona como a camada de inteligência legal, financeira e administrativa que ampara os três pilares anteriores. Este pilar armazena contratos de aquisição, termos de confidencialidade (NDAs), garantias de hardware, acordos de nível de serviço (SLA) de consultorias externas e obrigações recorrentes de telecomunicações.

### Exemplos de Registro:

- **Exemplo 1 (Contrato de Suporte de Hardware):**
    
    - **ID do Contrato:** CT-DELL-2025-003
        
    - **Objeto:** Cobertura de Garantia Dell ProSupport (Atrelada aos ativos de User Endpoints)
        
    - **Vencimento/Aviso:** Expira em 15/12/2028 (Gatilho de alerta de renovação 90 dias antes)
        
- **Exemplo 2 (Contrato de Links de Telecomunicação):**
    
    - **ID do Contrato:** CT-CLARO-2026-A
        
    - **Objeto:** Link Dedicado de Internet 1Gbps + Serviços de Telefonia Corporativa
        
    - **Vencimento/Aviso:** Renovação automática anual com reajuste pelo IGPM
        
- **Exemplo 3 (Contrato de Prestação de Serviços / Outsourcing):**
    
    - **ID do Contrato:** CT-CONSULT-04
        
    - **Objeto:** Suporte terceirizado e administração de banco de dados (SLA de atendimento de 2h para chamados críticos)
        
    - **Vencimento/Aviso:** Expira em 31/01/2027 (Necessita de revisão de escopo prévia)
        

## Próximos Passos do Projeto

Com este documento base aprovado e alinhado com as melhores práticas de mercado, as fases consecutivas da implantação do ITAM seguirão o seguinte cronograma lógico:

1.  **Escolha da Ferramenta:** Definição do software centralizador (CMDB/ITAM) que comportará esta estrutura de dados.
    
2.  **Inventário Inicial (Discovery):** Varredura automática e manual da rede para capturar os primeiros registros físicos e de software.
    
3.  **Desenho de Processos:** Criação dos fluxos formais de Entrada de Ativos (Compras), Movimentação (Termos de Responsabilidade) e Saída (Descarte ou Cancelamento).
    

[000 - Gestão Patrimonial x ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/000%20-%20Gestão%20Patrimonial%20x%20ITAM%20x%20CMDB.md)

[001 - ITAM x CMDB](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/001%20-%20ITAM%20x%20CMDB.md)

[002 - ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM.md)

[002 - ITAM - Estação de Trabalho](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/002%20-%20ITAM%20-%20Estação%20de%20Trabalho.md)

[003 - ITAM - Exemplo](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/003%20-%20ITAM%20-%20Exemplo.md)

[004 - GEMINI](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/004%20-%20ITAM%20-%20Estrutura.md)

[005 - Como fica as contratações de IA](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/005%20-%20ITAM%20-%20Como%20fica%20as%20contratações%20de%20IA.md)

[006 - Proposta para o projeto](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/006%20-%20Proposta%20para%20o%20projeto.md)

[007 - Proposta para o Projeto ITAM](../020%20-%20ITAM%20-%20Gestão%20de%20ATIVOS/007%20-%20Proposta%20para%20o%20Projeto%20ITAM.md)