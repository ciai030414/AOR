# COVID-19 Infection Rate Prediction and Analysis (Los Angeles County)

## Overview
This repository contains the deliverables for our project on predicting COVID-19 infection rates in Los Angeles County. The project explores multiple predictive models, including Bayesian SIR, ARIMA, LSTM, XGBoost, and Random Forest, to determine the most effective model for forecasting infection trends. The analysis leverages publicly available COVID-19 datasets and applies statistical and machine learning methodologies.

## Repository Structure
```
📂 covid19-prediction
│── 📂 code
│   │── data_preprocessing.ipynb  # Data cleaning and feature engineering
│   │── exploratory_analysis.ipynb  # Exploratory Data Analysis (EDA)
│   │── model_training.ipynb  # Model training and evaluation
│ 
│
│── 📂 images
│   │── eda_plots/  # Data visualizations (trends, distributions, etc.)
│   │── model_performance/  # Model comparison charts
│
│── 📂 reports
│   │── project_progress.pdf  # Progress report
│
│── 📂 data
│   │── raw/  # Original datasets (CSV files from public sources)
│   │── processed/  # Cleaned and transformed datasets
│
│── README.md  # Project documentation and usage instructions
```

## Dataset Sources
The data used in this project is sourced from publicly available COVID-19 reports and repositories:
- **Los Angeles County COVID-19 Data**: [GitHub Repository](https://github.com/ANRGUSC/lacounty_covid19_data)
- **California State COVID-19 Data**: [Data Desk](https://github.com/datadesk/california-coronavirus-data)


## Installation & Setup
To run the code locally, follow these steps:
1. Clone this repository:
   ```bash
   git clone https://github.com/your_username/covid19-prediction.git
   cd covid19-prediction
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebooks in the `code/` directory using Jupyter Notebook or Jupyter Lab:
   ```bash
   jupyter lab
   ```

## Model Overview
We explored the following models to predict infection rates:
- **Bayesian SIR Model**: Epidemiological model estimating infection risk.
- **ARIMA**: Time-series forecasting model.
- **LSTM**: Deep learning-based sequence model.
- **XGBoost**: Gradient boosting-based machine learning model.
- **Random Forest**: Ensemble learning model.

After comparing performance metrics (MAE, RMSE), the best-performing model was selected and fine-tuned.

## Deliverables
- **Preprocessed datasets** for training and analysis.
- **EDA visualizations** for trend analysis and feature importance.
- **Model comparison reports** showing accuracy and predictions.
- **Final optimized model** for forecasting COVID-19 infections.
- **Project documentation** detailing methodology, assumptions, and constraints.

## Contributors
- **Mengqiu Cao**  
- **Junrong Qian**  
- **Yiqiu Pan**  
- **Yue Cao**  

## License
This project is released under the MIT License.

## Contact
For any questions, please reach out to the project team or open an issue on GitHub.
