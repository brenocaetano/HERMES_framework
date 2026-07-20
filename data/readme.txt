
# HERMES Framework - Datasets Repository

This directory contains the synthetic and real-world datasets used for the empirical validation of HERMES (Heterogeneous Ensemble Ranking for Model-free Early Selection in Cold-start Scenarios). 

The datasets are divided into three progressive experimental stages: topological stability (synthetic), latent class discovery (real-world benchmarks with ground truth), and a complex cold-start case study.

## 1. Synthetic Benchmarks
These datasets are used as controlled laboratory environments to isolate and stress-test the core algorithmic components of HERMES (multi-objective ranking mechanics and geometric label diffusion).

*   **Linear:** 
    *   **Description:** A geometric representation of a line segment in a 3D space.
    *   **Size:** 512 instances.
    *   **Purpose:** Validates the method's behavior and label diffusion in structures with low intrinsic dimensionality and a perfect continuous gradient.

*   **DTLZ-2:** 
    *   **Description:** A complex Pareto frontier generated from the DTLZ-2 multi-objective benchmark function solved using the NSGA-II algorithm (evolved over 10 generations).
    *   **Size:** 446 instances.
    *   **Purpose:** Evaluates multi-objective ranking mechanics, sample crowding, and Pareto-front stability under stochastic noise.

## 2. Real-World Benchmarks (UCI Machine Learning Repository)
These datasets contain hidden ground-truth labels used strictly for empirical validation ("glass-box" testing). They measure whether the topological stability discovered by HERMES translates into accurate latent class discovery.

*   **Diabetes (130-US Hospitals for Years 1999-2008):**
    *   **Description:** A clinical dataset utilizing numerical clinical indicators (inpatient visits, outpatient visits, emergency visits, and total diagnoses) as conflicting objectives.
    *   **Size:** Subsampled to 1,500 instances (due to the strict O(N^3) computational complexity of the Neighbor-Joining tree construction).
    *   **Target:** Patient readmission (Class 0: Not Readmitted; Class 1: Readmitted).

*   **Student Performance:**
    *   **Description:** An educational dataset mapping demographic and behavioral attributes. Uses five objectives with distinct optimization directions (failures, absences, study time, health status, and free time).
    *   **Size:** 395 instances.
    *   **Target:** Academic success (Class 0: G3 < 10; Class 1: G3 >= 10). Provides a class imbalance scenario.

## 3. Real-World Case Study
This dataset represents a strict Cold-Start environment without pre-existing ground-truth labels, requiring heterogeneous data fusion.

*   **Food Insecurity (São Paulo, Brazil):**
    *   **Description:** A multimodal administrative dataset created through a feature-level fusion of three distinct sources: IPVS (social vulnerability index), RAIS (density of fresh food commercial establishments), and CAISAN (open-air markets). 
    *   **Size:** 96 instances (representing the 96 districts of São Paulo).
    *   **Purpose:** Illustrates the potential of HERMES for exploratory public policy analysis and vulnerability mapping where heterogeneous data fusion is required and access to an oracle is limited.

---
**Note on Reproducibility:** 
Ensure that the respective distance metrics are applied correctly when running the HERMES pipeline on these datasets (Euclidean for Synthetic; Geodesic for UCI datasets; Normalized Levenshtein for the categorical Food Insecurity dataset).