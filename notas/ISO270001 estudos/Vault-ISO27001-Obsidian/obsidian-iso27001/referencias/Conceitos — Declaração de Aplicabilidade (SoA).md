# 📄 Conceitos — Declaração de Aplicabilidade (SoA)

> Tags: #conceitos #SoA #controles #ISO27001
← [[🏛️ Mapa Mental — ISO 27001 e 27701|Índice]]

---

## O que é a SoA?

A **Declaração de Aplicabilidade (Statement of Applicability — SoA)** é o documento-chave do SGSI. Ela mapeia **todos os controles do Anexo A** e registra para cada um:

| Campo | Descrição |
|-------|-----------|
| **Controle** | Identificação do controle (ex: A.9.1.1) |
| **Aplicável?** | Sim ou Não |
| **Justificativa** | Por que é ou não aplicável ao escopo |
| **Status** | Implementado / Em implementação / Planejado |
| **Como implementado** | Referência ao controle, política ou processo |

> ⚠️ **IMPORTANTE:** Todos os controles do Anexo A devem ser analisados. A **exclusão** de qualquer controle deve ser **justificada formalmente**. Não justificar uma exclusão é não conformidade.

---

## Por que a SoA é tão importante?

1. É o **elo** entre a avaliação de riscos e os controles implementados
2. Demonstra ao auditor que a organização considerou todos os controles
3. Evidencia a **maturidade** do SGSI
4. Serve como índice do sistema de gestão

---

## Estrutura típica de uma SoA

```
Controle | Título | Aplicável | Justificativa | Status | Implementação
---------|--------|-----------|---------------|--------|---------------
A.5.1.1  | PSI    | Sim       | Requisito base| 100%   | Doc. POL-001
A.11.2.5 | Remoção| Sim       | Equipam. móveis| 80%  | Proc. PROC-012
A.13.2.3 | Mensag.| Não       | Sem e-mail ext.| N/A  | Fora do escopo
```

---

## Processo de Elaboração

```
1. Listar todos os controles do Anexo A
2. Para cada controle: é aplicável ao nosso contexto/escopo?
3. Se SIM → definir como está/será implementado
4. Se NÃO → documentar justificativa clara
5. Revisar com os proprietários de ativo e riscos
6. Aprovar formalmente pela Alta Direção
7. Manter atualizada a cada revisão do SGSI
```

---

## 🔗 Veja também
- [[Cláusulas 4 a 10 — Requisitos Mandatórios#Cláusula 6]]
- [[Anexo A — Controles ISO 27001]]
- [[Processo de Certificação]]

---
---

# 📊 Conceitos — Avaliação de Riscos

> Tags: #conceitos #risco #avaliação #ISO27001
← [[🏛️ Mapa Mental — ISO 27001 e 27701|Índice]]

---

## Metodologia de Avaliação de Risco

A ISO 27001 **não prescreve** uma metodologia específica — a organização escolhe. O importante é que seja **consistente, documentada e reproduzível**.

### Metodologias comuns
- **OCTAVE** — foco em ativos e processos organizacionais
- **MEHARI** — framework francês, muito detalhado
- **EBIOS Risk Manager** — metodologia francesa moderna
- **ISO/IEC 27005** — guia específico para risco em SI
- **Planilha própria** — muitas PMEs usam matrizes customizadas

---

## Processo Mínimo Exigido pela ISO 27001

```
1. DEFINIR critérios de risco
   ├── Critérios de aceitação (ex: baixo e médio = aceito)
   └── Critérios de avaliação (escala de 1 a 5)

2. IDENTIFICAR riscos
   ├── Inventário de ativos
   ├── Ameaças por ativo
   └── Vulnerabilidades por ativo

3. ANALISAR riscos
   ├── Probabilidade de ocorrência
   └── Impacto se ocorrer

4. AVALIAR riscos
   └── Risco = Probabilidade × Impacto
       Comparar com critérios de aceitação

5. TRATAR riscos
   └── Mitigar / Transferir / Evitar / Aceitar

6. APROVAR risco residual
   └── Proprietário do risco deve aceitar formalmente
```

---

## Exemplo de Matriz de Risco

| | Impacto Baixo (1) | Impacto Médio (3) | Impacto Alto (5) |
|---|---|---|---|
| **Prob. Baixa (1)** | 1 — Aceitar | 3 — Aceitar | 5 — Monitorar |
| **Prob. Média (3)** | 3 — Aceitar | 9 — Mitigar | 15 — Mitigar |
| **Prob. Alta (5)** | 5 — Monitorar | 15 — Mitigar | 25 — Tratar urgente |

---

## Termos Importantes

| Termo | Definição |
|-------|-----------|
| **Ativo** | Qualquer item de valor para o SGSI |
| **Ameaça** | Causa potencial de um incidente indesejado |
| **Vulnerabilidade** | Fragilidade que pode ser explorada por uma ameaça |
| **Risco** | Efeito da incerteza nos objetivos |
| **Risco Residual** | Risco remanescente após tratamento |
| **Proprietário do Risco** | Pessoa com autoridade para gerenciar o risco |
| **Apetite de Risco** | Nível de risco que a organização está disposta a aceitar |

## 🔗 Veja também
- [[Fundamentos — Tríade CIA e Gestão de Risco]]
- [[Cláusulas 4 a 10 — Requisitos Mandatórios#Cláusula 6]]
