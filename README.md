# US Securities Market Analysis: How Different Markets Behave and Connect(2019-2021)

**Author:** Emma Nagy  
**Date:** September 2025  
**Data Source:** SIFMA & FRED (2019-2021)

[![View Notebook](https://img.shields.io/badge/View-Notebook-orange?logo=jupyter)](https://nbviewer.org/github/enagy827/understanding-US-securities-markets/blob/main/US_Securities_Market_Analysis.ipynb)
[![PDF Report](https://img.shields.io/badge/Download-PDF%20Report-red?logo=adobe)](report/Portfolio_Project_3__Understanding_US_Securities_Markets.pdf)

---

## 📊 Project Overview

This project analyzes trading volumes, issuance patterns, and macroeconomic relationships across seven major US securities markets during 2019-2021, a period encompassing both normal conditions and the COVID-19 crisis. The analysis reveals that markets are fundamentally heterogeneous—not just different in size, but responding to economic conditions through distinct mechanisms.

---

## 🔍 Key Findings

**Markets Are Fundamentally Different**: Market heterogeneity runs deeper than size differences. Equity trading surges when interest rates fall (correlation: -0.803 with Federal Funds rate), certain repo segments move in the opposite direction (+0.767), while Treasury markets remain relatively stable (-0.026).

**Different Levers Pull Different Markets**: Monetary policy powerfully affects equity markets and repo funding, but barely touches Treasuries and shows weak effects on corporate bonds. Credit stress drives corporate bond trading activity (0.581 correlation with high yield spreads) but doesn't significantly deter issuance (0.011).

**Negative Correlations Create Natural Hedges**: Equity Trading and GCF Repo show strong negative correlation (-0.639), suggesting natural portfolio diversification opportunities. These relationships represent real structural offsets in financial intermediation.

**Market Plumbing Matters**: Repo markets handle $2-4 trillion monthly yet showed surprising segmentation—the three major repo types behave almost independently (correlations 0.030-0.434) despite serving similar functions.

**Primary and Secondary Markets Differ**: Companies strategically time bond issuance to interest rate levels (-0.626 correlation) but continue issuing during credit stress when secondary trading is turbulent, revealing resilience in primary markets.

---

## 📁 Repository Contents

```
us-securities-market-analysis/
├── outputs/
│   └── figures/                                 # All 95 visualizations (PNG)
│       ├── figure_001.png                       # Treasury time series
│       ├── figure_002.png                       # Treasury vs Fed Funds
│       ├── ...
│       ├── figure_051.png                       # Cross-market correlation heatmap
│       └── figure_095.png                       # Corporate issuance vs HY spread
├── report/
│   ├── US_Securities_Market_Analysis.pdf        # LaTeX-compiled report
├──  README.md                                    # This file
└── US_Securities_Market_Analysis.ipynb          # Complete Jupyter notebook with analysis
└── requirements.txt                             # Python dependencies
```

---

## 🚀 How to Run This Analysis

### View Online (No Installation Required)
**[View the interactive notebook on nbviewer →](https://nbviewer.org/github/enagy827/understanding-US-securities-markets/blob/main/US_Securities_Market_Analysis.ipynb)**

### Run Locally

#### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Excel files from SIFMA 

#### Option 1: Using Git
```bash
# Clone the repository
git clone https://github.com/enagy827/us-securities-market-analysis.git
cd us-securities-market-analysis

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook

# Open US_Securities_Market_Analysis.ipynb and run all cells
```

#### Option 2: Download ZIP
1. Click the green "Code" button at the top of this repository
2. Select "Download ZIP"
3. Extract the files to your desired location
4. Open terminal/command prompt and navigate to the extracted folder
5. Install dependencies: `pip install -r requirements.txt`
6. Launch Jupyter: `jupyter notebook`
7. Open `US_Securities_Market_Analysis.ipynb` and run the cells

---

## 🛠️ Methodology

### Markets Analyzed

**Trading Volume Analysis:**
1. US Treasury Securities
2. US Repo Markets (Primary Dealer, GCF, Triparty)
3. US Equity Markets (Issuance and Trading)
4. US Fixed Income Securities
5. US Structured Finance (ABS and MBS)
6. US Agency Debt
7. US Corporate Bonds

**Issuance and Outstanding Analysis:**
1. US Marketable Treasury Securities
2. US Mortgage-Backed Securities (MBS)
3. US Asset-Backed Securities (ABS)
4. US Fixed Income Securities
5. US Asset-Backed Commercial Paper (ABCP)
6. US Municipal Bonds
7. US Corporate Bonds

### Data Sources

**SIFMA (Securities Industry and Financial Markets Association)**
- Trading volumes and issuance data
- Coverage: 2019-2021 (monthly and annual frequency)
- Source: https://www.sifma.org/resources/research/statistics/

**FRED (Federal Reserve Economic Data)**
- Federal Funds Rate (monthly)
- Consumer Price Index Year-over-Year (monthly)
- High Yield Spread / Option-Adjusted Spread (monthly)
- Source: https://fred.stlouisfed.org/

### Analytical Approach

**Descriptive Statistics:**
- Mean, median, standard deviation, coefficient of variation
- Time trends via correlation with sequential dates
- Identification of structural breaks during COVID-19

**Correlation Analysis:**
- Pearson correlations between trading volumes and macroeconomic indicators
- Within-market correlations (e.g., Treasury securities by tenor)
- Cross-market correlations (total trading volumes across markets)

**Visual Analysis:**
- Time series plots showing market evolution
- Dual-axis plots comparing volumes with macro indicators
- Correlation heatmaps for within-market and cross-market relationships

---

## 💻 Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib & Seaborn**: Visualizations
- **Jupyter**: Reproducible analysis environment
- **LaTeX**: Professional report generation

---

## 🎯 Key Insights

This analysis challenges conventional assumptions about market behavior:

**Markets Don't Move Uniformly** — During crises, different markets respond through distinct channels: equity markets react to monetary policy, corporate bonds to credit stress, and Treasuries remain relatively stable.

**Size ≠ Sensitivity** — Repo markets handle trillions of dollars monthly but showed weaker macro correlations than smaller equity markets. Market size and sensitivity are orthogonal dimensions.

**Crisis Validated Structural Relationships** — COVID-19 provided a natural experiment. Markets responded exactly as their correlation patterns predicted: equity trading surged after rate cuts, corporate bond trading spiked with widening spreads, Treasury issuance exploded.

**Diversification Opportunities Exist** — Negative correlations between equity trading and certain repo segments (-0.639) provide genuine hedging opportunities beyond traditional asset class diversification.

**Primary Markets Are Resilient** — While secondary market corporate bond trading responds strongly to credit stress, issuance continues largely unaffected, suggesting primary markets are more robust than secondary market volatility implies.

### Implications

**For Traders:** Portfolio construction should exploit correlation structure, not just asset class labels. Markets with correlations below 0.3 or negative provide meaningful diversification.

**For Risk Managers:** Stress testing must account for heterogeneous transmission channels. Treasury-Fixed Income coupling (0.954) will amplify shocks, while Equity-Repo GCF divergence (-0.639) provides natural offsets.

**For Policymakers:** Comprehensive crisis response requires multiple targeted tools. Rate cuts reach equity markets (-0.803) but not corporate bonds (-0.134), explaining why the Fed needed credit facilities alongside monetary easing.

**For Researchers:** The diversity of market behaviors demonstrates that "the market" is not a useful analytical unit. Each segment requires separate analysis given distinct participants, functions, and macro sensitivities.

---

## 📄 Technical Report

For detailed methodology, statistical analysis, comprehensive discussion, and policy implications, see the complete technical report:

**[Download PDF Report →](report/Portfolio_Project_3__Understanding_US_Securities_Markets.pdf)**

The report includes:
- Comprehensive literature review and theoretical framework
- Detailed descriptive statistics for all markets
- Complete correlation analysis with statistical significance tests
- Discussion of COVID-19 as a natural experiment
- Policy implications for crisis response design
- Limitations and directions for future research

---

## 📊 Data Access

All data used in this analysis is publicly available:

**SIFMA Statistics**
- Navigate to: https://www.sifma.org/resources/research/statistics/
- Download Excel files for each market (Treasury, Repo, Corporate Bonds, etc.)
- Data is freely available; SIFMA updates quarterly

**FRED Economic Data**
- Access at: https://fred.stlouisfed.org/
- Search for: "Federal Funds Rate", "CPI YoY", "High Yield Spread"
- Download as CSV and import into analysis

---

## 📚 Project Context

This project demonstrates proficiency in:

- **Financial market analysis**: Understanding of market microstructure, liquidity, and interconnections
- **Quantitative analysis**: Statistical correlation analysis, time series analysis, panel data methods
- **Data visualization**: Clear communication of complex relationships through multiple plot types
- **Economic interpretation**: Translating statistical findings into economic mechanisms and policy insights
- **Technical communication**: Professional report writing for academic and practitioner audiences

### Research Questions Addressed

1. **How do different securities markets respond to macroeconomic conditions?**
   - Finding: Dramatically different sensitivities, from -0.803 to +0.767 for Federal Funds rate

2. **Do markets move together or independently?**
   - Finding: Wide range from perfect correlation (0.954) to strong negative correlation (-0.639)

3. **How do primary and secondary markets differ?**
   - Finding: Issuance responds to interest rates, trading responds to credit stress—distinct mechanisms

4. **Did COVID-19 change market relationships?**
   - Finding: Correlations held under extreme stress, validating their structural nature

5. **What are the implications for portfolio construction and policy design?**
   - Finding: Heterogeneity requires targeted tools and correlation-based diversification strategies

---

## 🔗 Contact

For questions, collaboration opportunities, or to discuss this research:

- **Portfolio**: [[emmanagy.net](https://www.emmanagy.net/)]
- **LinkedIn**: [[Emma Nagy](https://www.linkedin.com/in/emma-nagy/)]

---

## 📝 Citation

If you use this analysis or methodology in your research, please cite:

```
Nagy, E. (2025). US Securities Market Analysis: Market Heterogeneity and Crisis Response (2019-2021). 
Analysis of SIFMA and FRED data examining structural differences across securities markets.
https://github.com/enagy827/us-securities-market-analysis
```

---

## 📜 License

This project is available for educational and research purposes. Please credit appropriately if you use this work.

---

**Last updated:** January 2026
