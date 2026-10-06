# Solar-cell simulations using SIMsalabim

Drift-diffusion exercise: tune a badly-designed solar cell to above
25 % PCE using [SIMsalabim](https://github.com/kostergroup/SIMsalabim) through its
online GUI at <http://simsalabim-online.com/>. Full instructions are in
[`instructions.pdf`](instructions.pdf). An interactive JV parameter explorer is also available from this repo at <https://nsdt-zhaw.github.io/jv-dd-simulations/explorer/>.

## Files in this repo

```
instructions.pdf                   # tutorial write-up (read this first)
main.tex                           # LaTeX source of instructions.pdf
README.md                          # this file
figures/                           # figures used by instructions.pdf
bad_start/                         # starting point — upload this folder's contents
    simulation_setup.txt           # global simulation setup
    ETL_parameters.txt             # electron transport layer
    ABS_parameters.txt             # absorber — the file you edit
    HTL_parameters.txt             # hole transport layer
    Data_nk/nk_absorber_Eg*.txt    # three absorber nk options (1.20 / 1.43 / 1.74 eV)
    Data_nk/nk_{Au,C60_1,ITO,PTAA,SiO2}.txt  # stack optical constants
    Data_spectrum/AM15G.txt        # solar spectrum (not needed on the online GUI)
    simss.exe                      # SIMsalabim v5.36 Windows binary (optional local run)
```

## Upload workflow (summary)

In the online GUI's right-hand menu, click **Upload a file**:

1. **Simulation setup** — `simulation_setup.txt` *plus* the three layer files
   (`ETL_parameters.txt`, `ABS_parameters.txt`, `HTL_parameters.txt`) in the
   same dialog, then **Submit** and **Save device parameters**.
2. **nk file** — `Data_nk/nk_absorber_Eg1.43eV.txt`, then **Save device parameters**.

Edit `ABS_parameters.txt` in the GUI's text editor (**Save device parameters**
after each change), then press **Run Simulation**. See `instructions.pdf` for
screenshots and the full walk-through.
