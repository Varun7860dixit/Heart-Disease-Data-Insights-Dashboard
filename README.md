<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Heart Disease Data Insights — README</title>
  <style>
    body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; line-height:1.6; color:#222; padding:24px; max-width:1000px; margin:0 auto; background:#fafafa; }
    header { display:flex; align-items:center; gap:18px; margin-bottom:18px; }
    header img { width:84px; height:84px; object-fit:cover; border-radius:12px; box-shadow:0 6px 18px rgba(0,0,0,0.08); }
    h1 { margin:0; color:#e33b2f; }
    h2 { margin-top:28px; color:#333; }
    p.lead { margin:8px 0 18px; color:#444; }
    .badges img { height:20px; margin-right:8px; vertical-align:middle; }
    .grid { display:grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap:16px; }
    .card { background:#fff; padding:14px; border-radius:12px; box-shadow:0 6px 18px rgba(0,0,0,0.06); }
    img.screenshot { width:100%; border-radius:10px; box-shadow:0 8px 20px rgba(0,0,0,0.06); }
    pre { background:#0f1724; color:#e6eef8; padding:12px; border-radius:8px; overflow:auto; }
    code { background:#f3f4f6; padding:2px 6px; border-radius:6px; font-family:monospace; }
    ul { margin-top:6px; }
    footer { margin-top:28px; color:#666; font-size:0.95rem; }
    .highlight { background:#ffefee; border-left:4px solid #ff6a4d; padding:10px 12px; border-radius:6px; }
    .meta { display:flex; gap:12px; flex-wrap:wrap; align-items:center; margin-top:8px; }
    .meta b { color:#333; }
  </style>
</head>
<body>
  <header>
    <img src="./images/icon_heart.png" alt="Heart Icon (place in images/)">
    <div>
      <h1>Heart Disease Data Insights</h1>
      <div class="meta">
        <span>Interactive Power BI dashboard for exploring heart disease risk factors and metrics</span>
      </div>
    </div>
  </header>

  <p class="lead">
    This repository contains a Power BI dashboard project that analyzes heart disease data for ~9,500 patients.
    The dashboard highlights population metrics, risk factor distributions, correlations between health indicators,
    and interactive filters to explore subsets of patients (by age, gender, smoking status, and disease status).
  </p>

  <h2>Quick demo / Screenshots</h2>
  <div class="grid">
    <div class="card">
      <h3>Overview</h3>
      <img class="screenshot" src="./images/Overview.png" alt="Overview screenshot">
      <p style="margin-top:8px">Summary metrics, BMI distribution, age-wise case counts and blood pressure trend.</p>
    </div>
    <div class="card">
      <h3>Health Factors</h3>
      <img class="screenshot" src="./images/Health_Factors.png" alt="Health Factors screenshot">
      <p style="margin-top:8px">Charts for alcohol, sugar, stress levels plus cholesterol trends by BP and disease status.</p>
    </div>
    <div class="card">
      <h3>Correlation</h3>
      <img class="screenshot" src="./images/Correlation.png" alt="Correlation heatmap screenshot">
      <p style="margin-top:8px">Correlation heatmap of numeric indicators: Age, BP, BMI, Cholesterol, CRP, Sugar, etc.</p>
    </div>
  </div>

  <h2>Features</h2>
  <ul>
    <li>Interactive Power BI report (.pbix) with multiple pages: Overview, Health Factors, Correlation.</li>
    <li>Key population metrics: total patients, heart disease rate, avg. cholesterol, avg. BMI, high BP rate.</li>
    <li>Distribution charts: BMI categories, age groups, gender comparison, alcohol/sugar/stress levels.</li>
    <li>Correlation heatmap to identify relationships between numeric health variables.</li>
    <li>Filters for Heart Disease status, Gender, Age Group, and Smoking status for on-the-fly exploration.</li>
  </ul>

  <h2>Repository Contents</h2>
  <div class="card">
    <ul>
      <li><code>pro.pbix</code> — Power BI Desktop file (dashboard project)</li>
      <li><code>data/</code> — (optional) cleaned dataset CSV or data dictionary if included</li>
      <li><code>images/</code> — screenshots and icons used in this README (place your exported PNGs here)</li>
      <li><code>README.html</code> — this file</li>
      <li><code>LICENSE</code> — project license</li>
    </ul>
  </div>

  <h2>Data</h2>
  <p>
    The dashboard was built from a de-identified patient dataset containing clinical and lifestyle metrics.
    If you include the raw or cleaned CSV in the <code>data/</code> folder, note any privacy considerations and the data source.
  </p>

  <h2>How to open / view the dashboard</h2>
  <div class="card">
    <ol>
      <li>Download and install <b>Power BI Desktop</b> (Windows) if you don't have it: <code>https://powerbi.microsoft.com/</code></li>
      <li>Clone or download this repo, then open the <code>pro.pbix</code> file with Power BI Desktop.</li>
      <li>Use the left page navigator to switch between <em>Overview</em>, <em>Health Factors</em>, and <em>Correlation</em>.</li>
      <li>Use the slicers on the left pane (Heart Disease, Gender, Age Group, Smoking) to filter visuals interactively.</li>
    </ol>
    <pre><code>git clone https://github.com/yourusername/heart-disease-dashboard.git
cd heart-disease-dashboard
# open pro.pbix in Power BI Desktop</code></pre>
  </div>

  <h2>How it was built</h2>
  <ul>
    <li>Data cleaning & pre-processing: Python / pandas or Power Query (depending on files you include)</li>
    <li>Visuals & report creation: Power BI Desktop (custom visuals / standard charts)</li>
    <li>Design: consistent color theme (coral/soft red), rounded cards, legible annotations and labels</li>
  </ul>

  <h2>Notes & Recommendations</h2>
  <div class="highlight">
    <strong>Note:</strong> The correlation heatmap shows pairwise Pearson correlation for numeric columns — correlations near 0 indicate weak linear relationships.
    Always consult a subject-matter expert when interpreting clinical findings. This dashboard is for exploratory analysis and demonstration purposes only.
  </div>

  <h2>Presentation Tips</h2>
  <ul>
    <li>Start with the Overview page to set the context (population size, overall heart disease rate).</li>
    <li>Use filters live to show how metrics change by age group or gender.</li>
    <li>Demonstrate the correlation heatmap to highlight which numeric indicators move together.</li>
    <li>Finish with actionable insights and suggestions for further analysis (e.g., regression modeling, cohort studies).</li>
  </ul>

  <h2>Troubleshooting</h2>
  <ul>
    <li>If visuals do not render, ensure the dataset is properly loaded in Power BI and column names match the visuals' expected fields.</li>
    <li>Large datasets can slow rendering — consider sampling or using aggregated tables for interactive demos.</li>
  </ul>

  <h2>License</h2>
  <p>
    This project is released under the <b>MIT License</b>. See the <code>LICENSE</code> file for details.
  </p>

  <h2>Contact & Credits</h2>
  <p>
    Author: <strong>Varun Dixit</strong><br>
    Repository: <code>https://github.com/yourusername/heart-disease-dashboard</code><br>
    Email: <code>your-email@example.com</code>
  </p>

  <footer>
    <p>Thanks for checking out this project — feel free to open an issue, suggest improvements, or submit a pull request!</p>
  </footer>
</body>
</html>
