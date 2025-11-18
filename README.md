# 📘 Sampling Distribution & Central Limit Theorem — Python Simulation

This project demonstrates how sampling variability, sampling distributions, and the Central Limit Theorem (CLT) work in practice using real-world AQI (Air Quality Index) data.
It uses a simulation-based approach to show how repeated random sampling leads to stable and predictable statistical patterns.

---

## 🔍 Overview

The project walks through:

* Drawing random samples from a dataset
* Calculating sample means
* Repeating the sampling process thousands of times
* Visualizing how these sample means form a **sampling distribution**
* Showing how the **Central Limit Theorem** naturally emerges
* Computing the **Standard Error** for sample means

This provides an intuitive understanding of why and how inferential statistics work.

---

## 🧪 What This Project Does

### **1. Explore the Dataset**

* Load AQI data (EPA dataset)
* Inspect the data structure and summary statistics
* Compute the **population mean** — used as a baseline

---

### **2. Take a Random Sample (n = 50)**

```python
sample = data.sample(n=50, replace=True, random_state=42)
sample_mean = sample["aqi"].mean()
```

Shows how a single sample can differ from the true population mean.

---

### **3. Generate the Sampling Distribution**

* Perform **10,000 bootstrap samples**
* Each sample = size 50, with replacement
* Compute the mean of each sample
* Store all 10,000 sample means into a DataFrame

This produces the empirical **sampling distribution of the mean**.

---

### **4. Visualize the Distribution**

Visualization includes:

* Histogram of the 10,000 sample means
* The **population mean**
* The **mean of the sampling distribution**
* The **first sample’s mean** (to show variability)
* A fitted **normal curve**, as predicted by CLT

The resulting plot clearly shows a bell-shaped distribution centered around the population mean.

---

### **5. Calculate Standard Error**

[
SE = \frac{SD}{\sqrt{n}}
]

The Standard Error quantifies how much the sample mean fluctuates from sample to sample.

---

## 🎯 Key Insights

* Repeated sample means form a **normal distribution**, even when original data isn’t perfectly normal.
* The center of the sampling distribution ≈ **population mean**.
* Increasing sample size decreases **standard error**, making estimates more precise.
* This simulation visually and numerically confirms the **Central Limit Theorem**.

---

## 🧰 Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* SciPy
* Jupyter Notebook

---



---

## 📌 Summary

This project builds a complete simulation-based understanding of sampling distributions and the Central Limit Theorem.
Through repeated random sampling and visualization, it shows why sample means behave predictably — and why inferential statistics is possible at all.


