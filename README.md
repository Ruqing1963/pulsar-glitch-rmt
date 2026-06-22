# The Memory Spectrum of Neutron Star Glitches

From Poisson (Crab) to quasi-periodic repulsion (J0537-6910): a per-pulsar RMT analysis

Ruqing Chen, GUT Geoservice Inc., Montreal, Canada - June 2026

The 11th study in a unified RMT program. Pulsar glitches are the purest astrophysical
charge-and-release system: interior superfluid accumulates angular momentum relative to
the slowing crust, vortices unpin at a critical lag and transfer it in a sudden spin-up
(glitch), then re-accumulate. The extreme-density analogue of seismic elastic rebound.

The result is a MEMORY SPECTRUM. Different neutron stars span random to repulsive; the
RMT spacing ratio measures how clock-like each one charge-and-release cycle is.

## Key results (per-pulsar, NEVER pooled). Poisson=0.386 GOE=0.531 GUE=0.603

| Pulsar | n | r | CV | sig vs Poisson | sig vs GOE | state |
|---|---|---|---|---|---|---|
| B1338-62 | 35 | 0.575 | 0.57 | +3.4 | +0.8 | repulsion (GOE/GUE) |
| J0537-6910 | 45 | 0.562 | 0.55 | +3.6 | +0.7 | clean GOE (quasi-periodic) |
| B1758-23 | 15 | 0.545 | 0.57 | +1.8 | +0.1 | GOE |
| J2229+6114 | 9 | 0.536 | 0.48 | +1.1 | -0.1 | GOE |
| B1800-21 | 6 | 0.526 | 0.39 | +0.4 | -0.4 | GOE (small n) |
| J0631+1036 | 17 | 0.495 | 0.75 | +1.3 | -0.4 | transitional |
| B1046-58 | 12 | 0.482 | 0.82 | +0.9 | -0.5 | transitional |
| B1737-30 | 38 | 0.461 | 0.77 | +1.4 | -1.3 | transitional |
| Vela (B0833-45) | 26 | 0.399 | 0.57 | +0.2 | -2.1 | near Poisson |
| Crab (B0531+21) | 32 | 0.387 | 0.82 | -0.0 | -2.5 | pure Poisson (random) |

### Two anchors
- J0537-6910 (most frequent glitcher): r=0.562, +3.6 sigma above Poisson, = GOE. The
  cleanest charge-and-release clock; first detection of level repulsion in neutron star
  interior dynamics. (A single 2264-day obs gap 2011-2017 removed; n=45.)
- Crab: r=0.387, exactly Poisson, -2.5 sigma from GOE. Glitches are random.

## Why per-pulsar matters
Different stars glitch differently (Vela quasi-periodic, Crab irregular). Pooling
independent stars superposes independent point processes and collapses repulsion to
Poisson (superposition theorem). The spectrum is visible ONLY per-pulsar.

## Method notes
- Discrete, precisely timed events: no peak-picking artifact.
- Unfolding removes non-stationary glitch rate (Crab 1995-2006 increase).
- Observation gaps handled (J0537 2264-day gap removed). Undetected gaps bias r DOWNWARD,
  making repulsive detections conservative.

## Reproduce
    pip install -r requirements.txt
    python code/pulsar_glitch_rmt_pipeline.py data/glitch_epochs.json

## Data
data/glitch_epochs.json - per-pulsar glitch epochs (MJD), Jodrell Bank Observatory glitch
catalogue (Basu+2022, Espinoza+2011), http://www.jb.man.ac.uk/pulsar/glitches.html
(727 glitches, 222 pulsars). Cite those sources when using these data.

## The unified program (11 systems)
1 Stratigraphy GOE 20774581; 2 Seismotectonics 20768130; 3 Mantle plumes 20768420;
4 Metallogeny 20768849; 5 Evolution 20783763; 6 Hydrogeology 20780389;
7 Solar flares Poisson 20784967; 8 Orbital GUE 20785613; 9 Lunar craters 20787412;
10 Geomagnetic reversals weak-memory 20788648; 11 Pulsar glitches full-spectrum (this work).

## License
MIT (code). Glitch data: Jodrell Bank Observatory (Basu+2022, Espinoza+2011).
