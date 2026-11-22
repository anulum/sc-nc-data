<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-DATA — repository foundation
-->

# SC-NC Data

SC-NC Data is being built as the data layer split out of SC-NeuroCore: dataset manifests, the encoders that turn signals into spikes, the codecs that compress spike streams without loss, and the event datasets and sensor sources they draw on. It imports SC-NC Core, SC-NC Catalogue and SC-NC Engine. This checkout contains repository validation tooling and documentation only. Full foundation qualification is in progress. There is no installed dataset loader, input encoder, spike codec or qualified record schema.

SC-NC Data is part of the **SC Neuromorphic Computing Systems** group (SC-NEUROMORPHIC-COMPUTING-SYSTEMS). The [group and project map](https://github.com/anulum/sc-neurocore/blob/main/docs/ecosystem.md) shows the whole programme and where this repository sits in it.

**What does not exist yet:**
- any code moved from SC-NeuroCore;
- a registered runtime record schema;
- an installed dataset loader, input encoder or spike codec.

## Boundary

**What this project owns:**

| Record | Scope |
|---|---|
| Dataset manifest | A dataset's source, licence, split, size and content digests |
| Encoder configuration | How a signal is encoded into spikes: method, rates, windows and seed |
| Codec stream | A compressed spike stream with its codec, parameters and integrity fields |

**Schemas it takes over from SC-NeuroCore:** sc-neurocore.event-dataset (v1) and sc-neurocore.input-encoder (v1).

**Static imports:** only SC-NC Core, SC-NC Catalogue and SC-NC Engine.

**Records read without importing their code:** Spike Log, Spike Codec Bench, Spike Encoder Characteriser, SC-NC Hardware, SC-NC Learn and SC-NC Bridges read this repository's records.

**Records it reads without importing their code:** those of SC-NC Core and Spike Format Bridge.

**Code planned to move here from SC-NeuroCore,** package by package, when SC-NeuroCore's split import gate allows it: `datasets`, `encoding`, `spike_codec`, `spike_dsp`, `audio`, `augmentation`, `sensors`, `sources` and `fusion`.

**Explicit non-claims and operating boundaries:**
- It contains no trainer and no simulator; it supplies and encodes data.
- A dataset manifest records a licence; it does not grant one.

## Current tooling

Repository controls inspect:
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and repository inventory;
- preflight orchestration.

Metadata declares architecture-only maturity with empty implemented domain capability and claim inventories.

- Use the exact environment in [Contributing](CONTRIBUTING.md).
- Full CI and preflight belong in CI or in an explicitly admitted pre-push environment.
- See [Validation](VALIDATION.md) for the maintained validation scope.

## Intended evidence

Every future record will carry its source and environment digests, its numeric formats where it has them, and its explicit verification boundary. None of the planned record schemas is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a performed simulation, hardware measurement or benchmark result.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
