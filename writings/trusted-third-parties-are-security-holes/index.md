---
title: Trusted Third Parties Are Security Holes
authors:
  - Nick Szabo|nick-szabo
year: 2001
language: en
type: essay
glossary:
  - cryptography
  - smart-contract
  - cypherpunk
  - bitcoin
  - decentralization
sources:
  - path: main.md
    format: md
references:
  - url: 'https://szabo.nautilus.cat/trusted-third-parties/'
    role: original
  - url: 'https://nakamotoinstitute.org/library/trusted-third-parties/'
    role: archive-mirror
license: free to redistribute without alteration (per author)
---
Szabo's 2001 essay argues that every "trusted third party" (TTP) invoked in a security
protocol is itself a security hole — a vulnerability that must be plugged at great cost.
Certificate authorities, DNS registries, and similar institutions became the most expensive
and failure-prone parts of PKI and the web not despite cryptography but because protocol
designers assumed TTPs away instead of minimizing them.

The paper proposes designing protocols around the cheapest credible trust assumptions,
preferably eliminating TTPs entirely through mathematics — digital mixes, multiparty
computation, Byzantine-resilient replication, and remote attestation of server code.
Written as Szabo was developing [[smart-contract|smart contract]] ideas and reusable
proofs of work toward [[bitcoin|bit gold]], it became a foundational critique of
centralized trust in [[cryptography|cryptographic]] systems and a design methodology for
[[decentralization|decentralized]] security.
