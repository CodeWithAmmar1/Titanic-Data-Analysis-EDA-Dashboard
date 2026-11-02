# 🚢 Titanic Data Analysis & EDA Dashboard

An end-to-end Data Analytics project built with **Python (Pandas, NumPy, Matplotlib, Seaborn)** to perform Exploratory Data Analysis (EDA), data cleaning, missing value imputation, IQR outlier detection, and survival analysis on the Titanic dataset.

---

## 📊 Project Preview

<img width="486" height="432" alt="image" src="https://github.com/user-attachments/assets/86973e46-7bcb-4b55-bfa5-7425a8633d1e" />
<img width="514" height="354" alt="image" src="https://github.com/user-attachments/assets/550c3608-71a5-44d6-9497-4ca741e3e845" />
<img width="599" height="407" alt="image" src="https://github.com/user-attachments/assets/634c73bd-dea0-45e5-87a6-381fcab7ef32" />
<img width="466" height="311" alt="image" src="https://github.com/user-attachments/assets/c06e1696-fa23-44f5-b1e2-807a96dbf095" />
<img width="1202" height="380" alt="image" src="https://github.com/user-attachments/assets/dd5c03f0-ee4c-4fa7-af9a-6a1fbd536497" />
<img width="471" height="446" alt="image" src="https://github.com/user-attachments/assets/e188cbca-9cc5-427f-a67f-2f5a1d38c477" />
<img width="463" height="436" alt="image" src="https://github.com/user-attachments/assets/0e05115e-364b-49d1-86e5-570a229f7942" />


---

## 💡 Key Data Insights

- **Passenger Survival:** The overall survival rate was low, with less than 40% of total passengers surviving the disaster.
- **Gender Impact:** **Female passengers** had a significantly higher survival rate compared to **Male passengers**, following the "women and children first" protocol.
- **Socio-Economic Class:** **1st Class (Upper)** passengers had the highest rate of survival, while **3rd Class (Lower)** passengers experienced the highest mortality rate.
- **Age Distribution:** Children (under 10 years old) showed higher survival rates, whereas median passenger age hovered around 28 years.
- **Fare Outliers:** Passenger fares contained extreme high-value outliers (detected via IQR methods), representing luxury suites in 1st class.

---

## 📈 Analysis & Feature Engineering Highlights

1. **Dataset Overview & Metadata:** Load `.csv` files into Pandas DataFrames and assess initial column data types, non-null counts, and metrics.
2. **Missing Data Handling:** 
   - Imputed **`Age`** missing values using column **Median**.
   - Imputed **`Embarked`** missing values using column **Mode** (most frequent port).
   - Filled **`Cabin`** missing values with `"Unknown"` due to a high missing percentage.
3. **Outlier Detection via IQR:** 
   - Calculated 1st Quantile ($Q1$), 3rd Quantile ($Q3$), and Interquartile Range ($IQR$).
   - Defined lower bound ($Q1 - 1.5 \times IQR$) and upper bound ($Q3 + 1.5 \times IQR$) to isolate extreme **`Fare`** values.
4. **Demographic & Survival Visualizations:**
   - **Boxplots** for outlier detection in continuous variables (`Fare`, `Age`).
   - **Count plots & Bar charts** showing survival rates across **Gender (`Sex`)** and **Ticket Class (`Pclass`)**.
   - **Correlation Heatmaps** to analyze relationships between variables (`Fare`, `SibSp`, `Parch`, `Survived`).

---

## 🛠️ Data Dictionary

| Variable | Definition | Key / Values |
| :--- | :--- | :--- |
| **Survived** | Outcome of survival | `0 = No`, `1 = Yes` |
| **Pclass** | Socio-economic class | `1 = Upper`, `2 = Middle`, `3 = Lower` |
| **Name** | Name of passenger | Text string |
| **Sex** | Sex of passenger | `male`, `female` |
| **Age** | Age in years | Numeric (Imputed median for NaNs) |
| **SibSp** | # of siblings / spouses aboard | Integer count |
| **Parch** | # of parents / children aboard | Integer count |
| **Ticket** | Ticket number | Text string |
| **Fare** | Passenger fare | Numeric (Contains outliers) |
| **Cabin** | Cabin number | Text string (`Unknown` for NaNs) |
| **Embarked** | Port of Embarkation | `C = Cherbourg`, `Q = Queenstown`, `S = Southampton` |

---

