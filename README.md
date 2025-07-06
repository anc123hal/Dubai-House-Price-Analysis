# 📊 Dubai House Price Analysis

**Description**  
A Power BI dashboard analyzing Dubai’s residential property market—examining price trends, listing categories, property size, age, and more to provide clear insights for investors and stakeholders.

---

## 🧭 Project Overview

- **Objective**  
  - Analyze historical real estate data for Dubai to extract insights on pricing, size, property age, and listing categories.  
  - Showcase KPIs: average price, average size, price per square foot, and maximum price.  
  - Enable dynamic filtering (by bedrooms and listing category) for exploratory analysis.

- **Key Questions**  
  - How does property price change with bedroom count and year built?  
  - How are listing categories (Budget, Mid‑Range, High‑End) distributed?  
  - What relationship exists between price and size across categories?

---

## 🛠️ Data & Cleaning

1. **Data Source**: Raw CSV file with fields such as Price, SquareFeet, YearBuilt, Bedrooms, ListingCategory, etc.  
2. **Cleaning Steps**:  
   - Removed duplicate rows.  
   - Dropped or handled nulls in critical fields.  
3. **Custom Columns**:  
   - `PricePerSqFt = Price / SquareFeet`  
   - `PropertyAge = CurrentYear – YearBuilt`  
   - Cleaned up `ListingCategory` values (Budget, Mid‑Range, High‑End)

---

## 📐 Data Modeling

- Used Power BI data types: Decimal (Price, Size), Whole Number (Bedrooms, YearBuilt, PropertyAge), Text (ListingCategory).  
- No additional relationships; all data resides in a single table.

---

## 📊 DAX Measures

- **AveragePrice** = AVERAGE(Price)  
- **AverageSize** = AVERAGE(SquareFeet)  
- **AvgPricePerSqFt** = AVERAGE(PricePerSqFt)  
- **MaxPrice** = MAX(Price)

These metrics are displayed via KPI cards in the report.

---

## 📈 Dashboard Visuals

- **Slicers**: `Bedrooms`, `ListingCategory`  
- **Cards**: Average Price, Average Size, Price/SqFt, Maximum Price  
- **Visualizations**:  
  - *Column Chart*: Avg Price by Bedrooms  
  - *Line Chart*: Avg Price by YearBuilt  
  - *Stacked Bar Chart*: Counts of ListingCategories by Neighborhood  
  - *Pie Chart*: Distribution of Listing Categories  
  - *Scatter Chart*: Size vs Price (color-coded by category)

*(Add your screenshots in the `media/` folder and link them here.)*

---

## 🔍 Insights

- Prices rise with more bedrooms.  
- Average prices hover around AED 220–230K historically.  
- Mid‑Range listings dominate the dataset.  
- Strong size–price correlation across categories.  
- Urban areas have higher frequencies of Mid‑Range and High‑End listings.

---

## ✅ Recommendations & Next Steps

- Enhance geospatial resolution (e.g., district-level breakdown).  
- Add trend forecasting or regression lines.  
- Integrate external data (e.g., interest rates, development projects).  
- Introduce drill‑through functionality for detailed analysis.  
- Publish to Power BI Service for scheduled refresh and sharing.

---

## 💻 Technical Details

- **Tool**: Power BI Desktop (latest version)  
- **Data Refresh**: Manual from CSV  
- **Transformations**: Power Query  
- **Modeling**: DAX measures & calculated columns  
- **Delivery**: Local PBIX file; optionally publishable

---

## 📁 File Structure

