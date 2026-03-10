# 🥷 Nível 3 — Isolamento e Anonimato (OPSEC)

> **Para quem lida com dados altamente sensíveis, pesquisa segurança ou quer pegada digital mínima.**
> Tags: #segurança #OPSEC #anonimato #isolamento #privacidade #avançado

← [[🛡️ Mapa Mental — Cibersegurança|Voltar ao índice]] | ← [[Nível 2 — Rede e Navegação]]

---

## O que é OPSEC?

**OPSEC (Operations Security)** é a prática de identificar e proteger informações que, se obtidas por um adversário, poderiam comprometer você. Originou-se na inteligência militar e foi adaptada para segurança digital.

Veja mais → [[Conceitos — OPSEC]]

**Pergunta central do OPSEC:** *"O que um adversário poderia fazer com essa informação?"*

---

## 1. 🖼️ Limpeza de Metadados (EXIF)

Toda foto tirada com celular ou câmera digital contém metadados **invisíveis mas presentes**:

```
Dados EXIF típicos de uma foto:
├── GPS: latitude -23.5505, longitude -46.6333  ← sua localização exata
├── Data e hora: 2026-03-04 14:32:11
├── Dispositivo: iPhone 15 Pro
├── Software: iOS 18.2
├── Abertura, ISO, velocidade do obturador
└── Às vezes: nome do proprietário do dispositivo
```

### Por que isso é crítico
- Jornalistas, ativistas e vítimas de assédio já foram localizados por metadados em fotos
- Redes sociais como Facebook e Twitter removem EXIF ao fazer upload — mas WhatsApp e e-mail não

### Ferramentas para remoção

| Ferramenta | Plataforma | Uso |
|------------|-----------|-----|
| **ExifTool** | Windows / macOS / Linux | CLI — mais completo e confiável |
| **Scramble** | Web / Mobile | Interface simples |
| **MAT2** | Linux | Suporta múltiplos formatos além de imagem |
| **Metapho** | iOS | Visualiza e remove metadados |

### Comando rápido ExifTool
```bash
# Remover todos os metadados de uma foto
exiftool -all= foto.jpg

# Remover de todas as fotos numa pasta
exiftool -all= *.jpg

# Verificar metadados antes de remover
exiftool foto.jpg
```

Veja também → [[Checklist — Antes de Enviar Arquivos ou Fotos]]

---

## 2. 📦 Ambientes Confinados (Sandboxing)

**Nunca abra arquivos suspeitos ou links desconhecidos no seu sistema principal.**

Um PDF malicioso aberto no seu sistema pode instalar malware, exfiltrar dados ou criptografar arquivos (ransomware). A solução: isolamento.

### Conceito
Veja → [[Conceitos — Sandboxing e Isolamento]]

### Ferramentas de Sandboxing

#### Leves (para uso cotidiano)
| Ferramenta | Plataforma | Descrição |
|------------|-----------|-----------|
| **Windows Sandbox** | Windows 10/11 Pro | VM descartável nativa — fecha e apaga tudo |
| **Firejail** | Linux | Sandbox por processo — excelente para apps individuais |
| **Flatpak** | Linux | Apps isolados por design |

#### Avançadas
| Ferramenta | Descrição |
|------------|-----------|
| **Kasm Workspaces** | Navegadores e desktops em contêineres na nuvem — feche a aba, ambiente destruído |
| **VirtualBox / VMware** | Máquinas virtuais completas — snapshots permitem reverter ao estado limpo |
| **Dangerzone** | Converte PDFs e documentos suspeitos em versões seguras |

### Fluxo recomendado para arquivos suspeitos
```
Recebeu arquivo suspeito?
  ↓
1. NÃO abra no sistema principal
2. Upload no VirusTotal (virustotal.com) — escaneia com 70+ antivírus
3. Se precisar abrir: use Kasm, Windows Sandbox ou VM descartável
4. Se for PDF: use Dangerzone para sanitizar
```

---

## 3. 💻 Sistemas Operacionais Focados em Privacidade

### 🟢 Tails — O Sistema Amnésico

**Filosofia:** Deixar zero rastros. Cada sessão começa do zero.

- Roda diretamente de um **pendrive** (Live USB)
- Todo o tráfego passa pela **rede Tor** automaticamente
- Ao desligar, **apaga completamente** a memória RAM — não deixa rastros no computador
- Inclui ferramentas: Tor Browser, KeePassXC, Thunderbird, MAT2, OnionShare

**Ideal para:** Jornalistas, ativistas, acesso a documentos sensíveis em computadores de terceiros.

> ⚠️ **Limitação:** Não é para uso diário. Sem persistência por padrão (configurável).

---

### 🔵 Whonix — Anonimato via Isolamento de Rede

**Filosofia:** Separação total entre o que você usa e como você se conecta.

```
Whonix-Gateway (VM 1)     Whonix-Workstation (VM 2)
  ↕ Rede Tor               ↕ Sem acesso direto à internet
  └─────────────────────────┘
         Comunicação interna apenas
```

- A Workstation é incapaz de vazar seu IP real — mesmo com malware
- Roda em cima de VirtualBox ou Qubes OS
- Aplicativos na Workstation não sabem seu IP real

---

### 🔴 Qubes OS — Segurança por Compartimentação

**Filosofia:** Cada tarefa em uma VM separada. Comprometer uma não compromete as outras.

```
Qubes OS
├── Qube: Trabalho (acesso a arquivos corporativos)
├── Qube: Pessoal (redes sociais, e-mail pessoal)
├── Qube: Banco (apenas acesso bancário)
├── Qube: Pesquisa (abrir links e arquivos suspeitos)
├── Qube: Tor (navegação anônima via Whonix)
└── Qube: Vault (sem internet — apenas senha e chaves)
```

- Baseado em Xen Hypervisor
- Considerado um dos sistemas mais seguros para uso desktop
- Curva de aprendizado alta — não é para iniciantes
- Recomendado por Edward Snowden

---

### Comparativo dos Sistemas

| Sistema | Anonimato | Facilidade | Uso diário | Hardware |
|---------|-----------|------------|-----------|----------|
| Tails | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ❌ | Qualquer |
| Whonix | ⭐⭐⭐⭐⭐ | ⭐⭐ | Parcial | Moderado |
| Qubes OS | ⭐⭐⭐⭐ | ⭐ | ✅ | Alto (16GB+ RAM) |
| Kali Linux | ⭐⭐ | ⭐⭐ | ❌ | Qualquer |

---

## 4. 🧅 Rede Tor — Entendendo o Anonimato

O Tor roteia seu tráfego por **3 nós voluntários** ao redor do mundo, cada um conhecendo apenas o anterior e o próximo — nenhum conhece origem + destino ao mesmo tempo.

```
Você → [Nó 1: Guard] → [Nó 2: Middle] → [Nó 3: Exit] → Site destino
         Sabe: você          Nada             Sabe: destino
```

### Quando usar Tor
- ✅ Acessar .onion sites
- ✅ Máxima privacidade em pesquisas sensíveis
- ✅ Contornar censura

### Limitações do Tor
- Lento — múltiplos saltos aumentam latência
- O nó de saída pode ver tráfego não-HTTPS
- Não protege contra malware no dispositivo
- Alguns sites bloqueiam IPs Tor

---

## 5. 🔏 Comunicações Seguras Avançadas

### OnionShare
Compartilhe arquivos e hospede sites através da rede Tor.
- Receptor não precisa de conta
- Link `.onion` temporário
- Zero rastros no servidor (você *é* o servidor)

### PGP / GPG — Criptografia de E-mail
Padrão de criptografia assimétrica para e-mails.
```bash
# Gerar par de chaves
gpg --full-generate-key

# Exportar chave pública (compartilhe com contatos)
gpg --export --armor seu@email.com > publica.asc

# Criptografar arquivo para destinatário
gpg --encrypt --recipient contato@email.com arquivo.txt
```

> 💡 O Signal é mais prático para comunicação diária — veja [[Nível 4 — Engenharia Social]].

---

## 🔗 Links relacionados

- ← [[Nível 2 — Rede e Navegação]]
- → [[Nível 4 — Engenharia Social]]
- Conceitos → [[Conceitos — OPSEC]] | [[Conceitos — Sandboxing e Isolamento]] | [[Conceitos — Metadados EXIF]]
- Ferramentas → [[Ferramentas — Sistemas Operacionais Seguros]]
- Checklist → [[Checklist — Antes de Enviar Arquivos ou Fotos]]
