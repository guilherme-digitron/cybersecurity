# 🧠 Nível 4 — Engenharia Social e Fator Humano

> **A maior vulnerabilidade não é o software — é a mente humana.**
> Tags: #segurança #engenharia-social #phishing #fator-humano

← [[🛡️ Mapa Mental — Cibersegurança|Voltar ao índice]] | ← [[Nível 3 — Isolamento e Anonimato]]

---

## Por que o fator humano é crítico?

Você pode ter o melhor firewall, senhas complexas e VPN premium — e ainda assim ser comprometido porque:
- Clicou em um link convincente
- Abriu um anexo "do seu banco"
- Atendeu uma "ligação do suporte técnico"
- Inseriu sua senha em um site falso idêntico ao real

**95% dos incidentes de cibersegurança envolvem erro humano** (IBM Security Report).

---

## 1. ⚠️ Reconhecendo Ataques de Phishing

Veja detalhes → [[Ataques — Phishing e Engenharia Social]]

### Gatilhos emocionais usados por atacantes

| Gatilho | Exemplo de mensagem falsa |
|---------|--------------------------|
| **Urgência** | "Sua conta será bloqueada em 2 horas" |
| **Medo** | "Detectamos acesso suspeito — confirme agora" |
| **Ganância** | "Você ganhou R$ 5.000 — clique para resgatar" |
| **Autoridade** | "Mensagem da Receita Federal — pendência fiscal" |
| **Curiosidade** | "Veja quem visitou seu perfil" |

### Sinais de alerta em e-mails e mensagens

- [ ] Remetente com domínio estranho (`suporte@bradesco-seguro.com` em vez de `@bradesco.com.br`)
- [ ] Erros ortográficos ou gramática estranha
- [ ] Links que não batem com o domínio real (passe o mouse sobre o link **sem clicar**)
- [ ] Senso de urgência extremo que não dá tempo de pensar
- [ ] Pedido de informações sensíveis por e-mail ou WhatsApp
- [ ] Anexos `.exe`, `.zip`, `.docm` não solicitados

### Processo de verificação

```
Recebeu mensagem suspeita?
  ↓
PARE. Respire. Não clique.
  ↓
Acesse o site OFICIAL digitando a URL no navegador.
  ↓
Ligue para o número OFICIAL da empresa (não o do e-mail).
  ↓
Se ainda suspeito: encaminhe para equipe de segurança ou delete.
```

> 💡 **Regra de ouro:** Organizações legítimas NUNCA pedem senhas, tokens ou dados de cartão por e-mail ou WhatsApp.

---

## 2. 📞 Vishing e Smishing

Engenharia social não é só e-mail.

### Vishing (Voice + Phishing)
Ligações falsas fingindo ser:
- Banco ("Detectamos fraude no seu cartão")
- Suporte técnico da Microsoft ("Seu computador está infectado")
- Governo ("Há um mandado de prisão em seu nome")

**Defesa:** Desligue e ligue de volta para o número oficial. Jamais forneça dados por telefone para quem ligou para você.

### Smishing (SMS + Phishing)
Mensagens SMS com links maliciosos:
- "Sua encomenda está retida — clique: [link]"
- "Você tem um Pix pendente no valor de R$ 800"

**Defesa:** Não clique em links de SMS. Acesse diretamente o app ou site da empresa.

### Quishing (QR Code + Phishing)
QR codes falsos colados sobre legítimos em restaurantes, cartazes ou e-mails.

**Defesa:** Visualize a URL antes de abrir. Se redirecionar para domínio estranho, não continue.

---

## 3. 🔐 Comunicações Criptografadas

Para conversas críticas, use mensageiros com [[Conceitos — Criptografia E2EE|criptografia de ponta-a-ponta (E2EE)]] real **por padrão**.

### Comparativo de mensageiros

| App | E2EE Padrão | Open Source | Metadata | Recomendação |
|-----|------------|-------------|----------|--------------|
| **Signal** | ✅ | ✅ | Mínimo | 🥇 Melhor opção |
| **WhatsApp** | ✅ | ❌ | Meta coleta | 🥈 Aceitável |
| **Telegram** | ❌* | Parcial | Armazena | ⚠️ Cuidado |
| **iMessage** | ✅ (Apple) | ❌ | Apple vê | 🥈 Se no ecossistema Apple |
| **SMS** | ❌ | — | Totalmente exposto | ❌ Evite para dados sensíveis |

*Telegram: E2EE apenas em "Chats Secretos" — conversas normais ficam nos servidores deles.

### Por que o Signal?
- Protocolo Signal (open source, auditado) — o mais confiável do mundo
- Coleta mínimo de metadados (só o número de telefone e data de cadastro)
- Mensagens que desaparecem automaticamente
- Sem anúncios, sem rastreamento

---

## 4. 🎭 Pretexting e Ataques de Insider

### Pretexting
Atacante cria um cenário (pretexto) convincente para obter informações:
- Finge ser novo funcionário pedindo credenciais
- Finge ser auditor pedindo acesso a sistemas
- Finge ser técnico de suporte pedindo para instalar "ferramenta de diagnóstico"

### Ataques de Insider
Funcionários ou ex-funcionários com acesso privilegiado.

**Defesas organizacionais:**
- Princípio do menor privilégio (dar apenas o acesso necessário)
- Revogar imediatamente acessos de ex-funcionários
- Logs de acesso e auditoria

---

## 5. 🧬 Higiene Digital nas Redes Sociais

O que você posta publicamente pode ser usado em ataques direcionados (Spear Phishing).

### Informações a proteger

- **Nome completo + data de nascimento** → recuperação de senhas
- **Nome do pet, escola, cidade natal** → perguntas de segurança
- **Planos de viagem** → sinaliza casa vazia
- **Local de trabalho + cargo** → phishing direcionado

### Configurações recomendadas
- [ ] Perfis privados ou com visibilidade limitada
- [ ] Revise apps conectados à sua conta (configurações → apps autorizados)
- [ ] Pesquise seu próprio nome no Google periodicamente
- [ ] Use ferramentas como **Have I Been Pwned** (`haveibeenpwned.com`) para verificar vazamentos

---

## 6. 🛡️ Cultura de Segurança — Mindset

### Princípio de Desconfiança Saudável
Trate toda comunicação inesperada como suspeita até verificar:
1. **Verifique o remetente** (não apenas o nome exibido)
2. **Confirme por outro canal** (ligação, app oficial)
3. **Nunca aja sob pressão** — atacantes adoram urgência

### Frases para internalizar
> *"Se parece urgente demais para verificar, é exatamente quando você precisa verificar."*

> *"Nenhum banco pede sua senha por telefone ou e-mail. Jamais."*

> *"Um link encurtado não tem dono identificável — não clique."*

---

## 🔗 Links relacionados

- ← [[Nível 3 — Isolamento e Anonimato]]
- Ataques detalhados → [[Ataques — Phishing e Engenharia Social]] | [[Ataques — SIM Swapping]]
- Conceitos → [[Conceitos — Criptografia E2EE]] | [[Conceitos — OPSEC]]
- Checklist → [[Checklist — Setup Inicial de Segurança]]
