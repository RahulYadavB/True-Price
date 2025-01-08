# Design Plan: Price Estimator Tool

## Overview
This tool estimates the fair price and boost price for products on marketplaces.

## User Workflow
1. User inputs product details.
2. Tool validates inputs.
3. Fair price and boost price are calculated.
4. Results are displayed to the user.

## Input-Output Details
### Inputs
- **Product Category** (e.g., Furniture, Electronics)
- **Condition**: New or Used
- **Original Price**: $ value
- **Product Age**: Time since purchase

### Outputs
- **Estimated Fair Price**
- **Boost Price**

## Core Logic
### Price Estimation
- Formula: `Fair Price = Original Price × (1 - Depreciation × Age)`
- Depreciation rates by category:
  - Furniture: 15% per year
  - Electronics: 20% per year

### Boost Price Calculation
- Formula: `Boost Price = Fair Price × 5%`

## Data Handling
- Static data for categories and depreciation rates.

## Technology Stack
- Frontend: HTML, CSS, JavaScript
- Backend: Python Flask
- Data: CSV file for initial category rates

## Future Enhancements
- Automated marketplace data fetching.
- Feedback for price adjustment based on trends.
