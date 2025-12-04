# Zomato Data Analysis & Exploratory Data Analysis (EDA) Project

## 📊 Project Overview

This project performs comprehensive **Exploratory Data Analysis (EDA)** on Zomato restaurant data to uncover business insights and customer preferences. The analysis leverages Python data manipulation libraries to identify patterns in restaurant types, customer ratings, and spending behaviors.

### Business Objectives
This analysis addresses key business questions:
- What types of restaurants do customers order from the most?
- How do different restaurant categories perform in terms of customer engagement?
- What are the typical ratings and customer spending patterns?
- How do online vs. offline ordering experiences compare?
- Which price range attracts the most couples?

---

## 🎯 Key Findings

### 1. **Restaurant Type Distribution**
- **Majority Category**: Dining restaurants dominate the dataset
- **Customer Preference**: Most customers prefer dining establishments over buffets and cafes

### 2. **Customer Engagement (Votes)**
- Dining restaurants receive the maximum votes from customers
- Clear indication of higher customer engagement in dining category

### 3. **Rating Patterns**
- **Rating Range**: Majority of restaurants have ratings between 3.5 to 4.0 out of 5
- Distribution shows consistent quality across most establishments

### 4. **Customer Spending Behavior**
- **Couples' Preference**: Most couples prefer restaurants with an approximate cost of **₹300** for two people
- Strong price sensitivity in the mid-range segment

### 5. **Online vs. Offline Ordering**
- **Online Orders**: Receive higher average ratings
- **Offline Orders**: Receive relatively lower ratings compared to online
- **Channel Preference**: 
  - Dining restaurants: Primarily accept offline orders
  - Cafes: Primarily receive online orders

---

## 📁 Project Structure

```
ZOMATO-DATA-ANALYSIS-EDA-PROJECT/
├── ZOMATO PROJECT.ipynb       # Main analysis notebook
├── Zomato data .csv           # Raw dataset (148 restaurant records)
├── README.md                  # Project documentation
└── .ipynb_checkpoints/        # Jupyter notebook checkpoints
```

---

## 📊 Dataset Information

### Data Specifications
- **Total Records**: 148 restaurants
- **Total Features**: 7 columns
- **Data Quality**: No missing values

### Dataset Columns

| Column Name | Data Type | Description |
|---|---|---|
| `name` | Object | Restaurant name |
| `online_order` | Object | Yes/No - Accepts online orders |
| `book_table` | Object | Yes/No - Table booking available |
| `rate` | Float | Restaurant rating (0-5 scale) |
| `votes` | Integer | Number of customer votes/reviews |
| `approx_cost(for two people)` | Integer | Approximate cost in rupees |
| `listed_in(type)` | Object | Restaurant category (Buffet, Dining, Cafe) |

---

## 🛠️ Technologies & Libraries

### Core Technologies
- **Python 3.x** - Programming language
- **Jupyter Notebook** - Interactive analysis environment

### Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data manipulation and analysis |
| `numpy` | Numerical computations |
| `matplotlib.pyplot` | Data visualization |
| `seaborn` | Statistical data visualization |

---

## 🔍 Analysis Methodology

### Step 1: Data Preparation
- Import necessary libraries (NumPy, Pandas, Matplotlib, Seaborn)
- Load CSV data into pandas DataFrame
- Initial data exploration

### Step 2: Data Cleaning & Transformation
- Convert rating column from string format (e.g., "4.1/5") to float
- Handle missing data (verified - no missing values found)
- Data type validation

### Step 3: Exploratory Data Analysis
- **Univariate Analysis**: Individual feature distributions
- **Bivariate Analysis**: Relationships between variables
- **Categorical Analysis**: Restaurant type comparisons
- **Visualization**: Count plots, histograms, box plots, heatmaps

### Step 4: Business Insights
- Correlation analysis between features
- Customer preference patterns
- Performance metrics by restaurant category

---

## 📈 Visualizations & Analysis

### Key Visualizations Included
1. **Count Plot**: Restaurant type distribution
2. **Line Plot**: Votes received by restaurant category
3. **Histogram**: Rating distribution (5 bins)
4. **Count Plot**: Couples' spending preferences
5. **Box Plot**: Online vs. Offline rating comparison
6. **Heatmap**: Restaurant type vs. Online ordering correlation

---

## 💡 Business Recommendations

1. **For Restaurant Owners**:
   - Focus on the ₹300 price point for couples dining
   - Consider enabling online ordering to improve ratings
   - Emphasize dining category for higher engagement

2. **For Zomato Platform**:
   - Promote online ordering features (higher customer satisfaction)
   - Highlight dining restaurants in recommendations
   - Implement targeted pricing strategies for mid-range segment

3. **For Investors**:
   - Dining establishments show strongest customer engagement
   - Mid-range price point (₹300) has proven market demand
   - Online-enabled restaurants receive better ratings

---

## 🚀 How to Run the Project

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Execution Steps
1. Clone the repository
2. Navigate to the project directory
3. Open the Jupyter notebook:
   ```bash
   jupyter notebook "ZOMATO PROJECT.ipynb"
   ```
4. Run all cells sequentially to see the analysis and visualizations

---

## 📚 Code Highlights

### Data Type Conversion Example
```python
def handleRate(value):
    value = str(value).split('/')
    value = value[0]
    return float(value)

dataframe['rate'] = dataframe['rate'].apply(handleRate)
```

### Grouping & Aggregation
```python
groupdata = dataframe.groupby('listed_in(type)')['votes'].sum()
result = pd.DataFrame({'votes': groupdata})
```

---

## 🎓 Learning Outcomes

This project demonstrates proficiency in:
- ✅ Data loading and cleaning with pandas
- ✅ Data type conversions and transformations
- ✅ Exploratory Data Analysis (EDA) techniques
- ✅ Statistical analysis and data interpretation
- ✅ Data visualization with matplotlib and seaborn
- ✅ Business insight derivation from data
- ✅ Professional documentation of analysis

---

## 📝 Conclusions

This comprehensive EDA reveals that:
- **Dining restaurants** are the dominant and most preferred category
- **Customers prioritize value** - ₹300 price point is the sweet spot for couples
- **Online ordering improves satisfaction** - platforms should encourage digital adoption
- **Rating consistency** shows healthy market with mostly 3.5-4.0 ratings
- **Engagement patterns** indicate strong customer preferences for specific restaurant types and ordering methods

These insights can drive strategic decisions for restaurant marketing, platform optimization, and investment decisions.

---

## 📧 Contact & Portfolio

**Author**: Surag Devadiga  
**GitHub**: [surag29](https://github.com/surag29)  
**LinkedIn**: [surag-devadiga-233477329](https://linkedin.com/in/surag-devadiga-233477329)  
**Email**: surudev29@gmail.com

---

## 📄 License

This project is open source and available under the MIT License.

---

**Last Updated**: December 2025  
**Project Status**: ✅ Complete
