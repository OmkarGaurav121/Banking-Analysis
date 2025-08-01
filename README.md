# 💼 Banking Analytics Dashboard (Power BI)

> A complete Power BI project designed to analyze banking customer behavior across loans, deposits, demographics, and account types.  
> Combines Excel Power Query for cleaning, Python for EDA, and Power BI for visual storytelling.

---

## 📌 Objective

To create a comprehensive business intelligence dashboard that provides actionable insights into customer segments, product engagement, financial behaviors, and advisor performance—supporting smarter decision-making for banks.

---

## 📁 Dataset Details

| Category        | Sample Attributes                                                          |
|----------------|------------------------------------------------------------------------------|
| Demographics    | Age, GenderId, Nationality, Occupation                                      |
| Financial Info  | Estimated Income, Bank Loans, Credit Card Balances, Superannuation Savings  |
| Accounts        | Saving, Checking, Business Lending, Foreign Currency Accounts               |
| Engagement      | Joined Bank (Date), Loyalty Tier, Risk Weighting, Fee Structure             |
| Relationship    | Branch ID (BRId), Advisor ID (IAId), Contact Method                         |

- **Rows**: 3,000  
- **Columns**: 25  
- **Files Used**: `Banking.csv`, `clients.csv`

---

## 🧼 Data Preparation (Excel Power Query + Python)

- Removed duplicates and irrelevant rows  
- Formatted `Joined Bank` into Date type  
- Created `Income Band` column using income ranges  
- Replaced missing values with defaults like `"Unknown"`  
- Verified clean dataset with **zero nulls**  
- Performed EDA using Python – `Banking EDA.pdf` included

```python
bins = [0, 100000, 300000, float('inf')]
labels = ['Low', 'Mid', 'High']
df['Income Band'] = pd.cut(df['Estimated Income'], bins=bins, labels=labels)
```

---

## 📊 Dashboard Walkthrough (Power BI)

The dashboard is divided into 4 professional pages—each focused on a key banking theme with filters, KPIs, and visual exploration.

---

### 🏠 1. Home Dashboard – Executive Snapshot

![Home Dashboard](https://raw.githubusercontent.com/OmkarGaurav121/Banking-Analytics-Dashboard/main/Home%20Dashboard.png)

**Filters**: Year | Gender

**Key Metrics:**
- Total Clients: 3,000  
- Loan Amount: ₹4.38B  
- Total Deposits: ₹3.77B  
- Business Lending: ₹2.60B  
- Saving Accounts: ₹698M  
- Checking Accounts: ₹963M  

**Insights:**
- Balanced customer distribution across genders  
- Most clients are in **Jade** loyalty tier (new but engaged)  
- Income bands show even segmentation across client base  
- Strong loan-to-deposit ratio indicating healthy growth  

---

### 💳 2. Loan Analysis Dashboard – Credit Behavior

![Loan Analysis Dashboard](https://raw.githubusercontent.com/OmkarGaurav121/Banking-Analytics-Dashboard/main/Loan%20Analysis%20Dashboard.png)

**Filters**: Year | Advisor | Contact | Gender

**Loan Metrics:**
- Total Loans: ₹4.38B  
- Business Lending: ₹2.60B  
- Bank Loans: ₹1.77B  
- Credit Card Balance: ₹9.53M  

**Insights:**
- High-income groups drive most of the loan volume  
- Engineers and Managers take the largest loan shares  
- Europeans lead in loan consumption  
- Filtering by advisors reveals top performers in loan generation  

---

### 💰 3. Deposit Analysis Dashboard – Savings Focus

![Deposit Analysis Dashboard](https://raw.githubusercontent.com/OmkarGaurav121/Banking-Analytics-Dashboard/main/Deposit%20Anaslysis%20Dashboard.png)

**Filters**: Year | Relationship Type | Advisor

**Deposit Metrics:**
- Total Deposits: ₹3.77B  
- Bank Deposits: ₹2.01B  
- Savings: ₹698M  
- Checking: ₹963M  

**Insights:**
- Most deposits come from **Mid and High Income** bands  
- Stable professions (Professors, HR, Engineers) dominate deposits  
- Balanced growth in saving and checking accounts  
- Asian and American clients show strong saving behavior  

---

### 📋 4. Summary Dashboard – Combined Metrics View

![Summary Dashboard](https://raw.githubusercontent.com/OmkarGaurav121/Banking-Analytics-Dashboard/main/Summary%20Dashboard.png)

**Filters**: Year | Advisor | Contact | Loyalty Tier

**KPIs Tracked:**
- Loans vs Deposits side-by-side  
- Business Lending & Credit Card Balances  
- Foreign Currency Accounts (₹89.65M)  
- Advisor-wise contributions  

**Insights:**
- Best page for overall executive decision-making  
- Highlights trends across products and advisors  
- Foreign currency usage increasing, though still niche  
- Helps in cross-branch and advisor-level benchmarking  

---

## 📈 Business-Level Insights

| Theme                | Strategic Takeaway                                                   |
|----------------------|----------------------------------------------------------------------|
| 📊 Client Behavior   | High earners dominate loan and deposit segments                      |
| 💼 Lending Profile   | Business lending is key revenue area                                 |
| 🧠 Advisor Insights  | Some advisors significantly outperform others                        |
| 🌍 Demographics      | European and Asian clients hold majority of assets                   |
| 💳 Credit Use        | Clients with higher card balances also seek more bank loans          |

---

## 💡 Key Skills Applied

- ✅ Excel Power Query (Data Cleaning)  
- ✅ Python EDA (`Banking EDA.pdf`)  
- ✅ Power BI Visual Design & KPIs  
- ✅ Data Modeling (Relationships, Calculated Columns)  
- ✅ Business Insight Extraction & Storytelling  

---

## 📦 Project Files

| File Name                          | Description                                |
|-----------------------------------|--------------------------------------------|
| `Banking.csv`                     | Cleaned dataset used in Power BI           |
| `clients.csv`                     | Additional client metadata                 |
| `Banking EDA.pdf`                 | Python EDA (PDF report)                    |
| `Home Dashboard.png`              | Executive summary dashboard screenshot     |
| `Loan Analysis Dashboard.png`     | Loan metrics and visuals                   |
| `Deposit Anaslysis Dashboard.png` | Deposit insights dashboard                 |
| `Summary Dashboard.png`           | Overall performance view                   |
| `README.md`                       | Project documentation (this file)          |

---

## 🚀 Future Scope

- 📌 Add churn prediction model (logistic regression or decision tree)  
- 📌 Segment clients using KMeans clustering  
- 📌 Add Row-Level Security for advisor-specific dashboard access  
- 📌 Embed live dashboard using Power BI Service  

---

## 🙋‍♂️ Created By

**Omkar Gaurav**  
📧 [omkargaurav121@gmail.com](mailto:omkargaurav121@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/omkar-gaurav-1508b6303)  
🔗 [GitHub](https://github.com/OmkarGaurav121)

---

> 📢 *If you found this project helpful, feel free to ⭐ star the repo and connect on LinkedIn!*
