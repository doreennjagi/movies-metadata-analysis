🎬 Movie Dataset Exploratory Data Analysis (EDA)

## 📌 Project Overview
The goal of this project is to explore and analyze the **Movies Metadata dataset** from Kaggle.  
I've focused on financial insights such as **budget, revenue, profit, return on investment (ROI)**, and trends over time.  
This EDA helps us understand what makes a movie financially successful.

---

## 📂 Dataset
- **Source**: Kaggle – [Movies Metadata](https://www.kaggle.com/datasets)  
- **Shape**: ~45,000 movies, multiple features  
- **Key Columns** used:
  - `title` – Movie name  
  - `release_date` – Release year  
  - `budget` – Production budget  
  - `revenue` – Box office revenue  
  - `popularity`, `vote_average`, `vote_count` – Audience engagement metrics  

---

## ⚙️ Data Preparation
1. **Loaded dataset** with `low_memory=False` to avoid type-inference issues in Pandas.  
2. **Converted financial columns** (`budget`, `revenue`, `popularity`, `vote_average`, `vote_count`) into numeric.  
3. **Created new features**:  
   - `profit = revenue – budget`  
   - `roi = profit / budget` (return on investment)  
   - `year` and `decade` extracted from `release_date`.  
4. **Handled missing values** by coercing invalid entries into `NaN`.  

---

## 📊 Exploratory Data Analysis

### 🔹 1. Overall Distribution
- Most movies have **low budgets and low revenues**.  
- A few blockbusters (e.g., *Avatar*, *Titanic*) dominate the revenue distribution.  

📌 *Tools*: `histplot`, KDE plots  

---

### 🔹 2. Profitability Over Time
- Created a `decade` column.  
- Calculated **average profit by decade**.  
- 📈 Found that **2000s–2010s** were the most profitable decades in Hollywood.  

📌 *Tools*: `groupby`, line plots  

---

### 🔹 3. Top 10 Most Profitable Movies
- Movies like *Avatar*, *Titanic*, *Star Wars* rank among the highest in profits.  
- Visualized with horizontal bar charts.  

📌 *Tools*: `sort_values`, `barplot`  

---

### 🔹 4. Correlation Analysis
- Strong correlation between **budget and revenue**.  
- ROI has weaker correlation with budget → high budget ≠ always high return.  

📌 *Tools*: `heatmap`  

---

### 🔹 5. Outlier Handling
- Extreme outliers (e.g., inflated budget/revenue values) were filtered for better scatterplots.  
- Clean scatterplot showed positive trend: higher budgets generally lead to higher revenues.  

---

## 📌 Key Insights
1. 🎥 **Most movies don't make massive profits** – only a few blockbusters skew the data.  
2. 💰 **Budgets and revenues are strongly correlated**.  
3. 📈 **2000s–2010s** were the most financially successful decades.  
4. ⚖️ **High budget ≠ high ROI** – smaller films sometimes achieve higher returns.  

---

## 🛠️ Tools & Libraries
- **Python 3**  
- **Pandas** → data cleaning, feature engineering  
- **Matplotlib / Seaborn** → visualization  
- **NumPy** → numeric operations  

---

## ✅ Conclusion
This project demonstrates how to:
- Clean and preprocess messy datasets.  
- Perform financial analysis with Pandas.  
- Use EDA to uncover trends and insights in movies data.  
