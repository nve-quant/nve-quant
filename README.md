<div align="center">

# Nicholas van Eerde

### Quant Engineer · CTO

**Low-latency trading infrastructure in Rust** <br/>
Market data · mark-pricing oracles · on-chain execution across CEX and DEX venues

<br/>

![Rust](https://img.shields.io/badge/Rust-0D1117?style=for-the-badge&logo=rust&logoColor=FF7043)
![C++](https://img.shields.io/badge/C%2B%2B-0D1117?style=for-the-badge&logo=cplusplus&logoColor=6DB3F2)
![Python](https://img.shields.io/badge/Python-0D1117?style=for-the-badge&logo=python&logoColor=FFD43B)
![Solana](https://img.shields.io/badge/Solana-0D1117?style=for-the-badge&logo=solana&logoColor=14F195)
![Ethereum](https://img.shields.io/badge/EVM-0D1117?style=for-the-badge&logo=ethereum&logoColor=8C8CFF)

<sub>Most of my work lives in private repositories. This profile is a pointer, not a portfolio.</sub>

</div>

---

## ⚡ What I work on

**📡 Low-latency market data**
Solo-built a ~250k-LOC market-data and pricing-oracle platform in Rust: 45 crypto
venue-feeds across 7 chains normalized into one event model, feeding an
Avellaneda–Stoikov mark-pricing engine with triple-transport egress (shared-memory
ring / UDP / NATS Core). Benchmarked **~20µs p50** producer wire-to-publish;
**~7µs p50** delivery to co-located shared-memory consumers.

**🦄 On-chain market making**
Production Rust LP market-making engine for concentrated-liquidity DEXs (Uniswap
V3/V4, Aerodrome), live on Base, Arbitrum and Optimism through four custody backends
including Fireblocks MPC and Zodiac Roles v2. Integer-exact concentrated-liquidity
math implemented from scratch, atomic single-tx repositioning, oracle-gated
adverse-selection control, and gas-EV bounded execution.

**◎ Solana execution**
Near-zero-slot DEX execution via ShredStream/gRPC decoding and Jito/SWQoS transaction
routing across 10+ Solana DEXs and launchpads, with MEV market-making and cross-pool
arbitrage strategies.

**🛡 Risk & execution quality**
Sub-5ms risk loop with automated circuit breakers across 15+ perpetual futures venues;
post-fill markout attribution, effective and realized spread, VPIN, Kyle's λ and
price-impact decomposition materialized in ClickHouse.

---

## 🧰 Stack

**Core**

![Rust](https://img.shields.io/badge/Rust-0D1117?style=flat-square&logo=rust&logoColor=FF7043)
![C++](https://img.shields.io/badge/C%2B%2B-0D1117?style=flat-square&logo=cplusplus&logoColor=6DB3F2)
![Python](https://img.shields.io/badge/Python-0D1117?style=flat-square&logo=python&logoColor=FFD43B)
![TypeScript](https://img.shields.io/badge/TypeScript-0D1117?style=flat-square&logo=typescript&logoColor=4FA3E3)

**Trading systems**

![FIX Protocol](https://img.shields.io/badge/FIX_Protocol-0D1117?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxZW0iIGhlaWdodD0iMWVtIiB2aWV3Qm94PSIwIDAgMjQgMjQiPjxnIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzU4QTZGRiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiPjxwYXRoIGQ9Ik0xNyAxOWExIDEgMCAwIDEtMS0xdi0yYTIgMiAwIDAgMSAyLTJoMmEyIDIgMCAwIDEgMiAydjJhMSAxIDAgMCAxLTEgMXptMCAydi0yIi8%2BPHBhdGggZD0iTTE5IDE0VjYuNWExIDEgMCAwIDAtNyAwdjExYTEgMSAwIDAgMS03IDBWMTBtMTYgMTF2LTJNMyA1VjMiLz48cGF0aCBkPSJNNCAxMGEyIDIgMCAwIDEtMi0yVjZhMSAxIDAgMCAxIDEtMWg0YTEgMSAwIDAgMSAxIDF2MmEyIDIgMCAwIDEtMiAyem0zLTVWMyIvPjwvZz48L3N2Zz4%3D)
![Orderbook Reconstruction](https://img.shields.io/badge/Orderbook_Reconstruction-0D1117?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxZW0iIGhlaWdodD0iMWVtIiB2aWV3Qm94PSIwIDAgMjQgMjQiPjxnIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzU4QTZGRiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiPjxwYXRoIGQ9Ik0xMi44MyAyLjE4YTIgMiAwIDAgMC0xLjY2IDBMMi42IDYuMDhhMSAxIDAgMCAwIDAgMS44M2w4LjU4IDMuOTFhMiAyIDAgMCAwIDEuNjYgMGw4LjU4LTMuOWExIDEgMCAwIDAgMC0xLjgzWiIvPjxwYXRoIGQ9Im02LjA4IDkuNWwtMy41IDEuNmExIDEgMCAwIDAgMCAxLjgxbDguNiAzLjkxYTIgMiAwIDAgMCAxLjY1IDBsOC41OC0zLjlhMSAxIDAgMCAwIDAtMS44M2wtMy41LTEuNTkiLz48cGF0aCBkPSJtNi4wOCAxNC41bC0zLjUgMS42YTEgMSAwIDAgMCAwIDEuODFsOC42IDMuOTFhMiAyIDAgMCAwIDEuNjUgMGw4LjU4LTMuOWExIDEgMCAwIDAgMC0xLjgzbC0zLjUtMS41OSIvPjwvZz48L3N2Zz4%3D)
![Avellaneda–Stoikov](https://img.shields.io/badge/Avellaneda%E2%80%93Stoikov-0D1117?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxZW0iIGhlaWdodD0iMWVtIiB2aWV3Qm94PSIwIDAgMjQgMjQiPjxwYXRoIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzU4QTZGRiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiIGQ9Ik0xOCA3VjVhMSAxIDAgMCAwLTEtMUg2LjVhLjUuNSAwIDAgMC0uNC44bDQuNSA2YTIgMiAwIDAgMSAwIDIuNGwtNC41IDZhLjUuNSAwIDAgMCAuNC44SDE3YTEgMSAwIDAgMCAxLTF2LTIiLz48L3N2Zz4%3D)
![VPIN · Kyle's λ · Markouts](https://img.shields.io/badge/VPIN_%C2%B7_Kyle's_%CE%BB_%C2%B7_Markouts-0D1117?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxZW0iIGhlaWdodD0iMWVtIiB2aWV3Qm94PSIwIDAgMjQgMjQiPjxwYXRoIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzU4QTZGRiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiIGQ9Ik0yMiAxMmgtMi40OGEyIDIgMCAwIDAtMS45MyAxLjQ2bC0yLjM1IDguMzZhLjI1LjI1IDAgMCAxLS40OCAwTDkuMjQgMi4xOGEuMjUuMjUgMCAwIDAtLjQ4IDBsLTIuMzUgOC4zNkEyIDIgMCAwIDEgNC40OSAxMkgyIi8%2BPC9zdmc%2B)

**Systems & latency**

![NATS](https://img.shields.io/badge/NATS-0D1117?style=flat-square&logo=natsdotio&logoColor=27AAE1)
![Kernel Tuning](https://img.shields.io/badge/Kernel_Tuning-0D1117?style=flat-square&logo=linux&logoColor=FCC624)
![Shared Memory IPC](https://img.shields.io/badge/Shared_Memory_IPC-0D1117?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxZW0iIGhlaWdodD0iMWVtIiB2aWV3Qm94PSIwIDAgMjQgMjQiPjxnIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzU4QTZGRiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiPjxwYXRoIGQ9Ik0xMiAxMnYtMm0wIDh2LTJtNC00di0ybTAgOHYtMk0yIDExaDEuNU0yMCAxOHYtMm0uNS01SDIyTTQgMTh2LTJtNC00di0ybTAgOHYtMiIvPjxyZWN0IHdpZHRoPSIyMCIgaGVpZ2h0PSIxMCIgeD0iMiIgeT0iNiIgcng9IjIiLz48L2c%2BPC9zdmc%2B)
![Lock-free · Wait-free](https://img.shields.io/badge/Lock--free_%C2%B7_Wait--free-0D1117?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxZW0iIGhlaWdodD0iMWVtIiB2aWV3Qm94PSIwIDAgMjQgMjQiPjxnIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzU4QTZGRiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiPjxyZWN0IHdpZHRoPSIxOCIgaGVpZ2h0PSIxMSIgeD0iMyIgeT0iMTEiIHJ4PSIyIiByeT0iMiIvPjxwYXRoIGQ9Ik03IDExVjdhNSA1IDAgMCAxIDkuOS0xIi8%2BPC9nPjwvc3ZnPg%3D%3D)

**Data**

![ClickHouse](https://img.shields.io/badge/ClickHouse-0D1117?style=flat-square&logo=clickhouse&logoColor=FFCC01)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0D1117?style=flat-square&logo=postgresql&logoColor=4FA3E3)
![Dragonfly](assets/badges/dragonfly.svg)
![Redis](https://img.shields.io/badge/Redis-0D1117?style=flat-square&logo=redis&logoColor=FF4438)
![Prometheus](https://img.shields.io/badge/Prometheus-0D1117?style=flat-square&logo=prometheus&logoColor=E6522C)
![Grafana](https://img.shields.io/badge/Grafana-0D1117?style=flat-square&logo=grafana&logoColor=F46800)

**Chain**

![Solana](assets/badges/solana.svg)
![Ethereum](assets/badges/ethereum.svg)
![Arbitrum](assets/badges/arbitrum.svg)
![BNB Chain](assets/badges/bnb-chain.svg)
![Base](assets/badges/base.svg)
![Optimism](assets/badges/optimism.svg)
![Solidity](https://img.shields.io/badge/Solidity-0D1117?style=flat-square&logo=solidity&logoColor=A8B3CF)
![Foundry · Anvil](https://img.shields.io/badge/Foundry_%C2%B7_Anvil-0D1117?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxZW0iIGhlaWdodD0iMWVtIiB2aWV3Qm94PSIwIDAgMjQgMjQiPjxnIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzU4QTZGRiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiPjxwYXRoIGQ9Im0xNSAxMmwtOS4zNzMgOS4zNzNhMSAxIDAgMCAxLTMuMDAxLTNMMTIgOW02IDZsNC00Ii8%2BPHBhdGggZD0ibTIxLjUgMTEuNWwtMS45MTQtMS45MTRBMiAyIDAgMCAxIDE5IDguMTcydi0uMzQ0YTIgMiAwIDAgMC0uNTg2LTEuNDE0bC0xLjY1Ny0xLjY1N0E2IDYgMCAwIDAgMTIuNTE2IDNIOWwxLjI0MyAxLjI0M0E2IDYgMCAwIDEgMTIgOC40ODVWMTBsMiAyaDEuMTcyYTIgMiAwIDAgMSAxLjQxNC41ODZMMTguNSAxNC41Ii8%2BPC9nPjwvc3ZnPg%3D%3D)

**DEX**

![Uniswap V3/V4](assets/badges/uniswap-v3-v4.svg)
![Aerodrome](assets/badges/aerodrome.svg)
![Balancer](assets/badges/balancer.svg)
![PancakeSwap](assets/badges/pancakeswap.svg)
![Raydium](assets/badges/raydium.svg)
![Orca](assets/badges/orca.svg)

**Infrastructure**

![Bare Metal · Equinix Colo](https://img.shields.io/badge/Bare_Metal_%C2%B7_Equinix_Colo-0D1117?style=flat-square&logo=equinixmetal&logoColor=ED1C24)
![Docker](https://img.shields.io/badge/Docker-0D1117?style=flat-square&logo=docker&logoColor=2496ED)
![Linux](https://img.shields.io/badge/Linux-0D1117?style=flat-square&logo=linux&logoColor=FCC624)

**Dashboards** — order books, execution quality, microstructure, venue intelligence

![React](https://img.shields.io/badge/React-0D1117?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-0D1117?style=flat-square&logo=typescript&logoColor=4FA3E3)

---

<div align="center">

<sub>Background in aerospace engineering · MSc Innovation & Technology Management, University of Bath</sub>

<br/>

[![LinkedIn](assets/badges/linkedin.svg)](https://www.linkedin.com/in/nicholas-van-eerde)
[![Email](https://img.shields.io/badge/Email-0D1117?style=for-the-badge&logo=maildotru&logoColor=E5484D)](mailto:nicovaneerde@hotmail.com)

</div>
