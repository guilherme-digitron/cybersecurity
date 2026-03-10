# 🔩 Nível 0 — Fundamentos

> **Sem estes pilares, qualquer ferramenta avançada perde eficácia.**
> Tags: #segurança #fundamentos #básico

← [[🛡️ Mapa Mental — Cibersegurança|Voltar ao índice]]

---

## Por que o Nível 0 é inegociável?

Ataques sofisticados frequentemente exploram o básico negligenciado. Um sistema desatualizado com VPN ainda é vulnerável. Um backup ausente torna o ransomware catastrófico. Comece aqui.

---

## 1. 🔄 Atualização Contínua (Patch Management)

Mantenha o sistema operacional e **todos** os aplicativos na versão mais recente. A maioria das atualizações corrije brechas críticas — incluindo [[Conceitos — Zero-Day|vulnerabilidades Zero-Day]] e falhas conhecidas publicamente.

### Por que isso importa
- Em 2017, o [[Ataques — Ransomware e Malware|WannaCry]] infectou 200.000 sistemas em 150 países em 24h — explorava uma vulnerabilidade corrigida pela Microsoft 2 meses antes.
- Atacantes escaneiam a internet automaticamente em busca de versões desatualizadas.

### Checklist
- [ ] Windows Update / macOS Software Update ativado
- [ ] Atualização automática de navegadores ligada
- [ ] Apps do celular com atualização automática na App Store / Play Store
- [ ] Firmware do roteador atualizado (verifique a cada 3-6 meses)
- [ ] Extensões do navegador atualizadas

> 💡 **Dica:** No Linux, configure o `unattended-upgrades` para pacotes de segurança.

---

## 2. 💾 Rotina de Backups — Regra 3-2-1

O backup é a **única defesa garantida** contra [[Ataques — Ransomware e Malware|Ransomware]] e falhas de hardware.

### A Regra 3-2-1

```
3 cópias dos dados importantes
  ├── 2 em mídias físicas diferentes
  │     ├── Ex: SSD externo
  │     └── Ex: Pendrive ou NAS local
  └── 1 fora de casa (nuvem criptografada ou local remoto)
```

### Ferramentas recomendadas
- **Nuvem criptografada:** [[Ferramentas — Backup e Armazenamento|Proton Drive, Tresorit, Cryptomator + qualquer nuvem]]
- **Local (macOS):** Time Machine
- **Local (Windows):** Veeam Free, Macrium Reflect
- **Local (Linux):** Rsync + cron, BorgBackup, Timeshift

### Boas práticas adicionais
- Teste a restauração do backup periodicamente (um backup não testado é suspeito)
- Criptografe os backups antes de enviá-los à nuvem
- Backups offline (desconectados) são imunes a ransomware — mantenha ao menos um
- Defina uma frequência: críticos diariamente, demais semanalmente

> ⚠️ **Atenção:** Nuvens como Google Drive ou iCloud **não são backups** — se você deletar um arquivo localmente, ele some da nuvem também.

---

## 3. 🔒 Bloqueio Físico de Dispositivos

**O acesso físico derruba qualquer segurança lógica.** Um atacante com acesso físico ao seu computador pode contornar senhas de login, copiar dados ou instalar keyloggers em minutos.

### Configurações essenciais

| Dispositivo | Ação recomendada |
|-------------|------------------|
| Computador | Bloqueio automático em 1-3 min de inatividade |
| Celular | PIN de 6+ dígitos ou biometria forte |
| Notebook | Criptografia de disco completo (BitLocker / FileVault / LUKS) |
| Roteador | Senha do painel admin alterada (nunca deixe o padrão) |

### Criptografia de Disco Completo (FDE)
- **Windows:** BitLocker (Pro/Enterprise) ou VeraCrypt (gratuito)
- **macOS:** FileVault (nativo, ative nas preferências)
- **Linux:** LUKS (configurado na instalação)
- **Celular:** Android e iOS já criptografam por padrão com PIN ativo

> 💡 **Por que importa?** Sem FDE, basta remover o HD ou inicializar via pendrive para ler todos os seus arquivos — sem precisar da senha do sistema.

### Segurança física adicional
- Nunca deixe dispositivos desbloqueados em locais públicos
- Use cabos de segurança Kensington em notebooks em ambientes compartilhados
- Desconfie de pendrives encontrados — ataque [[Ataques — Phishing e Engenharia Social|"USB Drop"]]
- Cubra a câmera do notebook quando não estiver em uso (webcam covers)
- Cuidado com "shoulder surfing" — olhares por cima do ombro em locais públicos

---

## 🔗 Links relacionados

- Próximo nível → [[Nível 1 — Identidade e Acessos]]
- Ataques que este nível mitiga → [[Ataques — Ransomware e Malware]]
- Ferramentas de backup → [[Ferramentas — Backup e Armazenamento]]
- Checklist prático → [[Checklist — Setup Inicial de Segurança]]
