---
title: "Security Without Identification: Transaction Systems to Make Big Brother Obsolete"
authors:
  - David Chaum|david-chaum
year: 1985
language: en
type: paper
glossary:
  - cryptography
  - privacy
  - anonymous-communication
  - cypherpunk
sources:
  - path: main.md
    format: md
  - path: main.pdf
    format: pdf
references:
  - url: 'https://www.cs.ru.nl/~jhh/pub/secsem/chaum1985bigbrother.pdf'
    role: original
  - url: 'https://dl.acm.org/doi/10.1145/4372.4373'
    role: publisher
  - url: 'https://nakamotoinstitute.org/library/security-without-identification/'
    role: archive-mirror
license: ACM (see paper for redistribution terms)
---
Chaum's landmark *Communications of the ACM* paper (October 1985) argues that
large-scale automated transaction systems need not build a dossier society. Instead
of universal identifiers linking every purchase, message, and credential, individuals
could use separate digital pseudonyms with each organization — unlinkable even if all
institutions collude.

The paper sketches a personal "card computer" for [[cryptography|cryptographic]]
communication, [[privacy-protected|privacy]] payments via blind signatures, and
credential transfer without identification. It introduced unconditionally untraceable
messaging (the dining cryptographers problem), digital cash mechanics later realized
in DigiCash, and pseudonymous credential systems. [Satoshi Nakamoto](people:satoshi-nakamoto) cited Chaum's
earlier work; this article is the broadest statement of the vision that shaped
[[anonymous-communication|anonymous communication]] research and
[[cypherpunk|cypherpunk]] electronic commerce.
