# MINBAR Burst Analysis

Analysis of Type I X-ray bursts as standard candles, using data from the [Multi-INstrument Burst ARchive (MINBAR)](https://burst.sci.monash.edu/).

## Notebooks

### `bursts_analysis.ipynb`
analysis of Photospheric Radius Expansion bursts in globular cluster and field LMXBs.

- Verify PRE burst peak flux consistency within single sources
- Compute Eddington luminosities for globular cluster LMXBs using cluster distances
- Infer distances for field LMXBs and compares against Gaia parallaxes and other catalog values
- Apply anisotropy corrections for inclination-dependent flux effects

### `Gaia-zp.ipynb`
Estimates the Gaia DR3 parallax zero point local to a target  

- Queries Gaia DR3 for background quasars in a field around the target
- Compute a parallax zero point for use in correcting LMXB distance estimates
- Apply zero-point corrections reported by Ding et al. and re-infers distances to 5 sources
- Explore simpler correction schemes 

## Data

| File | Description |
|------|-------------|
| `data/raw/minbar/minbar_bursts_web.txt` | MINBAR burst catalogue |
| `data/raw/fortin_lmxb/LMXBwebcat_latest.csv` | Fortin et al. LMXB catalogue |

for an interactive exploration of the MINBAR data, visit: https://minbar.streamlit.app/

## References

- Kuulkers et al. (2003) — PRE bursts as standard candles
- Galloway et al. (2020) — MINBAR catalogue
- Harris (1998) — Globular cluster distances
- Ding et al. (2021) — Gaia parallax zero-point method
