# Photometry demo data

Public example data for William Silver's Neuromodulators photometry preprocessing demo.
Publication of these example sessions is approved by the data owner.

Each `data/SUBJECT/YYYY-MM-DD-HHMMSS/` directory contains a matched bundle:

- A pyPhotometry `.ppd` recording, copied byte-for-byte.
- `trials.htsv`: the existing processed behavioural trials derived from pyControl.
- `dlight.times.npy`: the existing per-sample photometry timestamps aligned to the
  same pyControl session. These are copied intact, without recomputing synchronisation.

## Default examples

| Neuromodulator | Region | Subject | Behavioural session | Recording |
| --- | --- | --- | --- | --- |
| 5-HT | NAc | WS04 | 2024-05-31-155317 | `WS04_NAc-2024-05-31-155314.ppd` |
| 5-HT | mFC | WS28 | 2026-02-25-103019 | `WS28_mFC-2026-02-25-103016.ppd` |
| DA | NAc | WS16 | 2025-05-07-161658 | `WS16_NAc-2025-05-07-161655.ppd` |
| DA | mFC | WS16 | 2025-04-30-140336 | `WS16_mFC-2025-04-30-140329.ppd` |

The earlier `data/WS28/2026-02-17-140841/` NAc/5-HT example remains available unchanged.

Recording filenames retain their original acquisition timestamps, which can differ
by a few seconds from the behavioural session timestamps. Pairing is explicit in
`manifest.json`; timestamps or trials must never be mixed between sessions.
The manifest records exact byte counts and SHA-256 hashes. Consumers should pin
an immutable Git commit and verify all three files before processing the bundle.

Raw pyControl TSVs are not needed by the current demo: it consumes the matching
processed behavioural trials and aligned timestamps. Local raw data files were
read only during preparation and were not edited.

This repository contains data only: no application deployment, credentials, local
paths, training outputs or workflow. No broad reuse licence is asserted here;
contact the owner about reuse beyond this demonstration.
