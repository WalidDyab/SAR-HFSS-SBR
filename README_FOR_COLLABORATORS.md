# HFSS SBR+ canonical-target data package

Open `index.html` for the collaboration report, downloads, HFSS snapshots, verified grid summary, and processing guidance.

## Recommended starting point

Start with `derived/four_cases_dep30_sar_ready_master_table.csv`. It contains all four targets at `IWaveTheta = 120 deg`, interpreted here as a 30 deg depression slice. For an initial coherent demonstration, form `S(aspect, frequency) = s_phi_real + j*s_phi_imag`. Retain the Theta component for vector or polarization-aware processing.

The report convention is:

- `aspect_deg = (IWavePhi - 180) mod 360`
- `depression_deg = IWaveTheta - 90`

## Raw HFSS data

The four CSVs under `data/` contain the complete complex monostatic RCS sweeps. Each has 265,327 rows on the same 71 Phi x 37 Theta x 101 frequency grid (9-11 GHz, 0.02 GHz step).

## Sharing

Zip the entire folder. Keep `index.html`, `data/`, `derived/`, `assets/`, and `images/` together so relative links remain valid. The CSV data is phase-history-like input for downstream SAR/inverse-SAR processing, not a final SAR image.
