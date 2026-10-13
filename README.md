# GEVP agentic-finance profile

**How the Gravit verification stack applies to transactions initiated by AI agents in finance**
(agentic payments such as x402, stablecoin settlement, delegated trading).

> **Renamed (13 Oct 2026).** This repository was called `ERC-8004-GT`. That name suggested an
> extension of [ERC-8004 "Trustless Agents"](https://eips.ethereum.org/EIPS/eip-8004), an Ethereum
> standard by other authors; this work is not an Ethereum ERC and not part of ERC-8004. The old
> name is retired, as are "VCP" and any "GT" suffix; the earlier text stays in the git history.

## What the profile says

An agent may *propose* a financial action; it executes only when:

1. the action passes the institution's hard rules (limits, counterparties, assets);
2. every claim the action relies on is a **Verified Fact** under
   [VEDS-00](https://datatracker.ietf.org/doc/draft-gravit-verifiable-epistemic-decision/00/) and
   [GEVP-08](https://datatracker.ietf.org/doc/draft-gravit-gevp/08/): signed evidence from at least
   two independent, registered operators, bound to exactly this action, fresh — never an aggregate
   of weak or non-independent evidence;
3. the decision is written as a content-addressed record with an explanation of what independence
   rests on, so that a third party can re-check it without the agent or its operator.

## Running code

| What | Where |
|---|---|
| Reference verifier (Python + Rust), decision explanations | [verifier](https://github.com/gravit-open-network-foundation/verifier) |
| x402 payments in stablecoins (AllUnity CHFAU/EURAU/SEKAU), simulated | [gravit-allunity-poc](https://github.com/gravit-open-network-foundation/gravit-allunity-poc) |
| Bank transfer proposals via MCP, simulated | [gravit-sygnum-poc](https://github.com/gravit-open-network-foundation/gravit-sygnum-poc) |
| Market-making decisions with corroborated market data | [gravit-easymm-poc](https://github.com/gravit-open-network-foundation/gravit-easymm-poc) |
| SAFR v1.1 runtime governance (MAS BuildFin.ai) | [gravit-safr-adapter](https://github.com/gravit-open-network-foundation/gravit-safr-adapter) |
| One-command reproduction of all published results | [gravit-eval-pack](https://github.com/gravit-open-network-foundation/gravit-eval-pack) |

## Relation to ERC-8004

ERC-8004 defines on-chain identity, reputation and validation registries for agents. A GEVP decision
record could serve as off-chain evidence referenced from such a validation entry; that mapping is
not specified yet. Nothing here claims compatibility or endorsement.

Licence: Apache-2.0 · Gravit Open Network Foundation, Zurich.
