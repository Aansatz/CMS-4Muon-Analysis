# CMS 4-Muon Invariant Mass Analysis ($H \to ZZ^* \to 4\mu$)

A high-energy physics analysis pipeline utilizing CMS open data to reconstruct the 4-muon invariant mass spectrum. This project focuses on isolating the "Golden Channel" and extracting resonance structures like the Z boson using advanced background-plus-signal mathematical modeling.

## 📌 Project Overview
This repository contains data analysis scripts and Jupyter Notebooks designed to process muon collision datasets from CERN/CMS open data archives. Key analysis steps include:
* Filtering and selecting high-purity 4-muon events.
* Calculating invariant mass distributions ($m_{4\mu}$).
* Implementing rigorous mathematical modeling (Exponential background + Gaussian signal fit) using `SciPy`.

---

## 🖥️ Environment: Local/WSL vs. Google Colab
While Google Colab is a popular tool for standard data science, high-energy physics analyses often require specialized setups. We recommend running this project in a local **WSL/Ubuntu** environment rather than Google Colab for the following reasons:
1. **Data Management:** CMS collision datasets are massive. Managing them locally or on grid storage is much more efficient than repeatedly uploading/downloading to Google Drive.
2. **Specialized Libraries:** Managing complex dependencies (like custom ROOT bindings or Awkward arrays) is much more stable in a persistent local/WSL environment. 

*(Note: If you still prefer to run this on Google Colab, you will need to manually upload the dataset to your session and execute `%pip install uproot awkward mplhep scipy -q` in the very first cell).*

---

## 🛠️ Libraries & Dependencies
The analysis relies on standard scientific computing and specialized HEP libraries:
* **`numpy`**: Array manipulations and vector calculations.
* **`matplotlib`**: Publication-ready visualizations.
* **`scipy`**: Non-linear least squares fitting (`curve_fit`) for signal/background extraction.
* **`uproot` & `awkward`**: Efficient handling of ROOT-format data structures in pure Python.
* **`mplhep`**: CMS style formatting for plots.

---

## 🚀 Usage

### 1. Clone the Repository
To get started, clone this repository to your local machine:
```bash
git clone [https://github.com/Aansatz/CMS-4Muon-Analysis.git](https://github.com/Aansatz/CMS-4Muon-Analysis.git)
cd CMS-4Muon-Analysis
