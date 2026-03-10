# 📋 ISO 27001 — Visão Geral

> **O que é, para que serve, e onde se encaixa.**
> Tags: #ISO27001 #SGSI #segurança #gestão

← [[🏛️ Mapa Mental — ISO 27001 e 27701|Voltar ao índice]] | ← [[Fundamentos — Tríade CIA e Gestão de Risco]]

---

## O que é a ISO 27001?

A ISO 27001 é a norma internacional que especifica os **requisitos para estabelecer, implementar, manter e melhorar continuamente** um Sistema de Gestão da Segurança da Informação (SGSI).

- Aplicável a **qualquer tipo de organização** (pública, privada, com ou sem fins lucrativos, de qualquer porte)
- Foco em proteger a **tríade CIA** → [[Fundamentos — Tríade CIA e Gestão de Risco]]
- Possibilita **certificação** por organismo independente (ex: QMS, BSI, Bureau Veritas)
- Versão atual: **ISO 27001:2022** (transição da versão 2013)

---

## Relação com outras normas da família ISO 27000

```
ISO/IEC 27000 ← Vocabulário e termos comuns
       ↓
ISO/IEC 27001 ← SGSI: REQUISITOS (certificável)
       ↓
ISO/IEC 27002 ← Código de práticas (guia de controles)
       ↓
ISO/IEC 27701 ← SGPI: Extensão para privacidade (certificável)
       ↓
ISO/IEC 27018 ← Proteção de DP em nuvens públicas
ISO/IEC 29100 ← Framework de privacidade
ISO/IEC 29151 ← Orientações para controladores de DP
```

> 💡 A **ISO 27002** não é certificável — ela funciona como o "manual de instruções" dos controles listados no Anexo A da 27001.

---

## Estrutura da Norma

```
Seções 0–3  → Introdutórias (não implementáveis)
Seções 4–10 → Requisitos obrigatórios (SGSI)
Anexo A     → Catálogo de controles (ISO 27001:2013: 114 controles / ISO 27001:2022: 93 controles)
```

| Seção | Título | Fase PDCA |
|-------|--------|-----------|
| 4 | Contexto da Organização | Plan |
| 5 | Liderança | Plan |
| 6 | Planejamento | Plan |
| 7 | Suporte | Plan |
| 8 | Operação | Do |
| 9 | Avaliação de Desempenho | Check |
| 10 | Melhoria | Act |

*Veja detalhes em → [[Cláusulas 4 a 10 — Requisitos Mandatórios]]*

---

## Onde a ISO 27001 se encaixa no universo corporativo

A gestão de riscos é o núcleo que une todas as áreas:

```
          Gestão de Riscos (cobertura total)
         /                                  \
   Segurança da Informação       Continuidade do Negócio
         |                                  |
   Cyber Segurança           Tecnologia da Informação
         \____________________________________/
                    ISO 27001
```

A ISO 27001 **não é apenas TI** — ela engloba processos, pessoas e tecnologia.

---

## Por que implementar?

### Benefícios diretos
- Redução de custos com tratamento de incidentes
- Conformidade com requisitos legais (LGPD, GDPR, BACEN, etc.)
- Credibilidade de marca — demonstra maturidade em segurança
- Vantagem competitiva em processos licitatórios e contratos
- Gestão estruturada e documentada dos riscos

### A falácia do custo
> "Implementar um SGSI vai custar muito e retornar pouco."

**Realidade:** O custo de implementação é compensado pela **prevenção e redução do impacto** dos incidentes de segurança. Use o modelo ALE para comparar → [[Conceitos — Avaliação de Riscos]]

---

## Versão 2013 vs 2022 — O que mudou?

| Aspecto | ISO 27001:2013 | ISO 27001:2022 |
|---------|----------------|----------------|
| Controles no Anexo A | 114 controles em 14 seções | 93 controles em 4 temas |
| Temas/Categorias | 14 seções (A.5 a A.18) | 4 temas: Org., Pessoas, Físico, Tecnológico |
| Novos controles | — | 11 novos (Threat Intel, DLP, Nuvem, etc.) |
| Prazo de transição | — | Até outubro de 2025 |

*Veja controles em detalhes → [[Anexo A — Controles ISO 27001]]*

---

## 🔗 Links relacionados

- ← [[Fundamentos — Tríade CIA e Gestão de Risco]]
- → [[Cláusulas 4 a 10 — Requisitos Mandatórios]]
- → [[Anexo A — Controles ISO 27001]]
- → [[ISO 27701 — Extensão de Privacidade]]
- → [[Processo de Certificação]]
- → [[Conceitos — PDCA e SGSI]]
