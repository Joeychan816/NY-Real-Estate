# 🏙️ New York Real Estate Analysis

This project explores and analyzes real estate listings across New York City using a dataset of property listings. The analysis focuses on price trends, property types, borough distribution, and relationships between key features such as square footage, number of bedrooms/bathrooms, and location.

## 📂 Dataset

- **Source:** Uploaded CSV file `NY-House-Dataset.csv`
- **Fields Used:** `BROKERTITLE`, `TYPE`, `PRICE`, `BEDS`, `BATH`, `PROPERTYSQFT`, `ADDRESS`, `STATE`

## 🧼 Data Cleaning and Preparation

- Removed unnecessary columns
- Cleaned `BROKERTITLE` column by removing "Brokered by"
- Dropped rows where `PROPERTYSQFT` equals `2184.207862` (common outlier)
- Extracted ZIP codes and created a new column
- Classified properties into NYC boroughs based on ZIP code ranges
- Verified uniqueness of property types and borough classifications

## 📊 Exploratory Data Analysis (EDA)

- Summary statistics (`count`, `mean`, `min`, `max`, etc.) by **borough** and **property type**
- Visualizations:
  - Average and max prices per **borough** and **property type**
  - Price trends by **bedrooms** and **bathrooms**
  - Histograms and boxplots to detect price distribution and outliers
  - Scatter plots comparing **price** vs. **square footage**
  - Geographic scatterplot of **latitude vs longitude**

## 📈 Statistical Modeling

- **Linear Regression** between `PRICE` and `PROPERTYSQFT` using `scipy.stats.linregress`
- **Multiple Linear Regression** to analyze the impact of `BEDS`, `BATH`, and `PROPERTYSQFT` on `PRICE` using `statsmodels`

## 🗄️ Database Integration

- Exported cleaned data to a SQLite database (`NYC_real_estate.db`)
- Sample SQL queries:
  - View all listings
  - Filter listings with `PRICE > $100M`
  - View most expensive `Condo for sale` listings

## 📍 Geospatial Visualization

- Scatterplot of listings by **latitude and longitude** to observe geographic distribution

---

## 🚀 How to Use

1. Clone the repo or open the notebook in Google Colab
2. Upload `NY-House-Dataset.csv` when prompted
3. Execute cells to perform cleaning, analysis, and visualization

---

## 🛠️ Technologies Used

- Python (Pandas, NumPy, Matplotlib, Statsmodels, SciPy)
- SQLite (via `sqlite3` and `pandas`)
- Google Colab (for interactive analysis)

---

## 📈 Key Insights

- Manhattan has the highest property prices overall
- Condos and multi-family homes tend to be the most expensive types
- Square footage has a moderate correlation with price
- Outliers significantly impact the price distribution

---

Feel free to contribute or fork this project for deeper NYC housing market exploration!

---
