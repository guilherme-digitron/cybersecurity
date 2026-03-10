# 🌐 Nível 2 — Rede e Navegação

> **Defenda o tráfego de dados — seus dados não devem ser interceptados ou rastreados.**
> Tags: #segurança #rede #DNS #VPN #navegação #firewall

← [[🛡️ Mapa Mental — Cibersegurança|Voltar ao índice]] | ← [[Nível 1 — Identidade e Acessos]]

---

## 1. 🔍 DNS Customizado com Filtro

O DNS (Domain Name System) é a "lista telefônica" da internet — traduz `google.com` para `142.250.x.x`. Por padrão, você usa o DNS do seu provedor de internet (ISP), o que expõe **todo o seu histórico de navegação** para ele.

### Problemas com o DNS padrão do ISP
- Registra quais sites você acessa (pode ser vendido ou requisitado judicialmente)
- Não bloqueia domínios maliciosos
- Pode ser manipulado (DNS Hijacking) para redirecionar para sites falsos

### Alternativas recomendadas

| Provedor | Endereço | Foco |
|----------|----------|------|
| Cloudflare | `1.1.1.1` / `1.0.0.1` | Velocidade + privacidade |
| Cloudflare Malware | `1.1.1.2` / `1.0.0.2` | Bloqueia malware nativamente |
| Quad9 | `9.9.9.9` / `149.112.112.112` | Privacidade + segurança |
| NextDNS | Personalizado | Controle total — listas customizadas |
| AdGuard DNS | `94.140.14.14` | Bloqueio de anúncios e rastreadores |

> 💡 **NextDNS:** Permite criar um perfil com listas de bloqueio (anúncios, rastreadores, malware, NSFW) e ver logs de consultas. Excelente para redes domésticas.

### DNS over HTTPS (DoH) e DNS over TLS (DoT)
Protocolos que **criptografam** as consultas DNS, impedindo que seu ISP as leia.
- Configure no próprio navegador (Firefox, Brave)
- Ou no sistema operacional (Windows 11, macOS Ventura+, Android 9+)

---

## 2. 🧱 Firewall

Filtra o tráfego de entrada e saída da sua rede ou dispositivo.

### Camadas de firewall

```
Internet
   ↓
[Roteador / Firewall de Rede]  ← primeira barreira
   ↓
[Firewall do Sistema Operacional]  ← segunda barreira
   ↓
[Firewall de Aplicação / Host-based]  ← terceira barreira
```

### Para uso doméstico
O firewall nativo do sistema + do roteador são suficientes se configurados corretamente:
- **Windows:** Defender Firewall (ativado por padrão) — crie regras de bloqueio de saída para apps suspeitos
- **macOS:** Firewall nativo (Preferências → Segurança → Firewall)
- **Linux:** `ufw` (Uncomplicated Firewall) — simples e eficaz

### Para laboratórios ou controle avançado

| Solução | Uso |
|---------|-----|
| **pfSense** | Firewall open source para roteadores dedicados |
| **OPNsense** | Fork do pfSense, interface mais moderna |
| **FortiGate** | Solução empresarial com inspeção profunda de pacotes |
| **Little Snitch** (macOS) | Controle por aplicativo de conexões de saída |
| **GlassWire** (Windows) | Monitoramento visual de tráfego por app |

> 💡 **Segmentação de rede:** Em redes avançadas, separe dispositivos IoT (câmeras, smart TVs) em uma VLAN isolada — eles costumam ter segurança fraca.

---

## 3. 🌐 Navegação e Extensões Blindadas

### Navegadores recomendados

| Navegador | Destaque |
|-----------|----------|
| **Brave** | Bloqueio nativo de anúncios, rastreadores e fingerprinting |
| **Firefox** | Altamente configurável, open source — use com hardening |
| **Tor Browser** | Anonimato via rede Tor — lento, mas máximo em privacidade |

> ❌ Evite Chrome para fins de privacidade — coleta extensivos dados de comportamento para o Google.

### Extensões essenciais

| Extensão | Função |
|----------|--------|
| **uBlock Origin** | Bloqueador de anúncios e scripts maliciosos — **mandatório** |
| **Privacy Badger** | Aprende e bloqueia rastreadores automaticamente |
| **HTTPS Everywhere** | Força HTTPS (já desnecessária em browsers modernos, mas útil) |
| **Cookie AutoDelete** | Limpa cookies de abas fechadas automaticamente |
| **LocalCDN / Decentraleyes** | Serve bibliotecas JS localmente, evitando CDNs rastreadores |

### Configurações de privacidade no Firefox (Hardening)
```
about:config → privacy.resistFingerprinting = true
about:config → privacy.firstparty.isolate = true
Configurações → DNS sobre HTTPS → Ativar com NextDNS ou Cloudflare
```

> ⚠️ **Fingerprinting:** Sites podem identificar você sem cookies, usando combinação de: resolução de tela, fontes instaladas, fuso horário, GPU, etc. O Brave e Tor Browser combatem isso nativamente.

### HTTPS — Sempre
- Verifique o cadeado 🔒 na barra de endereços
- Nunca insira senhas ou dados sensíveis em sites `http://`
- Certificados SSL gratuitos estão disponíveis (Let's Encrypt), então "tem cadeado" ≠ "é confiável" — phishing pode usar HTTPS também

---

## 4. 🔒 VPNs — Quando e Como Usar

### O que uma VPN faz
- Cria um **túnel criptografado** entre você e o servidor VPN
- Seu ISP vê apenas tráfego criptografado, não os sites acessados
- O site destino vê o IP do servidor VPN, não o seu

### O que uma VPN **NÃO** faz
- ❌ Não te torna anônimo — a VPN vê seu tráfego no lugar do ISP
- ❌ Não protege contra malware ou phishing
- ❌ Não substitui HTTPS

### Quando usar
- ✅ **Redes Wi-Fi públicas** (café, aeroporto, hotel) — proteção contra [[Ataques — Man-in-the-Middle (MitM)|ataques MitM]]
- ✅ Contornar bloqueios geográficos
- ✅ Ocultar navegação do ISP

### VPNs recomendadas

| Serviço | Destaque |
|---------|----------|
| **Mullvad** | Sem conta, pagamento em dinheiro/crypto, sem logs |
| **ProtonVPN** | Open source, auditado, gratuito com limites |
| **IVPN** | Focado em privacidade, sem logs verificado |

> ⚠️ **Evite VPNs gratuitas** — em geral, o produto é *você*. Seus dados são vendidos para custear o serviço.

### WireGuard vs OpenVPN
- **WireGuard:** Mais rápido, código menor (menor superfície de ataque), moderno
- **OpenVPN:** Mais antigo, amplamente auditado, mais lento

---

## 5. 📡 Desligar Rádios Ociosos

Bluetooth e Wi-Fi ativos são vetores de ataque mesmo quando não conectados.

### Riscos
- **Bluetooth:** Ataques BlueBorne, Bluesnarfing (acesso a dados), rastreamento de localização
- **Wi-Fi:** Redes "honeypot" (redes falsas com nomes conhecidos), rastreamento por MAC address

### Boas práticas
- [ ] Desative Bluetooth quando sair de casa (ou não estiver usando)
- [ ] Desative Wi-Fi em locais públicos onde não vai conectar
- [ ] Ative a **aleatorização de endereço MAC** (Android 10+, iOS 14+, Windows 10+)
- [ ] Não conecte em redes abertas sem VPN ativa
- [ ] Esqueça redes públicas após o uso (impedem reconexão automática)

> 💡 No Android: Configurações → Privacidade → MAC aleatório por rede.

---

## 🔗 Links relacionados

- ← [[Nível 1 — Identidade e Acessos]]
- → [[Nível 3 — Isolamento e Anonimato]]
- Ataques mitigados → [[Ataques — Man-in-the-Middle (MitM)]] | [[Ataques — Ransomware e Malware]]
- Ferramentas → [[Ferramentas — VPN e DNS]] | [[Ferramentas — Navegadores e Extensões]]
- Checklist → [[Checklist — Antes de Usar Wi-Fi Público]]
