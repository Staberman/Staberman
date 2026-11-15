<div align="center">
  <img src="assets/banner.svg" alt="Lautaro Antunez, full-stack developer" width="100%">
</div>

<div align="center">

  <a href="https://staberman.com.ar"><img src="https://img.shields.io/badge/staberman.com.ar-F2B441?style=for-the-badge&logo=safari&logoColor=0B0F14" alt="Website"></a>
  <a href="mailto:lautaro@staberman.com.ar"><img src="https://img.shields.io/badge/lautaro@staberman.com.ar-161C24?style=for-the-badge&logo=maildotru&logoColor=F2B441" alt="Email"></a>

</div>

<br>

I build products end to end: architecture, code, the servers they run on, and the App Store listing.

Founder of **[Staberman](https://staberman.com.ar)**, a one-person studio. I ship software for clients and run a few products of my own.

---

## Open source

<sub>Pulled out of the products below. This is the part of my work you can read and run yourself.</sub>

**[SplitFlap](https://github.com/Staberman/splitflap)**: split-flap departure board components for SwiftUI, extracted from Pomotti. Tiles flip, rows spell themselves out, and a `Canvas` fast path keeps a large board at frame rate. MIT.

**[ntag213-ndef](https://github.com/Staberman/ntag213-ndef)**: NDEF bytes that iOS background tag reading actually accepts, plus an NTAG213 lock verifier that reads page `02h` instead of the one that misleads you. Zero dependencies. MIT.

**[app-attest-gate](https://github.com/Staberman/app-attest-gate)**: the parts of Apple App Attest people usually hand-roll wrong. Single-use challenges, atomic replay protection, per-assertion environment pinning and request-body binding, paired with StoreKit 2 entitlements and a server-metered free tier. MIT.

**[AppAttestClient](https://github.com/Staberman/app-attest-client)**: the Swift half. A Secure Enclave request signer whose concurrent registrations collapse into one, so a fresh install can't race itself into a 401. MIT.

**[claude-watch](https://github.com/Staberman/claude-watch)**: control Claude Code from an Apple Watch. My fork keeps the session controls within reach and holds the bridge connection when you lower your wrist.

### Contributions

**[Tomari](https://github.com/elrincondeldev/tomari)** (macOS, Swift): Claude Code sessions as little creatures on the edge of the screen. I made it usable with plain terminal sessions, without the desktop app ([merged](https://github.com/elrincondeldev/tomari/pulls?q=is%3Apr+author%3AStaberman+is%3Amerged)), and have more PRs open: a hotkey to jump to a waiting session, chimes, per-project colors.

**[AsoBeast](https://github.com/AsoBeast/asobeast)** (TypeScript): open-source ASO and keyword rank tracking for the App Store and Google Play. I fixed error states in the web app so a failed load says what failed ([merged](https://github.com/AsoBeast/asobeast/pulls?q=is%3Apr+author%3AStaberman+is%3Amerged)).

---

## What I build

**📱 iOS & macOS**
Three apps built solo and submitted to the App Store: a Pomodoro timer styled as a split-flap departure board (SwiftUI, iOS + iPadOS + macOS), a journaling app with an AI backend (SwiftUI), and an expense tracker with native StoreKit 2 subscriptions (React Native / Expo).

**🪪 Wallet passes**
A loyalty platform where the card lives in Apple Wallet, with Google Wallet in a pilot. Customers scan a QR and get the card without installing anything; the business adds stamps and sends messages to the lock screen. Next.js 16, an append-only points ledger, and a separate Node worker that is the only process allowed to touch the signing certificate. In production.

**🏗️ Multitenant SaaS**
A marketing analytics panel on Next.js 16 and self-hosted Supabase: row-level security across a five-role tenant hierarchy, batched ingestion that collapsed **9,000 API calls into 18**, cron-driven alerting, and **1,229 passing tests**.

**⚡ Commerce & automation**
Digital storefronts with paid acquisition on Meta, a WhatsApp sales bot with its own CRM, and an outbound prospecting pipeline that runs unattended on my own server and has worked through **700+ leads**.

**🧾 Client work**
An offline-first point-of-sale PWA for a restaurant that keeps taking orders when the network drops. An operations panel for a currency exchange business with live bank connections through Plaid. A dynamic QR and NFC redirect service on the client's own domain. An eyewear and watch storefront whose stock and prices sync from Tiendanube every hour.

---

## Stack

<p>
  <img src="https://img.shields.io/badge/TypeScript-161C24?style=for-the-badge&logo=typescript&logoColor=3178C6">
  <img src="https://img.shields.io/badge/Swift-161C24?style=for-the-badge&logo=swift&logoColor=F05138">
  <img src="https://img.shields.io/badge/Next.js-161C24?style=for-the-badge&logo=nextdotjs&logoColor=FFFFFF">
  <img src="https://img.shields.io/badge/React-161C24?style=for-the-badge&logo=react&logoColor=61DAFB">
  <img src="https://img.shields.io/badge/SwiftUI-161C24?style=for-the-badge&logo=swift&logoColor=F2B441">
</p>
<p>
  <img src="https://img.shields.io/badge/PostgreSQL-161C24?style=for-the-badge&logo=postgresql&logoColor=4169E1">
  <img src="https://img.shields.io/badge/Supabase-161C24?style=for-the-badge&logo=supabase&logoColor=3FCF8E">
  <img src="https://img.shields.io/badge/Node.js-161C24?style=for-the-badge&logo=nodedotjs&logoColor=5FA04E">
  <img src="https://img.shields.io/badge/Tailwind_CSS-161C24?style=for-the-badge&logo=tailwindcss&logoColor=06B6D4">
  <img src="https://img.shields.io/badge/Vitest-161C24?style=for-the-badge&logo=vitest&logoColor=6E9F18">
</p>
<p>
  <img src="https://img.shields.io/badge/Vercel-161C24?style=for-the-badge&logo=vercel&logoColor=FFFFFF">
  <img src="https://img.shields.io/badge/Docker-161C24?style=for-the-badge&logo=docker&logoColor=2496ED">
  <img src="https://img.shields.io/badge/Expo-161C24?style=for-the-badge&logo=expo&logoColor=FFFFFF">
  <img src="https://img.shields.io/badge/GitHub_Actions-161C24?style=for-the-badge&logo=githubactions&logoColor=2088FF">
</p>

I work in **hexagonal** and **screaming architecture**, with tests that describe behavior instead of implementation. Most of what I build is meant to be maintained for years.

---

## How I work

> **Specs before code.** Larger changes start as a written spec, a design and a task list, and get checked against them before they merge.

> **Review scales with risk.** Anything touching auth, payments or infrastructure gets an adversarial review before it ships. Copy changes don't.

> **I run my own infrastructure.** When something breaks in production, I'm usually the first to know.

---

<div align="center">

<sub>Most of my repositories are private: client work, live commercial products, or personal data.<br>Happy to walk through any of it on a call.</sub>

<br><br>

<a href="mailto:lautaro@staberman.com.ar"><b>lautaro@staberman.com.ar</b></a> · <a href="https://staberman.com.ar"><b>staberman.com.ar</b></a>

</div>
