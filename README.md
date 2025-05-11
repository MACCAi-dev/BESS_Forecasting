# Frequency Response Forecasting for Battery Storage

This repository contains a Jupyter Notebook that implements a forecasting model for dynamic frequency response (DFR) service prices in battery storage systems. The notebook covers the entire workflow—from data preprocessing and feature engineering to model training, evaluation, and interpretability analysis. This project was part of the LCP Delta Hackaton, using data provided by their data integration platform, Enact.

## Overview

Battery storage operators and grid managers need accurate forecasts of DFR prices to optimize capacity and revenue. In this project, we focus on forecasting prices for dynamic services such as Dynamic Containment (DC), Dynamic Moderation (DM), and Dynamic Regulation (DR). The notebook includes:

- **Data Preprocessing:**  
  Loading and merging multiple datasets (e.g., day-ahead prices, generation data, frequency, ancillary volumes), handling missing values, timestamp conversion, and resampling into 4-hour intervals.

- **Feature Engineering:**  
  Generating time-based features (EFA block, day of week, month), market features (price averages, spreads, lagged prices), and system-specific indicators (renewable generation percentage, dynamic service triggers).

- **Model Training & Evaluation:**  
  Building a forecasting model using XGBoost within a pipeline that includes robust scaling and Bayesian hyperparameter optimization. The notebook demonstrates time-series cross-validation and evaluates model performance using metrics such as MAE, RMSE, and R².

- **Interpretability:**  
  Analyzing feature importance through both XGBoost's built-in methods and SHAP values, offering insights into the key drivers of DFR pricing.

## Getting Started

### Prerequisites

Ensure you have the following installed:
- Python 3.8 or higher
- Jupyter Notebook or Jupyter Lab

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/esemsc-kds24/BESS_Project
   cd your-repository
   ```

2. **Set up a virtual environment and install dependencies:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # For Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

### Usage

1. **Launch Jupyter Notebook or Lab:**
   ```bash
   jupyter notebook
   ```
   or
   ```bash
   jupyter lab
   ```

2. **Open the Notebook:**
   Open the main notebook file (e.g., `main.ipynb`) to run through the complete workflow.

## Project Structure

```
├── main.ipynb    # Main Jupyter Notebook
```

## Team Members

This project is developed by Group 16.  
- Andi Rosita Dewi (andi.dewi24@imperial.ac.uk)
 
- Zahrotuts Tsaniyah (zahrotuts.tsaniyah24@imperial.ac.uk)
 
- Nevio Muhammad Kamel (nevio.kamel24@ic.ac.uk)
 
- Kevin Danniel Suoth (kevin.suoth24@imperial.ac.uk)
## Contact

For any questions or feedback, please reach out to Rosita at [andi.dewi24@imperial.ac.uk].

```
