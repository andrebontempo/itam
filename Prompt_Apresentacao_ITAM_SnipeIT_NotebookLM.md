# PROMPT PARA GERAÇÃO DE ROTEIRO DE APRESENTAÇÃO EM SLIDES NO NOTEBOOKLM

> **Como usar no NotebookLM:**
> 1. Faça o upload do documento `Implantação do IT Asset Management (ITAM) no Snipe-IT.md` no seu espaço de trabalho no NotebookLM.
> 2. Copie o prompt abaixo na íntegra e cole no chat do NotebookLM.

---

```text
Você é um Especialista Sênior em Governança de TI, ITIL® 4, IT Asset Management (ITAM) e Design de Apresentações Executivas de Alto Impacto, atuando como Consultor Principal para a Diretoria Executiva e a Secretaria de TI da Embrapa (Empresa Brasileira de Pesquisa Agropecuária).

Com base exclusivamente no documento de diretrizes corporativas anexado ("Implantação do IT Asset Management (ITAM) no Snipe-IT.md"), elabore um ROTEIRO COMPLETO E ESTRUTURADO DE APRESENTAÇÃO EM SLIDES voltado à aprovação pela Diretoria Executiva, pelo Comitê de Governança de TI e pelas Chefias de Administração das 43 Unidades Descentralizadas (UDs).

A apresentação deve ser persuasiva, altamente técnica, estratégica e visualmente deslumbrante, combinando rigor normativo (ITIL 4, ISO 19770, LGPD, FinOps) com uma LINGUAGEM DE DESIGN MODERNA E PREMIUM (UI/UX corporativo avançado).

---

### DIRETRICES DE DESIGN MODERNO & VISUAL SYSTEM

Para CADA SLIDE, você deve incluir especificações diretas de UI/UX e Design Visual seguindo o sistema abaixo:

1. 🎨 **Paleta de Cores Premium & Tecnológica**:
   - **Background**: Dark Navy Executivo (`#0F172A`) ou Clean Crisp White (`#F8FAFC`).
   - **Cor Primária**: Verde Institucional / AgroTech (`#16A34A` / `#15803D`).
   - **Cor Secundária / Acentos**: Azul Cyan Tecnológico (`#0EA5E9`) e Índigo (`#6366F1`).
   - **Badges de Status (Snipe-IT)**:
     - Verde Neon (`#22C55E`): `Deployable` (Em Uso / Pronto para Uso)
     - Amarelo Ocre (`#EAB308`): `Pending` (Em Aquisição / Staging)
     - Laranja Alerta (`#F97316`): `Undeployable` (Em Assistência / Manutenção)
     - Cinza Grafite (`#64748B`): `Archived` (Descartado / Sanitizado)

2. 📐 **Tipografia & Layout Visual Moderno**:
   - Fonte primária limpa e moderna (Inter, Outfit ou Plus Jakarta Sans).
   - Uso de **Cards com Glassmorphism** (bordas sutis translúcidas, sombras suaves e efeito fosco).
   - Layouts organizados em **Grids de 2 a 3 Colunas** para evitar blocos monolíticos de texto.
   - **Métricas e KPIs em destaque gigante (Stat Callouts)** com tipografia em negrito e rótulos curtos.
   - Uso de **Ícones SVG minimalistas** para indicar fluxos, pilares e categorias.

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

- **Slide 1: Capa Executiva & Visão Geral Estratégica**
  - Título: Diretrizes Corporativas para Gestão de Ativos de TI (ITAM) na Embrapa com Snipe-IT.
  - Design: Dark mode sofisticado, logo institucional, badge "Proposta Executiva v3.0", subtítulo com abrangência (Sede + 43 UDs).

- **Slide 2: O Desafio Institucional & A Visão ITIL® 4**
  - Desafio da dispersão geográfica nacional (43 UDs) e opacidade orçamentária.
  - As 4 Dimensões do ITAM na Embrapa (Pessoas, Tecnologia, Parceiros e Processos) apresentadas em um grid 2x2 em cards translúcidos.

- **Slide 3: Por que o Snipe-IT? (Arquitetura Multi-Company & Autonomia)**
  - Plataforma Open-Source Enterprise sem custo de licenciamento.
  - Suporte nativo *Multi-Company* (`full_multiple_companies_support = true`), combinando visibilidade corporativa para a Sede e autonomia operacional para as 43 UDs.

- **Slide 4: Escopo Corporativo Exclusivo de TI**
  - Restrição estrita a recursos tecnológicos: Hardware (HAM), Licenciamento (SAM), Cloud (FinOps) e Contratos (ITCM).
  - Cards visuais segregando Endpoints de Pesquisa, Infraestrutura de Data Center, Equipamentos Científicos de Campo e Licenças de Alto Valor.

- **Slide 5: Aceite Digital do Termo de Responsabilidade (EULA Nativo)**
  - Eliminação do papel: fluxo automático por e-mail, assinatura digital, log inalterável (IP, Timestamp, AD).
  - Infográfico do fluxo em 5 etapas e métrica de cobrança em 48h.

- **Slide 6: Dicionário de Dados – Campos Nativos Globais Obrigatórios**
  - Tabela moderna estilo dashboard apresentando a matriz de preenchimento obrigatório no Snipe-IT (Asset Tag, Model, Status Label, Serial Number, Company, Location, Purchase Date/Cost, Supplier, Order Number, Warranty).

- **Slide 7: Dicionário de Dados – Custom Fieldsets por Categoria de TI**
  - Layout em abas/cards comparativos: Endpoints (HostName, MAC, BitLocker, Processo SEI), Servidores/Data Center (IP Out-of-Band iDRAC/iLO, Rack/U, Cofre de Senhas), Dispositivos Móveis (IMEI 1/2, ICCID, MDM) e Equipamentos Científicos (Projeto SEG, Pesquisador Responsável).

- **Slide 8: Gestão de Licenças e Softwares Científicos (SAM)**
  - Monitoramento de licenças corporativas e científicas de alto valor (ArcGIS, MATLAB, SAS, SPSS).
  - Controle de assentos (*Seats*), recolheita de licenças ociosas (*License Harvesting*) e alertas de expiração.

- **Slide 9: Governança, LGPD e Sanitização de Mídias (Wiping)**
  - Exigência de Laudo Técnico de Sanitização (*Wiping* NIST SP 800-88 / DoD) antes da baixa.
  - Certificado de Destruição Ecológica (Logística Reversa) e desvinculação de dados pessoais (LGPD).

- **Slide 10: Protocolo Inter-UDs & Integração Snipe-IT (ITAM) <-> ITSM (CMDB)**
  - Fluxo de transferência de ativos entre UDs via SEI e Snipe-IT.
  - Separação clara: Snipe-IT como *Single Source of Truth* do ITAM (financeiro/patrimonial) e ITSM corporativo via API REST para a CMDB (topologia operacional e chamados de incidentes/ativos "limões").

- **Slide 11: Plano de Rollout Regional em 4 Fases (12 Meses)**
  - Timeline horizontal moderna: Fase 1 (Infra/Sede/Piloto), Fase 2 (Onda 1 Sul/Sudeste), Fase 3 (Onda 2 CO/Nordeste), Fase 4 (Onda 3 Norte e SAM Consolidados).

- **Slide 12: KPIs Executivos & Aprovação Solicitada**
  - Stat Callouts com fórmulas em LaTeX: Taxa de Cobertura de Inventário ($\text{TCI} > 98\%$), Taxa de Aceite Digital ($\text{TAD} = 100\%$), Ociosidade SAM ($\text{TOL} < 5\%$) e Desvio Orçamentário Cloud ($\Delta_{\text{Budget}} \le 0$).
  - Solicitação formal de aprovação da Diretoria Executiva para início da Fase 1.

---

Gere a apresentação completa seguindo rigorosamente a estrutura de 6 seções por slide e o guia de design moderno.
```
