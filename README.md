# Plural Intertemporal Discounting Under Normative Uncertainty  

## Overview

This repository contains the full computational implementation accompanying the paper *Plural Intertemporal Discounting Under Normative Uncertainty*.

The central contribution is the Composite Intertemporal Valuation Instrument (CIVI), a weighted aggregation framework designed to operationalise normative uncertainty (the condition of acting under uncertainty about which moral theory is correct) directly within long-horizon valuation.

Rather than embedding ethical assumptions inside a single discount rate, CIVI aggregates twenty-two discount functions and permits explicit assignment of moral weights across competing ethical priors. 

The full draft is available here:  
[Plural Intertemporal Discounting Under Normative Uncertainty](https://docs.google.com/document/d/1bim28OeAk_5zrDljibx1Wbk4OLVdif_wDUfCUTfaOSU/edit?usp=sharing)

---

## Repository Structure

The codebase includes:

- All twenty-two discounting functions discussed in the paper  
- Baseline parameter definitions  
- CIVI aggregation framework  
- Deterministic comparative analysis  
- Policy application via tonne-year accounting  
- Uncertainty modelling using Monte Carlo simulation  
- Sensitivity analysis across parameter regimes  
- A catastrophic fat-tails scenario examining tail risk sensitivity  

---

## Implementation Notes

Most of the notebook can be executed sequentially without modification.

However, special attention is required in:

Section 3 — Baseline Parameters & CIVI Aggregation

In this section, the analyst must explicitly select:

- Moral weight configuration  
- Aggregation mode  

A dropdown interface is provided for this purpose.

Failure to make an active selection in this section will result in downstream cells inheriting null or default values, causing subsequent computations to misfire or return flat trajectories. (This is not a bug; it simply reflects the model’s requirement that ethical priors be explicitly specified.)

---

## Reproducibility

All figures and quantitative results in the paper are generated directly from this codebase.

To replicate:

1. Execute all discount function definitions.
2. Configure baseline parameters and moral weights in Section 3.
3. Run deterministic analysis.
4. Run policy application modules.
5. Execute Monte Carlo uncertainty modelling.
6. Run sensitivity and catastrophic tail-risk scenarios.

Dependencies are just standard scientific Python libraries:
- numpy
- scipy
- matplotlib
- pandas 

---


## Citation

If referencing this implementation, please cite:

Shah, M. H.  
Plural Intertemporal Discounting Under Normative Uncertainty.  
Working paper draft.

---

## Contact

For questions, feedback, or collaboration inquiries, please reach out via GitHub Issues. Critical and constructive feedback in particular is most  welcome. 
