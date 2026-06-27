# 🏥 Insurance Cost Charges Analysis

An Exploratory Data Analysis (EDA) and visualization project focused on identifying key factors that influence medical insurance cost charges. This project utilizes Python data science libraries to profile demographics, examine health metrics, and model the correlations between individual features and total charges.

---

## 📊 Dataset Profile

The dataset (`insurance.csv`) contains **1,338 records** of individual beneficiaries with 7 clinical and demographic features:

| Column | Data Type | Description |
| :--- | :--- | :--- |
| **`age`** | `int64` | Age of primary beneficiary (ranging from 18 to 64 years) |
| **`sex`** | `object` | Gender of beneficiary (`female`, `male`) |
| **`bmi`** | `float64` | Body Mass Index ($kg/m^2$), representing body weight relative to height |
| **`children`** | `int64` | Number of children / dependents covered by the insurance |
| **`smoker`** | `object` | Smoking status (`yes`, `no`) |
| **`region`** | `object` | Beneficiary's residential area in the US (`northeast`, `northwest`, `southeast`, `southwest`) |
| **`charges`** | `float64` | Individual medical costs billed by health insurance |

---

## 🔍 Analysis Workflow & Notebook Structure

The analysis is documented in [insurance_analysis.ipynb](file:///c:/Users/admin/Documents/OneNote%20Notebooks/Insurance%20cost%20charges/insurance_analysis.ipynb) and consists of the following steps:

1. **Data Loading & Profiling**:
   - Importing dependencies (`pandas`, `matplotlib`, `seaborn`).
   - Loading the dataset, inspecting shape, column data types, missing values, and generating descriptive statistics.

2. **Regional Charges & Distributions**:
   - Aggregate charges grouped by region.
   - Proportional distribution of charges using a **Pie Chart**.
   - Analysis of regional representation (even distribution across all four regions).

3. **Health Metrics Exploration (BMI & Age)**:
   - Visualizing BMI distributions with Kernel Density Estimates (KDE).
   - Examining how BMI ranges correlate with beneficiary age.
   - Boxplot comparisons of age/BMI distributions across smoking and non-smoking groups.

4. **Categorical & Correlation Analysis**:
   - **Heatmap Cross-tabulation**: Inspecting demographic proportions between sex and smoking habits.
   - **Correlation Heatmap**: Analyzing linear correlations between numerical variables (`age`, `bmi`, `charges`).
   - **Pairplot Grid**: Visualizing pairwise relationships across the entire dataset.

5. **Insurance Cost Drivers**:
   - Investigating the impact of age on charges using line plots.
   - Analyzing the relationship between smoking and billed charges using boxplots.
   - Evaluating the interaction between BMI, Smoking Status, and Charges using scatter plots and regression models.

---

## 💡 Key Insights from the Data

- **Smoking is the Primary Driver of Charges**: Smokers face substantially higher charges than non-smokers, showing a stark contrast in cost distributions regardless of age or gender.
- **BMI & Smoking Interaction**: A high BMI combined with smoking status results in exponentially higher medical charges. For non-smokers, high BMI has a much gentler impact on charges.
- **Age Correlation**: Billed charges generally increase with age, reflecting a steady baseline increase in medical costs over time.
- **Regional Contribution**: The **Southeast** region accounts for the highest total billed charges (~$5.36M) compared to the other three regions (which average ~$4.0M to $4.3M each).

---

## 🛠️ Getting Started

### Prerequisites

To run this notebook, you need Python and the required data science packages. It is recommended to run this inside the configured virtual environment:

```bash
# Activate the virtual environment (Windows PowerShell)
.venv\Scripts\Activate.ps1

# Run Jupyter Notebook
jupyter notebook
```

### Dependencies
- `pandas`
- `matplotlib`
- `seaborn`
- `notebook` or `jupyterlab`

---

## 📁 Repository Contents
* `insurance.csv` — The raw comma-separated values dataset.
* `insurance_analysis.ipynb` — The Jupyter notebook containing the full visualization and analysis pipeline.
* `.venv/` — Virtual environment containing dependencies.
