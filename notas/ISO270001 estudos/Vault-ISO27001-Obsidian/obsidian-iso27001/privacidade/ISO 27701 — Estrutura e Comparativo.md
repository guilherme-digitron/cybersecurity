# 📊 ISO 27701 — Estrutura e Comparativo com ISO 27001

> **Como a 27701 se encaixa sobre a 27001 — requisito a requisito.**
> Tags: #ISO27701 #ISO27001 #comparativo #estrutura #SGPI

← [[🏛️ Mapa Mental — ISO 27001 e 27701|Voltar ao índice]] | ← [[ISO 27701 — Extensão de Privacidade]]

---

## Mapeamento das Cláusulas: ISO 27001 ↔ ISO 27701

| ISO 27001 | Título | ISO 27701 | Observações Adicionais de Privacidade |
|-----------|--------|-----------|--------------------------------------|
| 4 | Contexto da Organização | 5.2 | Determinar papel como controlador e/ou operador; incluir tratamento de DP no escopo do SGPI |
| 5 | Liderança | 5.3 | Sem requisitos específicos de SGPI |
| 6 | Planejamento | 5.4 | **Avaliar riscos de privacidade** além dos riscos de segurança; considerar riscos dos titulares de DP |
| 7 | Suporte | 5.5 | Sem requisitos específicos de SGPI |
| 8 | Operação | 5.6 | Sem requisitos específicos de SGPI |
| 9 | Avaliação de Desempenho | 5.7 | Sem requisitos específicos de SGPI |
| 10 | Melhoria | 5.8 | Sem requisitos específicos de SGPI |

> 💡 As principais adições estão nas **Cláusulas 4 e 6** (Contexto e Planejamento), além das Seções 7 e 8 exclusivas da 27701.

---

## Adições Críticas da ISO 27701 ao Planejamento (5.4.1.2)

A avaliação de riscos da 27701 exige **duas camadas**:

```
ISO 27001 (apenas)          ISO 27701 (extensão)
┌─────────────────┐     ┌────────────────────────────┐
│ Riscos de SI:   │ +   │ Riscos de Privacidade:      │
│ - Confidenciali-│     │ - Riscos para os titulares  │
│   dade          │     │   de dados pessoais         │
│ - Integridade   │     │ - Tratamento ilegal de DP   │
│ - Disponibilid. │     │ - Transferência indevida    │
└─────────────────┘     │ - Falta de consentimento    │
                        └────────────────────────────┘
```

---

## Seção 6 — Diretrizes SGPI (extensão da ISO 27002)

A Seção 6 espelha os domínios da ISO 27002 com adições de privacidade:

| Seção 6.x | Domínio |
|-----------|---------|
| 6.2 | Políticas de segurança da informação |
| 6.3 | Organização da segurança da informação |
| 6.4 | Segurança em recursos humanos |
| 6.5 | Gestão de ativos |
| 6.6 | Controle de acesso |
| 6.7 | Criptografia |
| 6.8 | Segurança física e do ambiente |
| 6.9 | Segurança nas operações |
| 6.10 | Segurança nas comunicações |
| 6.11 | Aquisição, desenvolvimento e manutenção de sistemas |
| 6.12 | Relacionamento na cadeia de suprimento |
| 6.13 | Gestão de incidentes de segurança da informação |
| 6.14 | Aspectos da SI na gestão da continuidade do negócio |
| 6.15 | Compliance (inclui proteção e privacidade de DP — 6.15.1.4) |

---

## Seção 7 — Diretrizes para Controladores de DP

Controles exclusivos para quem é **Controlador** de dados pessoais:

### 7.2 — Condições para Coleta e Tratamento
- Identificar e documentar o **propósito** de cada tratamento
- Identificar a **base legal** (consentimento, legítimo interesse, contrato, obrigação legal, etc.)
- Obter e registrar consentimento quando necessário
- Realizar **DPIA — Avaliação de Impacto à Privacidade** quando necessário
- Estabelecer contratos com operadores de DP (DPA — Data Processing Agreement)
- Manter registros de atividades de tratamento

### 7.3 — Obrigações para os Titulares de DP
- Determinar e cumprir obrigações com titulares (direitos LGPD/GDPR)
- Fornecer informações claras sobre o tratamento
- Mecanismos para cancelar/modificar consentimento
- **Acesso, correção e/ou exclusão** de dados
- Resposta a solicitações dos titulares
- Endereçar **decisões automatizadas** (algoritmos, IA)

### 7.4 — Privacy by Design e Privacy by Default
Veja → [[ISO 27701 — Extensão de Privacidade#Privacy by Design e Privacy by Default]]

### 7.5 — Transferência Internacional de DP
- Identificar bases legais para transferência entre países
- Registros de transferências realizadas
- Mapeamento de países com adequação reconhecida

---

## Seção 8 — Diretrizes para Operadores de DP

Controles exclusivos para quem é **Operador** (processa em nome de outro):

### 8.2 — Condições para Coleta e Tratamento
- Agir somente conforme instruções do cliente (controlador)
- Definir claramente o propósito do processamento
- Regras para uso de marketing e propaganda
- Obrigações contratuais com o controlador

### 8.4 — Privacy by Design para Operadores
- Gestão de arquivos temporários
- Retorno, transferência ou descarte seguro de DP
- Controles de transmissão

### 8.5 — Transferência e Divulgação de DP
- Bases para transferência entre jurisdições
- Notificação ao controlador sobre solicitações de divulgação
- Uso de subcontratados para tratar DP (aprovação do controlador)

---

## 🔗 Links relacionados

- ← [[ISO 27701 — Extensão de Privacidade]]
- → [[ISO 27701 — Mapeamento LGPD e GDPR]]
- → [[Anexo A — Controles ISO 27001]]
- → [[Conceitos — Declaração de Aplicabilidade (SoA)]]
