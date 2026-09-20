# J.A.R.V.I.S — MARK XLVIII

**Official downloads for JARVIS, the real-time voice AI assistant by Ananix Inc.**

This repository contains **compiled Windows binaries only**. Source code is proprietary and not distributed.

**🌐 Website:** **https://ananix-jarvis.vercel.app**

---

## Download

**Latest release:** https://github.com/aliakbarhyder/JARVIS-releases/releases/latest

Every release ships **four** artifacts — one per platform:

| Platform | File | How to install |
| --- | --- | --- |
| **Windows 10 / 11** | `JARVIS-Setup-<version>.exe` | Double-click, Next → Next → Install. Adds Start Menu shortcut, uninstallable from Add/Remove Programs. |
| **Windows** (portable) | `JARVIS.exe` | Bare app. No install — double-click to run. |
| **macOS 12+** | `JARVIS-<version>.dmg` | Open the DMG, drag `JARVIS.app` onto the `Applications` shortcut inside. |
| **Linux** (any distro) | `JARVIS-<version>.AppImage` | `chmod +x` the file and run it. Portable, no install, no root. |
| **Ubuntu / Debian** | `jarvis_<version>_amd64.deb` | `sudo dpkg -i jarvis_*.deb` — installs to `/opt/jarvis`, runnable as `jarvis`. |

Older builds are on the [releases page](https://github.com/aliakbarhyder/JARVIS-releases/releases). You should always be on the latest — JARVIS auto-updates itself on Windows once installed (Mac/Linux auto-update is on the roadmap).

**System requirements:**
- Windows 10/11 · macOS 12+ · Linux with glibc 2.35+ (Ubuntu 22.04+, Fedora 36+, Arch, etc.)
- 64-bit only
- ~500 MB free disk space
- Internet connection (for the Gemini Live API and updates)
- Microphone
- Google Gemini API key ([free from AI Studio](https://aistudio.google.com/apikey))

---

## Buy a licence

JARVIS requires a valid `.jarvis` licence (`some `.jarvis` files come encrypted as a `.jarcrypt` file, which requires a password to unencrypt. Ananix Inc. provides this password to you when sending an encrypted licence`) file to run. Licences are issued personally to you by Ananix Inc., machine-bound, and non-transferable.

### Personal · 1 computer

| Duration | Price |
| --- | --- |
| 1 week   | **15,000 PKR** |
| 1 month  | **35,000 PKR** |
| 1 year   | **75,000 PKR** |

### Lifetime · 3 computers

| Plan | Price |
| --- | --- |
| **Lifetime** | **135,000 PKR** |

### Enterprise · multi-computer

| Plan | Computers | Price |
| --- | --- | --- |
| **Enterprise** | 20 – 50 | **800,000 PKR** |
| **Custom**     | 50+     | Contact us to bargain a price |

**To buy a licence, email:** **ananix.inc@gmail.com**

Include:
- Your name and organisation
- How many computers you need to activate on
- Whether you want single-user or enterprise pricing

We'll reply with the licence file (a `.jarvis` attachment or a paste-friendly code) and payment instructions.

---

## First launch

1. Double-click `JARVIS.exe`
2. Paste your **licence code** (or drop your `.jarvis` file) — sent to you by email
3. Paste your **Gemini API key**
4. Say hello

That's it. JARVIS creates its config folder inside your user profile automatically — no admin rights, no manual setup.

---

## Auto-updates

Once installed, JARVIS silently checks this repository on every launch. When a newer release is published:

- JARVIS says *"Installing an update, sir. I'll be right back."*
- Downloads the new `JARVIS.exe`
- Swaps itself in place and restarts on the new version
- Your licence, API key, memory, and settings all carry over

To disable auto-updates, set `"auto_update": false` in `%LOCALAPPDATA%\JARVIS\config\api_keys.json`.

---

## Legal

Use of `JARVIS.exe` is governed by the [LICENSE](./LICENSE) in this repository. In summary: this is proprietary software. You may use it under a paid licence. You may not modify, redistribute, republish, reverse-engineer, or resell it. **Read the LICENSE file before using the software.**

## Security

See [SECURITY.md](./SECURITY.md) for our vulnerability-reporting policy and what to do if you suspect the `JARVIS.exe` on this repo has been tampered with.

---

## Support & contact

**Email:** ananix.inc@gmail.com

This is a downloads-only repository. Issues and pull requests are **not accepted here**.

For sales, licence renewal, activation problems, or bug reports: email us at the address above.

---

© Ananix Inc. All rights reserved.
