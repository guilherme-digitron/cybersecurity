# 🥷 Conceitos — OPSEC

> Tags: #conceitos #OPSEC #privacidade #segurança
← [[🛡️ Mapa Mental — Cibersegurança|Índice]]

---

**OPSEC (Operations Security)** — disciplina de identificar e proteger informações que, se obtidas por um adversário, comprometeriam sua segurança ou missão.

## As 5 etapas do OPSEC

```
1. Identificar informações críticas
   └── O que precisa ser protegido? (senhas, localização, planos)

2. Analisar ameaças
   └── Quem pode querer essa informação? (hackers, empresas, governos)

3. Analisar vulnerabilidades
   └── Como poderiam obtê-la? (phishing, metadados, OSINT)

4. Avaliar riscos
   └── Probabilidade × Impacto

5. Aplicar contramedidas
   └── Ações práticas de proteção
```

## OPSEC no cotidiano digital
- Não revelar padrões de rotina em redes sociais
- Remover metadados de fotos antes de compartilhar
- Usar aliases de e-mail para compartimentação
- Não reutilizar usernames em plataformas diferentes

## Veja também
- [[Nível 3 — Isolamento e Anonimato]]
- [[Ataques — Metadados e Rastreamento]]

---
---

# 🔐 Conceitos — Criptografia E2EE

> Tags: #conceitos #criptografia #E2EE #privacidade
← [[🛡️ Mapa Mental — Cibersegurança|Índice]]

---

**Criptografia de Ponta a Ponta (End-to-End Encryption)** garante que apenas o remetente e o destinatário podem ler uma mensagem. Nem o provedor do serviço consegue.

## Como funciona
```
Alice (chave privada A)              Bob (chave privada B)
      ↓                                     ↓
[Mensagem criptografada com chave pública B]
      ↓                                     ↓
   Servidor                          Bob descriptografa
   (vê apenas                        com sua chave privada
   texto cifrado)
```

## E2EE vs. Criptografia em Trânsito
- **Em trânsito (TLS/HTTPS):** Protege entre você e o servidor — mas o servidor lê o conteúdo
- **E2EE:** O servidor nunca vê o conteúdo — apenas dados criptografados

## Serviços com E2EE verdadeiro
- ✅ Signal (mensagens)
- ✅ ProtonMail (e-mail, entre usuários Proton)
- ✅ Proton Drive, Tresorit (armazenamento)
- ⚠️ WhatsApp (E2EE para conteúdo, mas metadados vão para a Meta)
- ❌ Telegram (E2EE apenas em "chats secretos")
- ❌ Gmail (Google lê o conteúdo)

## Veja também
- [[Nível 4 — Engenharia Social#Comunicações Criptografadas]]

---
---

# 🖼️ Conceitos — Metadados EXIF

> Tags: #conceitos #metadados #EXIF #privacidade #fotos
← [[🛡️ Mapa Mental — Cibersegurança|Índice]]

---

**EXIF (Exchangeable Image File Format)** são dados embutidos em fotos digitais contendo informações sobre como a imagem foi capturada.

## Dados típicos em uma foto de smartphone
```json
{
  "GPS Latitude": "-23.5505200",
  "GPS Longitude": "-46.6333090",
  "GPS Altitude": "760 m",
  "Date/Time": "2026:03:04 14:32:11",
  "Make": "Apple",
  "Model": "iPhone 15 Pro",
  "Software": "18.2",
  "Camera Serial Number": "XXXXXXXXX"
}
```

## Riscos reais
- Jornalistas localizados por fotos enviadas a redações
- Vítimas de assédio encontradas por endereço GPS em fotos
- Denunciantes identificados por metadados de documentos

## Defesas
- [[Nível 3 — Isolamento e Anonimato#Limpeza de Metadados (EXIF)]]
- [[Checklist — Antes de Enviar Arquivos ou Fotos]]

---
---

# 📦 Conceitos — Sandboxing e Isolamento

> Tags: #conceitos #sandbox #isolamento #segurança
← [[🛡️ Mapa Mental — Cibersegurança|Índice]]

---

**Sandboxing** é a técnica de executar código ou abrir arquivos em um ambiente isolado que não tem acesso ao sistema real.

## Princípio
```
Sistema real (seus dados, senhas, arquivos)
       ↑ barreira de isolamento
   Sandbox (ambiente descartável)
       ↑
   Arquivo/link suspeito
```

Se o arquivo for malicioso, o dano fica **confinado à sandbox** — que pode ser destruída.

## Níveis de isolamento

| Nível | Tecnologia | Isolamento |
|-------|-----------|------------|
| **Processo** | Firejail, AppArmor | Baixo — mesmo kernel |
| **Contêiner** | Docker, Kasm | Médio — namespace isolado |
| **VM completa** | VirtualBox, VMware | Alto — hardware virtualizado |
| **Hardware separado** | Computador dedicado | Máximo |

## Veja também
- [[Nível 3 — Isolamento e Anonimato#Sandboxing]]
