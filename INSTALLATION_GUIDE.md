# Healthcare Fraud Detection - Installation Guide

## Quick Start

### 1. Install Python Dependencies

```bash
pip install -r requirements.txt
```

### 2. Alternative: Install Individually

```bash
pip install pandas numpy openpyxl scikit-learn scipy matplotlib seaborn jupyter
```

### 3. Run the Notebook

#### Option A: Jupyter Notebook
```bash
jupyter notebook COMPLETE_FRAUD_ANALYSIS.ipynb
```

#### Option B: JupyterLab
```bash
jupyter lab COMPLETE_FRAUD_ANALYSIS.ipynb
```

#### Option C: Google Colab
1. Go to https://colab.research.google.com
2. Upload `COMPLETE_FRAUD_ANALYSIS.ipynb`
3. Upload your `Health_Insurance_Fraud_Claims.xlsx` file
4. Run all cells

---

## System Requirements

- **Python:** 3.8 or higher
- **RAM:** 4GB minimum (8GB recommended)
- **Disk Space:** 500MB for libraries
- **OS:** Windows, macOS, or Linux

---

## Package Versions

| Package | Version | Purpose |
|---------|---------|---------|
| pandas | ≥2.0.0 | Data manipulation |
| numpy | ≥1.24.0 | Numerical computing |
| openpyxl | ≥3.1.0 | Excel file reading |
| scikit-learn | ≥1.3.0 | Machine learning models |
| matplotlib | ≥3.7.0 | Data visualization |
| seaborn | ≥0.12.0 | Statistical plots |
| scipy | ≥1.11.0 | Scientific computing |
| jupyter | ≥1.0.0 | Notebook interface |

---

## Installation by Environment

### Windows

```bash
# Using pip
python -m pip install -r requirements.txt

# Using Anaconda
conda install pandas numpy openpyxl scikit-learn matplotlib seaborn scipy
conda install jupyter notebook
```

### macOS/Linux

```bash
# Using pip
pip3 install -r requirements.txt

# Using Anaconda
conda install pandas numpy openpyxl scikit-learn matplotlib seaborn scipy
conda install jupyter notebook
```

---

## Virtual Environment (Recommended)

### Create Virtual Environment

```bash
# Windows
python -m venv fraud_detection_env
fraud_detection_env\Scripts\activate

# macOS/Linux
python3 -m venv fraud_detection_env
source fraud_detection_env/bin/activate
```

### Install Packages

```bash
pip install -r requirements.txt
```

### Deactivate When Done

```bash
deactivate
```

---

## Troubleshooting

### Issue: "No module named 'openpyxl'"
**Solution:** `pip install openpyxl`

### Issue: "Microsoft Visual C++ required" (Windows)
**Solution:** Install Visual C++ Build Tools from Microsoft

### Issue: Jupyter not opening
**Solution:** 
```bash
pip install --upgrade jupyter notebook
jupyter notebook --version
```

### Issue: Import errors in notebook
**Solution:** Restart kernel and run all cells:
- Kernel → Restart & Run All

---

## Verify Installation

Run this Python script to verify all packages:

```python
import sys
print(f"Python version: {sys.version}")

packages = ['pandas', 'numpy', 'sklearn', 'matplotlib', 'seaborn', 'openpyxl']
for pkg in packages:
    try:
        __import__(pkg)
        print(f"✓ {pkg} installed")
    except ImportError:
        print(f"✗ {pkg} NOT installed")
```

---

## Running the Analysis

### Step-by-Step

1. **Activate environment** (if using virtual env)
   ```bash
   source fraud_detection_env/bin/activate  # macOS/Linux
   fraud_detection_env\Scripts\activate     # Windows
   ```

2. **Start Jupyter**
   ```bash
   jupyter notebook
   ```

3. **Open notebook**
   - Click on `COMPLETE_FRAUD_ANALYSIS.ipynb`

4. **Update file path** in Cell 2:
   ```python
   df = pd.read_excel('Health_Insurance_Fraud_Claims.xlsx')
   ```

5. **Run all cells**
   - Cell → Run All
   - Or press Shift+Enter for each cell

6. **View results**
   - Visualizations appear inline
   - Metrics printed after each section

---

## Expected Runtime

- **Data Loading:** < 5 seconds
- **EDA & Visualizations:** 10-15 seconds
- **Model Training:** 30-60 seconds
- **Total Runtime:** ~2 minutes

---

## Need Help?

### Common Commands

```bash
# Check Python version
python --version

# List installed packages
pip list

# Update pip
pip install --upgrade pip

# Install specific version
pip install pandas==2.0.0

# Uninstall package
pip uninstall package_name
```

### Resources

- Python Download: https://www.python.org/downloads/
- Anaconda: https://www.anaconda.com/products/distribution
- Jupyter Documentation: https://jupyter.org/documentation
- scikit-learn: https://scikit-learn.org/

---

## File Structure

```
fraud-detection/
├── requirements.txt
├── INSTALLATION_GUIDE.md (this file)
├── COMPLETE_FRAUD_ANALYSIS.ipynb
├── Health_Insurance_Fraud_Claims.xlsx
└── outputs/
    ├── model_performance_results.csv
    ├── feature_importance.csv
    └── visualizations/
```

---

## Optional: GPU Support

For faster model training with large datasets:

```bash
# NVIDIA GPU (CUDA support)
pip install scikit-learn[gpu]

# Note: Most analyses in this notebook run fast enough on CPU
```

---

**Last Updated:** February 6, 2026  
**Support:** For issues, check the troubleshooting section above
