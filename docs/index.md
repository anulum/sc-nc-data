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

SC-NC Data is being built as the data layer split out of SC-NeuroCore: dataset manifests, the encoders that turn signals into spikes, the codecs that compress spike streams without loss, and the event datasets and sensor sources they draw on. It imports SC-NC Core, SC-NC Catalogue and SC-NC Engine. Its current executable surface is repository validation tooling. It has no installed dataset loader, input encoder, spike codec or qualified record schema.

Read [Architecture](ARCHITECTURE.md), [validation tooling](validation-tooling.md), [data boundaries](THREAT_MODEL.md) and the [repository boundary decision](adr/0001-repository-boundary.md).
