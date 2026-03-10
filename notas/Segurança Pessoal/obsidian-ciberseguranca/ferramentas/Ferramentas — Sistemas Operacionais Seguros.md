# 💻 Ferramentas — Sistemas Operacionais Seguros

> Tags: #ferramentas #Tails #Qubes #Whonix #Linux #privacidade
← [[🛡️ Mapa Mental — Cibersegurança|Índice]] | Contexto: [[Nível 3 — Isolamento e Anonimato]]

---

## Tails
- **Site:** https://tails.boum.org
- **Instalação:** Pendrive bootável (Live USB)
- **Tráfego:** 100% via Tor
- **Rastros:** Zero — sistema amnésico
- **Uso:** Sessões sensíveis ocasionais, acesso em computadores de terceiros

## Whonix
- **Site:** https://www.whonix.org
- **Instalação:** Par de VMs (Gateway + Workstation)
- **Tráfego:** 100% via Tor (isolamento de rede)
- **Uso:** Desenvolvimento e uso anônimo em estação de trabalho dedicada

## Qubes OS
- **Site:** https://www.qubes-os.org
- **Instalação:** Sistema operacional principal
- **Arquitetura:** Múltiplas VMs isoladas (qubes)
- **Hardware mínimo:** 16GB RAM, CPU com VT-x/VT-d
- **Uso:** Usuários avançados que precisam de compartimentação no dia a dia

---

# 💾 Ferramentas — Backup e Armazenamento

> Tags: #ferramentas #backup #criptografia #armazenamento
← [[🛡️ Mapa Mental — Cibersegurança|Índice]] | Contexto: [[Nível 0 — Fundamentos]]

---

## Soluções de Backup

| Ferramenta | Plataforma | Tipo | Destaque |
|------------|-----------|------|----------|
| **Proton Drive** | Web / Mobile | Nuvem criptografada | E2EE nativo |
| **Tresorit** | Web / Desktop / Mobile | Nuvem criptografada | Zero-knowledge |
| **Cryptomator** | Todas | Camada de cripto | Criptografa qualquer nuvem |
| **BorgBackup** | Linux / macOS | Local / remoto | Deduplicação, incremental |
| **Restic** | Todas | Local / remoto | Simples, verificação de integridade |
| **Veeam Free** | Windows | Local | Backup de sistema completo |
| **Time Machine** | macOS | Local | Nativo, simples |

## Cryptomator — Use com qualquer nuvem
Permite criptografar arquivos **antes** de enviá-los para Google Drive, Dropbox, etc.:
```
Seus arquivos → Cryptomator (criptografa localmente) → Google Drive / Dropbox
```
A nuvem armazena apenas arquivos criptografados ilegíveis.

---

## 🔗 Veja também
- [[Nível 0 — Fundamentos#Rotina de Backups]]
- [[Ataques — Ransomware e Malware]]
