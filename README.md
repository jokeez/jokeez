<!--
  GitHub profile README — https://github.com/jokeez
-->

<div align="center">

<pre aria-label="HackMe Network">
██╗  ██╗ █████╗  █████╗ ██╗  ██╗███╗   ███╗███████╗
██║  ██║██╔══██╗██╔════╝██║ ██╔╝████╗ ████║██╔════╝
███████║███████║██║     █████╔╝ ██╔████╔██║█████╗  
██╔══██║██╔══██║██║     ██╔═██╗ ██║╚██╔╝██║██╔══╝  
██║  ██║██║  ██║╚██████╗██║  ██╗██║ ╚═╝ ██║███████╗
╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝╚═╝     ╚═╝╚══════╝
</pre>

### Your computer mines HMC by finding real security bugs.

Proof-of-Hash blocks + coverage-guided fuzzing of open-source code — one network, one wallet.<br/>
Hub: **[hackme.tech](https://hackme.tech)** · Exchange: **[exchange.hackme.tech](https://exchange.hackme.tech)**

<br/>

[![Release](https://img.shields.io/github/v/release/jokeez/hackme?include_prereleases&label=release&style=for-the-badge&color=39ff14)](https://github.com/jokeez/hackme/releases/latest) [![Block](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhackme.tech%2Fapi%2Fstatus%3Flite%3D1&query=%24.tip_height&label=block&style=for-the-badge&color=00d1ff)](https://explorer.hackme.tech) [![Miners](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhackme.tech%2Fapi%2Fpool%2Fstats&query=%24.miners&label=miners%20online&style=for-the-badge&color=a855f7)](https://hackme.tech/downloads.html) [![Economics v2](https://img.shields.io/badge/Economics_v2-block_550%2C000-ff9f1c?style=for-the-badge)](https://github.com/jokeez/hackme/blob/main/docs/RFC_ECONOMICS_V2.md)

[![Exchange](https://img.shields.io/badge/Exchange-live-22c55e?style=flat-square)](https://exchange.hackme.tech) [![Proof of reserves](https://img.shields.io/badge/proof_of_reserves-public-22c55e?style=flat-square)](https://exchange.hackme.tech/info/reserves.html) [![Checkpoints](https://img.shields.io/badge/checkpoints-Bitcoin_OpenTimestamps-f7931a?style=flat-square&logo=bitcoin&logoColor=white)](https://github.com/jokeez/hackme-checkpoints) [![License](https://img.shields.io/badge/core-AGPL--3.0-blue?style=flat-square)](https://github.com/jokeez/hackme) [![Telegram](https://img.shields.io/badge/Telegram-@hackme__tech-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/hackme_tech) [![YouTube](https://img.shields.io/badge/YouTube-@HackmeTech-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/@HackmeTech)

<br/>

<a href="https://www.youtube.com/watch?v=KdRr6zK2QVE">
  <img src="https://img.youtube.com/vi/KdRr6zK2QVE/maxresdefault.jpg" alt="HackMe walkthrough" width="820" />
</a>

<sub>**[▶ Watch the walkthrough](https://www.youtube.com/watch?v=KdRr6zK2QVE)** — what the network is and how to start mining</sub>

</div>

---

## ⏳ Economics v2 — block 550,000 (≈ Nov 15, 2026)

The schedule is compiled into **0.1.0-rc19**: every updated node switches at the same height on its own.

| | Before | **From block 550,000** |
|---|---|---|
| Block reward | 0.01 HMC | **0.1 HMC** — halving every ~4 years from genesis, then a permanent **0.002** tail |
| SUP | — | **0.002 SUP / block**, hard cap **21,000** |
| Fuzzing orders | — | **10% upfront: 5% burned 🔥 + 5% platform** · Dig & Hunt open immediately |
| Addresses | `HMC-` + 16 hex | **+ `HMC-` + 64 hex** (full key hash) — old addresses keep working, no forced migration |
| Network id | — | transfers signed for **`hackme-mainnet-1`** |

> **Running a node or miner?** Update to **rc19** and start the app once before the fork — older versions stop following the chain at 550,000.
> Full spec: **[RFC Economics v2](https://github.com/jokeez/hackme/blob/main/docs/RFC_ECONOMICS_V2.md)**

---

## Ecosystem

| | What it is | Status | Code |
|---|---|---|---|
| ⛏ **Core node + pool** | PoH blocks (Blake3), share-PPS pool, **Dig** / **Hunt** fuzzing rails with on-chain escrow, Windows · Linux · deb · rpm · Arch · HackMe OS · Docker | **Live · rc19** | [jokeez/hackme](https://github.com/jokeez/hackme) |
| 💱 **HackMe Exchange** | Spot HMC · SUP · USDT (BEP-20), convert, deposits & withdrawals, 2FA, public proof of reserves | **Live · early access** | [jokeez/hackme-exchange](https://github.com/jokeez/hackme-exchange) |
| 🧾 **Checkpoints** | Signed daily chain checkpoints anchored in Bitcoin via OpenTimestamps — verify history yourself | **Live** | [jokeez/hackme-checkpoints](https://github.com/jokeez/hackme-checkpoints) |
| 🗂 **Useful PoW Index** | Curated registry of projects where hashrate does real work | **Live** | [jokeez/hackme-app](https://github.com/jokeez/hackme-app) |
| 🔐 **HMS** | Encrypted storage / seal lane | **Preview** | in [hackme](https://github.com/jokeez/hackme) · [roadmap](https://hackme.tech/roadmap.html) |

```mermaid
flowchart LR
  you((you))
  subgraph net [HackMe network]
    node["⛏ node · pool<br/>PoH + Dig / Hunt"]
    chain[("HMC · SUP chain")]
    cp["🧾 checkpoints<br/>Bitcoin OTS"]
  end
  subgraph market [Exchange]
    ex["💱 spot · convert"]
    por["proof of reserves"]
  end
  you -->|mine / order fuzzing| node
  node --> chain
  chain --> cp
  you -->|buy / sell HMC| ex
  chain <-->|deposits & withdrawals| ex
  ex --> por
```

---

## How the work is paid

| Rail | What it does | Customer pays | What a result means |
|---|---|---|---|
| **PoH** | Blake3 proof-of-hash blocks | — (block reward) | secures the chain |
| **Dig** | WASM detector / property depth across the pool | escrow · smoke 20/80 · deep 40/60 | crash-class gate; detector hits are coverage signals, not CVEs |
| **Hunt** | Coverage-guided ASAN fuzzing (libFuzzer fleet, AFL++ when present) | Lite 20 · Standard 60 · Heavy 150+ HMC | CLEAN = no qualifying native crash within budget — not an OSS-Fuzz replacement |

Teams order campaigns from their node or the **HackMe Orders** profile (no mining needed) — [fuzz guide](https://hackme.tech/fuzz-guide.html).

---

## Road to 1.0

```
 Nov 15            Nov 15–21            Nov 22–27                    Dec
 ──●─────────────────●────────────────────●─────────────────────────●──▶
 Economics v2      watch week            audits by zone + rc20        1.0 stable
 (block 550,000)   daily reconciliation  wallet login on exchange,    node + exchange
                                         long addresses by default
```

1.0 ships when it is ready, not on a date: no open critical findings, a clean week after the fork, and the exchange fully covered by on-chain reserves.

---

## Quick links

**Get started** · [Downloads](https://hackme.tech/downloads.html) · [Fuzz guide](https://hackme.tech/fuzz-guide.html) · [Developers](https://hackme.tech/developers.html)<br/>
**Exchange** · [Trade](https://exchange.hackme.tech) · [How to buy HMC](https://exchange.hackme.tech/info/buy.html) · [Proof of reserves](https://exchange.hackme.tech/info/reserves.html)<br/>
**Verify** · [Explorer](https://explorer.hackme.tech) · [Checkpoints](https://github.com/jokeez/hackme-checkpoints) · [Release checksums](https://github.com/jokeez/hackme/releases/latest)<br/>
**Read** · [News](https://hackme.tech/news.html) · [Research](https://hackme.tech/research.html) · [Roadmap](https://hackme.tech/roadmap.html) · [Economics v2 RFC](https://github.com/jokeez/hackme/blob/main/docs/RFC_ECONOMICS_V2.md)<br/>
**Talk** · [Telegram](https://t.me/hackme_tech) · [YouTube](https://www.youtube.com/@HackmeTech) · [Bitcointalk ANN](https://bitcointalk.org/index.php?topic=5583373.0)

<div align="center">

<br/>

<sub>Not financial advice · Official hub: <a href="https://hackme.tech">hackme.tech</a> only · verify checksums before you install</sub>

</div>
