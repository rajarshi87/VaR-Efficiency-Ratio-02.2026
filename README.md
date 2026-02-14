# Early Detection of VaR Model Deterioration: A Cantelli-Bound Ratio Approach for Proactive Risk Management

## Overview
This repository contains the code and outputs used in this paper.

## Requirements
- Python 3.14.2  
- yfinance 1.1.0  
- pandas 3.0.0  
- numpy 2.3.5  
- statsmodels 0.14.6  
- scipy 1.17.0  
- matplotlib 3.10.8  
- arch 8.0.0  
- scikit-learn 1.8.0  
- shap 0.50.0  
- seaborn 0.13.2  
- xlsxwriter 3.2.9  

## How to Run
1. Download or clone this repository.
2. Install required packages:
   ```bash
   pip install yfinance==1.1.0 pandas==3.0.0 numpy==2.3.5 statsmodels==0.14.6 scipy==1.17.0 matplotlib==3.10.8 arch==8.0.0 scikit-learn==1.8.0 shap==0.50.0 seaborn==0.13.2 xlsxwriter==3.2.9

3. Open main.ipynb and run (Kernel → Restart & Run All)
4. Outputs (tables,plots) will be saved in the same folder.

## Data Availability
All market data is retrieved directly from Yahoo Finance using the `yfinance` Python package.  
No datasets are stored in this repository. Data is downloaded automatically when running `main.ipynb`.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
