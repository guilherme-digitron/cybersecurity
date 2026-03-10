# 🔐 ISO 27701 — Extensão de Privacidade (SGPI)

> **A ponte entre segurança da informação e proteção de dados pessoais.**
> Tags: #ISO27701 #SGPI #privacidade #LGPD #GDPR #dadospessoais

← [[🏛️ Mapa Mental — ISO 27001 e 27701|Voltar ao índice]] | ← [[ISO 27001 — Visão Geral]]

---

## O que é a ISO 27701?

A ISO 27701 especifica requisitos para um **SGPI — Sistema de Gestão da Privacidade da Informação**. É uma **extensão direta** da ISO 27001 e ISO 27002, focada no tratamento de dados pessoais.

### Regra fundamental
```
ISO 27701 NÃO EXISTE SEM ISO 27001

Não é possível certificar em ISO 27701
sem implementar (ou implementar simultaneamente) a ISO 27001.

As duas podem ser implementadas como
um único sistema integrado de gestão.
```

---

## Pilares da 27701

A ISO 27701 eleva de 3 para **5 pilares** a base da segurança:

```
ISO 27001 (3 pilares)          ISO 27701 (5 pilares)
┌────────────────────┐    ┌────────────────────────────┐
│ Confidencialidade  │    │ Confidencialidade           │
│ Integridade        │ +  │ Integridade                 │
│ Disponibilidade    │    │ Disponibilidade             │
└────────────────────┘    │ Tratamento de Dados Pessoais│
                          │ Proteção da Privacidade     │
                          └────────────────────────────┘
```

### Pilar 4 — Tratamento de Dados Pessoais
Operações realizadas sobre dados pessoais ao longo de seu ciclo de vida:
- Coleta, armazenamento, alteração, recuperação
- Consulta, divulgação, disseminação
- **Anonimização, pseudoanonimização**
- Exclusão ou destruição

### Pilar 5 — Proteção da Privacidade
Conjunto de valores e práticas governando a proteção de dados pessoais em sistemas de TIC.

---

## Controlador vs. Operador — Conceitos Chave

A ISO 27701 distingue dois papéis com responsabilidades diferentes:

| Papel | Definição | Responsabilidade | Seção da 27701 |
|-------|-----------|-----------------|----------------|
| **Controlador** | Decide o propósito e meios do tratamento | Maior — define "por que" e "como" | Seção 7 + Anexo A |
| **Operador** | Trata dados em nome do controlador | Menor — executa conforme instrução | Seção 8 + Anexo B |

**Exemplos:**
- Empresa de e-commerce que coleta dados dos clientes = **Controlador**
- Empresa de cloud/processamento contratada pela e-commerce = **Operador**
- Uma empresa pode ser controladora E operadora simultaneamente

---

## Privacy by Design e Privacy by Default

Conceitos centrais incorporados na ISO 27701 (seção 7.4):

### Privacy by Design
Privacidade incorporada ao projeto desde o início:
- Limite de coleta (colete apenas o necessário)
- Limite de tratamento (use apenas para o propósito declarado)
- Precisão e qualidade dos dados
- Anonimização e exclusão ao final do tratamento
- Gestão de arquivos temporários e retenção

### Privacy by Default
Configurações padrão já respeitam a privacidade:
- Mínimo de dados coletados por padrão
- Sem opt-in pré-selecionado
- Usuário deve escolher ativamente compartilhar mais

---

## Estrutura da ISO 27701

| Seção | Conteúdo |
|-------|----------|
| 1 | Escopo — aplicável a qualquer organização |
| 2 | Referências: ISO 27000, 27001, 27002, 29100 |
| 3 | Termos e definições |
| 4 | Conceitos gerais e estrutura do documento |
| **5** | **Requisitos SGPI (extensão da ISO 27001)** |
| **6** | **Diretrizes SGPI (extensão da ISO 27002)** |
| **7** | **Diretrizes para Controladores de DP** |
| **8** | **Diretrizes para Operadores de DP** |
| Anexo A | Controles para Controladores (Normativo) |
| Anexo B | Controles para Operadores (Normativo) |
| Anexo C | Mapeamento com princípios ISO 29100 (Informativo) |
| Anexo D | Mapeamento com GDPR (Informativo) |
| Anexo E | Mapeamento com ISO 27018 e 29151 (Informativo) |
| Anexo F | Como aplicar 27701 junto com 27001/27002 (Informativo) |
| **Anexo N/A** | **Mapeamento com LGPD (Informativo)** |

*Veja estrutura detalhada → [[ISO 27701 — Estrutura e Comparativo]]*

---

## Benefícios da ISO 27701

- ✅ Demonstra preocupação com privacidade para partes interessadas → **aumento de confiança**
- ✅ Atende as principais exigências da **LGPD e GDPR**
- ✅ Define responsabilidades claras sobre privacidade dos dados
- ✅ Melhora processos internos, reduzindo risco de vazamentos
- ✅ Transparência nos controles de gestão de privacidade
- ✅ Integração nativa com o SGSI (ISO 27001)
- ✅ Redução de custos por prevenção de incidentes de privacidade
- ✅ Aumento de competitividade (diferencial em licitações e contratos)

---

## 🔗 Links relacionados

- ← [[ISO 27001 — Visão Geral]]
- → [[ISO 27701 — Estrutura e Comparativo]]
- → [[ISO 27701 — Mapeamento LGPD e GDPR]]
- → [[Anexo A — Controles ISO 27001]]
- → [[Processo de Certificação]]
