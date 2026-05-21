# MINBAR Burst Analysis

Analysis of Type I X-ray bursts as standard candles, using data from the [Multi-INstrument Burst ARchive (MINBAR)](https://burst.sci.monash.edu/).

## Notebooks

### `bursts_analysis.ipynb`
Core analysis of Photospheric Radius Expansion (PRE) bursts in globular cluster and field LMXBs.

- Verifies PRE burst peak flux consistency within single sources
- Computes Eddington luminosities for globular cluster LMXBs using Harris (1998) cluster distances
- Infers distances for field LMXBs and compares against Gaia parallaxes and catalog values
- Applies anisotropy corrections (factor ξ) for inclination-dependent flux effects

### `Gaia-zp.ipynb`
Estimates the Gaia DR3 parallax zero point local to a target source (Cyg X-2).

- Queries Gaia DR3 for background quasars in a field around the target
- Applies the Ding et al. (2021) filtering scheme (ecliptic latitude, magnitude, colour)
- Computes a weighted-mean parallax zero point for use in correcting LMXB distance estimates

## Data

| File | Description |
|------|-------------|
| `data/raw/minbar/minbar_bursts_web.txt` | MINBAR burst catalogue |
| `data/raw/fortin_lmxb/LMXBwebcat_latest.csv` | Fortin et al. LMXB catalogue |

## Dependencies

```
numpy pandas scipy matplotlib seaborn astropy astroquery ipyaladin
```

## References

- Kuulkers et al. (2003) — PRE bursts as standard candles
- Galloway et al. (2020) — MINBAR catalogue
- Harris (1998) — Globular cluster distances
- Ding et al. (2021) — Gaia parallax zero-point method
