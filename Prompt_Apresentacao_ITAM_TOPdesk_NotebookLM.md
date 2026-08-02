# PROMPT PARA GERAÇÃO DE ROTEIRO DE APRESENTAÇÃO EM SLIDES NO NOTEBOOKLM

> **Como usar no NotebookLM:**
> 1. Faça o upload do documento `Implantação do IT Asset Management (ITAM) no TOPdesk.md` no seu espaço de trabalho no NotebookLM.
> 2. Copie o prompt abaixo na íntegra e cole no chat do NotebookLM.

---

```text
Você é um Especialista Sênior em Governança de TI, ITIL® 4, IT Asset Management (ITAM) e Design de Apresentações Executivas de Alto Impacto, atuando como Consultor Principal para a Diretoria Executiva e a Secretaria de TI da Embrapa (Empresa Brasileira de Pesquisa Agropecuária).

Com base exclusivamente no documento de diretrizes corporativas anexado ("Implantação do IT Asset Management (ITAM) no TOPdesk.md"), elabore um ROTEIRO COMPLETO E ESTRUTURADO DE APRESENTAÇÃO EM SLIDES voltado à aprovação pela Diretoria Executiva, pelo Comitê de Governança de TI e pelas Chefias de Administração das 43 Unidades Descentralizadas (UDs).

A apresentação deve ser persuasiva, altamente técnica, estratégica e visualmente deslumbrante, combinando rigor normativo (ITIL 4, ISO 19770, ISO 55000, LGPD, FinOps) com uma LINGUAGEM DE DESIGN MODERNA E PREMIUM (UI/UX corporativo avançado).

---

### DIRETRICES DE DESIGN MODERNO & VISUAL SYSTEM

Para CADA SLIDE, você deve incluir especificações diretas de UI/UX e Design Visual seguindo o sistema abaixo:

1. 🎨 **Paleta de Cores Premium & Tecnológica**:
   - **Background**: Dark Navy Executivo (`#0F172A`) ou Clean Crisp White (`#F8FAFC`).
   - **Cor Primária**: Verde Institucional / AgroTech (`#16A34A` / `#15803D`).
   - **Cor Secundária / Acentos**: Azul Cyan Tecnológico (`#0EA5E9`) e Índigo (`#6366F1`).
   - **Badges de Status (TOPdesk Asset Lifecycle)**:
     - Azul Cyan (`#0284C7`): `Planejado` (Em Aquisição / Pedido Emitido)
     - Verde Neon (`#22C55E`): `Disponível` / `Em Uso` (Reserva Técnica ou Em Custódia)
     - Amarelo Ocre (`#EAB308`): `Em Preparação` / `Em Empréstimo`
     - Laranja Alerta (`#F97316`): `Em Manutenção` / `Aguardando Peças`
     - Cinza Grafite (`#64748B`): `Desativado` / `Baixado` / `Descartado`

2. 📐 **Tipografia & Layout Visual Moderno**:
   - Fonte primária limpa e moderna (Inter, Outfit ou Plus Jakarta Sans).
   - Uso de **Cards com Glassmorphism** (bordas sutis translúcidas, sombras suaves e efeito fosco).
   - Layouts organizados em **Grids de 2 a 3 Colunas** para evitar blocos monolíticos de texto.
   - **Métricas e KPIs em destaque gigante (Stat Callouts)** com tipografia em negrito e rótulos curtos.
   - Uso de **Ícones SVG minimalistas** e diagramas de conectores para indicar fluxos, pilares e topologias de CMDB.

---

### ESTRUTURA EXIGIDA PARA CADA SLIDE

Estruture a resposta em exatamente **12 SLIDES EXECUTIVOS**. Para CADA SLIDE, forneça rigorosamente as seguintes 6 seções:

1. 📌 **TÍTULO DO SLIDE** (Claro, conciso e impactante)
2. 🎯 **OBJETIVO DO SLIDE** (Objetivo estratégico da mensagem)
3. 🎨 **LAYOUT & DESIGN SUGERIDO (UI/UX)** (Instruções detalhadas de design, esquema de cores, disposição de cards, grid, badges e componentes gráficos)
4. 🖼️ **CONTEÚDO VISUAL DA TELA** (Bullet points curtos, tabelas formatadas, diagramas de fluxo em blocos ou visualizadores de dados)
5. 📊 **CAMPOS OBRIGATÓRIOS / KPIS / FÓRMULAS DE DESTAQUE** (Se aplicável ao tema do slide)
6. 🎙️ **SCRIPT DE FALA DO APRESENTADOR** (Discurso fluído, profissional, envolvente e altamente persuasivo em Português do Brasil)

---

### ESTRUTURA DOS 12 SLIDES A SEREM GERADOS:

- **Slide 1: Capa Executiva & Co-criação de Valor (ITIL® 4)**
  - Título: Diretrizes Corporativas para Implementação da Gestão de Ativos de TI (ITAM) no TOPdesk.
  - Design: Dark mode sofisticado, logo institucional Embrapa, badge "Proposta Executiva v3.0", alinhamento da TI com a Pesquisa Agropecuária (PD&I) sob o conceito de Co-criação de Valor (ITIL 4).

- **Slide 2: O Desafio Institucional & As Quatro Dimensões do ITAM**
  - Desafio da dispersão geográfica nacional (Sede + 43 UDs) e otimização orçamentária.
  - As 4 Dimensões do ITAM (Organizações e Pessoas, Informação e Tecnologia, Parceiros e Fornecedores, Fluxos de Valor e Processos) organizadas em um grid 2x2 em cards translúcidos.

- **Slide 3: Por que o TOPdesk Asset Management? (Single Source of Truth & Módulo Flexível)**
  - O Módulo Flexível de Ativos do TOPdesk como repositório central unificado (*Single Source of Truth*).
  - Eliminação de silos informacionais, integração nativa ao Service Desk e automação via Action Sequences e APIs REST.

- **Slide 4: Os Quatro Pilares do Programa ITAM Corporativo**
  - Visão geral integrada dos 4 pilares: HAM (Hardware Asset Management), SAM (Software Asset Management), Cloud/FinOps (Gestão de Nuvem) e ITCM (IT Contract Management).
  - Cards detalhando a abrangência desde Endpoints/Data Center até Licenças Científicas (MATLAB, ArcGIS, SAS) e Contratos de Suporte.

- **Slide 5: Aceite Digital do Termo de Responsabilidade no SSP**
  - Substituição do papel por fluxo nativo no Portal de Autoatendimento (SSP) do TOPdesk.
  - Infográfico do fluxo em 4 etapas (TI altera status para Disponível -> Tarefa criada no SSP -> Aceite do Colaborador -> Atualização automática para "Em Uso" com log de IP, Data/Hora e e-mail).

- **Slide 6: Diferenciação Estratégica: ITAM vs. CMDB no TOPdesk**
  - Matriz comparativa entre ITAM (Visão Financeira/Patrimonial - "Quanto custou e quem é o dono?") e CMDB (Visão Operacional/CIs - "Como está conectado e qual o impacto?").
  - Consolidação no mesmo Cartão de Ativo do TOPdesk com segregação de perfis de acesso via Abas (Aba Operacional vs. Aba Financeira/Administrativa).

- **Slide 7: Mapeamento de Dependências (CMDB) & Gestão de "Ativos Limões"**
  - Diagrama de conectores de dependências (On-Premise vs. Nuvem/Microserviços) e análise de impacto em Mudanças (Change Management).
  - Vinculação obrigatória de Ativos/CIs em Incidentes e Requisições para identificação automática de "Ativos Limões" (equipamentos com alta reincidência de falhas) e aceleração de *Hardware Refresh*.

- **Slide 8: Cloud Asset Management (FinOps) & Alertas via Webhooks**
  - Delimitação arquitetural: TOPdesk mantém metadados estruturais e Centros de Custo (sem sobrecarga de telemetria fina de consumo diário).
  - Régua de alertas preventivos de orçamento (80%, 90% e 100% Estouro) e integração de Webhooks disparando chamados automáticos de incidentes para intervenção da infraestrutura em picos de consumo (*spend spikes*).

- **Slide 9: Arquitetura de Integrações & Regras de Conciliação (Reconciliation Rules)**
  - Diagrama de integrações: TOPdesk conectado a Ferramentas de Descoberta (Intune, Lansweeper), Diretório de Identidades (Entra ID / AD) e Provedores Cloud (AWS, Azure, GCP).
  - Tabela de Regras de Conciliação de Dados definindo prioridade de gravação entre fontes automáticas (specs técnicas) e cadastros manuais/workflows (metadados de negócio e centro de custo).

- **Slide 10: Governança, Matriz RACI, LGPD e Sanitização de Mídias (Wiping)**
  - Matriz RACI sintetizando papéis (Governança, Operação TI, Compras, Patrimônio e Usuários/Gestores).
  - Conformidade com LGPD (retenção por interesse legítimo, restrição de acesso a histórico de custódia e anonimização na desativação) e Laudo de Sanitização (*Wiping* ISO 27001) com Certificado de Destruição Ambiental.

- **Slide 11: Modelo de Maturidade (Níveis 1 a 5) & Régua de Alertas Contratuais (ITCM)**
  - Evolução tática de maturidade (alcançar Nível 4 - Controlado em 18 meses).
  - Régua de alertas contratuais de antecedência no TOPdesk (120, 90, 60 e 30 dias antes do vencimento) para mitigar interrupções de SLA e suporte.

- **Slide 12: KPIs Executivos & Solicitação de Aprovação**
  - Stat Callouts com fórmulas em LaTeX: Taxa de Cobertura de Inventário ($\text{TCI} > 98\%$), Índice de Ociosidade SAM ($\text{IOL} < 5\%$), Desvio Orçamentário Cloud ($\Delta_{\text{Budget}} \le 0$) e Taxa de Aceite Digital ($\text{TAD} = 100\%$).
  - Solicitação formal de aprovação da Diretoria Executiva para início da implantação do programa no TOPdesk.

---

Gere a apresentação completa seguindo rigorosamente a estrutura de 6 seções por slide e o guia de design moderno.
```
