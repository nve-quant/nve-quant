<div align="center">

# Nicholas van Eerde

### Quant Engineer · CTO

**Low-latency trading infrastructure in Rust** <br/>
Market data · mark-pricing oracles · on-chain execution across CEX and DEX venues

<br/>

![Rust](https://img.shields.io/badge/Rust-0D1117?style=for-the-badge&logo=rust&logoColor=FF7043)
![C++](https://img.shields.io/badge/C++-0D1117?style=for-the-badge&logo=cplusplus&logoColor=6DB3F2)
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
![C++](https://img.shields.io/badge/C++-0D1117?style=flat-square&logo=cplusplus&logoColor=6DB3F2)
![Python](https://img.shields.io/badge/Python-0D1117?style=flat-square&logo=python&logoColor=FFD43B)
![TypeScript](https://img.shields.io/badge/TypeScript-0D1117?style=flat-square&logo=typescript&logoColor=4FA3E3)

**Trading systems**

![FIX](https://img.shields.io/badge/FIX_Protocol-0D1117?style=flat-square&labelColor=0D1117&color=1F6FEB)
![Orderbooks](https://img.shields.io/badge/Orderbook_Reconstruction-0D1117?style=flat-square&labelColor=0D1117&color=1F6FEB)
![Avellaneda–Stoikov](https://img.shields.io/badge/Avellaneda–Stoikov-0D1117?style=flat-square&labelColor=0D1117&color=1F6FEB)
![Microstructure](https://img.shields.io/badge/VPIN_·_Kyle's_λ_·_Markouts-0D1117?style=flat-square&labelColor=0D1117&color=1F6FEB)

**Systems & latency**

![NATS](https://img.shields.io/badge/NATS-0D1117?style=flat-square&logo=natsdotio&logoColor=27AAE1)
![Linux](https://img.shields.io/badge/Kernel_Tuning-0D1117?style=flat-square&logo=linux&logoColor=FCC624)
![Shared Memory](https://img.shields.io/badge/Shared_Memory_IPC-0D1117?style=flat-square&labelColor=0D1117&color=1F6FEB)
![Lock-free](https://img.shields.io/badge/Lock--free_·_Wait--free-0D1117?style=flat-square&labelColor=0D1117&color=1F6FEB)

**Data**

![ClickHouse](https://img.shields.io/badge/ClickHouse-0D1117?style=flat-square&logo=clickhouse&logoColor=FFCC01)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0D1117?style=flat-square&logo=postgresql&logoColor=4FA3E3)
![Redis](https://img.shields.io/badge/Dragonfly_·_Redis-0D1117?style=flat-square&logo=redis&logoColor=FF4438)
![Prometheus](https://img.shields.io/badge/Prometheus-0D1117?style=flat-square&logo=prometheus&logoColor=E6522C)
![Grafana](https://img.shields.io/badge/Grafana-0D1117?style=flat-square&logo=grafana&logoColor=F46800)

**Chain**

![Solana](https://img.shields.io/badge/Solana-0D1117?style=flat-square&logo=solana&logoColor=14F195)
![Ethereum](https://img.shields.io/badge/EVM_L2s-0D1117?style=flat-square&logo=ethereum&logoColor=8C8CFF)
![Solidity](https://img.shields.io/badge/Solidity-0D1117?style=flat-square&logo=solidity&logoColor=A8B3CF)
![Uniswap](https://img.shields.io/badge/Uniswap_V3%2FV4-0D1117?style=flat-square&labelColor=0D1117&color=FF007A)
![Aerodrome](https://img.shields.io/badge/Aerodrome_·_Raydium_·_Orca-0D1117?style=flat-square&labelColor=0D1117&color=1F6FEB)
![Foundry](https://img.shields.io/badge/Foundry_·_Anvil-0D1117?style=flat-square&labelColor=0D1117&color=1F6FEB)

**Infrastructure**

![Bare Metal](https://img.shields.io/badge/Bare_Metal_·_Equinix_Colo-0D1117?style=flat-square&logo=equinixmetal&logoColor=ED1C24)
![Docker](https://img.shields.io/badge/Docker-0D1117?style=flat-square&logo=docker&logoColor=2496ED)
![Linux](https://img.shields.io/badge/Linux-0D1117?style=flat-square&logo=linux&logoColor=FCC624)

**Also** — React/TypeScript for trading dashboards (order books, execution quality,
microstructure, venue intelligence)

![React](https://img.shields.io/badge/React-0D1117?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-0D1117?style=flat-square&logo=typescript&logoColor=4FA3E3)

---

<div align="center">

<sub>Background in aerospace engineering · MSc Innovation & Technology Management, University of Bath</sub>

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&labelColor=0A66C2&color=0A66C2)](https://www.linkedin.com/in/nicholas-van-eerde)
[![Email](https://img.shields.io/badge/Email-0D1117?style=for-the-badge&logo=maildotru&logoColor=E5484D)](mailto:nicovaneerde@hotmail.com)

</div>
