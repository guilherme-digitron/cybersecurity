# 🔒 Ferramentas — VPN e DNS

> Tags: #ferramentas #VPN #DNS #rede #privacidade
← [[🛡️ Mapa Mental — Cibersegurança|Índice]] | Contexto: [[Nível 2 — Rede e Navegação]]

---

## VPNs Recomendadas

| Serviço | Preço | Logs | Destaques |
|---------|-------|------|-----------|
| **Mullvad** | €5/mês | Nenhum | Sem conta (número ID), aceita dinheiro/crypto |
| **ProtonVPN** | Grátis / Pago | Nenhum | Open source, auditado, gratuito generoso |
| **IVPN** | US$6/mês | Nenhum | Focado em privacidade, auditado |

> ❌ Evite: HolaVPN, SuperVPN, UFO VPN, e qualquer VPN "grátis" sem modelo de negócio claro.

---

## DNS Recomendados

| Provedor | IPv4 Primário | Secundário | Foco |
|----------|--------------|------------|------|
| **Cloudflare** | `1.1.1.1` | `1.0.0.1` | Velocidade + privacidade |
| **Cloudflare Malware** | `1.1.1.2` | `1.0.0.2` | Bloqueia malware |
| **Quad9** | `9.9.9.9` | `149.112.112.112` | Segurança + privacidade |
| **AdGuard DNS** | `94.140.14.14` | `94.140.15.15` | Bloqueia anúncios |
| **NextDNS** | Personalizado | — | Controle total, logs, listas customizadas |

### DNS over HTTPS (DoH)
- Firefox: Configurações → DNS sobre HTTPS → Ativar
- Windows 11: Configurações → Rede → Servidor DNS → DoH
- Android 9+: Configurações → Rede → DNS privado → `dns.nextdns.io`

---

## 🔗 Veja também
- [[Nível 2 — Rede e Navegação]]
- [[Ataques — Man-in-the-Middle (MitM)]]
