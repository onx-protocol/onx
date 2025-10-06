## 2. Motivation

A stable unit of account is a prerequisite for mainstream economic activity such as pricing, invoicing, payroll, lending, and long-duration settlement. While Nano’s block-lattice architecture offers instant, feeless, and energy-efficient transfers, the absence of native, stable-value assets constrains the breadth of use cases that can be realized atop the network. In particular, commerce denominated in fiat units, credit formation, hedging, and inter-organizational accounting all benefit from instruments whose value is insulated from underlying asset volatility.

Designing such instruments on Nano must contend with several constraints. 

- Nano *does not implement on-chain general-purpose scripting*, foreclosing typical smart-contract mechanisms for collateral management, liquidation logic, and automated governance. There is a very strong opinion within the developer group that Nano should not support 'meta' information in transactions, which could lead to a burden on the network, where Nanocurrency creates conditions forcing Principle Representatives to support sub-protocols created via use/abuse of the meta information field, with no reward.

- *Security and legitimacy must be tied to Nano’s Open Representative Voting (ORV)*, which derives trust from user-delegated voting weight. Third, transparency and auditability are essential: stable assets require continuous verification of collateral adequacy, issuance discipline, and redemption fidelity. 

- *Operational safety must be preserved* under degraded network conditions; any approach that allows unilateral movement of funds or issuance without robust quorum is unacceptable.

The ONX Protocol proposes a minimal, cryptography-first architecture that aligns with Nano’s strengths while addressing the above constraints:

- Domain-separated multi-currency operation via network numbers, each defining its own custody, oracle set, and governance parameters, enabling concurrent issuance without cross-asset interference.
- Custody implemented through threshold signatures, established by a Network Enable Mint (NEM) ceremony per network number, with zero-knowledge proofs attesting correct distributed key generation and membership.
- A privacy-preserving quorum mechanism that combines aggregated Schnorr signatures with zero-knowledge proofs of threshold participation, allowing authorization of minting, redemption, and governance while minimizing information disclosure about individual signers.
- A Participation Guard that makes recent, sufficient quorum a cryptographic prerequisite for any vault-affecting operation, automatically freezing funds upon participation shortfalls to preserve solvency and prevent unsafe state transitions.
- A sidecar ledger whose state transitions are anchored to the Nano ledger via compact commitments, furnishing reproducible audit trails for supply, collateral balances, and governance decisions.
- An oracle layer aggregating multiple signed feeds to produce medianized time-weighted prices per network number, guarded by deviation caps, staleness bounds, and quorum-certified configuration updates.

ONX can be seen as constructing a layered protocol atop Nano that replaces Turing-complete on-chain logic with verifiable off-chain processes and succinct on-chain anchors. Its contribution is the combination of threshold cryptography, zero-knowledge quorum attestations, and liveness-sensitive controls to achieve stability, privacy, and safety without invoking complex smart contracts. By grounding governance in ORV and isolating each currency in its own domain, ONX seeks to harmonize decentralization and operational rigor, offering a template for trust-minimized financial primitives on non-programmable ledgers.
