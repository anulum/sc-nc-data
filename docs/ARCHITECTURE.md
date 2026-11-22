<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-DATA — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared local scope.

**What received metadata cannot do:** select another acceptance policy or grant domain authority.

Foundation qualification is in progress.

## Intended domain boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Dataset manifest | A dataset's source, licence, split, size and content digests | Licence, split and digest checks before any use |
| Encoder configuration | How a signal is encoded into spikes: method, rates, windows and seed | Encoding reproduced from the configuration and seed |
| Codec stream | A compressed spike stream with its codec, parameters and integrity fields | Lossless round trip, and every packet refused when an integrity field differs |

## Planned record schemas

- `sc_nc_data.dataset_manifest.v1`
- `sc_nc_data.encoder_config.v1`
- `sc_nc_data.codec_stream.v1`

These are planned identifiers. None of them is registered or qualified here.

It also takes over, unchanged, sc-neurocore.event-dataset (v1) and sc-neurocore.input-encoder (v1) from SC-NeuroCore when their code moves here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
