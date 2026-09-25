# CertLens - Certificates and Keystores

Support, documentation and legal documents for the **CertLens** plugin for JetBrains IDEs.

**[Get it on the JetBrains Marketplace](https://plugins.jetbrains.com/plugin/34504-certlens--certificates-and-keystores)**

**This repository holds no source code.** It exists so that the plugin has a real issue tracker and
real documentation, both linked from the Marketplace listing.

- **Report a bug or ask for a feature:** [open an issue](../../issues). Every issue is read and
  answered.

---

## What the plugin does

It reads certificates and keystores inside your IDE, and tells you about expiry before production
does.

Open a JKS keystore, a PKCS#12 file or a PEM bundle and CertLens shows what is inside: every
certificate, its chain, its names and its dates, with a banner at the top that says straight away
whether anything in the file has expired or is about to.

## Getting started

1. Install **CertLens** from **Settings, Plugins, Marketplace**.
2. Open any certificate or keystore in your project. It opens in the CertLens viewer.
3. For a keystore, enter the store password. Tick **Remember password** to keep it in the IDE's
   own password safe, so the Certificate Radar can read it too.

## Free: the viewer

- **Keystores:** JKS, JCEKS and PKCS#12 (.p12, .pfx).
- **Certificate files:** PEM bundles, single certificates, DER, P7B and PKCS#10 signing requests.
- **Every detail on one screen:** subject, issuer, subject alternative names, key algorithm and
  size, signature algorithm, SHA-1 and SHA-256 fingerprints and the validity period.
- **A validity banner** on every file: expired, expiring within 30 days, or valid.
- **ASN.1 view** of any opened certificate.

## Pro: the Certificate Radar and the tools

- **Certificate Radar.** Scans the whole project when it opens and lists every expired
  certificate, every certificate expiring within 30 days, weak keys (RSA under 2048 bits, EC under
  256), self-signed certificates and chains in the wrong order. A notification says what it found.
  Double-click a finding to open the file.
- **Convert:** a keystore's certificates to PEM, or a DER certificate to PEM.
- **Generate:** a self-signed certificate with the DNS names you list, written as a PKCS#12
  keystore and a PEM certificate.
- **Compare:** two certificates field by field, side by side, to see what a renewal changed.

The tools are in **Tools, CertLens**. The Radar is its own tool window.

## Pricing

- **The viewer is free**, with no time limit.
- **CertLens Pro, personal:** $1.50 per month, or $15 per year.
- **CertLens Pro, commercial:** $4.90 per month, or $49 per year.
- **30-day free trial** of everything in Pro. Start it from the link in the Certificate Radar tool
  window, or from **Help, Manage Subscriptions**.

## Known limits

- BKS and UBER keystores are not supported. They are reported as unsupported rather than shown half
  read.
- The Radar reads a keystore only once its password has been entered and remembered in the IDE.
- Private keys cannot be exported, by design.
- Files larger than 8 MB are skipped by the Radar.

## Privacy

CertLens makes no network requests. Keystore passwords go only into the IDE's password safe, and
only when you ask it to remember them.

## Support

Open an issue here. Include the IDE and version (**Help, About**), the plugin version, and the kind
of file involved. **Never attach a real private key or keystore.** A certificate on its own is
public information; a key is not.

## Legal

- [End User Licence Agreement](EULA.md)
- [Privacy Policy](PRIVACY.md)
- [Third-party notices](THIRD-PARTY.md)

The plugin itself is not open source. This repository is for support and documentation only.
