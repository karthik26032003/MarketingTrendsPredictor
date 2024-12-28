# Marketing Analytics and Prediction Tool
This project analyzes 1P (First-Party) and 3P (Third-Party) marketing data to provide actionable insights. It uses Linear Regression, Ridge, and Lasso models for predictions and evaluates key metrics like Clicks, Impressions, CTR, and Admission Season trends.

## Features
- **Branded vs Non-Branded Click Analysis**: Categorizes and analyzes branded and non-branded queries.
- **Variance Analysis**: Provides Week-over-Week (WoW), Month-over-Month (MoM), and Year-over-Year (YoY) trends for clicks.
- **Correlation Analysis**: Evaluates relationships between clicks, impressions, CTR, and seasonal trends.
- **Predictive Modeling**: Uses Linear Regression to forecast future clicks based on historical data and external trends.
- **Scenario Analysis**: Simulates how changes in inputs (e.g., Impressions, CTR) impact clicks.

- ## Setup Instructions

### Prerequisites
- Python 3.x
- Jupyter Notebook
- Required Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `pytrends`, `statsmodels`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/repository-name.git
   cd repository-name
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook UNIVSENSE.ipynb
   ```

   ## How It Works
1. **Data Cleaning**: Cleans and preprocesses data from Google Search Console and external sources like Google Trends.
2. **Branded vs Non-Branded Analysis**: Separates queries into branded and non-branded categories for performance analysis.
3. **Predictive Modeling**: Uses Linear Regression, Ridge, and Lasso models to forecast clicks based on:
   - CTR (Click-Through Rate)
   - Impressions
   - Admission Season (Google Trends data)
4. **Scenario Simulation**: Simulates the impact of changing inputs on click performance.

## Usage Examples
- **Forecasting Clicks**:
  ```python
  future_data = pd.DataFrame({
      'admission season': [50, 60, 70],
      'CTR': [0.02, 0.03, 0.025],
      'Impressions': [15000, 16000, 15500]
  })
  predictions = lr_model.predict(future_data)
  print(predictions)
  ```

**Scenario Analysis**:
  ```python
  scenario_data = X_test.copy()
  scenario_data['CTR'] *= 1.1  # Increase CTR by 10%
  scenario_predictions = lr_model.predict(scenario_data)
  print(scenario_predictions)
  ```

  ## Results
- **Linear Regression**: Achieved an R-squared of 0.91 with an RMSE of 6.79.
- **Ridge and Lasso Regression**: Performed comparably after tuning, with slight variations in feature importance.
- **Key Insights**:
  - Impressions had the most significant impact on clicks.
  - Admission Season trends correlated positively with click performance.

## Results
- **Linear Regression**: Achieved an R-squared of 0.91 with an RMSE of 6.79.
- **Ridge and Lasso Regression**: Performed comparably after tuning, with slight variations in feature importance.
- **Key Insights**:
  - Impressions had the most significant impact on clicks.
  - Admission Season trends correlated positively with click performance.

## Contributing
Contributions are welcome! Please fork this repository and submit a pull request with your enhancements or bug fixes.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Acknowledgments
- Data sourced from Google Search Console and Google Trends.
- Inspired by marketing analytics and prediction challenges.
 
    
