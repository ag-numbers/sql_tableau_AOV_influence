# sql_tableau_AOV_influence
SQL + Tableau project exploring what drives higher Average Order Value (AOV) 
# 📊 Factors Influencing Average Order Value (AOV)

## 🧠 Project Overview
This project started with a simple question:  
**What makes some customers spend more than others?**

To answer that, I explored demographic, behavioral, decision-based, and contextual factors that might explain variations in AOV.  
The dataset was downloaded from **Kaggle** and contains data representing customer demographics, purchase behaviors, and decision-related attributes.

This project helped me deepen my SQL data cleaning and analytical thinking — especially around hypothesis testing and building a clear story in Tableau.

---

## 🧹 Data Preparation (SQL)
All data cleaning and transformation were done in **PostgreSQL**:

- Explored data
- Renamed columns for clarity
- Checked for missing values and verified dataset consistency
- Cleaned categories and removed special characters  
- Converted amount values from text to numeric  
- Created new calculated fields:
  - `age_group` (18–24, 25–32, 33-41, 42-50)
  - `decision_group` (Very fast, Average, Slow)
  - `loyalty_group` (High, Low)
  - `satisfaction_group` (High, Medium, Low)
---

## 🔍 Analysis Approach
- I built hypotheses based on real marketing segmentation frameworks
- Each hypothesis was tested in SQL
- The data was visualized in Tableau to either support or reject each hypotheses

## 📊 Hypotheses and Conclusions

| Slice Type | Hypothesis | Conclusion |
|-------------|-------------|------------|
| **Demographic** | Higher **income customers** have higher AOV | ❌ Not supported. Income level does not significantly influence purchase amount in this dataset. |
| **Demographic** | **Older** customers have higher AOV | ❌ Not supported. The youngest customer group (18–24) has the highest AOV. AOV gradually decreases with age but increases again for the oldest group. |
| **Behavioral** | Customers with higher **satisfaction rating** have higher AOV | ❌ Not supported. AOV does not increase with satisfaction. Medium satisfaction group has the highest AOV, which may be influenced by incentives. |
| **Behavioral** | Customers with high **ad engagement** have higher AOV | ❌ Not supported. Spending does not increase with ad engagement. |
| **Decision-based** | Customers with shorter **decision times** have higher AOV | ❌ Not supported. Customers with average decision times have the highest AOV. |
| **Decision-based** | Customers with strong **intent** (“planned”) have higher AOV than impulsive buyers | ❌ Not supported. Desire-driven (wants-based) purchases lead to the highest AOV, while impulsive intent shows the lowest. |
| **Contextual** | **Smartphone** users have higher AOV than desktop users | ✅ Supported. Smartphone customers have the highest AOV. |
| **Contextual** | Customers have higher AOV on **online** purchases than in-store | ⚠️ Partially supported. Customers using mixed channels** have the highest AOV, suggesting the importance of omnichannel integration. |

## 🔗 Cross-Dimensional Hypotheses

To explore how multiple factors interact to influence spending behavior, I also tested several **cross-dimensional hypotheses**.  
These combine demographic, behavioral, and contextual variables to uncover deeper insights into customer spending patterns.

### 📊 Cross-Dimensional Findings

| Dimensions | Conclusion |
|-------------|-------------|
| **AOV by loyalty group & member** | Loyalty membership increases AOV. |Loyal customers spend more than non-members. |
| **AOV by income & age** | Income is a stronger driver for higher AOV than age.|
| **AOV by social media influence & ad engagement** | Social media ads and enagegment do not increase AOV. | 
| **AOV by intent & income** | High-income customers who want or plan their purchases spend the most. Impulsive buyers spend less even if they earn more.|

---
## 💡 Business Recommendations

1. Improving the mobile website or app can directly increase order value.
2. Phrase marketing campaigns on those who want something, not just need it.
3. 4. Make it easy for customers to switch between channels (let them browse online and buy in store).
4. Encourage customers to join loyalty memebrship program and reward current members.

---

## 🛠 Tools Used
- **SQL (PostgreSQL):** Data cleaning, transformation, and hypothesis testing  
- **Tableau:** Data visualization and dashboard creation  
- **Excel / Notion:** Project mapping and documentation
- **Kaggle:** Datadet 

---

## 🧩 Dashboard Structure
Each dashboard page explores a different perspective:

1. **Demographic & Behavioral Factors**
2. **Decision-based & Contextual Factors**
3. **Combined Factors (Cross-dimensional View)**

You can filter by **gender** or **category** to explore different spending patterns.

**Link to the dashboard** https://public.tableau.com/app/profile/alina.lihostaieva/viz/FactorsinfluencingAOV/Story1 

[<img width="875" height="619" alt="Screenshot 2025-11-05 at 15 37 48" src="https://github.com/user-attachments/assets/6d763f8c-5cb4-4fee-bedc-84dee0c7a588" />](https://github.com/ag-numbers/sql_tableau_AOV_influence/blob/main/README.md)


<img width="889" height="635" alt="Screenshot 2025-11-05 at 15 37 27" src="https://github.com/user-attachments/assets/6f30b82d-41d8-4873-89a5-0c7cb359c9b2" />

---<img width="880" height="618" alt="Screenshot 2025-11-05 at 15 35 48" src="https://github.com/user-attachments/assets/582c74af-bb05-42a2-9499-787f72e9e7d7" />


## Data structure
<img width="158" height="619" alt="Screenshot 2025-11-05 at 15 40 30" src="https://github.com/user-attachments/assets/be408bde-6292-4892-bca4-176b44648fd8" />
---

## ⚙️ Dataset Disclaimer
The dataset was downloaded from **Kaggle** and contains **synthetic, anonymized data**.  
It is used **for learning and portfolio purposes only** — all customer information is fictional.
