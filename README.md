Code and data for  
**“Surrogate modeling for interpreting black-box LLMs in medical predictions”**

This repository provides the official implementation of the surrogate modeling framework proposed in the manuscript, along with proof-of-concept experiments demonstrating how the framework can be applied to explain knowledge encoded in large language models (LLMs).

---

## Overview

Large language models encode extensive domain knowledge in a black-box manner.  
This repository implements a surrogate modeling framework that systematically elicits LLM input–output behavior using simulated data and translates it into interpretable statistical models.

The repository includes:
- Code for querying LLMs
- Paired simulated inputs and LLM-generated predictions
- Statistical modeling and analysis used in the manuscript
- Proof-of-concept experiments across multiple medical prediction tasks and LLMs

---

## Experiments

The following proof-of-concept experiments are included:

- Experiment 1: Cardiovascular disease risk prediction  
- Experiment 2: Estimation of glomerular filtration rate (GFR)  
- Experiment 3: Stroke risk prediction  
- Experiment 4: Pulmonary function estimation (FEV1, FVC, PEFR)

Each experiment is implemented separately for:
- GPT-4  
- Claude  
- Gemini  

The corresponding CSV files contain pairs of simulated inputs and LLM-generated predictions, which are used to construct surrogate statistical models.

---

## Workflow

1. LLM querying  
   Each simulated sample is converted into a structured prompt and queried to the target LLM.

2. Surrogate modeling  
   Statistical models (e.g., linear or log-linear regression) are fitted to the simulated data–LLM output pairs to approximate LLM-encoded knowledge.

3. Analysis and interpretation  
   Regression coefficients and model outputs are analyzed to reveal encoded associations, inaccuracies, and potential biases.

---

## Installation

This codebase requires **Python 3.10.6**.  
Clone the repository and install dependencies:

```bash
pip install -r requirements.txt
```


---

## Notes

- This repository is framework-oriented and is not intended for exhaustive benchmarking across all LLMs or modeling strategies.
- The included experiments serve as proof-of-concept demonstrations of how surrogate modeling can be applied to explain LLM-encoded knowledge.
- The framework can be readily extended to other models, topics, datasets, or statistical approaches.

---

## Citation

To be updated
