# 📰 Byline - Secure Messenger for Journalists

> **For journalists and their sources**  
> Operational Security by Design

---

## 🎯 What is Byline?

Byline is a secure messaging application built specifically for journalists, activists, and media organizations working in environments with press freedom restrictions.

**Unlike other messengers, Byline protects against operational security failures—not just cryptography failures.**

The inspiration: Signal scandal (March 2025) where a journalist was accidentally added to a classified group chat. The crypto was fine. The problem was *design*.

---

## 💡 Why Byline?

### ✅ Operational Security by Design
- Group actions are logged and auditable
- No silent member additions
- Device fingerprinting for visibility
- Full group history

### ✅ Military-Grade Encryption
- Double Ratchet algorithm (like Signal)
- End-to-end encryption on every message
- Perfect forward secrecy
- No backdoors, no master keys

### ✅ Zero Knowledge
- Server knows nothing (can't decrypt)
- No metadata (server doesn't know who messaged whom)
- No logs (no user activity tracking)
- Cryptographic identity only (no phone number)

### ✅ Open Source & Transparent
- Full source code on GitHub
- Reproducible builds
- Independent security audits
- Complete transparency

### ✅ DPI Bypass (coming v1.1)
- Works where other messengers are blocked
- Masquerades as normal HTTPS traffic
- VLESS + REALITY protocol
- Tested and proven

---

## 🗓️ Development Status

### Current Phase: MVP Planning
- [x] Positioning & strategy finalized
- [x] Competitive analysis completed
- [x] Go-to-market strategy defined
- [x] Brand naming completed (Byline)
- [ ] Closed beta development (8 weeks)
- [ ] Public release & open source

### Timeline
- **Weeks 1-8:** Closed beta MVP (E2EE + ops logging)
- **Week 9+:** v1.1 patch (DPI bypass)
- **Month 4+:** Public beta + scale

---

## 🏗️ Tech Stack

### Client
- **iOS / macOS:** SwiftUI
- **Core Engine:** Rust (Crypto, Transport, Storage)
- **Cryptography:** Double Ratchet, Ed25519, libsodium
- **Storage:** SQLite + SQLCipher (AES-256)
- **Bridge:** UniFFI (Swift ↔ Rust)

### Server
- **Language:** Go
- **Transport:** Xray-core (VLESS + REALITY for v1.1)
- **Storage:** Redis (temporary, 24h TTL)
- **Architecture:** Relay server (zero knowledge)

### Deployment
- **Docker Compose**
- **Self-hosted** (not relying on cloud giants)

---

## 📋 MVP Scope (v1.0)

### ✅ Included
- User registration (Public Key ID, no phone)
- 1-to-1 E2EE messaging
- Group messaging with ops logging
- Device fingerprinting
- Local encrypted history
- Seed phrase recovery
- Zero metadata on server

### ❌ Coming Later
- DPI bypass (→ v1.1)
- File sharing (→ v1.1)
- Multi-device sync (→ v2.0)
- Desktop clients (→ v2.0)
- Voice/video calls (→ v2.0+)

---

## 🎯 Target Audience

**Primary:** Journalists in countries with press freedom restrictions  
**Secondary:** Activists, NGO workers, human rights defenders  
**Global:** Anyone who can't afford operational security failures

### Examples
- Journalists in Turkey, Belarus, Russia, Iran
- Whistleblowers and leakers
- International news organizations
- Human rights groups

---

## 🚀 Getting Started (Development)

### For Contributors

```bash
# Clone the repo
git clone https://github.com/byline-messenger/byline
cd byline

# Install dependencies
# See CONTRIBUTING.md for detailed setup

# Run tests
cargo test

# Build for local testing
# See DEVELOPMENT.md for instructions
```

### For Users

Closed beta is coming soon. [Sign up here](https://byline-messenger.github.io/#beta).

---

## 📚 Documentation

- **[Vision & Strategy](./docs/VISION.md)** - Product positioning, competitive analysis
- **[MVP Plan](./docs/MVP_PLAN.md)** - 8-week development roadmap
- **[Architecture](./docs/ARCHITECTURE.md)** - Technical architecture
- **[Security Model](./docs/SECURITY.md)** - Trust model and threat analysis
- **[Contributing](./CONTRIBUTING.md)** - How to contribute

---

## 🔒 Security & Privacy

### Cryptography
- Double Ratchet Algorithm (industry standard)
- Ed25519 for identity
- AES-256-GCM for encryption
- libsodium for all crypto operations

### Architecture
- Zero-knowledge relay server
- No plaintext logs
- No metadata tracking
- Reproducible builds for verification

### Audits
- [Planned security audit (Phase 2.0)]
- Code review before public release
- Bug bounty program planned

---

## 📊 Competitive Analysis

| Feature | Signal | Telegram | Briar | Byline |
|---------|--------|----------|-------|--------|
| E2EE | ✅ | ⚠️ | ✅ | ✅ |
| Ops Security | ❌ | ❌ | ⚠️ | ✅ |
| Zero Metadata | ❌ | ❌ | ✅ | ✅ |
| DPI Bypass | ❌ | ❌ | ✅ | ✅ |
| Open Source | ✅ | ❌ | ✅ | ✅ |
| Easy to Use | ✅ | ✅ | ❌ | ⚠️ |

**Our unique position:** Security professional's messenger for journalists.

---

## 💬 Join Us

### Closed Beta Signup
If you're a journalist or activist interested in helping shape Byline, [sign up for the closed beta](https://byline-messenger.github.io/#beta).

### Contributors
We'll open contributions after MVP launch. Stay tuned!

### Questions?
[Open an issue](https://github.com/byline-messenger/byline/issues) or email dmitriy_kh@outlook.com

---

## 📜 License

[To be determined - likely GPL or similar for privacy protection]

---

## 🙏 Acknowledgments

Inspired by the need for operational security-first design.  
Built by journalists for journalists.

---

**Last Updated:** 2026-05-24  
**Status:** MVP Development Starting  
**Website:** https://byline-messenger.github.io
