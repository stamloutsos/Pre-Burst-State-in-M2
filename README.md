# Pre-Burst State in M2 Encodes a Gating Variable for Lick Initiation

**Dissociating preparation from execution in mouse secondary motor cortex**

Stamelos Loutsos · ORCID: 0009-0008-0479-748X  
Figshare: https://doi.org/10.6084/m9.figshare.32253159

---

### What this is

We reanalyzed open Neuropixels data (Steinmetz et al. 2019, DANDI:000139) and found that M2 doesn't just "prepare" movement — it bursts. That burst crosses a threshold ~190 ms before a lick. But the burst alone doesn't decide.

45.8% of bursts never lead to movement. What matters is the *state* of M2 50 ms before the burst. That pre-burst state predicts whether the mouse will actually lick (65% accuracy, p=8.6e-4).

This completes a two-stage model with our earlier Langevin work: M2 samples, bursts, then basal ganglia gates.

### Reproduce in 2 commands

```bash
pip install -r requirements.txt
dandi download DANDI:000139
python src/batch_steinmetz_analysis.py
```

### Results

| Test | Value |
|------|-------|
| Burst latency | -190 ms, p=7.9e-14 |
| Pre-burst prediction | t=3.4, p=8.6e-4 |
| Granger MOs→lick | 80 ms, p=2.8e-81 |
| MSD linearity | R²>0.98 |

Full tables in `/results/`

### Cite

> Loutsos, S. (2026). Pre-Burst State in M2. Figshare. doi:10.6084/m9.figshare.32253159

### License

Code MIT · Content CC BY 4.0 · © 2026 Stamelos Loutsos
