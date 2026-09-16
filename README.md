# On-chain scam address datasets — OFAC sanctions + documented rug pulls

Machine-readable, re-verifiable datasets for **crypto compliance, wallet screening and scam
research**. Maintained by [ScytheRadar](https://scytheradar.com) — an on-chain risk scanner.

**Two datasets, no paywall, no signup. Both are plain files in this repository.**

| Dataset | File | Rows |
|---|---|---|
| US Treasury OFAC SDN — cryptocurrency addresses | [`data/ofac-sanctioned-addresses.json`](data/ofac-sanctioned-addresses.json) · [`.csv`](data/ofac-sanctioned-addresses.csv) | **492** |
| Documented dead tokens (rug pulls), with full contract addresses | [`data/dead-token-archive.json`](data/dead-token-archive.json) · [`.csv`](data/dead-token-archive.csv) | **19** |

---

## 1. OFAC sanctioned cryptocurrency addresses

Source: **US Treasury OFAC SDN list (sanctionslistservice.ofac.treas.gov)**
Official export: `https://sanctionslistservice.ofac.treas.gov/api/publicationpreview/exports/sdn.csv`
Snapshot date: **2026-09-13** · Exported: **2026-09-16** · Addresses: **492** across **12** chains.

This file is a re-export of official, public US government data — **not** our opinion.
Always re-verify against the source URL above before acting on it.

### Coverage by chain

| Chain | Addresses |
|---|---|
| Bitcoin | 253 |
| TRON | 117 |
| EVM (Ethereum / BSC / Base / Arbitrum) | 92 |
| Litecoin | 8 |
| Monero | 6 |
| Dash | 5 |
| Zcash | 3 |
| Solana | 2 |
| Dogecoin | 2 |
| Bitcoin Cash | 2 |
| Verge | 1 |
| Bitcoin Gold | 1 |

> Note the long tail: sanctioned crypto is not only Bitcoin and USDT. It also sits on
> Monero, Zcash, Dash, Litecoin, Dogecoin, Bitcoin Gold and more.

### Top sanctions programs

| Program code | Addresses |
|---|---|
| `CYBER2` | 93 |
| `ILLICIT-DRUGS-EO14059` | 65 |
| `CYBER4` | 37 |
| `SDGT` | 30 |
| `DPRK3` | 29 |
| `CYBER2] [ELECTION-EO13848` | 29 |
| `DPRK4` | 24 |
| `TCO` | 24 |

### Fields

| Field | Meaning |
|---|---|
| `address` | The sanctioned crypto address, verbatim |
| `chain` | Normalised chain key (`evm`, `btc`, `tron`, `sol`, …) |
| `chain_label` | Human-readable chain name |
| `asset` | Asset ticker as recorded by OFAC |
| `sanctions_program` | OFAC program code (e.g. `CYBER2`, `DPRK4`) |
| `entity_name` | The sanctioned entity the address belongs to |
| `sdn_entry` | OFAC SDN entry number — the key back to the official list |

---

## 2. Dead token archive

**19 EVM (BSC) tokens** that reached zero, or whose liquidity pool was drained to
nothing. Each row carries the **full contract address** so you can open it in a block explorer
and check every claim yourself.

| Token | Contract address | Status | Peak TVL | Full report |
|---|---|---|---|---|
| ARK / 方舟之境 | `0xcae117ca6bc8a341d2e7207f30e180f0e5618b9d` | 重启盘 | — | [report](https://scytheradar.com/death/ark-ark-realm.html) |
| BCASH / BＣＡＳＨ | `0x43f595a9a438f0f26bae8458ca29d4ceb5e0c143` | 已归零 | — | [report](https://scytheradar.com/death/bcash-b.html) |
| BeeToken / Bee Token | `0xb0a2416fd12711cbcfafb429031c0f7037fab970` | 已拔池 | — | [report](https://scytheradar.com/death/beetoken-bee-token.html) |
| BIT / Interbits | `0x1d249e02fb188447c73127fee4cc3e5adb7556a3` | 已拔池 | — | [report](https://scytheradar.com/death/bit-interbits.html) |
| BLK / Black Whale Token | `0xc0e6ad13bd58413ed308729b688d601243e1cf77` | 已拔池 | — | [report](https://scytheradar.com/death/blk-black-whale-token.html) |
| BSL / B-LAUNCH | `0xb60501346240fcde1615de56ea9fff1ac1da5673` | 已拔池 | — | [report](https://scytheradar.com/death/bsl-b-launch.html) |
| BZP / BitZipp Token | `0xb49988a9ecbf0455b3b43fff7e64960d8399ccb8` | 已归零 | — | [report](https://scytheradar.com/death/bzp-bitzipp-token.html) |
| EASYMONEY / Easy Money | `0x21ec484e79a360ac66c7ab284e99a9e83a9ccd8d` | 已归零 | — | [report](https://scytheradar.com/death/easymoney-easy-money.html) |
| GRT / GRT | `0xba7c07fe1f6e6e540b50b13373052f10976f5510` | 已归零 | — | [report](https://scytheradar.com/death/grt-grt.html) |
| HEXFLOKI / HEXFloki | `0x052905446647f54c4280bb1af9b0037fb633a012` | 已拔池 | — | [report](https://scytheradar.com/death/hexfloki-hexfloki.html) |
| LABUBU 假币 | `0xb0378817a0a97ea668a64a22dcbeea8389f7cb07` | 已归零 | — | [report](https://scytheradar.com/death/labubu-fake.html) |
| LAX / 拉菲 | `0x7f9bd73e51e66e0b2c7a87db0ca530a11eb7a7e9` | 已拔池 | $45.9M | [report](https://scytheradar.com/death/lax-lafite.html) |
| MODO / MoonDoge | `0xf9f89ef3c1b96a662db5fc9184dbf6ca1416dfe5` | 已拔池 | — | [report](https://scytheradar.com/death/modo-moondoge.html) |
| mSHIB / Meta Shiba | `0x3121a5c0d014714b0b82d6e017bc2112c7f5a8d1` | 已拔池 | — | [report](https://scytheradar.com/death/mshib-meta-shiba.html) |
| SAFEP / Safe Protocol | `0xa8c514d991f59bab02d32b68f04204cb89261c88` | 已拔池 | — | [report](https://scytheradar.com/death/safep-safe-protocol.html) |
| SHIBAKING / SHIBAKING | `0x62be34ec0147e5804f19239021f6117216fcdffc` | 已拔池 | — | [report](https://scytheradar.com/death/shibaking-shibaking.html) |
| SOL22 / SOLANA 2K22 | `0xf73eaca9f09ccd39c22d2659780ed6bd37b6249c` | 已归零 | — | [report](https://scytheradar.com/death/sol22-solana-2k22.html) |
| SUP / Super Token | `0x9739a6e18ef75e529ec41f82a4f281b42128b996` | 已拔池 | — | [report](https://scytheradar.com/death/sup-super-token.html) |
| TSW / TRUMPSWAP | `0xd9294bdb1a11d61de047de5b8034b20bc7eaab79` | 已拔池 | — | [report](https://scytheradar.com/death/tsw-trumpswap.html) |

### What is deliberately **not** in this dataset

1. **Attribution to individuals or groups.** Some of these cases look like the work of a common
   operator, but "looks like" is not evidence. We publish what the chain shows, not who we
   suspect.
2. **A single "total lost" number.** Peak TVL, residual liquidity and single-transaction
   cash-outs are different quantities. Collapsing them into one figure produces a headline that
   is arithmetically wrong. They stay separate.
3. **Residual liquidity after the drain** is often a few dollars. That is the point — it is
   recorded as-is rather than rounded into something that sounds more dramatic.

### Fields

| Field | Meaning |
|---|---|
| `contract_address` | Token contract address (verifiable) |
| `token_name` / `token_name_en` | Token name |
| `chain` | Chain |
| `status` / `status_en` | Outcome class (pool drained / relaunching / zeroed) |
| `outcome` | Short outcome description |
| `peak_tvl` | Highest pool value reached |
| `current_pool` | Pool value at time of documentation |
| `mechanism` / `mechanism_en` | The mechanism used (e.g. a `recycle()` drain function) |
| `early_warning` | What would have been detectable at deploy time |
| `victims_note` | Scale note, in its original denomination |
| `timeline_span` | First → last recorded stage |
| `detail_url` | Full forensic report on https://scytheradar.com |

---

## Licence & attribution

- **Data** (`data/*`): [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) — public
  domain. Use it commercially, no attribution required. Attribution is appreciated.
- The OFAC subset is US government public data and carries no copyright in the first place.

If you cite this work, a link to <https://scytheradar.com> helps us keep maintaining it.

## How to consume

```bash
git clone https://github.com/<owner>/scythe-radar-datasets.git
```

```python
import json
d = json.load(open("data/ofac-sanctioned-addresses.json"))
blocked = {r["address"].lower() for r in d["addresses"]}

def is_sanctioned(addr: str) -> bool:
    return addr.lower() in blocked
```

```sql
-- DuckDB / Postgres: read the CSV straight in
SELECT chain, count(*) FROM read_csv_auto('data/ofac-sanctioned-addresses.csv') GROUP BY 1 ORDER BY 2 DESC;
```

## Refresh cadence

The upstream OFAC SDN list is updated by the US Treasury, typically several times a month.
This snapshot is **2026-09-13**. If you need it current, pull the official export
(`https://sanctionslistservice.ofac.treas.gov/api/publicationpreview/exports/sdn.csv`) yourself — we would rather you use the authoritative source than trust
our copy.

## What ScytheRadar does with this

These datasets are the raw layer. On top of them we run a scanner that answers the questions
that actually cost people money:

- **Is this token a honeypot?** — buy/sell restriction, dynamic tax, blacklist functions
- **Is this address connected to dirty funds?** — multi-hop tracing toward known cash-out points
- **Did I just receive contaminated USDT?** — screening against the sanctions list above
- **Is this the real token, or a same-name impostor?** — symbol-collision detection

Start here: <https://scytheradar.com/detective.html> · Chinese guides: <https://scytheradar.com/zh/index.html>

---

*This repository is data and analysis only. It is not legal advice, not investment advice, and
we do not guarantee the recovery of any funds. "Not found in this dataset" never means "safe".*
