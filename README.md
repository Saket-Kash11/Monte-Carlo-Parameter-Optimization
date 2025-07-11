=======
# Monte-Carlo-Parameter-Optimization
Monte Carlo simulation framework to optimize signal  processing parameters through automated baseline correction, data normalization, and RMSE-based model

This project, developed as part of a computational modeling course, optimizes the fit between experimental and simulated signals in calcium dynamics modeling. Using the Li-Rinzel model, we applied baseline correction, normalization, Monte Carlo simulations, and Principal Component Analysis (PCA) to identify parameters (v1, v2, v3) that minimize oscillation frequency differences and RMSE.

My Contributions

- Implemented Monte Carlo simulations to evaluate 27,000 parameter combinations.
- Developed PCA to analyze data covariance and reduce dimensionality.
- Created visualizations for comparing experimental and simulated signals.

Features

- Data Preprocessing: Reads Group6_Data.xlsx, applies baseline correction (second-degree polynomial), and normalizes data using Min-Max scaling.
- Li-Rinzel Model: Simulates calcium concentration dynamics using Euler's method.
- Monte Carlo Simulation: Tests 27,000 combinations of v1 ∈ [0, 10], v2 ∈ [0, 1], v3 ∈ [0, 2] to find optimal parameters.
- Analysis: Computes RMSE and oscillation frequencies; applies PCA for dimensionality reduction.
- Visualization: Plots original, baseline-corrected, normalized, and simulated signals, including top five best-fitting simulations.

Requirements
- Python 3.8+
- Libraries: pandas, numpy, matplotlib

Running the Project
- Clone the repository:git clone https://github.com/your-username/signal-processing-simulation.git
- Install dependencies:pip install -r requirements.txt
- Run the main analysis: Hyperparameter_optimisation.ipynb

Methodology
- Baseline Correction: Fits a second-degree polynomial to remove signal drift.
- Normalization: Applies Min-Max scaling to standardize signal intensity.
- Simulation: Uses Euler's method to solve the Li-Rinzel model for calcium dynamics.
- Monte Carlo: Samples v1, v2, v3 (30 values each) to minimize RMSE and frequency differences.
- Evaluation: Computes RMSE and oscillation frequencies via autocorrelation.
- PCA: Reduces dimensionality to analyze data covariance.

Results
- Signal Behavior: Experimental signals show decaying oscillations; simulated signals (Li-Rinzel) exhibit stable periodic patterns.
- Best Parameters: Example optimal set: v1=6.07, v2=0.09, v3=0.93.
- Visualization: Plots compare experimental and simulated data; PCA scatter plots highlight data structure.

Dataset
- The dataset (`Group_6_simulated_data_1.xlsx`) is included in the `data/` folder.

References

Li, Y. X., & Rinzel, J. (1994). Equations for InsP3 receptor-mediated [Ca2+]i oscillations. Journal of Theoretical Biology.

License
MIT License. See LICENSE for details.

>>>>>>> e99414711ec491c8402109cb8cc3de697e2db2f0
