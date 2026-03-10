# ✅ Checklist — Setup Inicial de Segurança

> Tags: #checklist #setup #segurança
← [[🛡️ Mapa Mental — Cibersegurança|Índice]]

> Use este checklist ao configurar um novo dispositivo ou revisar sua segurança anualmente.

---

## 🔩 Nível 0 — Fundamentos
- [ ] Sistema operacional atualizado
- [ ] Atualizações automáticas ativadas
- [ ] Antivírus / Defender ativo
- [ ] Criptografia de disco ativada (BitLocker / FileVault / LUKS)
- [ ] Bloqueio automático de tela configurado (1-3 min)
- [ ] PIN forte ou biometria no celular
- [ ] Backup configurado seguindo a Regra 3-2-1
- [ ] Backup testado (restauração verificada)
- [ ] Firmware do roteador atualizado

## 🔑 Nível 1 — Identidade
- [ ] Gerenciador de senhas instalado e em uso → [[Ferramentas — Gerenciadores de Senha]]
- [ ] Master Password forte criada e guardada fisicamente
- [ ] Todas as senhas importantes migradas para o gerenciador
- [ ] 2FA ativo nas contas críticas (banco, e-mail, Google, Apple ID)
- [ ] App TOTP instalado → [[Ferramentas — Autenticação 2FA]]
- [ ] Códigos de recuperação 2FA salvos offline
- [ ] SMS como 2FA desativado onde possível
- [ ] E-mails compartimentados (bancário, pessoal, cadastros)
- [ ] Carregamento automático de imagens em e-mail desativado
- [ ] E-mails verificados em haveibeenpwned.com

## 🌐 Nível 2 — Rede
- [ ] DNS personalizado configurado → [[Ferramentas — VPN e DNS]]
- [ ] Extensão uBlock Origin instalada no navegador
- [ ] VPN instalada para uso em redes públicas → [[Ferramentas — VPN e DNS]]
- [ ] Wi-Fi e Bluetooth desligados quando não em uso
- [ ] Aleatorização de MAC Address ativada no celular
- [ ] Redes públicas esquecidas após uso

## 🧠 Nível 4 — Humano
- [ ] Leu sobre os principais tipos de phishing → [[Ataques — Phishing e Engenharia Social]]
- [ ] Compartilhou estas práticas com pessoas próximas

---

## 📅 Revisão periódica (a cada 6 meses)
- [ ] Verificar vazamentos em haveibeenpwned.com
- [ ] Revisar apps com acesso às suas contas (Google, Apple, Facebook)
- [ ] Revogar acessos desnecessários
- [ ] Testar backup
- [ ] Atualizar firmware do roteador

---

# ✅ Checklist — Antes de Usar Wi-Fi Público

> Tags: #checklist #wifi #segurança
← [[🛡️ Mapa Mental — Cibersegurança|Índice]]

---

- [ ] VPN ativada **antes** de conectar à rede
- [ ] Nenhum acesso bancário sem VPN
- [ ] Confirmar nome exato da rede com o estabelecimento (evitar Evil Twin)
- [ ] Bluetooth desligado
- [ ] Compartilhamento de arquivos desativado
- [ ] Após uso: esquecer a rede no dispositivo

**Se a VPN não estiver disponível:** evite qualquer site sensível. Use dados móveis.

---

# ✅ Checklist — Antes de Enviar Arquivos ou Fotos

> Tags: #checklist #metadados #privacidade #EXIF
← [[🛡️ Mapa Mental — Cibersegurança|Índice]]

---

## Para fotos
- [ ] Verificar metadados EXIF: `exiftool foto.jpg`
- [ ] Remover metadados: `exiftool -all= foto.jpg`
- [ ] Confirmar que GPS foi removido

## Para documentos (Word, PDF, Excel)
- [ ] Remover metadados do autor
  - Word: Arquivo → Inspecionar Documento → Remover
  - Linux: `mat2 documento.docx`
- [ ] Verificar histórico de revisões e comentários ocultos

## Para qualquer arquivo antes de abrir (recebido)
- [ ] Escanear em https://virustotal.com
- [ ] Se suspeito: abrir em sandbox (Windows Sandbox, Kasm, VM)
- [ ] Não abrir `.exe`, `.docm`, `.xlsm` de remetentes desconhecidos

## Veja também
- [[Conceitos — Metadados EXIF]]
- [[Nível 3 — Isolamento e Anonimato]]
