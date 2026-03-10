# 📜 Cláusulas 4 a 10 — Requisitos Mandatórios

> **O coração da ISO 27001.** Essas sete cláusulas são obrigatórias para qualquer organização que deseje certificação.
> Tags: #ISO27001 #cláusulas #SGSI #PDCA #requisitos

← [[🏛️ Mapa Mental — ISO 27001 e 27701|Voltar ao índice]] | ← [[ISO 27001 — Visão Geral]]

---

## O Ciclo PDCA aplicado às Cláusulas

```
          ┌─────────────────────┐
          │  PLAN (Planejar)    │
          │  Cláusulas 4, 5, 6, 7│
          └─────────┬───────────┘
                    ↓
┌─────────────┐     ↓     ┌─────────────┐
│ ACT (Agir)  │←────────→│ DO (Executar)│
│ Cláusula 10 │           │ Cláusula 8  │
└─────────────┘           └─────────────┘
                    ↑
          ┌─────────┴───────────┐
          │ CHECK (Verificar)   │
          │ Cláusula 9          │
          └─────────────────────┘
```

---

## Cláusula 4 — Contexto da Organização

**Fase PDCA:** Plan

### 4.1 — Compreender a Organização e seu Contexto
Identificar questões **internas e externas** relevantes que afetam o SGSI.
- Internas: cultura, processos, tecnologia, estrutura
- Externas: requisitos legais, mercado, tecnologia, regulatório

**Ferramentas úteis:** Análise SWOT, PESTEL

### 4.2 — Necessidades e Expectativas das Partes Interessadas
Mapear **stakeholders** e seus requisitos:
- Clientes, reguladores, parceiros, funcionários, acionistas
- Requisitos legais (LGPD, BACEN, ISO, SOX, PCI-DSS, etc.)

### 4.3 — Determinação do Escopo do SGSI
Definir os **limites** do sistema:
- Quais processos, locais, ativos e pessoas estão incluídos
- Interfaces com processos externos
- O escopo deve ser documentado

### 4.4 — O SGSI
Estabelecer, implementar, manter e melhorar o SGSI usando o **ciclo PDCA**.

---

## Cláusula 5 — Liderança

**Fase PDCA:** Plan

> A Alta Direção é inegociável. Sem comprometimento real do topo, o SGSI não funciona.

### 5.1 — Liderança e Comprometimento
Evidências esperadas de comprometimento da Alta Direção:
- Aprovar e assinar a **Política de Segurança da Informação (PSI)**
- Provisionar **recursos** (orçamento, pessoas, tempo)
- Integrar o SGSI ao planejamento estratégico
- Apoiar e motivar os colaboradores
- Participar das Análises Críticas pela Direção

### 5.2 — Política de Segurança da Informação (PSI)
Documento que define as diretrizes do SGSI:
- Alinhada ao contexto e objetivos estratégicos
- Compromisso com melhoria contínua
- Compromisso com requisitos legais
- Comunicada e disponível para todos
- Revisada periodicamente

### 5.3 — Papéis, Responsabilidades e Autoridades
Definir claramente **quem faz o quê** no SGSI:
- CISO ou Gestor de Segurança da Informação
- Proprietários de ativo (Asset Owners)
- Equipe de resposta a incidentes
- Todos os colaboradores (responsabilidades gerais)

> 💡 A norma não exige um cargo específico — mas alguém deve ter autoridade formal para reportar o desempenho do SGSI à Alta Direção.

---

## Cláusula 6 — Planejamento

**Fase PDCA:** Plan

### 6.1 — Ações para Endereçar Riscos e Oportunidades

#### 6.1.1 — Generalidades
Considerar contexto (Cláusula 4) para determinar riscos e oportunidades.

#### 6.1.2 — Avaliação de Risco de Segurança da Informação
Processo formal e documentado:

```
1. Definir critérios de risco (aceitação, avaliação)
2. Identificar ativos, ameaças e vulnerabilidades
3. Analisar: probabilidade × impacto
4. Avaliar: comparar com critérios de aceitação
5. Priorizar riscos para tratamento
6. Atribuir proprietários de risco
```

*Veja detalhes → [[Conceitos — Avaliação de Riscos]]*

#### 6.1.3 — Tratamento de Risco
- Selecionar opções: **Mitigar, Transferir, Evitar, Aceitar**
- Selecionar controles do [[Anexo A — Controles ISO 27001|Anexo A]] (ou outros)
- Elaborar a **Declaração de Aplicabilidade (SoA)** → [[Conceitos — Declaração de Aplicabilidade (SoA)]]
- Elaborar o **Plano de Tratamento de Risco (PTR)**
- Obter aprovação dos proprietários de risco para o risco residual

### 6.2 — Objetivos de Segurança da Informação
Estabelecer objetivos mensuráveis e alinhados à PSI:
- O quê? Quem? Quando? Como medir? Recursos necessários?

---

## Cláusula 7 — Suporte

**Fase PDCA:** Plan → execução

### 7.1 — Recursos
A organização deve prover os recursos necessários: pessoas, tecnologia, orçamento.

### 7.2 — Competência
- Determinar competências necessárias para o SGSI
- Avaliar competências atuais e identificar lacunas
- Treinar, contratar ou terceirizar conforme necessário
- Documentar evidências de competência (diplomas, certificados, etc.)

### 7.3 — Conscientização
Todos sob controle da organização devem conhecer:
- A Política de Segurança da Informação
- Sua contribuição para a eficácia do SGSI
- As consequências de não conformidades

> 💡 **Conscientização ≠ Treinamento.** Todos precisam de conscientização; treinamento técnico é para papéis específicos.

### 7.4 — Comunicação
Definir o que comunicar, quando, para quem e como:
- Comunicações internas (boletins, campanhas, treinamentos)
- Comunicações externas (clientes, reguladores, fornecedores)

### 7.5 — Informações Documentadas
A norma exige manter **informações documentadas** específicas:

| Tipo | Obrigatório pela norma |
|------|----------------------|
| Escopo do SGSI | ✅ |
| Política de SI | ✅ |
| Processo de avaliação de risco | ✅ |
| Resultados da avaliação de risco | ✅ |
| Declaração de Aplicabilidade (SoA) | ✅ |
| Plano de Tratamento de Risco | ✅ |
| Objetivos de segurança | ✅ |
| Resultados de auditorias | ✅ |
| Análise crítica pela direção | ✅ |
| Não conformidades e ações corretivas | ✅ |

> 💡 "Informação documentada" pode ser em qualquer formato — digital, papel, vídeo. O importante é ser controlada e rastreável.

---

## Cláusula 8 — Operação

**Fase PDCA:** Do (Executar)

### 8.1 — Planejamento e Controle Operacional
- Executar o que foi planejado nas Cláusulas 6 e 7
- Controlar processos terceirizados que afetam o SGSI
- Gerenciar mudanças planejadas e suas consequências

### 8.2 — Avaliação de Riscos da Segurança da Informação
Executar o processo de avaliação de riscos:
- Em intervalos planejados (ex: anualmente)
- Quando mudanças significativas ocorrerem (novo sistema, fusão, novo serviço)
- Documentar os resultados

### 8.3 — Tratamento de Riscos
- Implementar o Plano de Tratamento de Risco
- Documentar os resultados

> 💡 A Cláusula 8 é onde o plano vira realidade — é aqui que os controles são efetivamente implementados.

---

## Cláusula 9 — Avaliação de Desempenho

**Fase PDCA:** Check (Verificar)

### 9.1 — Monitoramento, Medição, Análise e Avaliação
- Definir o que será medido (indicadores / KPIs de segurança)
- Como, quando e por quem
- Analisar e avaliar os resultados
- Exemplos de KPIs: tempo médio de detecção de incidentes, % de usuários treinados, nº de vulnerabilidades abertas

### 9.2 — Auditorias Internas
Programa de auditorias deve cobrir:
- Conformidade com a ISO 27001 e com políticas internas
- Se o SGSI está implementado e mantido com eficácia
- Frequência baseada em risco
- Auditores independentes da área auditada
- Documentar resultados e comunicar à gestão

### 9.3 — Análise Crítica pela Alta Direção
A Alta Direção deve analisar criticamente o SGSI periodicamente:

**Entradas obrigatórias:**
- Status de ações anteriores
- Mudanças no contexto externo/interno
- Feedback das partes interessadas
- Resultados de auditorias e monitoramento
- Desempenho dos controles
- Não conformidades e ações corretivas
- Oportunidades de melhoria

**Saídas obrigatórias:**
- Decisões sobre melhoria contínua
- Mudanças necessárias no SGSI
- Necessidades de recursos

---

## Cláusula 10 — Melhoria

**Fase PDCA:** Act (Agir)

### 10.1 — Não Conformidades e Ações Corretivas
Quando uma não conformidade ocorre:

```
1. Reagir → Corrigir e controlar as consequências imediatas
2. Investigar → Determinar a causa raiz
3. Agir → Implementar ação corretiva para eliminar a causa
4. Verificar → Confirmar eficácia da ação corretiva
5. Atualizar → Revisar riscos e documentação se necessário
```

**Fontes de não conformidades:**
- Auditorias internas e externas
- Reclamações de clientes
- Incidentes de segurança
- Resultados de monitoramento

### 10.2 — Melhoria Contínua
Buscar continuamente oportunidades de melhorar:
- A adequação e a eficácia do SGSI
- Os resultados de segurança da informação

---

## 🔗 Links relacionados

- ← [[ISO 27001 — Visão Geral]]
- → [[Anexo A — Controles ISO 27001]]
- → [[Conceitos — Declaração de Aplicabilidade (SoA)]]
- → [[Conceitos — Avaliação de Riscos]]
- → [[Conceitos — PDCA e SGSI]]
- → [[Processo de Certificação]]
- → [[Checklist — Implementação SGSI]]
