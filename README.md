# 👁️ EyeLab (OptoLab)
**The L.U.N.A. Optotypes (Logarithmically Unified Normative Acuity) Platform**

EyeLab is a comprehensive, client-side web application designed for advanced visual acuity studies, psychophysical metrics, and optotype optimization. It provides the tools necessary to evaluate, calibrate, and clinically validate visual stimuli on digital displays.

---

## 🔬 Scientific Rationale
The transition from printed charts (300 ppi) to standard digital clinical displays (~68 ppi) introduces pixelization challenges and uneven morphological complexity among traditional optotypes (like the Classic Sloan/ETDRS set). This asymmetry leads to visual crowding and "guessing inflation." 

EyeLab was developed to algorithmically scale individual optotypes based on their psychometric detection slope using Bayesian methods, ultimately isolating the most robust characters to form the **L.U.N.A. Set**.

## ✨ Key Features
* **Zero Backend Dependency:** Pure HTML5, CSS3, and Vanilla JavaScript. Runs entirely locally in the browser.
* **Psychometric Calibration (QUEST+):** Utilizes multidimensional Bayesian adaptive methods to estimate the detection threshold (Th75/Th90) and slope of individual letters.
* **Optotype Optimization Engine:** Runs 50,000 Monte Carlo simulations using a 5-parameter cost function to minimize morphological confusion and variability.
* **Clinical Validation Engine:** Compares paired patient data (Classic vs. L.U.N.A.) measuring partial lines ("Brick Wall" effect), global confusion, and test-retest reliability (ICC).
* **Automated Data Visualization:** Generates publication-ready Canvas graphics, including:
  * Psychometric Probability Curves
  * Asymmetrical Confusion Matrices (Heatmaps)
  * Bland-Altman Agreement Plots
  * Scatter Correlation Plots

---

## 🚀 Quick Start / Tutorial

Since EyeLab runs locally, installation is instant.

### 1. Installation
Clone this repository to your local machine:
```bash
git clone [https://github.com/yourusername/EyeLab.git](https://github.com/yourusername/EyeLab.git)
```

### 2. Launching the App
1. Navigate to the `Quest` directory within the cloned repository.
2. Open the `test.html` file in any modern web browser (Google Chrome or Mozilla Firefox recommended).
   * *Note: No local server (like Node.js or Apache) is required.*

### 3. Workflow Overview
The `test.html` dashboard is divided into specific tabs for the research lifecycle:

* **Tab 1: Psychometric Test (QUEST+)**
  * Conduct adaptive thresholding for visual stimuli. The system will dynamically adjust letter sizes based on patient responses to find the exact detection slope.
* **Tab 2: Clinical Validation (ETDRS)**
  * Run side-by-side standard clinical tests comparing the Classic Sloan set against the optimized L.U.N.A. Set.
* **Tab 3: Batch Analysis (Data Ingestion)**
  * Upload your raw `.csv` results from the tests. 
  * The engine will instantly parse the data, calculate *p-values*, ICC, and render the analytical Canvas charts.

## 📊 Data Formatting (CSV Imports)
To use the Batch Analysis tool, ensure your `.csv` files follow the required structure:

* **Psychometric Data:** Requires columns for `subject, letter, answer, logmar, correct`.
* **Clinical Data:** Requires columns for `subject, run, chart, line, logmar, letters, responses, correct, time, idade, sexo, esferico`.

## 🔠 Custom Typography
This project relies on a custom vectorial font (`Sloan2.otf`) located in the root directory to ensure precise geometric scaling of optotypes across different screen resolutions. The application loads this font automatically via CSS `@font-face`.

---

## 📄 License and Ethics
*(Add your specific license details here, e.g., MIT License. Mention if the clinical data usage requires specific ethical committee approvals, such as the Research Ethics Committee of the Faculdade de Ciências Médicas da Paraíba).*
