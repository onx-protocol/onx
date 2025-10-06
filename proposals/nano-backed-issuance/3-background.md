## 3. Background

Nanocurrency is a payment-focused, account-based ledger that achieves low-latency, feeless transfers through its block-lattice design. Each account maintains its own chain of send/receive blocks, and transaction finality is governed by Open Representative Voting (ORV): users delegate voting weight to representatives, which collectively determine canonical history and resolve conflicts. This architecture prioritizes throughput and energy efficiency, with consensus distilled to representative voting over simple state transitions rather than execution of general-purpose programs.

Several properties of Nano are especially relevant to this proposal:

- Minimal on-ledger programmability
  - Nano does not expose a Turing-complete virtual machine or native smart contracts.
  - Complex economic logic (collateralization, liquidation, fee accrual, governance timelocks) cannot be encoded directly in ledger scripts.
  - Protocols must externalize logic to off-chain processes and attest their outcomes on-chain with compact commitments.
- Representative-derived trust
  - ORV confers legitimacy by aggregating the voting weight of representatives chosen by Nano holders.
  - System upgrades and operational decisions that wish to align with Nano’s social contract should reflect representative participation and weight.
- Account-centric state and anchoring
  - All balances and transfers are observable at the account level.
 
  
