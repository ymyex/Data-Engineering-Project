# TTTC3213 ETL Project: Laptop E-Commerce Analysis

**Analysis of Laptop Price Distribution and Brand Popularity in E-Commerce Market**

[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-Educational-green.svg)]()
[![Status](https://img.shields.io/badge/Status-Complete-success.svg)]()

## Project Overview

This project implements a complete **ETL (Extract, Transform, Load)** pipeline to analyze laptop pricing and brand popularity in the e-commerce market. We scraped, cleaned, and analyzed **116 laptop products** from an online retailer to uncover valuable market insights.

### Project Goal

To analyze **laptop price distribution and brand popularity** by:
- Extracting product data from e-commerce websites
- Cleaning and transforming raw data
- Generating insights about pricing strategies and market positioning
- Understanding the relationship between price and customer satisfaction

### Data Source

- **Website**: [WebScraper.io E-Commerce Test Site](https://webscraper.io/test-sites/e-commerce/allinone/computers/laptops)
- **Legal Status**: Specifically designed for scraping practice and education
- **Records Collected**: 117 initial records → 116 after cleaning

---

## Key Findings

### Market Leadership
- **Acer** dominates with **21.6% market share** (25 products)
- Top 4 brands (Acer, Lenovo, Dell, Asus) control **72.4%** of the market

### Pricing Insights
- **Premium Brand**: Apple ($1,313.64 avg)
- **Budget Option**: Prestigio ($299.00 avg)
- **Market Average**: $907.76

### Customer Satisfaction
- **Highest Rated**: ProBook (4.00/5)
- **Most Engaged**: Lenovo (157 reviews)
- **Market Average**: 2.35/5

### Price-Quality Relationship
- **Correlation**: -0.091 (weak negative)
- **Insight**: Higher prices DON'T guarantee better ratings!
- **Recommendation**: Budget laptops can offer excellent value

---

## Quick Start

### Prerequisites

```bash
# Python 3.11 or higher required
python --version
```

### Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd Data-Engineering-Project

# Install dependencies
pip install -r requirements.txt
```

### Running the Analysis

Open and run the Jupyter notebooks in order:

1. **ETL_Laptop_Analysis.ipynb** - Extract, Transform, and Load data
2. **Data_Analysis.ipynb** - Analyze and generate visualizations

```bash
# Start Jupyter Notebook
jupyter notebook
```

### Expected Output

After running the notebooks, you'll find in the `output/` directory:
- `raw_data.csv` - Original scraped data (117 records)
- `laptops_clean_data.csv` - Cleaned dataset (116 records)
- 5 comprehensive visualization PNG files

---

## Project Structure

```
Data-Engineering-Project/
│
├── ETL_Laptop_Analysis.ipynb      # Main ETL pipeline notebook
├── Data_Analysis.ipynb            # Analysis & visualizations notebook
├── requirements.txt               # Python dependencies
├── README.md                      # This file
├── Report.md                      # Project report (Markdown)
├── final_report.pdf               # Project report (PDF)
│
└── output/                        # Generated files
    ├── raw_data.csv               # Original data
    ├── laptops_clean_data.csv     # Cleaned data
    ├── data_cleaning_comparison.png
    ├── price_distribution_analysis.png
    ├── brand_popularity_analysis.png
    ├── rating_price_correlation.png
    └── comprehensive_report_dashboard.png
```

---

## ETL Pipeline Details

### 1. **EXTRACT** - Data Scraping

**Attributes Collected** (6 total):
- Product Name
- Price (USD)
- Description
- Customer Rating (1-5 stars)
- Number of Reviews
- Extraction Timestamp

**Technology Stack**:
- `BeautifulSoup4` - HTML parsing
- `Requests` - HTTP client
- `Pandas` - Data handling

### 2. **TRANSFORM** - Data Cleaning

**6 Cleaning Operations**:
1. **Duplicate Removal** - Removed 1 duplicate record
2. **Missing Value Handling** - Filled all missing values
3. **Price Standardization** - Converted "$1,234.56" → 1234.56
4. **Brand Extraction** - Extracted 16 unique brands
5. **Rating Normalization** - Standardized 1-5 star ratings
6. **Review Count Cleaning** - Extracted numeric counts

### 3. **LOAD** - Data Storage

- **Format**: CSV (readable by Pandas)
- **Output**: `laptops_clean_data.csv`
- **Records**: 116 cleaned records
- **Size**: ~18 KB

---

## Visualizations

Our analysis generated 5 comprehensive visualizations:

### 1. Data Cleaning Comparison
Shows before/after metrics demonstrating cleaning effectiveness

### 2. Price Distribution Analysis
- Overall price histogram
- Brand-wise price comparison
- Price ranges by brand
- Box plots showing distribution

### 3. Brand Popularity Analysis
- Market share pie chart
- Product count by brand
- Total reviews by brand
- Average ratings by brand

### 4. Rating vs Price Correlation
- Scatter plot with trend line
- Rating distribution by price range
- Correlation coefficient analysis

### 5. Comprehensive Dashboard
Integrated view combining all key metrics and insights

---

## Technologies Used

| Technology | Version | Purpose |
|-----------|---------|---------|
| **Python** | 3.11 | Core programming language |
| **BeautifulSoup4** | 4.12.2 | HTML parsing |
| **Requests** | 2.31.0 | HTTP requests |
| **Pandas** | 2.1.4 | Data manipulation |
| **Matplotlib** | 3.8.2 | Visualization |
| **Seaborn** | 0.13.0 | Statistical plots |
| **NumPy** | 1.26.2 | Numerical computing |

---

## Dataset Statistics

| Metric | Value |
|--------|-------|
| **Total Products** | 116 laptops |
| **Unique Brands** | 16 brands |
| **Price Range** | $295.99 - $1,799.00 |
| **Average Price** | $907.76 |
| **Total Reviews** | 798 reviews |
| **Average Rating** | 2.35 / 5.0 |
| **Data Completeness** | 100% (no missing values) |

---

## Business Insights

### For Consumers:
1. Don't assume higher price = higher quality
2. Budget brands offer competitive value
3. Read reviews - more important than price

### For Retailers:
1. Stock top 4 brands (72% of demand)
2. Highlight budget options (good satisfaction)
3. Focus on brands with high engagement

### For Manufacturers:
1. Address low overall satisfaction (2.35/5)
2. Premium pricing needs quality justification
3. Mid-range segment needs improvement

---

## Academic Information

**Course**: TTTC3213 - Data Engineering
**Project Type**: Group Project (30% of final grade)
**Components**:
- Data Scraping (100+ records, 6+ attributes)
- Data Cleaning (6 operations)
- Data Visualization (5+ charts)
- Analysis Report (3,500 words)
- Clean CSV Output

---

## Documentation

For the complete project report including detailed methodology, code snippets, and analysis:
- [Full Report (PDF)](final_report.pdf)

---

## Contributing

This is an academic project. For educational purposes:
1. Fork the repository
2. Modify for your own analysis
3. Remember to cite if using our methodology

---

## Legal & Ethical Considerations

- **Legal Scraping**: Website explicitly allows scraping
- **Rate Limiting**: Responsible request patterns
- **Data Usage**: Academic/educational purposes only
- **Attribution**: Proper source citation

---

## Contact

For questions about this project:
- Open an issue on GitHub
- Contact project team members

---

## License

This project is for educational purposes as part of TTTC3213 coursework.

---

## Acknowledgments

- **WebScraper.io** for providing a legal and safe testing environment
- **Course Instructors** for project guidance
- **Python Community** for excellent data science libraries

