# 🔺 Fundamentos — Tríade CIA e Gestão de Risco

> **Base teórica antes de qualquer norma.** Dominar esses conceitos é pré-requisito para entender o porquê de cada cláusula.
> Tags: #fundamentos #CIA #risco #ameaça #vulnerabilidade

← [[🏛️ Mapa Mental — ISO 27001 e 27701|Voltar ao índice]]

---

## 1. A Tríade CIA — Os 3 Pilares da Segurança da Informação

A ISO 27001 existe para proteger **informação** sob três aspectos:

```
         Confidencialidade
              /\
             /  \
            /    \
           /  CIA \
          /________\
    Integridade   Disponibilidade
```

### 🔒 Confidencialidade
Garante que a informação é acessada **apenas por pessoas autorizadas**.
- Violação: acesso indevido, vazamento de dados, espionagem
- Controles: criptografia, controle de acesso, classificação da informação

### ✅ Integridade
Garante a **veracidade e precisão** da informação — que ela não foi alterada por pessoas não autorizadas.
- Violação: alteração maliciosa de registros, corrupção de dados, adulteração de logs
- Controles: hash/assinatura digital, controle de versão, segregação de funções

### 📶 Disponibilidade
Garante que sistemas e dados estejam **acessíveis quando necessários**.
- Violação: ataques DDoS, ransomware, falha de infraestrutura
- Controles: redundância, backups, BCP (Business Continuity Plan), Disaster Recovery

> 💡 **Relação com a ISO 27701:** A 27701 acrescenta dois pilares adicionais à tríade: **Tratamento de Dados Pessoais** e **Proteção da Privacidade**.
> Veja → [[ISO 27701 — Extensão de Privacidade#Pilares da 27701]]

---

## 2. A Equação do Risco

O risco não é absoluto — ele nasce da combinação de elementos:

```
RISCO = AMEAÇA × VULNERABILIDADE × IMPACTO
```

| Elemento | Definição | Exemplo |
|----------|-----------|---------|
| **Ativo** | O que precisa ser protegido | Banco de dados de clientes |
| **Ameaça** | Agente/evento que pode causar dano | Hacker, ex-funcionário, desastre |
| **Vulnerabilidade** | Fragilidade que pode ser explorada | Software desatualizado, senha fraca |
| **Risco** | Probabilidade × Impacto da exploração | Acesso não autorizado ao banco de dados |
| **Impacto** | Consequência se o risco se materializar | Multa LGPD, perda de reputação |

> Uma vulnerabilidade sem ameaça = risco baixo.
> Uma ameaça sem vulnerabilidade = risco inexistente.
> **Ambos presentes = exposição real.**

---

## 3. Abordagens de Avaliação de Risco

### 📝 Análise Qualitativa
- Baseada em **cenários descritivos** e impactos narrativos
- Classifica riscos como: Baixo / Médio / Alto / Crítico
- Mais subjetiva, mas aplicável a qualquer organização
- Exemplos: Matriz de Riscos (Probabilidade × Impacto)

### 📊 Análise Quantitativa
Baseada em **impacto financeiro mensurável**.

| Métrica | Fórmula | Significado |
|---------|---------|-------------|
| **SLE** (Single Loss Expectancy) | Valor do ativo × Fator de exposição | Perda financeira em um único incidente |
| **ARO** (Annual Rate of Occurrence) | Frequência esperada por ano | Quantas vezes o risco ocorre por ano |
| **ALE** (Annual Loss Expectancy) | SLE × ARO | **Perda financeira anualizada esperada** |

**Exemplo prático:**
```
Servidor com dados de clientes — valor estimado: R$ 500.000
Fator de exposição em caso de ataque: 40%
SLE = R$ 500.000 × 40% = R$ 200.000

Probabilidade de ataque: 2× ao ano (ARO = 2)
ALE = R$ 200.000 × 2 = R$ 400.000/ano
```
> Se um controle custar menos que R$ 400.000/ano para mitigar esse risco, o investimento se justifica.

---

## 4. Opções de Tratamento de Risco

A ISO 27001 (Cláusula 6.1.3) define quatro abordagens — não mutuamente exclusivas:

```
Risco identificado
       ↓
┌──────────────────────────────────┐
│  Mitigar  → Aplicar controles    │
│  Transferir → Seguro / terceiros │
│  Evitar   → Eliminar a atividade │
│  Aceitar  → Registrar e assumir  │
└──────────────────────────────────┘
       ↓
   Risco Residual
   (sempre existe — deve ser aceito pela Alta Direção)
```

> 💡 O **risco residual** é o risco que permanece após a aplicação dos controles. Ele deve ser documentado e aprovado formalmente pela Alta Direção.

---

## 5. Principais Ameaças Corporativas

As ameaças mapeadas no material QMS:

| Ameaça | Pilar CIA violado | Exemplo |
|--------|------------------|---------|
| Infecção por Malware | C, I, D | Ransomware criptografa arquivos |
| Exploração de Vulnerabilidades | C, I, D | Invasão via software desatualizado |
| Phishing | C | Roubo de credenciais por e-mail falso |
| Acesso Indevido | C | Ex-funcionário acessa sistema |
| Fraude Interna | C, I | Colaborador altera registros financeiros |
| Indisponibilidade | D | DDoS derruba sistema crítico |

---

## 🔗 Links relacionados

- → [[ISO 27001 — Visão Geral]]
- → [[Conceitos — Avaliação de Riscos]]
- → [[Cláusulas 4 a 10 — Requisitos Mandatórios#Cláusula 6 — Planejamento]]
- → [[Conceitos — PDCA e SGSI]]
