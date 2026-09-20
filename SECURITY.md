# Security Policy

## Reporting a vulnerability

If you believe you have found a security issue in **JARVIS.exe** — a way to bypass licence verification, escalate privileges, execute arbitrary code, exfiltrate a user's API key or licence, or otherwise cause harm — please report it to **Ananix Inc.** at **ananix.inc@gmail.com** privately.

**Do NOT open a public GitHub issue.** This repository does not accept issues; even if it did, public disclosure of an unfixed vulnerability puts every JARVIS user at risk.

**Private disclosure channel:** email **ananix.inc@gmail.com** (or use the contact you used to purchase your licence).

### What to include in a report

- A concise description of the vulnerability and its impact
- Step-by-step reproduction (JARVIS version, OS version, actions taken)
- Any proof-of-concept material (screenshots, short video, logs) — kept **strictly** between you and the publisher
- Your name (or an alias) if you'd like to be credited when the fix ships

### What we commit to

- We'll acknowledge receipt within a reasonable timeframe
- We'll investigate every report in good faith
- We'll ship a fix in a new release as soon as one is available (auto-updates will pick it up)
- We'll credit you in the release notes if you want that, or keep you anonymous if you'd rather

### What is out of scope

- Reports based on running JARVIS with a licence you did not legitimately purchase — that is a breach of the [LICENSE](./LICENSE) and will not be treated as a security research contribution
- Reports based on running JARVIS on modified/pirated Windows or with debuggers, rootkits, or hooks that a normal user would not have
- Denial-of-service attacks against your own machine (you can already close JARVIS at any time)
- Vulnerabilities in third-party libraries that JARVIS bundles but which have no exploitable path in JARVIS itself
- Missing security headers on GitHub-hosted download pages (those are GitHub's responsibility)

---

## Verifying your download

The `JARVIS.exe` on this repository is built by our automated CI pipeline on a clean GitHub-hosted Windows runner directly from the private source repository. We do not build releases on personal machines.

If you want to verify a specific download:

1. On the [releases page](https://github.com/aliakbarhyder2/JARVIS-releases/releases), each release lists a **published date**. Confirm the version tag (e.g. `v1.0.2`) matches what you expect.
2. The download URL for the `.exe` is `https://github.com/aliakbarhyder2/JARVIS-releases/releases/download/vX.Y.Z/JARVIS.exe`. If you fetched the file from anywhere else, do NOT run it — it did not come from us.
3. If you notice a file size that seems dramatically different from previous releases, or a release published from an account other than **@aliakbarhyder2**, treat it as suspicious and report it before running.

## If you suspect a compromised release

If you suspect a `JARVIS.exe` on this repository has been tampered with (uploaded by an attacker who obtained our release credentials):

1. **Do NOT run the suspicious `.exe`**
2. **Do NOT auto-update** — set `"auto_update": false` in your `%LOCALAPPDATA%\JARVIS\config\api_keys.json` immediately
3. Contact Ananix Inc. privately at **ananix.inc@gmail.com** with the details
4. Wait for confirmation before running any newer release

---

## Supported versions

Only the **latest** released version of JARVIS is supported for security updates. If a vulnerability is found, the fix ships in the next release; older versions do not receive backported patches. This is why JARVIS auto-updates by default — please keep it enabled unless you have a specific reason not to.

---

## Cryptographic model

For completeness, JARVIS's licence system uses **Ed25519** digital signatures:

- **Private key** — held only by Ananix Inc. on our internal signing machine. Never leaves that machine. Never included in `JARVIS.exe`. Used to sign every `.jarvis` licence file we issue.
- **Public key** — baked into every `JARVIS.exe`. Used at startup to verify that a `.jarvis` file was genuinely issued by Ananix Inc. and has not been altered since. Public keys can only verify signatures, never create them — publishing them is safe by design.

Only Ananix Inc. can produce licences that verify against the public key in `JARVIS.exe`. A licence purporting to come from us but signed by any other key will be rejected as tampered.

---

© Ananix Inc. All rights reserved.
