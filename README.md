# Early Detection of VaR Model Deterioration: A Cantelli-Bound Ratio Approach for Proactive Risk Management

## Overview

This repository contains Jupyter notebooks for the S&P 500 analysis and the additional out-of-sample, dependence and model-sensitivity exercises. The study uses the VaR Efficiency Ratio (VER) to compare model-implied VaR with a Cantelli benchmark.

## Requirements

The original project lists Python 3.14.2 and the following packages:

```bash
pip install yfinance==1.1.0 pandas==3.0.0 numpy==2.3.5 statsmodels==0.14.6 scipy==1.17.0 matplotlib==3.10.8 arch==8.0.0 scikit-learn==1.8.0 shap==0.50.0 seaborn==0.13.2 xlsxwriter==3.2.9
```

Jupyter Notebook or JupyterLab is also required to run the `.ipynb` files. Package versions reflect the original README; the installation has not been independently tested.

## Notebooks

| Notebook | Purpose |
| --- | --- |
| `Main_SP500_Analysis.ipynb` | Main S&P 500 GARCH(2,2)–FHS forecasts, backtests and empirical analyses. |
| `Out_of_Sample_Evaluation.ipynb` | Rolling-origin evaluation of breach-probability forecasts (Section 5.9 and Tables 15.1–15.2). |
| `Dependence_Robust_Inference.ipynb` | HAC sensitivity and block-bootstrap coverage checks (Tables 16.1–16.2). |
| `SP500_Volatility_Filter_Sensitivity.ipynb` | Comparison of Gaussian and Student-t GARCH(2,2)–FHS filters (Table 6.2 and Tables 14.1–14.3). |
| `BTC_Cross_Asset_Daily_Return.ipynb` | BTC-USD GARCH–FHS and rolling historical simulation, evaluated using daily returns at the forecast lead. |

The supplied notebook names may end in `.ipynb.ipynb`. Rename them with a single `.ipynb` extension to match the names above.

The filter-sensitivity notebook contains two implementations. **Use its second code cell** for the S&P 500 daily-return filter comparison; the first cell uses cumulative returns.

The BTC daily-return notebook uses the single-day return at t + h. The BTC cumulative-return results in the paper's Tables 12.1–12.2 have a different outcome definition and must be reproduced from the corresponding cumulative-return code and outputs. `Sensitivity of Model Selection.ipynb` is an earlier combined cumulative-return exercise; its relationship to the final BTC tables has not been confirmed.

## How to run

1. Download or clone the repository, install the requirements and open the notebooks in Jupyter.
2. Run `Main_SP500_Analysis.ipynb` to generate the main S&P 500 analysis. Market data is downloaded through Yahoo Finance. Running the rolling analyses can take considerable time.
3. The out-of-sample and dependence notebooks read `SP500_daily_forecasts.csv` from the working directory. Use the saved forecast file from the main analysis, or export the main notebook's `df_full` after it has been calculated:

   ```python
   df_full.to_csv("SP500_daily_forecasts.csv", index=False)
   ```

4. Run the out-of-sample and dependence notebooks. The dependence notebook can also read `SP500_factors.csv`; factor-based checks require the relevant factor columns in that file or in the forecast data. Check its reporting inventory for unavailable controls.
5. Run the second code cell of the filter-sensitivity notebook for the S&P 500 filter comparison. Run the BTC notebook separately for its daily-return analysis.

Outputs are displayed in the notebooks or written to the directories named in the code. Some manuscript table headings and p-value displays were edited manually. The output directories and the manuscript's presentation should therefore be checked before reproducing the published tables.

## Data availability

The main and market-data notebooks retrieve prices from Yahoo Finance using `yfinance`. The out-of-sample and dependence notebooks instead require the saved forecast CSV described above; the dependence analysis may also require the factor CSV. Yahoo Finance data and package behaviour can change over time, so reruns may not exactly reproduce saved results.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
