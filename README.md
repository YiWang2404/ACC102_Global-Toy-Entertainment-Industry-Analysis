# ACC102_Global-Toy-Entertainment-Industry-Analysis
As an accounting student, this analysis examines the revenue, profitability, and growth of the global toy &amp; entertainment industry. Using real financial data, I benchmark Pop Mart against peers to identify performance trends, aiming to provide investors and retail analysts with clear, data-driven financial insights.
# Global Toy & Entertainment Industry Analysis (2021-2025)

## Problem Statement

This project analyzes the financial performance of major toy and entertainment companies from 2021 to 2025, focusing on understanding:
- How different industry segments (Traditional Toys, Collectibles, Gaming & Toys, Media & Entertainment) performed during and after the pandemic
- Which companies demonstrated resilience and growth
- Key financial metrics including revenue trends, profit margins, and return on assets (ROA)

## Data Source

The analysis uses **WRDS (Wharton Research Data Services)** data from:
- **Compustat (funda/g_funda tables)** - Annual financial statements
- SIC codes for industry classification:
  - `3944` - Toys & Games
  - `7812` - Motion Picture/Video Production  
  - `7993` - Amusement/Recreation Services

## Companies Analyzed

| Company | Category | GVKey |
|---------|----------|-------|
| Disney | Media & Entertainment | 003980 |
| Bandai Namco | Gaming & Toys | 204009 |
| Hasbro | Traditional Toys | 005518 |
| Mattel | Traditional Toys | 007116 |
| Spin Master | Innovative Toys | 025507 |
| Funko | Collectibles | 032528 |
| JAKKS Pacific | Traditional Toys | 062745 |
| Pop Mart | Collectibles | 345680 |
| Aldeyra Therapeutics | Control Group | 020018 |

## Methodology

1. **Data Extraction**: Queried Compustat database via WRDS for financial data (revenue, net income, assets, employees)
2. **Data Cleaning**: Handled missing values, standardized currency (USD), calculated derived metrics
3. **Analysis**: 
   - Revenue trend analysis (2021-2025)
   - Profitability metrics (profit margin = net income/revenue)
   - ROA analysis (net income/total assets)
   - Year-over-year growth calculations
   - Category-based performance segmentation

## Key Findings

### Top Performers (2025)
- **Revenue Leader**: Disney ($91.4B)
- **Profitability Leader**: Pop Mart (19.2% margin)
- **Efficiency Leader**: Bandai Namco (15.3% ROA)

### Industry Trends
- **Media & Entertainment** (Disney) shows steady growth with strong profitability recovery (13.1% margin in 2025)
- **Traditional Toys** (Hasbro, Mattel, JAKKS) experienced post-pandemic normalization with mixed performance
- **Collectibles** (Pop Mart, Funko) shows high margins but volatility in revenue
- **Gaming & Toys** (Bandai Namco) demonstrates consistent double-digit profitability

### Areas of Concern
- Some traditional toy companies experienced negative margins during 2023
- Revenue volatility in collectibles segment

## How to Run

### Prerequisites
```
pip install pandas numpy matplotlib seaborn plotly wrds
```

### Setup
1. **WRDS Account Required**: You need a WRDS account with Compustat access
2. Update the username in cell 263:
   ```python
   username = "your_username"
   ```

### Execution
Run the Jupyter notebook cells sequentially:
1. **Cells 262-273**: Connect to WRDS and explore available data
2. **Cells 274-293**: Query and merge financial data
3. **Cells 294-300**: Data processing and metric calculation
4. **Cells 301-325**: Visualization and analysis

### Output Files
The notebook generates:
- `viz_1_revenue_trends.png` - Revenue trends for top 5 companies
- `viz_2_profitability_ranking.png` - Latest year profitability comparison
- `pie_chart_revenue_distribution.png` - Market share visualization
- `viz_4_category_trends.png` - Category-level performance
- `interactive_dashboard_filled.html` - Interactive Plotly dashboard
- `industry_summary.csv` - Summary statistics table
- `toy_industry_data.csv` - Raw processed data

## Notes
- Missing values in global data (Bandai Namco, Sanbio, Pop Mart) are noted in the analysis
- Aldeyra Therapeutics serves as a control group (pharmaceutical company, not in toy industry)
- Financial figures are in millions of USD unless otherwise noted
