# 🏛️ Mapa Mental — ISO 27001 e ISO 27701

> **Propósito:** Guia estruturado para estudo e implementação de SGSI (Sistema de Gestão da Segurança da Informação) e SGPI (Sistema de Gestão da Privacidade da Informação).
> **Fontes:** PDF QMS Certification Services + Notas de estudo (Gemini synthesis)
> **Última revisão:** 2026

---

## 🗺️ Índice Geral (MOC)

```
ISO 27001 / 27701
├── Fundamentos     → [[Fundamentos — Tríade CIA e Gestão de Risco]]
├── ISO 27001       → [[ISO 27001 — Visão Geral]]
│     ├── Cláusulas → [[Cláusulas 4 a 10 — Requisitos Mandatórios]]
│     └── Anexo A   → [[Anexo A — Controles ISO 27001]]
├── ISO 27701       → [[ISO 27701 — Extensão de Privacidade]]
│     ├── Estrutura → [[ISO 27701 — Estrutura e Comparativo]]
│     └── LGPD/GDPR → [[ISO 27701 — Mapeamento LGPD e GDPR]]
├── Certificação    → [[Processo de Certificação]]
└── Referências
      ├── Conceitos → [[Conceitos — PDCA e SGSI]]
      ├── Conceitos → [[Conceitos — Declaração de Aplicabilidade (SoA)]]
      ├── Conceitos → [[Conceitos — Avaliação de Riscos]]
      └── Checklists → [[Checklist — Implementação SGSI]]
```

---

## 📊 Visão Geral das Normas

| Norma | Foco | Dependência | Certificável |
|-------|------|-------------|--------------|
| **ISO 27001** | Sistema de gestão de segurança da informação | Base — independente | ✅ |
| **ISO 27002** | Código de práticas (controles detalhados) | Complementa a 27001 | ❌ (referência) |
| **ISO 27701** | Gestão de privacidade (SGPI) | Requer ISO 27001 | ✅ (em conjunto) |

---

## 🧭 Estrutura de Estudo Progressiva

| Nível | Tópico | Complexidade |
|-------|--------|--------------|
| 0 | [[Fundamentos — Tríade CIA e Gestão de Risco\|Fundamentos e Lógica do Risco]] | ⭐ |
| 1 | [[ISO 27001 — Visão Geral\|O que é a ISO 27001]] | ⭐⭐ |
| 2 | [[Cláusulas 4 a 10 — Requisitos Mandatórios\|Cláusulas Mandatórias (4–10)]] | ⭐⭐⭐ |
| 3 | [[Anexo A — Controles ISO 27001\|Anexo A — Controles]] | ⭐⭐⭐ |
| 4 | [[ISO 27701 — Extensão de Privacidade\|ISO 27701 + LGPD/GDPR]] | ⭐⭐⭐⭐ |
| 5 | [[Processo de Certificação\|Processo de Certificação]] | ⭐⭐⭐ |

---

## ⚔️ Principais Ameaças Corporativas

- Infecção por Malware
- Exploração de Vulnerabilidades
- Phishing e Engenharia Social
- Acesso Indevido (viola Confidencialidade)
- Fraude Interna (Insider Threat)
- Indisponibilidade de Sistemas (viola Disponibilidade)

*Veja detalhes em → [[Fundamentos — Tríade CIA e Gestão de Risco]]*

---

## 📋 Checklists e Referências Rápidas

- [[Checklist — Implementação SGSI]]
- [[Checklist — Pré-Auditoria ISO 27001]]
- [[Conceitos — Declaração de Aplicabilidade (SoA)]]
- [[Conceitos — PDCA e SGSI]]
- [[Conceitos — Avaliação de Riscos]]

---

> 💡 **Princípio central da ISO 27001:** Segurança da informação não é um produto — é um **sistema de gestão** baseado em melhoria contínua. A norma não prescreve soluções técnicas; ela exige um processo estruturado de identificar, avaliar e tratar riscos.
