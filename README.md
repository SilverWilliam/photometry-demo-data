# Photometry demo data

Public example data for William Silver's photometry preprocessing dynamics
explorer. Publication of this WS28 bundle was approved by the data owner.

## WS28 — 2026-02-17-140841

`data/WS28/2026-02-17-140841/` contains a matched recording bundle:

- `WS28_NAc-2026-02-17-140838.ppd`: pyPhotometry recording (NAc).
- `trials.htsv`: processed behavioural trials derived from pyControl.
- `dlight.times.npy`: photometry timestamps aligned to that behavioural session.

The three-second difference in recording filenames is retained from the original
acquisition; pairing is explicit, not inferred by matching filenames. Raw
pyControl TSV is not included: the current explorer consumes the processed pair.
The manifest records exact byte counts and SHA-256 hashes. Consumers should pin
a Git commit, verify all three files, then process them together. Do not mix
timestamps or trials from a different session.

This repository contains data only: no application deployment, credentials,
local paths, training outputs or workflow. No broad reuse licence is asserted
here; contact the owner about reuse beyond this demonstration.
