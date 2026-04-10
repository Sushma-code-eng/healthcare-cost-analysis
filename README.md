# Healthcare Cost Analysis

## Overview
This project performs an end-to-end analysis of healthcare costs using machine learning and statistical methods. By examining demographic, behavioral, and clinical factors, we identify the key drivers of medical expenditure and build predictive models to estimate individual healthcare costs. Our analysis reveals that **smoking is the single largest cost driver**, with smokers incurring costs approximately **4.8× higher** than non-smokers.

## Features
- **Exploratory Data Analysis (EDA)**: In-depth exploration of healthcare cost distributions, feature correlations, and demographic breakdowns.
- **Feature Engineering**: Creation of interaction terms (e.g., smoker × BMI) and non-linear transformations to capture complex relationships.
- **Predictive Modeling**: Comparison of multiple regression models including Linear Regression, Random Forest, Gradient Boosting, and XGBoost.
- **Model Interpretability**: SHAP (SHapley Additive exPlanations) analysis to explain individual predictions and global feature importance.
- **Comprehensive Reporting**: Detailed analysis report with actionable business recommendations.

## Getting Started

### Prerequisites
- Python 3.x
- Required packages listed in `requirements.txt`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Sushma-code-eng/healthcare-cost-analysis.git
   ```
2. Navigate to the project directory:
   ```bash
   cd healthcare-cost-analysis
   ```
3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
You can run the analysis scripts in the `src/` directory. Ensure that you have the necessary data files in the `data/` folder.

## Documentation
For comprehensive documentation, please refer to the `docs/` folder.

## Visualizations

### Target Distribution
![Target Distribution](01_target_distribution.png)

The distribution of healthcare charges is right-skewed, with the majority of individuals incurring lower costs and a long tail of high-cost patients. This skewness is largely driven by the smoking population, which forms a distinct high-cost cluster.

### Smoking Impact
![Smoking Impact](02_smoking_impact.png)

Smokers incur healthcare costs that are on average **4.8× higher** than non-smokers. This visualization breaks down cost distributions by smoking status, clearly showing the separation between the two groups across age and BMI categories.

### Multi-Feature Analysis
![Multi-Feature Analysis](03_multi_feature_analysis.png)

A multi-dimensional view of how age, BMI, smoking status, and number of dependents interact to influence healthcare costs. The plot reveals that the combined effect of smoking and high BMI produces the most extreme cost outliers.

### Correlation Heatmap
![Correlation Heatmap](04_correlation_heatmap.png)

The correlation matrix highlights the strongest linear relationships between features and healthcare charges. Smoking status and BMI show the highest positive correlations with cost, while features like region and sex have minimal linear impact.

### Model Comparison
![Model Comparison](05_model_comparison.png)

A side-by-side comparison of model performance (R² score, RMSE, MAE) across Linear Regression, Random Forest, Gradient Boosting, and XGBoost. The Gradient Boosting model achieves the best balance of accuracy and generalization.

### Actual vs Predicted
![Actual vs Predicted](06_actual_vs_predicted.png)

Scatter plot of actual vs. predicted healthcare charges for the best-performing model. Points close to the diagonal line indicate accurate predictions. The model performs well across the cost spectrum, with slight underestimation at the highest cost levels.

### Error Distribution
![Error Distribution](07_error_distribution.png)

The residual distribution is approximately normal and centered near zero, confirming that the model's prediction errors are unbiased. The spread of residuals indicates the typical magnitude of prediction error.

### SHAP Summary
![SHAP Summary](08_shap_summary.png)

The SHAP summary plot shows how each feature contributes to individual predictions. Each dot represents a single patient; the color indicates the feature value (red = high, blue = low) and the horizontal position shows the impact on the predicted cost. Smoking status dominates with consistently large positive SHAP values.

### SHAP Feature Importance
![SHAP Feature Importance](09_shap_bar.png)

The mean absolute SHAP values rank features by their overall importance to the model. Smoking status, BMI, and age are the top three contributors, together accounting for the majority of the model's predictive power.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any suggestions or changes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.