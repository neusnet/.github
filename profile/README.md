<div align="center">
  <img src="https://raw.githubusercontent.com/neusnet/neusnet/main/resources/img/neusnet-logo.png" width="260" alt="Neusnet Logo"><br><br>

  <h1>Neusnet</h1>

<i>"The world is hers, but she can share it with you."</i><br>

<strong>The Domain-Anchored Content Distribution Protocol</strong><br><br>

  <img src="https://img.shields.io/badge/License-Apache_2.0-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/Status-In_Development-orange.svg" alt="Status">
  <img src="https://img.shields.io/badge/Default_Port-22123-77dddd" alt="Default Port">
</div>

---

## What Is Neusnet?

Neusnet is a **domain-anchored, federated content distribution protocol** that lets a domain name work as a distributed filesystem. Publish files at `neus://yourdomain.com`, and anyone can browse them, mirror them, and help keep them alive.

It combines the **trust of DNS**, the **resilience of federation**, and the **simplicity of HTTP**.

**No blockchain. No tokens. No corporate control. Just the web, working right.**

_Pronounced "neus", like "news" — because information is meant to be shared._

## How It Works

- **Identity through DNS** — a TXT record at `_neusnet.example.com` publishes the domain's public key.
- **Content addressing** — files are stored by SHA-256 hash: immutable, deduplicated, verifiable.
- **Signed manifests** — Ed25519 signatures tie every manifest to the domain's DNS identity.
- **Edge-to-edge federation** — mirrors pull over plain, stateless HTTP and fall back to the origin. Popular content gets faster and more resilient as more nodes join.

## A Quick Taste

```bash
# Publish a folder from your domain
neus init --domain yourdomain.com
neus publish ./docs --bucket public --at collection

# Mirror someone else's domain
neus mirror example.com
neus vfs --mirror example.com
```

## Repositories

| Repository                                          | Description                                                          |
| --------------------------------------------------- | -------------------------------------------------------------------- |
| [neusnet/neusnet](https://github.com/neusnet/neusnet) | Reference implementation (Bun + TypeScript), CLI, daemon and protocol docs |

## Status

Neusnet is in **alpha**, currently in the **Edge Federation** phase: content-addressed storage, signed manifests, DNS-anchored identity, mirroring and a zero-copy virtual filesystem work today. Background sync, garbage collection and lazy hydration are next. See the [roadmap](https://github.com/neusnet/neusnet/blob/main/MANIFESTO.md#roadmap).

## Get Involved

Neusnet is open source and built by people who see the internet as shared infrastructure.

- 📜 Read the [Manifesto](https://github.com/neusnet/neusnet/blob/main/MANIFESTO.md) for the vision and philosophy
- 🛠️ Dive into the [Technical Specification](https://github.com/neusnet/neusnet/blob/main/docs/architecture/technical-spec.md)
- 🤝 Read [CONTRIBUTING](https://github.com/neusnet/neusnet/blob/main/CONTRIBUTING.md) — open an issue first; protocol changes always need one
- 💬 Share ideas and report problems in [Issues](https://github.com/neusnet/neusnet/issues)

---

<div align="center">
  <strong>Neusnet: the preservation of knowledge is everyone's responsibility.</strong>
</div>
