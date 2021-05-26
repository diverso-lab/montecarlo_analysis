# Monte Carlo Simulations for Variability Analyses in Highly Configurable Systems
This repository contains all the resources and artifacts of the paper entitled *Monte Carlo Simulations for Variability Analyses in Highly Configurable Systems* submitted in the 23rd International Workshop on Configuration (ConfWS'21) by the authors José Miguel Horcas, A. Germán Márquez, José A. Galindo, and David Benavides.

## Analysis results
The following files contains the results of the Monte Carlo simulations based analysis of the jHipster feature model used in the paper:
- [Analysis of the variation points and variants](https://github.com/diverso-lab/montecarlo_analysis/blob/main/results/jhipster_variants_analysis.csv)
- [Analysis of the variation points and variant combinations](https://github.com/diverso-lab/montecarlo_analysis/blob/main/results/jhipster_variants_combinations_analysis.csv)
- [Approximation of the Monte Carlo simulations to the real probability](https://github.com/diverso-lab/montecarlo_analysis/blob/main/results/jhipster_montecarlo_approximation_prob.csv)

## Experiment replication

### Requirements
- Python 3.9+

### How to
1. Clone/Download this repository:

    `git clone https://github.com/diverso-lab/montecarlo_analysis.git` 

2. Create a virtual environment and activate it:

    `python -m venv env` 
    
    In Linux: `source env/bin/activate`
    In Windows: `env\Scripts\Activate` 

3. Install the module dependencies:

    `pip install -r requirements.txt` 

4. Launch the analysis:

    `python main_jhipster_analysis.py`

    This will create the three output files listed above with the results.

### Configure the analysis
The following parameters can be configured in `main_jhipster_analysis.py` to change the behaviour of the analysis: 
    
    - Percentage of Monte Carlo simulations: Use the `PERCENTAGE_SIMULATIONS = 0.01` constant (e.g., 0.01 for 1%).
    - Number of experiments (runs) to calculate medians, means, and standard deviations: `RUNS = 30`.
    - Probability precision for results: `DIGIT_PRECISION = 4` for floating numbers with 4 decimal.
    - Maximum number of Monte Carlo simulations for verifying the approximation to the real probabilities: `MAX_SIMULATIONS_APPROXIMATION = 5000`.
    
## References
- [Python framework for AAFMs](https://github.com/diverso-lab/core)