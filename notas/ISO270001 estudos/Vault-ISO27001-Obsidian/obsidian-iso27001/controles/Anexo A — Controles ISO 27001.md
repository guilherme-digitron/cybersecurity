# 🛡️ Anexo A — Controles ISO 27001

> **O arsenal de controles de segurança.** O Anexo A é normativo — seus controles devem ser considerados e justificados via SoA.
> Tags: #ISO27001 #AnexoA #controles #segurança

← [[🏛️ Mapa Mental — ISO 27001 e 27701|Voltar ao índice]] | ← [[Cláusulas 4 a 10 — Requisitos Mandatórios]]

---

## ISO 27001:2013 — 114 Controles em 14 Seções

O Anexo A da versão 2013 organiza os controles em 14 domínios (A.5 a A.18):

| Seção | Domínio | Nº Controles |
|-------|---------|--------------|
| A.5 | Política de Segurança da Informação | 2 |
| A.6 | Organização da Segurança da Informação | 7 |
| A.7 | Segurança em Recursos Humanos | 6 |
| A.8 | Gestão de Ativos | 10 |
| A.9 | Controle de Acesso | 14 |
| A.10 | Criptografia | 2 |
| A.11 | Segurança Física e do Ambiente | 15 |
| A.12 | Segurança nas Operações | 14 |
| A.13 | Segurança nas Comunicações | 7 |
| A.14 | Aquisição, Desenvolvimento e Manutenção de Sistemas | 13 |
| A.15 | Relacionamento na Cadeia de Suprimento | 5 |
| A.16 | Gestão de Incidentes de Segurança da Informação | 7 |
| A.17 | Aspectos da SI na Gestão de Continuidade de Negócio | 4 |
| A.18 | Conformidade / Compliance | 8 |
| **Total** | | **114** |

---

## ISO 27001:2022 — 93 Controles em 4 Temas

A versão 2022 modernizou e reorganizou os controles:

```
93 controles
├── Organizacionais (37) → Políticas, processos, papéis, contratos
├── Pessoas (8)          → RH, conscientização, trabalho remoto
├── Físicos (14)         → Data centers, perímetro, equipamentos
└── Tecnológicos (34)    → Sistemas, redes, criptografia, logs
```

### Os 11 Novos Controles da versão 2022

| Controle | Descrição | Relevância |
|----------|-----------|------------|
| **Threat Intelligence** | Coleta e análise de inteligência de ameaças | SOC, Blue Team |
| **Segurança em Nuvem** | Controles para serviços em nuvem | Cloud Security |
| **ICT Readiness for BCM** | Prontidão de TIC para continuidade | BCP/DR |
| **Monitoramento de Atividades** | Logs e alertas de comportamento | SIEM, SOC |
| **Filtragem Web** | Controle de acesso a URLs | Gateway, Proxy |
| **Configuração Segura** | Hardening de sistemas e redes | DevSecOps |
| **DLP — Data Leakage Prevention** | Prevenção de vazamento de dados | DLP Tools |
| **Mascaramento de Dados** | Ofuscação de dados sensíveis | Privacidade |
| **Exclusão de Informações** | Destruição segura de dados | LGPD, GDPR |
| **Desenvolvimento Seguro** | Segurança no ciclo de vida de software | DevSecOps |
| **Segregação de Redes** | Isolamento de redes e segmentos | Zero Trust |

---

## Detalhamento dos Principais Domínios (versão 2013)

### A.5 — Política de Segurança
- Existência da PSI (Política de Segurança da Informação)
- Revisão periódica da PSI

### A.6 — Organização da Segurança
- Papéis e responsabilidades definidos
- Segregação de funções
- Contato com autoridades e grupos especiais
- Dispositivos móveis e trabalho remoto

### A.7 — Segurança em RH
- Triagem de candidatos (antes da contratação)
- Termos de confidencialidade nos contratos
- Conscientização e treinamento durante a contratação
- Processo de offboarding (devolução de ativos, revogação de acessos)

### A.8 — Gestão de Ativos
- **Inventário de ativos** (tudo que tem valor para o SGSI)
- Proprietário de ativo definido para cada item
- Classificação da informação (Pública, Interna, Confidencial, Secreta)
- Tratamento e descarte seguro de mídias

### A.9 — Controle de Acesso
- Política de controle de acesso
- Provisionamento e desprovisionamento de usuários
- Gerenciamento de contas privilegiadas (admins)
- Revisão periódica de direitos de acesso
- Senha e autenticação

### A.10 — Criptografia
- Política de uso de criptografia
- Gerenciamento de chaves criptográficas

### A.11 — Segurança Física e do Ambiente
- Perímetros de segurança física (data centers, salas de servidores)
- Controles de entrada física
- Proteção de equipamentos
- Descarte seguro de equipamentos
- Política de mesa limpa / tela limpa

### A.12 — Segurança nas Operações
- Documentação de procedimentos operacionais
- Gestão de capacidade
- Separação de ambientes (Dev/Test/Prod)
- Proteção contra malware
- Backups (cópias de segurança)
- Logs e monitoramento
- Gestão de vulnerabilidades técnicas

### A.13 — Segurança nas Comunicações
- Controles de rede e segmentação
- Políticas de transferência de informação
- Acordos de confidencialidade (NDAs)

### A.14 — Aquisição, Desenvolvimento e Manutenção
- Requisitos de segurança em novos sistemas
- Desenvolvimento seguro (SDLC seguro)
- Testes de segurança
- Proteção de dados em ambiente de teste

### A.15 — Cadeia de Suprimento
- Política de segurança com fornecedores
- SLAs de segurança em contratos com terceiros
- Monitoramento de fornecedores

### A.16 — Gestão de Incidentes
- Procedimentos de resposta a incidentes
- Notificação de eventos de segurança
- Coleta de evidências forenses
- Aprendizado com incidentes

### A.17 — Continuidade de Negócio
- Plano de Continuidade de Negócios (BCP)
- Plano de Recuperação de Desastres (DR)
- Testes regulares dos planos
- Redundância de infraestrutura

### A.18 — Conformidade / Compliance
- Mapeamento de legislação aplicável
- Proteção de dados pessoais (alinhamento LGPD/GDPR)
- Revisão independente de segurança
- Compliance técnico

---

## Como usar o Anexo A

O Anexo A **não é uma lista de verificação** — é um cardápio de controles. A organização deve:

```
1. Realizar avaliação de riscos (Cláusula 6.1.2)
2. Definir controles necessários para tratar os riscos
3. Comparar com o Anexo A (verificar se algo foi esquecido)
4. Documentar na SoA:
   - Quais controles são aplicáveis
   - Quais foram excluídos e por quê
   - Status de implementação de cada um
```

*Veja → [[Conceitos — Declaração de Aplicabilidade (SoA)]]*

---

## 🔗 Links relacionados

- ← [[Cláusulas 4 a 10 — Requisitos Mandatórios]]
- → [[Conceitos — Declaração de Aplicabilidade (SoA)]]
- → [[ISO 27701 — Estrutura e Comparativo]]
- → [[Processo de Certificação]]
