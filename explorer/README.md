# jv-parameter-explorer

Interactive JV explorer for a perovskite solar cell — companion to a
hands-on SIMsalabim tutorial. Five sliders (bandgap, absorber thickness,
bulk SRH lifetime τ, interface recombination velocity S, bulk mobility µ)
browse **384 pre-computed Setfos 6.0 drift-diffusion simulations** of a
fixed device stack:

```
glass  →  ITO (50 nm)  →  ETL (5 nm)  →  absorber  →  HTL (5 nm)  →  Au
```

## Live site

**https://mtorrec.github.io/jv-parameter-explorer/**

## Grid

| Parameter | Values | Units |
|---|---|---|
| Bandgap  | 1.20, 1.43, 1.74            | eV        |
| Thickness | 100, 200, 350, 500          | nm        |
| SRH τ    | 1, 10, 100, 10000           | ns        |
| Interface S | 10⁴, 10³, 10², 10⁻¹      | cm s⁻¹    |
| Mobility µ | 1, 10                       | cm² V⁻¹ s⁻¹ |

3 × 4 × 4 × 4 × 2 = 384 JVs. Each JV is a full drift-diffusion + optical
solve (350–1200 nm coherent transfer-matrix, AM1.5G) in Setfos 6.0.

## Files

* `index.html` — Plotly UI (no build step, plain vanilla JS).
* `grid.json` — pre-computed JVs. Shared V axis + one J-array per parameter tuple.
