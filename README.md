# Unsupervised Learning Workflow: Clustering & Dimensionality Reduction

**Practical implementation of K-means clustering and PCA for dimensionality reduction on digit recognition**

## Overview

This project demonstrates practical applications of unsupervised learning techniques for pattern discovery and data preprocessing in machine learning workflows. It covers K-means clustering with elbow method optimization, semi-supervised learning approaches, and Principal Component Analysis (PCA) for dimensionality reduction.

## Problem & Approach

**Problem:** Demonstrate how unsupervised learning techniques can be leveraged for pattern discovery, data preprocessing, and improving classification performance, particularly in scenarios with limited labeled data.

**Approach:**
- Apply K-means clustering to discover patterns in unlabeled handwritten digit data
- Use the elbow method to determine the optimal number of clusters
- Leverage clustering as a preprocessing step for semi-supervised learning
- Apply PCA for dimensionality reduction while preserving variance
- Evaluate the impact of these techniques on classification accuracy

## Tech Stack

- **Python 3.x** - Core programming language
- **Jupyter Notebook** - Interactive analysis environment
- **scikit-learn** - Machine learning algorithms (K-means, PCA, Logistic Regression)
- **NumPy** - Numerical computing and array operations
- **Matplotlib** - Data visualization

## Repository Structure

```
.
├── unsupervised_learning_analysis.ipynb  # Main analysis notebook
├── requirements.txt                       # Python dependencies
├── README.md                             # This file
└── project_identity.md                   # Project metadata
```

## Setup

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Raminyazdani/data-modeling-notebook-workflow.git
cd data-modeling-notebook-workflow
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

**Windows users:** The same commands work in PowerShell or Command Prompt.

## How to Run

Launch the Jupyter notebook from the repository root:

```bash
jupyter run unsupervised_learning_analysis.ipynb
```

The notebook will open in your default web browser. Execute cells sequentially using `Shift+Enter` or the "Run" button.

**Alternative:** If you prefer JupyterLab:
```bash
jupyter lab unsupervised_learning_analysis.ipynb
```

## Data / Inputs

This project uses the **scikit-learn digits dataset**, which is built-in and requires no external data files.

**Dataset Details:**
- **Source**: `sklearn.datasets.load_digits`
- **Description**: 8×8 pixel grayscale images of handwritten digits (0-9)
- **Samples**: 1,797 total samples (~180 per class)
- **Features**: 64 dimensions (flattened 8×8 pixel values, integers 0-16)
- **Classes**: 10 (digits 0-9)

The dataset is automatically downloaded when you first run the notebook.

## Outputs

All outputs are displayed inline within the Jupyter notebook:

1. **Clustering Analysis:**
   - Elbow curve visualization for optimal k selection
   - Sample digit visualizations
   - Cluster representative digit images

2. **Semi-Supervised Learning Results:**
   - Classification accuracy with limited labeled data
   - Performance comparison: baseline vs. cluster-based approach
   - Accuracy metrics for different training strategies

3. **Dimensionality Reduction Analysis:**
   - Explained variance plots for PCA components
   - Classification performance across different dimensionalities
   - Optimal component selection analysis

## Reproducibility Notes

- **Random State**: The notebook uses `random_state=42` for reproducibility of clustering and train/test splits
- **Dependencies**: All package versions specified in `requirements.txt`
- **Python Version**: Tested with Python 3.8+, compatible with Python 3.7+
- **Dataset**: Uses built-in scikit-learn dataset (consistent across runs)
- **Execution Order**: Cells should be executed sequentially from top to bottom

## Key Techniques Demonstrated

### 1. K-means Clustering
- Unsupervised pattern discovery in digit images
- Elbow method for optimal cluster count determination
- Cluster representative selection

### 2. Semi-Supervised Learning
- Using clustering to extend limited labeled data
- Automatic label propagation via cluster assignments
- Performance evaluation with partial supervision

### 3. Dimensionality Reduction (PCA)
- Variance-based feature reduction
- Trade-off analysis between dimensionality and performance
- Visualization of explained variance

## Troubleshooting

### Issue: "ModuleNotFoundError: No module named 'sklearn'"
**Solution:** Install scikit-learn:
```bash
pip install scikit-learn>=1.0.0
```

### Issue: Jupyter notebook command not found
**Solution:** Ensure Jupyter is installed:
```bash
pip install jupyter>=1.0.0
```

### Issue: Notebook kernel crashes or freezes
**Solution:** 
- Restart the kernel: Click "Kernel" → "Restart" in Jupyter
- Check available memory (clustering operations can be memory-intensive)
- Try running cells individually rather than "Run All"

### Issue: Plots not displaying
**Solution:** Ensure matplotlib backend is properly configured. Add to the top of the notebook if needed:
```python
%matplotlib inline
```

## Results Summary

The notebook demonstrates that:
- K-means clustering can effectively discover digit patterns without labels
- The elbow method suggests k≈10-15 for the digits dataset
- Clustering-based semi-supervised learning improves accuracy when labeled data is scarce
- PCA can reduce dimensionality significantly while maintaining classification performance
- Proper preprocessing can enhance model efficiency and interpretability

## License

This project is open source and available for educational and professional use.

## Author

**Ramin Yazdani**
