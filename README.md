# sql_tableau_AOV_influence
SQL + Tableau project exploring what drives higher Average Order Value (AOV) 
# 📊 Factors Influencing Average Order Value (AOV)

## 🧠 Project Overview
This project started with a simple question:  
**What makes some customers spend more than others?**

To answer that, I explored demographic, behavioral, decision-based, and contextual factors that might explain variations in AOV.  
The dataset was downloaded from **Kaggle** and contains data representing customer demographics, purchase behaviors, and decision-related attributes.

This project helped me deepen my SQL data cleaning and analytical thinking — especially around hypothesis testing and building a clear story in Tableau.

## Data structure
<img width="158" height="619" alt="Screenshot 2025-11-05 at 15 40 30" src="https://github.com/user-attachments/assets/be408bde-6292-4892-bca4-176b44648fd8" />
---

## 🧹 Data Preparation (SQL)
All data cleaning and transformation were done in **PostgreSQL**:

- Renamed columns for clarity  
- Cleaned categories and removed special characters  
- Converted amount values from text to numeric  
- Created new calculated fields:
  - `age_group` (e.g., 18–24, 25–32, etc.)
  - `decision_group` (Very fast, Average, Slow)
  - `loyalty_group` (High or Low)
  - `satisfaction_group` (High, Medium, Low)
- Checked for missing values and verified dataset consistency

---

## 🔍 Analysis Approach
I built hypotheses inspired by real marketing segmentation frameworks:

| Slice Type | Hypothesis |
|-------------|-------------|
| **Demographic** | Higher income customers have higher AOV |
| **Behavioral** | Customers with higher satisfaction or ad engagement have higher AOV |
| **Decision-based** | Customers with faster decision times or stronger intent (“planned”) have higher AOV |
| **Contextual** | Smartphone users or online shoppers have higher AOV |

Each hypothesis was tested in SQL, aggregated, and visualized in **Tableau**.

---

## 📈 Key Insights
- **Demographic** (age, income) and **behavioral** (satisfaction, ad engagement) factors had **low impact** on AOV  
- **Decision-based** and **contextual** factors had stronger influence:
  - Smartphone users showed the **highest AOV**
  - **Wants-based intent** led to higher spend than planned or impulsive purchases
  - Customers using **mixed channels (online + offline)** spent the most, highlighting the value of omnichannel experience
- Cross-dimensional findings:
  - **Loyalty membership** increases AOV  
  - **High income + young age** → higher AOV  
  - **Social media influence + ad engagement** show moderate correlation with AOV

---

## 💡 Business Takeaways
- Optimize **mobile shopping experience** — smartphone users spend more  
- Target **emotion-driven customers** (wants-based intent)  
- Use **upsell opportunities** for ad-engaged users  
- Support **multi-channel experiences** to increase overall spending  

---

## 🛠 Tools Used
- **SQL (PostgreSQL):** Data cleaning, transformation, and hypothesis testing  
- **Tableau:** Data visualization and dashboard creation  
- **Excel / Notion:** Project mapping and documentation
- **Kaggle:** For datadet 

---

## 🧩 Dashboard Structure
Each dashboard page explores a different perspective:

1. **Demographic & Behavioral Factors**
2. **Decision-based & Contextual Factors**
3. **Combined Factors (Cross-dimensional View)**

You can filter by **gender** or **category** to explore different spending patterns.



<img width="875" height="619" alt="Screenshot 2025-11-05 at 15 37 48" src="https://github.com/user-attachments/assets/6d763f8c-5cb4-4fee-bedc-84dee0c7a588" />


<img width="889" height="635" alt="Screenshot 2025-11-05 at 15 37 27" src="https://github.com/user-attachments/assets/6f30b82d-41d8-4873-89a5-0c7cb359c9b2" />

---<img width="880" height="618" alt="Screenshot 2025-11-05 at 15 35 48" src="https://github.com/user-attachments/assets/582c74af-bb05-42a2-9499-787f72e9e7d7" />



---

## ⚙️ Dataset Disclaimer
The dataset was downloaded from **Kaggle** and contains **synthetic, anonymized e-commerce data**.  
It is used **for learning and portfolio purposes only** — all customer information is fictional.
