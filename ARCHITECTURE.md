<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-DATA — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

No domain component of SC-NC Data is implemented yet, and no code has moved here from SC-NeuroCore. The metadata keeps domain capabilities, claims and qualified record formats empty.

## Intended records

1. **Dataset manifest:** A dataset's source, licence, split, size and content digests.
2. **Encoder configuration:** How a signal is encoded into spikes: method, rates, windows and seed.
3. **Codec stream:** A compressed spike stream with its codec, parameters and integrity fields.

## Ownership

**This project owns** the planned SC-NC Data records and boundary rules.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| simulation and native lanes | SC-NC Engine |
| training and conversion | SC-NC Learn |
| device acquisition frames | SC-NC Hardware |
| the public package, documentation and releases of the monolith | SC-NeuroCore |

## Interpretation

- **Datasets.** A manifest names a source and a licence; it is not a statement about the data's quality.
- **Moves.** Code arrives only through SC-NeuroCore's split import gate, unit by unit; a planned move is not a moved capability.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records, rules and schema identifiers.
