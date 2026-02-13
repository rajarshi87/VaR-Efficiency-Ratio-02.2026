# Early Detection of VaR Model Deterioration: A Cantelli-Bound Ratio Approach for Proactive Risk Management

## Overview
This repository contains the code and outputs used in this paper.

## Requirements
- Python 3.9.13
- yfinance 0.2.64
- pandas 1.4.4
- numpy 1.21.5
- statsmodels 0.13.2
- scipy 1.9.1
- matplotlib 3.5.2
- arch 6.1.0
- sklearn 1.0.2
- shap 0.41.0
- seaborn 0.11.2

## How to Run
1. Download or clone this repository.
2. Install required packages:
   ```bash
   pip install yfinance==0.2.64 pandas==1.4.4 numpy==1.21.5 statsmodels==0.13.2 scipy==1.9.1 matplotlib==3.5.2 arch==6.1.0 scikit-learn==1.0.2 shap==0.41.0 seaborn==0.11.2
3. Open main.ipynb and run (Kernel → Restart & Run All)
4. Outputs (tables,plots) will be saved in the same folder.

## Data Availability
All market data is retrieved directly from Yahoo Finance using the `yfinance` Python package.  
No datasets are stored in this repository. Data is downloaded automatically when running `main.ipynb`.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
