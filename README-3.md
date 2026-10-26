# Phishing URL Detector

**Author:** Sadhana
**Program:** IBM SkillsBuild Cyber Security 2026 (BharatCares)

## Project Description
A beginner-friendly machine learning project that classifies a URL as **legitimate** or **phishing**
using only features extracted from the URL text (length, IP address as host, `@` symbol, hyphens,
suspicious keywords, HTTPS usage, risky TLDs, etc.). The tool never opens the link, so it is safe to run.

## Dataset
The notebook generates a labelled synthetic dataset (1,200 URLs, 50% legitimate / 50% phishing) so it runs
with no downloads. To train on real data, use the public UCI Phishing Websites dataset:
<https://archive.ics.uci.edu/dataset/327/phishing+websites>
or any CSV with columns `url` and `label` (0 = legitimate, 1 = phishing).

## Technologies Used
- Python 3.9+
- pandas, NumPy
- scikit-learn (Random Forest classifier)
- matplotlib
- Jupyter Notebook

## Setup and Run
```bash
pip install -r requirements.txt
jupyter notebook Sadhana_PhishingURLDetector.ipynb
```
Run all cells from top to bottom (Cell > Run All). In the last section, call `check_url("<any url>")`
to test your own links.

## Key Information
- Model: Random Forest (150 trees), 75/25 train-test split
- Result on the synthetic test set: ~100% accuracy (expected, because the synthetic data is clean;
  real-world accuracy will be lower)
- Limitations: synthetic data, URL-text features only (no WHOIS, domain age, or page content)
- Future work: train on real datasets, add domain-age features, build a browser extension

## Files
| File | Purpose |
|------|---------|
| `Sadhana_PhishingURLDetector.ipynb` | Complete project code |
| `requirements.txt` | Python dependencies |
| `Sadhana_ProjectReport.docx` | Project documentation |
| `README.md` | This file |
