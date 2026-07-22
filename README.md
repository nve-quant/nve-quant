# Nicholas van Eerde

Quant engineer and CTO at a crypto market-making firm. I build low-latency trading
infrastructure in Rust — market-data ingestion, mark-pricing oracles, and on-chain
execution across CEX and DEX venues.

Most of my work lives in private repositories. This profile is a pointer, not a portfolio.

---

### What I work on

**Low-latency market data** — Solo-built a ~250k-LOC market-data and pricing-oracle
platform in Rust: 45 crypto venue-feeds across 7 chains normalized into one event model,
feeding an Avellaneda–Stoikov mark-pricing engine with triple-transport egress
(shared-memory ring / UDP / NATS Core). Benchmarked ~20µs p50 producer wire-to-publish;
~7µs p50 delivery to co-located shared-memory consumers.

**On-chain market making** — Production Rust LP market-making engine for
concentrated-liquidity DEXs (Uniswap V3/V4, Aerodrome), live on Base, Arbitrum and
Optimism through four custody backends including Fireblocks MPC and Zodiac Roles v2.
Integer-exact concentrated-liquidity math implemented from scratch, atomic single-tx
repositioning, oracle-gated adverse-selection control, and gas-EV bounded execution.

**Solana execution** — Near-zero-slot DEX execution via ShredStream/gRPC decoding and
Jito/SWQoS transaction routing across 10+ Solana DEXs and launchpads, with MEV
market-making and cross-pool arbitrage strategies.

**Risk & execution quality** — Sub-5ms risk loop with automated circuit breakers across
15+ perpetual futures venues; post-fill markout attribution, effective and realized spread,
VPIN, Kyle's λ and price-impact decomposition materialized in ClickHouse.

---

### Stack

**Core** — Rust · C++ · Python · TypeScript

**Trading** — FIX connectivity · WebSocket feeds · orderbook reconstruction ·
Avellaneda–Stoikov · markouts · VPIN / Kyle's λ · cross-venue arbitrage simulation

**Systems** — Lock-free and wait-free structures · shared-memory IPC · NATS Core &
JetStream · kernel tuning (isolcpus, nohz_full, SCHED_FIFO, C-state pinning) · PGO builds ·
nanosecond-resolution latency attribution

**Data** — ClickHouse · PostgreSQL · Dragonfly/Redis · Prometheus · Grafana

**Chain** — Solana (Anchor, Jito, ShredStream, gRPC) · EVM L2s (Base, Arbitrum, Optimism) ·
Uniswap V3/V4 · Aerodrome · Raydium · Orca · Meteora · Foundry/Anvil fork testing

**Infra** — Bare-metal dedicated servers and direct colocation at Equinix TY3, SG1, NY4,
LD4, FR5 · Docker · Linux

**Also** — React/TypeScript for trading dashboards (order books, execution quality,
microstructure, venue intelligence)

---

Background in aerospace engineering. MSc Innovation & Technology Management,
University of Bath.

[LinkedIn](https://www.linkedin.com/in/nicholas-van-eerde) · [Email](mailto:nicovaneerde@hotmail.com)
