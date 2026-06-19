<h1 align="center">🌱 GreenEHR: Green Computing Strategies for Healthcare Predictive Models</h1>

<p align="center">
  <b>University of Milano-Bicocca – MSc Data Science</b><br>
  Green Computing Course Project
</p>

<p align="center">
  <b>Authors:</b> Güldeniz Güzelay & Sude Aslan
</p>

<hr>

<h2>📖 Project Overview</h2>

<p>
This project investigates the relationship between predictive performance and environmental sustainability in healthcare machine learning applications.
Five Electronic Health Record (EHR) datasets were analyzed using multiple machine learning algorithms while monitoring energy consumption, carbon emissions, and execution time through CodeCarbon.
</p>

<p>
A second <b>Green Computing</b> version of the pipeline was developed using optimization strategies designed to reduce computational costs while preserving predictive performance.
</p>

<hr>

<h2>🏥 Datasets</h2>

<ul>
  <li>Neuroblastoma</li>
  <li>Pediatric Brain Tumor</li>
  <li>Colorectal Cancer</li>
  <li>Sepsis / SIRS</li>
  <li>Depression with Heart Failure</li>
</ul>

<hr>

<h2>⚙️ Methodology</h2>

<h3>1. Data Preparation & Cleaning</h3>

<ul>
  <li>Column name standardization</li>
  <li>Duplicate detection and removal</li>
  <li>Missing value handling</li>
  <li>Boolean feature conversion (0/1)</li>
  <li>Data type validation</li>
</ul>

<h3>2. Data Leakage Detection</h3>

<ul>
  <li>Target variables explicitly mapped for each dataset</li>
  <li>Leakage-prone features removed</li>
  <li>Future-information variables excluded</li>
</ul>

<h3>3. Feature Engineering</h3>

<p>
Domain-specific healthcare features were generated using clinical knowledge.
Examples include:
</p>

<ul>
  <li>Age Risk Groups</li>
  <li>Disease Severity Scores</li>
  <li>Treatment Intensity Scores</li>
  <li>Comorbidity Indicators</li>
  <li>Organ Dysfunction Metrics</li>
</ul>

<h3>4. Unified Preprocessing Pipeline</h3>

<ul>
  <li>Median Imputation</li>
  <li>One-Hot Encoding</li>
  <li>Feature Scaling (MinMaxScaler)</li>
  <li>Consistent preprocessing across all datasets</li>
</ul>

<hr>

<h2>🤖 Machine Learning Models</h2>

<table>
<tr>
<th>Model</th>
<th>Purpose</th>
</tr>

<tr>
<td>Logistic Regression</td>
<td>Lightweight baseline model</td>
</tr>

<tr>
<td>Random Forest</td>
<td>Captures nonlinear feature interactions</td>
</tr>

<tr>
<td>XGBoost</td>
<td>High-performance gradient boosting model</td>
</tr>

</table>

<hr>

<h2>📊 Evaluation Metrics</h2>

<h3>Predictive Performance</h3>

<ul>
  <li>Matthews Correlation Coefficient (MCC)</li>
</ul>

<h3>Environmental Metrics</h3>

<ul>
  <li>Energy Consumption (Wh)</li>
  <li>CO₂ Emissions (gCO₂eq)</li>
  <li>Execution Time (seconds)</li>
</ul>

<p>
All environmental metrics were measured using <b>CodeCarbon</b>.
</p>

<hr>

<h2>🌿 Green Computing Optimizations</h2>

<h3>Feature Pruning</h3>

<ul>
  <li>Removed low-importance features</li>
  <li>Reduced matrix dimensionality</li>
</ul>

<h3>Model Pruning</h3>

<ul>
  <li>Limited Random Forest depth and tree growth</li>
  <li>Constrained XGBoost complexity</li>
</ul>

<h3>Quantization</h3>

<ul>
  <li>float64 → float32 conversion</li>
  <li>Lower memory usage</li>
  <li>Reduced CPU workload</li>
</ul>

<h3>Computation-Aware Training</h3>

<ul>
  <li>Reduced estimator counts</li>
  <li>Histogram-based XGBoost</li>
  <li>Efficient Logistic Regression solver</li>
</ul>

<h3>Hardware-Aware Efficiency</h3>

<ul>
  <li>Single-core execution (n_jobs=1)</li>
  <li>Reduced thread-management overhead</li>
</ul>

<h3>Metric Streamlining</h3>

<ul>
  <li>MCC-only evaluation inside holdout loops</li>
  <li>Removed unnecessary metric calculations</li>
</ul>

<hr>

<h2>📈 Main Results</h2>

<table>
<tr>
<th>Metric</th>
<th>Baseline</th>
<th>Green Version</th>
<th>Improvement</th>
</tr>

<tr>
<td>Energy Consumption</td>
<td>3.97 Wh</td>
<td>2.05 Wh</td>
<td>▼ 48.4%</td>
</tr>

<tr>
<td>Execution Time</td>
<td>272.2 sec</td>
<td>140.8 sec</td>
<td>▼ 48.3%</td>
</tr>

</table>

<p>
The optimized pipeline significantly reduced computational requirements while maintaining competitive MCC performance.
</p>

<hr>

<h2>🐍 Python vs R Comparison</h2>

<table>
<tr>
<th>Model</th>
<th>Most Efficient Language</th>
</tr>

<tr>
<td>Random Forest</td>
<td>R</td>
</tr>

<tr>
<td>Logistic Regression</td>
<td>Comparable</td>
</tr>

<tr>
<td>XGBoost</td>
<td>Python</td>
</tr>

</table>

<hr>

<h2>🛠 Technologies</h2>

<p>
Python • R • Scikit-Learn • XGBoost • Pandas • CodeCarbon • Google Colab
</p>

<hr>

<h2>📂 Repository Structure</h2>

<pre>
GreenEHR/
│
├── data/
├── notebooks/
├── results/
├── figures/
├── README.md
└── requirements.txt
</pre>

<hr>

<h2>🎯 Key Takeaway</h2>

<p>
This project demonstrates that machine learning systems can be optimized not only for predictive accuracy but also for environmental sustainability. By applying Green Computing principles, substantial reductions in energy consumption and runtime can be achieved without sacrificing model quality.
</p>

<hr>

<h2>📚 Reference</h2>

<p>
CodeCarbon Contributors (2025). CodeCarbon: Track and reduce the carbon footprint of machine learning models.
</p>

<p align="center">
🌱 <b>Building Sustainable AI for Healthcare</b>
</p>
