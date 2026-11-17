# uTest Academy · Testing Tools · 05: Web Debugging Proxy

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído · quiz 10 de 10 / Completed · quiz 10 of 10 |
| Fonte / Source | [uTest Academy: Web Debugging Proxy](https://platform.utest.com/academy/tracks/6/courses/41/lessons/what-is-a-web-debugging-proxy) (login) |
| Referências / References | [Charles Proxy](https://www.charlesproxy.com/) · [Charles: SSL Proxying](https://www.charlesproxy.com/documentation/proxying/ssl-proxying/) · [Fiddler (Telerik)](https://www.telerik.com/fiddler) |

## O que é / What it is
🇧🇷 Um programa que fica **no meio** entre o seu aparelho e a internet, como um servidor proxy, e registra **todo o tráfego HTTP/HTTPS**. Ajuda os desenvolvedores a achar problemas de rede. 🇺🇸 A proxy that captures **all HTTP/HTTPS traffic** between your device and the internet.

~~~mermaid
flowchart LR
    M[Celular ou computador<br/>Phone or computer] -- proxy IP:porta --> P[Charles / Fiddler<br/>no computador<br/>on the computer]
    P --> I[Internet / site ou app testado<br/>tested site or app]
    P --> L[Log salvo<br/>.chls / .chlz / .saz]
~~~

## Requisitos do log / Log requirements
| 🇧🇷 | 🇺🇸 |
|---|---|
| **Descriptografado**: instale o **certificado raiz** para ver o HTTPS | **Decrypted**: install the **root certificate** |
| Precisa ter tráfego do **site ou app testado** | Must contain the **tested site/app** traffic |
| Formato: **Charles = .chls ou .chlz**, **Fiddler = .saz** | Format: **Charles .chls/.chlz**, **Fiddler .saz** |
| Envie **o log inteiro**, não só itens escolhidos | Upload the **entire log** |

## Antes de começar / Before starting
- 🇧🇷 **Desligue a VPN** (no computador e no celular). 🇺🇸 **Disable VPN** on both.
- 🇧🇷 **Firewall e antivírus**: adicione o Charles ou Fiddler como **exceção**, sem desligar a proteção inteira. 🇺🇸 Add as an **exception**, don't disable protection.
- 🇧🇷 Computador e celular na **mesma rede Wi-Fi**. Sem roteador? Use um **segundo celular como hotspot** e conecte os dois aparelhos nele. 🇺🇸 Same Wi-Fi; or use a second phone as a **hotspot**.

## Charles Proxy
**Computador / Desktop**
1. 🇧🇷 Instalar → Help → SSL Proxying → **Install Charles Root Certificate** (Windows: "Trusted Root Certification Authorities"; macOS: Acesso às Chaves → **Sempre confiar**). 🇺🇸 Install & trust the root certificate.
2. 🇧🇷 Proxy → **SSL Proxy Settings** → **Enable SSL Proxying** → Add → Host <code>*</code>, Port <code>443</code> (o <code>*</code> descriptografa tudo). 🇺🇸 Host <code>*</code>, Port <code>443</code> decrypts all.
3. 🇧🇷 🧹 limpar → reproduzir a partir da home → File → **Save Session** (.chls ou .chlz). 🇺🇸 Clear → reproduce → Save Session.

**Celular / Mobile**
1. 🇧🇷 No Charles: Help → **Local IP Address** (anote, ex.: 192.168.8.111); Proxy Settings → porta **8888**. 🇺🇸 Note the IP; port **8888**.
2. 🇧🇷 No Wi-Fi do celular: proxy **Manual** → host = IP do computador, porta 8888. Quando o Charles pedir permissão, **Allow**. 🇺🇸 Manual proxy → **Allow** the request in Charles.
3. 🇧🇷 No navegador do celular: **chls.pro/ssl** → instalar o certificado (Android 11+: Configurações → Segurança → Instalar certificado → **Certificado CA**; iOS: instalar o perfil e **ativar a confiança total**). 🇺🇸 Visit **chls.pro/ssl** and install/trust the cert.
4. 🇧🇷 Desligue o **macOS/Windows Proxy** dentro do Charles: assim ele **não grava o tráfego do computador**, só o do celular. 🇺🇸 Turn off the computer proxy so **computer traffic isn't recorded**.

**Perfis e filtros / Profiles and filters**
- 🇧🇷 Se o ciclo enviar um **perfil (.xml)**: Tools → Import/Export Settings → Import; trocar em Tools → **Profiles**. Sem perfil nem instrução: use o **padrão**, com todo o tráfego. 🇺🇸 Import the cycle's profile; otherwise use the default.
- 🇧🇷 Proxy → **Recording Settings** → **Include** (só aquele domínio) ou **Exclude** (tudo menos ele). <code>*utest*</code> pega utest.com, .net, .io…; <code>*utest.com*</code> pega só utest.com. 🇺🇸 Include/Exclude by host pattern.

## Fiddler
- 🇧🇷 **Fiddler Classic**: só Windows, grátis. **Fiddler Everywhere**: Windows, macOS e Linux, **trial de 10 dias** e precisa de conta. Veja no Overview qual o ciclo pede. 🇺🇸 Classic (Windows) vs Everywhere (cross-platform, 10-day trial).
- 🇧🇷 HTTPS: Settings → HTTPS → **Trust Fiddler CA** + **Capture HTTPS traffic** (Classic: Tools → Options → HTTPS → **Decrypt HTTPS traffic**). 🇺🇸 Trust the CA and enable HTTPS capture.
- 🇧🇷 Celular: Settings → Connections → **Allow remote computers to connect**, porta **8866**; certificado em <code>http://ipv4.fiddler:8866/FiddlerRoot.cer</code>; desligue o **Live Traffic** do computador; salvar em **.saz** sem criptografia. 🇺🇸 Port **8866**; save **.saz**.
- 🇧🇷 IP local: Windows <code>ipconfig /all</code> (IPv4); macOS **Utilitário de Rede** → Info. 🇺🇸 Local IP via ipconfig / Network Utility.

## FAQ rápido / Quick FAQ
- 🇧🇷 "Página não encontrada" no celular → confira se o proxy está aberto no computador, a mesma rede, a VPN desligada e o firewall liberado. 🇺🇸 Check proxy running, same network, no VPN, firewall exception.
- 🇧🇷 "Conexão não segura" ao instalar o certificado → Avançado → Prosseguir; ou digite <code>chls.pro/ssl</code> sem http/https. 🇺🇸 Proceed anyway or type without protocol.

## Quiz comentado / Commented quiz (10/10)
1. SSL Proxy que descriptografa tudo / Decrypts all → ✅ **Host: * e Port: 443** (❌ 8888 é a porta do proxy, não do SSL).
2. Por que instalar o certificado raiz / Why the root cert → ✅ **Permite descriptografar o HTTPS**.
3. Antes de usar o proxy / Before using it → ✅ **Todas**: tirar a VPN e liberar no firewall e no antivírus.
4. Link do certificado do Charles no celular / Cert link → ✅ **http://chls.pro/ssl**.
5. NÃO é web debugging proxy / NOT a proxy → ✅ **Google Chrome**.
6. Conectar o celular ao proxy / Connect mobile → ✅ **Todas**: proxy configurado, VPN e firewall desligados, mesma rede.
7. Formato do Charles / Charles format → ✅ **.chls ou .chlz** (.saz é do Fiddler).
8. Charles pediu permissão para conectar / Permission prompt → ✅ **Allow**.
9. Achar o IP local no macOS / Local IP on macOS → ✅ **Utilitário de Rede / Network Utility**.
10. Por que desligar o proxy do Windows/macOS ao gravar o celular / Why turn off the computer proxy → ✅ **Para não gravar o tráfego do computador**.
