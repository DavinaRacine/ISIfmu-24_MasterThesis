# Development Project Quality Assessment Using Event-Based Methods

This repository contains the research data and master calculation file for the Master Graduation Thesis **"Development Project Quality Assessment Using Event-Based Methods"** by Davina Racine Jackson.

The research proposes a hybrid methodology for assessing the quality of open-source software repositories by triangulating visual process discovery through process mining, holistic statistical scoring via the WASPAS method, and deterministic validation using Gemini 2.5 Pro.

## Analytical Scope
The analysis covers 15 diverse trending repositories and assesses them across four key metrics:
1.  **Review Rigor (RR)** - Proxy for the depth of code scrutiny.
2.  **Pull Request Merge Ratio (PRMR)** - Measures the efficiency of the contribution acceptance pipeline.
3.  **Issue Resolution Rate (IRR)** - Measures the project’s capacity to address bugs and user requests.
4.  **Contributor Diversity Index (CDI)** - Quantifiable proxy for the project's "Bus Factor" and structural resilience.

## Repository Structure
*   **/raw-data**: Contains the 15 individual raw Excel files extracted using the custom Python extraction algorithm found in the **/python-script** folder. These files include the structural lifecycles (Pull Requests, Issues, and Contributors) and the aggregated comment data.
*   **/calculations**: Contains the `Calculations_DJackson.xlsx`. This file contains the final results of the statistical analysis, including the following.
    *   **All Raw Excel Files.** Merged into one workbook for easier accessibility.
    *   **Raw Metrics Calculations.** Calculated per repository, serving as the foundation of the experiment.
    *   **Spearman Correlation Matrix.** Establishing the statistical trade-offs between metrics.
    *   **WASPAS Model.** The full calculation pipeline, including linear normalization, Weighted Sum Model, Weighted Product Model, and final $Q_i$ scores and rankings.
*   **/visualizations**: The complete collection of process mining models (Heuristics Nets and Petri Nets) generated using ProM 6.14.
*   **/python-script**: The custom Python extraction algorithm used to extract, clean, and normalize event data for the primary dataset (Appendix A of the thesis).

## Automated Cloud Pipeline Prototype 
To see the methodology in action, access the [Automated Cloud Pipeline Prototype here] (https://colab.research.google.com/drive/1bgnDV1Q-ieOvsur42mLhQqNd_N7yIpZL?usp=sharing) (Appendix B of the thesis). 

*This prototype utilizes optimized API extraction and cloud-native visualization (PM4Py) for real-time performance, while implementing a fault-tolerant mechanism to navigate regional LLM API restrictions within the European Union.*
