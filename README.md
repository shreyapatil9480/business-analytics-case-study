[![Python CI](https://github.com/shreyapatil9480/business-analytics-case-study/actions/workflows/python-ci.yml/badge.svg)](https://github.com/shreyapatil9480/business-analytics-case-study/actions/workflows/python-ci.yml)
![Python](https://img.shields.io/badge/python-3.11-blue)
![pytest](https://img.shields.io/badge/tested%20with-pytest-0A9EDC)

# Business Analytics Case Study

Which programs are at funding risk?

**Stakeholder:** Program Director

## Key Insights

- Three or more missed milestones precede at-risk funding reviews.
- Burn rate above 1.15x plan correlates with stakeholder escalation.
- Programs with 8+ stakeholders recover slower from milestone slips.

## Dataset

Primary file: `data/program_funding.csv`  
Target variable: `at_risk`

## Getting Started

```bash
pip install -r requirements.txt
jupyter notebook notebooks/eda.ipynb
```



## Testing

```bash
pip install -r requirements.txt
pytest tests/ --cov=src
```

## Next Steps

Automate SQL exports into a weekly stakeholder report.

---
*Analytics portfolio project — 2025-08*

<!-- build 4 -->

### Implemented

```bash
pip install -r requirements.txt
python scripts/weekly_report.py
```
