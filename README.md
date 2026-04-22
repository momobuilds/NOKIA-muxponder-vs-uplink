# Muxponder vs Uplink

Small course project for **Communication and Network Design** comparing two multilayer transport architectures: **Uplink** vs **Muxponder/Xponder**.

The notebook simulates traffic on two network topologies and checks how much traffic the network can carry before the blocking rate reaches **1%**.

## What this project does

- compares **Uplink** and **Xponder/Muxponder**
- tests both **with** and **without grooming**
- runs three approaches: **baseline**, **heuristic**, and **ILP**
- evaluates results on **NSFNET** and an **Italian national network**

## Main takeaway

In our simulations, **Muxponder/Xponder performs better than Uplink**, especially without grooming, because it uses OTN switch resources more efficiently.  
Grooming also makes a big difference for both architectures.

## Files

- `code.ipynb` — main notebook with the model, simulations, and plots
- `Numerical Result.csv` — summary of the final numerical results
- `Muxponder vs Uplink - Copy.pptx` — presentation version of the project

## Quick results

- On **NSFNET**, Xponder clearly outperforms Uplink in both grooming and no-grooming cases.
- On the **Italian network**, the gap is smaller, but Xponder still performs slightly better overall.
- The main bottlenecks are **OTN switch capacity** for Uplink and often **ODU limits** for Xponder.

## Run

Open the notebook and run all cells:

```bash
jupyter notebook code.ipynb
```

## Notes

This was built as a short academic project, so the code is mainly organized for clarity and experimentation rather than as a full software package.
