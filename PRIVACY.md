# Privacy Policy

**CertLens - Certificates and Keystores**
Version 1.0, 24 September 2026
Vendor: **Muhammad Zuhaib Zahid**

## The short version

**The plugin collects nothing.** It has no telemetry, no analytics, no crash reporting and no
network communication of its own. Your certificates, private keys, keystores, passwords and file
names never leave your machine.

That matters more here than for most plugins. A keystore holds the private keys that identify your
servers, and a leaked key is a security incident, not an inconvenience.

## What that means in detail

- **Your files.** CertLens reads certificates and keystores entirely on your own computer, inside
  your IDE's process. Nothing about them, including their contents, subjects, fingerprints, file
  names or folder paths, is transmitted, stored elsewhere or seen by the Vendor.
- **Private keys.** CertLens never displays or exports private key bytes. It reports a key's
  algorithm and size, and nothing more.
- **Passwords.** A keystore password you type is used to open that keystore and then discarded,
  unless you tick Remember password. In that case it is stored in the IDE's own password safe
  (which uses your operating system's credential store where available), never in a file of
  CertLens's own and never in a log.
- **The Certificate Radar** reads the files in your open project on your machine. Its findings are
  shown in the IDE and kept in memory only.
- **No usage tracking.** The plugin does not record which features you use or anything about your
  projects.
- **No accounts.** The plugin asks you for no personal information and has no sign-in of its own.
- **The bundled libraries do not collect anything either.** CertLens ships the Bouncy Castle
  libraries, listed in `THIRD-PARTY.md`. They parse and build certificates in memory and open no
  network connection.

## What the Vendor does receive

Only what you choose to send:

- **A purchase.** JetBrains sells CertLens Pro as merchant of record and shares with the Vendor the
  sales information needed to be paid and to comply with tax law. What JetBrains collects at
  purchase is covered by the [JetBrains Privacy Policy](https://www.jetbrains.com/legal/docs/privacy/privacy.html).
- **Support you initiate.** If you email the Vendor or open an issue, the Vendor receives what you
  write, including any file you attach. **Never attach a real private key or a keystore that holds
  one.** A public certificate, or a keystore you generated for the purpose, is enough to reproduce a
  problem.

## Licence validation

Checking that a licence or trial is valid is performed by **the JetBrains IDE**, not by this plugin,
using JetBrains' own licensing service. That exchange is governed by JetBrains' terms and privacy
policy.

## Changes

If this policy ever changes, the revised version will be published at this address with a new date
at the top.

## Contact

Questions about this policy: Muhammad Zuhaib Zahid, via the email address on the JetBrains
Marketplace vendor profile for CertLens - Certificates and Keystores, or by opening an issue on the
public issue tracker linked from the Marketplace listing.
