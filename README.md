# 🍷 Wine Quality Dataset Analysis

This project analyzes the **Wine Quality Dataset (red wine)** using Python.  
We explore the dataset with **vectors, matrices, covariance, eigen decomposition, and probability concepts**, along with visualizations.

---

## 📂 Dataset
- **File:** `winequality-red.csv`
- **Rows:** 1599
- **Columns:** 12 (chemical properties + quality score)
- **Features:** acidity, alcohol, citric acid, pH, residual sugar, density, etc.
- **Target:** `quality` (integer score 3–8)

---

## 🛠️ Tasks Implemented
1. **Data Cleaning**
   - Missing values handled by replacing with column mean.
   
2. **Vector Extraction**
   - Extracted columns as vectors:  
     - `alcohol`  
     - `citric acid`

3. **Covariance Matrix**
   - Computed covariance between `alcohol` and `density` using:
     ```python
     cov_mat = np.cov(X.T)
     ```

4. **Eigen Decomposition**
   - Performed on covariance matrix.
   - Identified top 2 eigenvalues and eigenvectors.
   - Found **alcohol explains almost all variance**, density contributes very little.

5. **Wine Quality Distribution**
   - Found most common wine quality is **5 (681 samples)**.
   - Distribution is centered around 5–6 with fewer extreme values.

---

## 📊 Visualizations
- **Histogram of Wine Quality**

- **Scatter Plot (Alcohol vs Density) with Eigenvectors**

---

## 🔎 Key Insights
- **Alcohol variance is high**, while **density variance is very small**.
- **Alcohol ↑ → Density ↓ (weak negative relationship)**.
- Eigen decomposition shows **alcohol dominates variation** between the two.
- Quality distribution is **skewed toward medium-quality wines (5–6)**.

---

## 🖥️ Tech Stack
- **Python**
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`

---

## 🚀 How to Run
1. Clone this repository
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
