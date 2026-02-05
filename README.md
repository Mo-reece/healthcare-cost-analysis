# Healthcare Cost Analysis: Identifying Key Cost Drivers

A comprehensive exploratory data analysis (EDA) of medical insurance costs to identify the primary factors driving healthcare expenses in the United States.

## Project Overview

This project analyzes the Medical Cost Personal Dataset to understand which demographic and lifestyle factors most significantly impact individual healthcare costs. The findings provide actionable insights for insurance companies, healthcare providers, and policymakers.

## Key Findings

### Primary Cost Drivers (Ranked by Impact)

| Factor | Correlation | p-value | Impact |
|--------|-------------|---------|--------|
| **Smoking Status** | 0.79 | < 0.001 | Smokers pay **283% more** than non-smokers |
| **Age** | 0.30 | < 0.001 | ~$257 increase per year of age |
| **BMI** | 0.20 | < 0.001 | Obese individuals have significantly higher costs |

### Critical Insight
**Obese smokers represent the highest-risk segment**, with average charges of **$41,557** compared to **$8,434** for non-smokers with normal BMI - a **393% difference**.

### Surprising Finding
- **Sex** and **Region** showed no statistically significant impact on medical charges
- This challenges common assumptions about regional healthcare cost disparities

## Visualizations

The analysis includes 10 publication-quality visualizations:

1. **Outlier Detection** - Box plots identifying data anomalies
2. **Charges Distribution** - Target variable analysis with log transformation
3. **Numeric Feature Distributions** - Age, BMI, and children analysis
4. **Categorical Distributions** - Sex, smoker, and region breakdowns
5. **Correlation Heatmap** - Feature relationships visualization
6. **Charges by Category** - Box plots by categorical variables
7. **Scatter Relationships** - Numeric features vs. charges
8. **Interaction Effects** - Multi-factor analysis
9. **Pairplot Matrix** - Comprehensive relationship overview
10. **Executive Summary** - Key findings dashboard

## Technical Stack

- **Python 3.9+**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **matplotlib** - Visualization framework
- **seaborn** - Statistical visualization
- **scipy** - Statistical testing

## Project Structure

```
healthcare-cost-analysis/
├── data/
│   ├── insurance.csv           # Raw dataset
│   └── insurance_cleaned.csv   # Processed dataset
├── notebooks/
│   └── healthcare_cost_eda.ipynb  # Main analysis notebook
├── visualizations/
│   ├── 01_outlier_boxplots.png
│   ├── 02_charges_distribution.png
│   ├── 03_numeric_distributions.png
│   ├── 04_categorical_distributions.png
│   ├── 05_correlation_heatmap.png
│   ├── 06_charges_by_category.png
│   ├── 07_scatter_relationships.png
│   ├── 08_interaction_effects.png
│   ├── 09_pairplot.png
│   └── 10_executive_summary.png
├── requirements.txt
└── README.md
```

## Getting Started

### Prerequisites

```bash
# Clone the repository
git clone https://github.com/yourusername/healthcare-cost-analysis.git
cd healthcare-cost-analysis

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Running the Analysis

```bash
# Launch Jupyter Notebook
jupyter notebook notebooks/healthcare_cost_eda.ipynb
```

Or use Jupyter Lab:
```bash
jupyter lab
```

## Data Source

**Dataset:** [Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance) from Kaggle

**Features:**
| Column | Description | Type |
|--------|-------------|------|
| age | Age of primary beneficiary | Numeric |
| sex | Gender (male/female) | Categorical |
| bmi | Body Mass Index (kg/m²) | Numeric |
| children | Number of dependents | Numeric |
| smoker | Smoking status (yes/no) | Categorical |
| region | US residential area | Categorical |
| charges | Medical costs billed ($) | Numeric (Target) |

## Statistical Methods

- **Descriptive Statistics**: Mean, median, standard deviation, IQR
- **Correlation Analysis**: Pearson and Spearman correlations
- **Hypothesis Testing**:
  - Independent t-tests (smoker vs non-smoker, male vs female)
  - One-way ANOVA (region and BMI category comparisons)
- **Effect Size**: Cohen's d for practical significance
- **Outlier Detection**: IQR method with 1.5× threshold

## Business Recommendations

### For Insurance Companies
1. Implement smoking status as the primary factor in premium calculations
2. Offer premium discounts for smoking cessation program completion
3. Develop wellness programs targeting the obese smoker segment

### For Healthcare Providers
1. Prioritize smoking cessation resources for high-BMI patients
2. Implement age-based preventive screening programs
3. Address smoking and obesity as interconnected health risks

### For Policymakers
1. Invest in public health anti-smoking campaigns
2. Mandate smoking cessation coverage in employer health plans
3. Fund research on smoking-obesity interaction effects

## Skills Demonstrated

- **Data Wrangling**: Cleaning, validation, and transformation
- **Statistical Analysis**: Hypothesis testing, correlation analysis
- **Data Visualization**: Publication-quality charts with matplotlib/seaborn
- **Domain Knowledge**: Healthcare economics, insurance pricing factors
- **Communication**: Translating analysis into business recommendations

## Future Enhancements

- [ ] Build predictive model for healthcare costs (Linear Regression, Random Forest)
- [ ] Perform feature engineering (interaction terms, polynomial features)
- [ ] Add cross-validation and model comparison
- [ ] Deploy as interactive dashboard (Streamlit/Dash)
- [ ] Incorporate external data (regional healthcare indices)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Dataset provided by [Miri Choi](https://www.kaggle.com/mirichoi0218) on Kaggle
- Inspired by healthcare cost research in actuarial science

---

**Author:** [Okurut Maurice Leonard]


