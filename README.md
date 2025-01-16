# Medical Data Analyzer

This tool is designed to facilitate the analysis and visualization of medical datasets using Python. The project was created and tested on Jupyter Notebook.

---

## Features
- **Data Cleaning**: Handles missing values and outliers in medical datasets.
- **Exploratory Data Analysis (EDA)**: Generates summary statistics, correlations, and visualizations.
- **Custom Visualizations**: Create detailed plots such as histograms, heatmaps, and category plot.
- **Correlation Analysis**: Calculate and visualize correlation matrices to identify relationships between variables.
- **Data Validation**: Filters out inconsistent data, such as cases where diastolic pressure is higher than systolic.
- **Disease Analysis**: Differentiates between the presence and absence of cardiovascular disease.
  

---

## Parameters
The analysis is based on the following parameters:
- `id`
- `age`
- `sex`
- `height`
- `weight`
- `ap_hi` (systolic blood pressure)
- `ap_lo` (diastolic blood pressure)
- `cholesterol`
- `gluc` (glucose level)
- `smoke`
- `alco` (alcohol consumption)
- `active` (physical activity)
- `cardio` (cardiovascular disease indicator)

---

## Getting Started

### Prerequisites
Ensure you have the following installed on your system:
- Python 3.7+
- Jupyter Notebook
- Required Python libraries:
  ```bash
  pandas
  numpy
  matplotlib
  seaborn
  scikit-learn
  ```
  Install these libraries using pip:
  ```bash
  pip install pandas numpy matplotlib seaborn scikit-learn
  ```

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/AyobamiMichael/medicaldata_analysis.git
   ```
2. Navigate to the project directory:
   ```bash
   cd medical_data_analysis
   ```
3. Open the project in Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Launch the main analysis notebook: `medical_data_visualizer.ipynb`.

---

## Usage
1. **Load Data**: Upload your medical dataset in `.csv` format.
2. **Clean Data**:
   - Filter out patient segments where diastolic pressure (`ap_lo`) is higher than systolic pressure (`ap_hi`).
   - Remove or handle other inconsistent or missing data as needed.
3. **Run Analysis**:
   - Perform exploratory data analysis to examine relationships between parameters.
   - Calculate the correlation matrix.
   - Generate a heatmap to visualize correlations.
   - Differentiate between the presence and absence of cardiovascular disease (`cardio`).
4. **Save Results**: Export cleaned datasets and visualizations.

---

## Example
Here's a snippet of the data cleaning and analysis process:
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load the dataset
data = pd.read_csv('medical_examination.csv')

# Filter out invalid data (diastolic > systolic)
data = data[data['ap_lo'] <= data['ap_hi']]

# Calculate the correlation matrix
corr_matrix = data.corr()

# Generate a heatmap
sns.heatmap(corr_matrix, annot=True, fmt='.2f', cmap='coolwarm')
plt.title('Correlation Matrix Heatmap')
plt.show()
```

---

## Contributing
Contributions are welcome! Follow these steps to contribute:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add new feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature-name
   ```
5. Submit a pull request.

---

## License
This project is licensed under the [MIT License](LICENSE).

---

## Contact
For any inquiries or feedback, please contact:
- **Author**: Ayobami Michael Opefeyijimi
- **Email**: ayobamiwealth@gmail.com
---

Thank you.

