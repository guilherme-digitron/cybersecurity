# 🔑 Nível 1 — Identidade e Acessos

> **Proteja "quem você é" na internet. Um vazamento não deve destruir toda sua vida digital.**
> Tags: #segurança #identidade #senhas #2FA

← [[🛡️ Mapa Mental — Cibersegurança|Voltar ao índice]] | ← [[Nível 0 — Fundamentos]]

---

## 1. 🔐 Senhas Fortes e Exclusivas

**Nunca reutilize senhas.** Uma credencial vazada em um fórum obscuro será testada automaticamente nos maiores serviços — isso é o ataque de [[Ataques — Credential Stuffing e Brute Force|Credential Stuffing]].

### Características de uma boa senha

| Critério | Ruim ❌ | Bom ✅ |
|----------|---------|--------|
| Comprimento | `senha123` (8 chars) | `Tr0v@o-Azul-Veloz!` (18+ chars) |
| Unicidade | Mesma em vários sites | Exclusiva por serviço |
| Previsibilidade | Data de nascimento | Aleatória ou passphrase |
| Complexidade | Só letras | Letras + números + símbolos |

### Passphrases
Uma alternativa memorável e segura:
```
Cachorro-Azul-Corre-Rapido-2026!
Montanha&Vento#Silencio99
```
> 4 palavras aleatórias já superam a entropia de senhas curtas complexas.

---

## 2. 🗄️ Gerenciadores de Senha

É humanamente impossível memorizar dezenas de senhas únicas e complexas. Use um gerenciador.

### Opções recomendadas

| Ferramenta | Tipo | Destaques |
|------------|------|-----------|
| [[Ferramentas — Gerenciadores de Senha\|Bitwarden]] | Cloud / Open Source | Gratuito, auditado, suporta Passkeys |
| [[Ferramentas — Gerenciadores de Senha\|KeePassXC]] | Offline / Open Source | Sem servidor, total controle local |
| [[Ferramentas — Gerenciadores de Senha\|1Password]] | Cloud / Pago | Interface excelente, funcionalidade de Travel Mode |
| Proton Pass | Cloud / Open Source | Integrado ao ecossistema Proton |

### Configuração da Master Password
- Use uma **frase longa** que só você conhece
- Jamais a anote digitalmente sem criptografia
- Ative 2FA no próprio gerenciador
- Guarde um backup da Master Password em local físico seguro (envelope lacrado)

> ⚠️ **Risco:** Se perder a Master Password sem backup, perde todos os acessos. Planeje a recuperação.

---

## 3. 🔒 Autenticação de Dois Fatores (2FA / MFA)

Adiciona uma camada além da senha. Mesmo com sua senha vazada, o atacante não entra.

### Hierarquia de segurança do 2FA

```
🥇 Chave de Segurança Física (YubiKey, Google Titan)  ← mais seguro
🥈 Aplicativo TOTP (Aegis, Ente Auth, Raivo)
🥉 Email como segundo fator
❌ SMS  ← evite: vulnerável a SIM Swapping
```

### Por que evitar SMS?
Veja → [[Ataques — SIM Swapping]]

### Apps TOTP recomendados

| App | Plataforma | Destaques |
|-----|-----------|-----------|
| [[Ferramentas — Autenticação 2FA\|Aegis]] | Android | Open source, backup criptografado |
| [[Ferramentas — Autenticação 2FA\|Ente Auth]] | Android / iOS / Desktop | Sincronização criptografada E2EE |
| [[Ferramentas — Autenticação 2FA\|Raivo]] | iOS | Open source, iCloud backup |

### Códigos de backup
Ao ativar o 2FA em qualquer serviço:
- [ ] Salve os códigos de recuperação
- [ ] Guarde em local offline seguro (impressos ou em KeePassXC)
- [ ] Nunca em fotos no celular

---

## 4. 🗝️ Passkeys (FIDO2)

O futuro do login — **sem senha, à prova de phishing.**

### Como funciona
Em vez de senha, você autentica com biometria (digital, face) do seu dispositivo. A chave privada nunca sai do seu aparelho.

- ✅ Imune a phishing (a chave é vinculada ao domínio real)
- ✅ Sem senha para vazar
- ✅ Mais rápido que digitar senha + 2FA
- Bitwarden, 1Password e Apple Keychain já armazenam Passkeys

### Serviços que já suportam
Google, Apple, GitHub, Microsoft, PayPal, Adobe, entre outros.

---

## 5. 📧 Compartimentação de E-mails

Divida sua presença digital por importância e exposição.

### Estrutura recomendada

```
📧 E-mail Ultra-Secreto (bancário/recuperação)
   └── Nunca divulgue. Apenas bancos, governo, senhas.

📧 E-mail Pessoal (redes sociais, amigos)
   └── Moderadamente exposto.

📧 E-mail de Cadastro / Lixo
   └── Para sites que exigem registro.

🎭 Aliases (SimpleLogin / Addy.io)
   └── Máscara para cada serviço. Descarte quando quiser.
```

### Serviços de alias recomendados
- **SimpleLogin** (adquirido pela Proton, open source)
- **Addy.io** (gratuito com limites generosos)
- **DuckDuckGo Email Protection** (simples, fácil de usar)

> 💡 **Benefício extra dos aliases:** Se um site começa a te mandar spam, você sabe *exatamente* quem vendeu seu e-mail.

### Provedores de e-mail focados em privacidade
- **ProtonMail** — criptografia E2EE, servidores na Suíça
- **Tutanota** — open source, criptografia nativa
- Evite Gmail/Outlook para e-mails sensíveis (mineração de dados)

---

## 6. 🖼️ Ocultar Imagens em E-mails (Pixel de Rastreamento)

Muitas empresas e golpistas embutem **pixels invisíveis (1x1px)** em imagens de e-mail para rastrear:
- Se você abriu a mensagem
- Quando abriu
- De qual IP (aproximadamente onde você está)
- Qual dispositivo e cliente de e-mail usou

### Como se proteger
- Desative o carregamento automático de imagens nas configurações do seu cliente de e-mail
- **Gmail:** Configurações → Imagens → "Perguntar antes de exibir imagens externas"
- **Thunderbird:** Ativado por padrão em configurações de privacidade
- Use o **SimpleLogin** ou **DuckDuckGo Email Protection** — eles removem pixels automaticamente

---

## 🔗 Links relacionados

- ← [[Nível 0 — Fundamentos]]
- → [[Nível 2 — Rede e Navegação]]
- Ataques mitigados → [[Ataques — Credential Stuffing e Brute Force]] | [[Ataques — SIM Swapping]]
- Ferramentas → [[Ferramentas — Gerenciadores de Senha]] | [[Ferramentas — Autenticação 2FA]]
- Checklist → [[Checklist — Setup Inicial de Segurança]]
