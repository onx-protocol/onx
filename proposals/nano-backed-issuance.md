# ONX Proposal : Nano Backed Issuance 

## ONX Proposal Over-Collateralised Digital Asset Issuance Framework, backed by Nanocurrency.

Proposed by: ONX Protocol (onx_protocol@proton.me)

Proposal Publish Date: 2025-10-06 (ISO International Date format)

Proposal Status: Draft

### Summary

The ONX Protocol is a decentralised, over-collateralised digital asset issuance framework built on Nano technology. 

The goal is to create any number of assets on the Nano network (e.g. oUSD "Open USD", oEUR "Open EUR" or any other desired asset) backed by Nanocurrency as collateral, in a permission-less, decentralised system. Each asset shares and benefits from the same underlying payment technology which powers the Nanocurrrency network itself, which is - Open Representative Voting. This enables each asset created through the ONX system to be transacted freely, without any fee mechanism to penalise a user or reward to centralise validators. It also creates an incentive for Principle Representatives on the Nanocurrency network to participate in a fee market for collateralising and minting any ONX asset, without creating conditions for emergent centralisation.

### Submission

ONX introduces:

- Global consensus and multi-currency isolation via network numbers (nn), each with its own governance, oracles, vault keys, and audit trail.
- Thresholds and safeguards that enable an over-collateralised network to exist and remain viable over time, in a hostile environment, along with clear processes for creation and destruction of asset backed networks (ABN).
- A Network Enable Genesis (NEG) ceremony to claim a unique fiat currency name against an nn, creating an immutable registry of asset backed coins.
- A Network Enable Mint (NEM) ceremony per nn that establishes a threshold group public key GPK_nn through distributed key generation and a zero-knowledge Proof of Shared Key (PSK_nn), anchoring custody and parameters to the Nano ledger.
- A zero-knowledge multisignature layer combining threshold Schnorr signatures with anonymous quorum proofs to authorize mints, redemptions, and governance without revealing signer identities or signing history.
- Open Representative Voting (ORV) alignment through a capped-weight consensus overlay, ensuring the Principal Representative (PR) set derives legitimacy from Nano’s trust model while preserving safety under a participation guard.
- A Participation Guard that freezes funds per nn if liveness drops below a quorum threshold; all vault outflows and collateralization events cryptographically require a recent Liveness QC (L-QC).
- A sidecar ledger with Nano-anchored proofs for transparent supply, collateral, and governance state, enabling real-time auditing by watchers.
- A multi-source oracle infrastructure that produces medianized TWAP prices, with per-nn safeguards against manipulation.

ONX avoids complex on-chain scripting, favouring cryptographically enforced custody and verifiability, while providing low-latency issuance and redemption when participation is healthy. When participation degrades, ONX prioritises solvency and safety by freezing vault movements until quorum is restored.
