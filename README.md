# monitor.openbankruptcyproject.org

Attorney Performance Monitor -- a public surveillance dashboard for the Open Bankruptcy Project.

## Overview

Static GitHub Pages site that displays bankruptcy attorney monitoring data:
- Attorney watchlist with dismissal/discharge rates, court coverage, and flag levels
- District-level case outcome summaries with national average comparison
- Client-side search, filtering, and sortable tables
- CSS-only bar chart of highest dismissal rates
- Zero external dependencies -- pure HTML/CSS/JS

## Data Pipeline

1. Run `python pacer/scripts/export_dashboard_json.py` from the repo root
2. Reads from `bankruptcy_master.db` (220K+ cases, 85 districts)
3. Outputs `data/dashboard.json`
4. `index.html` fetches the JSON at load time

## Deployment

GitHub Pages with custom domain. CNAME: `monitor.openbankruptcyproject.org`

## License

Data sourced from public federal court records (PACER / FJC IDB).
Open Bankruptcy Project is a 501(c)(3) nonprofit (EIN 41-5159631).
