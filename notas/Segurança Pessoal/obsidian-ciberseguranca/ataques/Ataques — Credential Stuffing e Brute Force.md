# 💥 Ataques — Credential Stuffing e Brute Force

> Tags: #ataques #credenciais #senhas #vazamento
← [[🛡️ Mapa Mental — Cibersegurança|Índice]] | Mitigação: [[Nível 1 — Identidade e Acessos]]

---

## Credential Stuffing
Usa listas de e-mail + senha vazadas de um site e testa automaticamente em outros serviços. Funciona porque pessoas reutilizam senhas.

**Escala:** Bilhões de credenciais circulam em fóruns como breachforums.

**Defesa:**
- Senhas únicas por serviço → [[Ferramentas — Gerenciadores de Senha]]
- 2FA → [[Ferramentas — Autenticação 2FA]]
- Verifique seus e-mails em https://haveibeenpwned.com

## Brute Force
Testa combinações de senhas sistematicamente. Senhas curtas são crackeadas em segundos.

```
6 caracteres numéricos   → < 1 segundo
8 caracteres alfanuméricos → minutos
16 caracteres mistos     → séculos
```

**Defesa:** Senhas longas (16+ caracteres) + lockout após tentativas falhas.

---
---

# 📱 Ataques — SIM Swapping

> Tags: #ataques #SIM #telefonia #2FA
← [[🛡️ Mapa Mental — Cibersegurança|Índice]] | Mitigação: [[Nível 1 — Identidade e Acessos]]

---

## O que é?
Atacante convence a operadora de telefonia a transferir seu número para um chip sob controle dele. A partir daí, recebe todos os seus SMS — incluindo códigos de 2FA.

## Como acontece
1. Atacante pesquisa dados pessoais da vítima (nome, CPF, data de nascimento)
2. Liga para a operadora fingindo ser a vítima
3. Solicita portabilidade ou segunda via do chip
4. Operadora transfere o número (processo falho de verificação)
5. Atacante recebe SMS de 2FA e reseta senhas

## Casos notáveis
- Jack Dorsey (co-fundador do Twitter) teve conta comprometida via SIM Swap

## Defesas
- **Nunca use SMS como 2FA** — use apps TOTP → [[Ferramentas — Autenticação 2FA]]
- Configure um PIN/senha na sua conta da operadora
- Use Passkeys quando possível → [[Nível 1 — Identidade e Acessos#Passkeys]]

---
---

# 🕵️ Ataques — Man-in-the-Middle (MitM)

> Tags: #ataques #rede #interceptação #MitM
← [[🛡️ Mapa Mental — Cibersegurança|Índice]] | Mitigação: [[Nível 2 — Rede e Navegação]]

---

## O que é?
Atacante se posiciona entre você e o servidor, interceptando ou modificando o tráfego.

## Variações

| Tipo | Contexto |
|------|---------|
| **ARP Spoofing** | Rede local — redireciona tráfego |
| **Rogue AP** | Ponto de acesso Wi-Fi falso com nome convincente |
| **SSL Stripping** | Downgrade de HTTPS para HTTP |
| **Evil Twin** | Cópia exata do Wi-Fi legítimo |

## Cenário típico
Wi-Fi "Starbucks_Free" em um café — criado pelo atacante. Qualquer dado não criptografado é capturado.

## Defesas
- Use VPN em Wi-Fi público → [[Ferramentas — VPN e DNS]]
- Verifique HTTPS sempre
- Desative conexão automática a redes abertas

---
---

# 🦠 Ataques — Ransomware e Malware

> Tags: #ataques #ransomware #malware #vírus
← [[🛡️ Mapa Mental — Cibersegurança|Índice]] | Mitigação: [[Nível 0 — Fundamentos]] | [[Nível 3 — Isolamento e Anonimato]]

---

## Ransomware
Criptografa seus arquivos e exige pagamento (geralmente crypto) para descriptografar.

### Casos históricos
- **WannaCry (2017):** 200.000 sistemas em 150 países em 24h
- **NotPetya (2017):** Causou US$ 10 bilhões em danos globais
- **REvil, LockBit:** Grupos especializados em empresas

### Vetor de entrada mais comum
- Anexos maliciosos em e-mails
- Vulnerabilidades em software desatualizado
- RDP exposto sem proteção

### Defesas
- Backup offline imune → [[Nível 0 — Fundamentos#Rotina de Backups]]
- Sistema atualizado → [[Nível 0 — Fundamentos#Atualização Contínua]]
- Sandboxing para arquivos suspeitos → [[Nível 3 — Isolamento e Anonimato#Sandboxing]]

---
---

# 🔍 Ataques — Metadados e Rastreamento

> Tags: #ataques #metadados #EXIF #privacidade #rastreamento
← [[🛡️ Mapa Mental — Cibersegurança|Índice]] | Mitigação: [[Nível 3 — Isolamento e Anonimato]] | Conceito: [[Conceitos — Metadados EXIF]]

---

## Tipos de Rastreamento

| Tipo | Método | Risco |
|------|--------|-------|
| **EXIF em fotos** | GPS, dispositivo, horário | Localização exata |
| **Pixel de rastreamento** | Imagem 1x1 em e-mails | Saber quando/onde abriu |
| **Fingerprinting** | Browser, GPU, fontes, tela | Identificar sem cookies |
| **MAC Address** | Identificador de rede | Rastreamento físico em redes |
| **Metadados em documentos** | Nome do autor, edições, software | Revelar identidade real |

## Metadados em documentos Office
Documentos Word, Excel e PowerPoint podem conter:
- Nome e empresa do autor
- Histórico de revisões com nomes
- Comentários ocultos
- Localização de impressoras

**Remoção:**
- Word: Arquivo → Informações → Verificar Problemas → Inspecionar Documento
- Linux: `mat2 documento.docx`

## Defesas
- [[Nível 3 — Isolamento e Anonimato#Limpeza de Metadados (EXIF)]]
- [[Checklist — Antes de Enviar Arquivos ou Fotos]]
