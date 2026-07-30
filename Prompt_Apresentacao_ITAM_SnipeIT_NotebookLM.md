# PROMPT PARA GERAÇÃO DE ROTEIRO DE APRESENTAÇÃO EM SLIDES NO NOTEBOOKLM

> **Como usar no NotebookLM:**
> 1. Faça o upload do documento `Implantação do IT Asset Management (ITAM) no Snipe-IT.md` no seu espaço de trabalho no NotebookLM.
> 2. Copie o prompt abaixo na íntegra e cole no chat do NotebookLM.

---

```text
Você é um Especialista Sênior em Governança de TI, ITIL® 4 e IT Asset Management (ITAM), atuando como Consultor Principal para a Diretoria Executiva e a Secretaria de TI da Embrapa (Empresa Brasileira de Pesquisa Agropecuária).

Com base exclusivamente no documento de diretrizes corporativas anexado ("Implantação do IT Asset Management (ITAM) no Snipe-IT.md"), elabore um ROTEIRO COMPLETO E ESTRUTURADO DE APRESENTAÇÃO EM SLIDES para ser apresentado à Diretoria Executiva, ao Comitê de Governança de TI e às Chefias de Administração das 43 Unidades Descentralizadas (UDs).

A apresentação deve ser persuasiva, altamente técnica e executiva, demonstrando o valor estratégico, o retorno sobre o investimento, a mitigação de riscos fiscais/LGPD e a padronização operacional proporcionada pela plataforma Snipe-IT.

Estruture a resposta em exatamente 12 SLIDES. Para CADA SLIDE, forneça rigorosamente a seguinte estrutura:

1. 📌 TÍTULO DO SLIDE
2. 🎯 OBJETIVO DO SLIDE
3. 🖼️ CONTEÚDO VISUAL (Bullet points sintéticos para a tela, tabelas ou esquemas gráficos)
4. 📊 CAMPOS OBRIGATÓRIOS / KPIS DE DESTAQUE (Se aplicável ao tema do slide)
5. 🎙️ SCRIPT DE FALA DO APRESENTADOR (Discurso fluído, profissional e convincente em Português do Brasil)

---

### ESTRUTURA DOS 12 SLIDES A SEREM GERADOS:

- **Slide 1: Capa Executiva & Visão Geral**
  - Título: Diretrizes Corporativas para Gestão de Ativos de TI (ITAM) na Embrapa com Snipe-IT.
  - Contexto: Sede + 43 Unidades Descentralizadas (UDs).

- **Slide 2: O Desafio Institucional & A Visão ITIL® 4**
  - O problema da descentralização geográfica e opacidade orçamentária.
  - As 4 Dimensões do ITAM na Embrapa (Pessoas, Tecnologia, Parceiros e Fluxos de Valor).

- **Slide 3: Por que o Snipe-IT? (Arquitetura & Vantagens)**
  - Solução Open-Source Enterprise, sem custo de licença.
  - Suporte Multi-Company (`full_multiple_companies_support = true`) unindo controle central da Sede e autonomia das 43 UDs.

- **Slide 4: Escopo Corporativo de Ativos**
  - Categorização: Endpoints de Pesquisa, Infraestrutura de Data Center, Equipamentos Científicos de Campo (GNSS/Drones), Licenças SAM e Insumos.

- **Slide 5: Aceite Digital do Termo de Responsabilidade (EULA Nativo)**
  - Eliminação do papel: envio por e-mail, assinatura digital, log de auditoria inalterável (IP, Timestamp, AD).
  - Régua de cobrança automática em 48h.

- **Slide 6: Dicionário de Dados – Campos Nativos Globais Obrigatórios**
  - Apresentação da matriz de preenchimento obrigatório para todos os ativos de hardware (Asset Tag, Model, Status Label, Serial Number, Company, Location, Purchase Date/Cost, Supplier, Order Number/NF, Warranty).

- **Slide 7: Dicionário de Dados – Custom Fieldsets por Categoria**
  - Detalhamento dos campos obrigatórios customizados: Endpoints (HostName, MAC, Processo SEI, BitLocker), Servidores (IP Out-of-Band iDRAC/iLO, Rack/U, Cofre de Senhas), Dispositivos Móveis (IMEI 1/2, ICCID, MDM) e Equipamentos Científicos (Projeto SEG, Pesquisador Responsável).

- **Slide 8: Gestão de Licenças e Softwares Científicos (SAM)**
  - Monitoramento de licenças de alto valor (ArcGIS, MATLAB, SAS, SPSS).
  - Controle de assentos (*Seats*), recolheita de licenças ociosas (*License Harvesting*) e alertas de expiração (90/60/30 dias).

- **Slide 9: Governança, LGPD e Sanitização de Mídias**
  - Exigência de Laudo Técnico de Sanitização/Wiping (NIST SP 800-88 / DoD) antes do descarte.
  - Certificado de Destruição Ecológica (Logística Reversa) e rastreabilidade patrimonial.

- **Slide 10: Protocolo de Transferência entre UDs & Conciliação Patrimonial (SIAFI)**
  - Fluxo de movimentação física/lógica inter-UDs com validação SEI.
  - Espelhamento `Asset Tag` = Tombamento Patrimonial e conciliação físico-contábil periódica.

- **Slide 11: Plano de Rollout Regional em 4 Fases (12 Meses)**
  - Cronograma: Fase 1 (Infra/Sede/Piloto), Fase 2 (Onda 1 Sul/Sudeste), Fase 3 (Onda 2 CO/Nordeste), Fase 4 (Onda 3 Norte e SAM Consolidados).

- **Slide 12: KPIs Executivos & Próximos Passos (Aprovação Solicitada)**
  - Metas: Taxa de Cobertura de Inventário (>98%), Aceite Digital (100% em 5 dias), Redução de Ociosidade.
  - Solicitação formal de aprovação para início imediato da Fase 1.

---
Gere a apresentação completa, mantendo o tom executivo e a riqueza técnica contida no documento.
```
