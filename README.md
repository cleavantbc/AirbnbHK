# Hong Kong Airbnb Market Analysis

## Overview
Brief 2-3 sentence summary: what data, what question, what tools.

## Tools Used
- SQL Server / SSMS
- Python (pandas, sqlalchemy) for ETL
- Power BI for visualization

## Data Source
- Dataset: Airbnb Listings & Reviews (Kaggle)
- Filtered to Hong Kong listings only (7,087 rows)

## Process

### 1. Data Loading & Cleaning
- Loaded CSV via Python, encountered encoding issues (mixed cp1252/UTF-8 
  from source file) causing garbled text in listing names
- Resolved by reading with cp1252 + error replacement, then stripping 
  non-ASCII characters from text fields
- Pushed to SQL Server using SQLAlchemy with NVARCHAR typing to preserve 
  Unicode-safe columns

### 2. Data Quality Checks
- Found one clear data error (listing priced at $1) — removed
- Identified legitimate price extremes: "bedspace" rentals (~$65-80) 
  reflecting Hong Kong's tight housing market, and luxury villas 
  ($20,000+) for large groups — kept both as real market segments

### 3. Analysis
- [Link to analysis_queries.sql]
- Key questions explored: pricing by neighbourhood, room type 
  distribution, superhost impact on pricing/ratings

### 4. Dashboard
- [Screenshot or link to Power BI dashboard]

## Key Findings
- (Fill in once you've finished the analysis — 3-4 bullet insights)
