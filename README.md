# 💳 FiTech: Data-Driven Credit Card Design  

This project explores **credit card product design and marketing optimization** through the **FiTech simulation case study**. The goal was to determine which product features (APR, annual fee, fixed vs. variable rate) should be offered to which customer segments to **maximize profitability** while managing credit risk.  

---

## 📌 Project Overview  
FiTech planned a large-scale email solicitation (750,000 customers) to promote **12 possible credit card products**, each with different combinations of:  
- **Annual Percentage Rate (APR):** 14.9%, 16.8%, 19.8%  
- **Annual Fee:** $0 or $20  
- **Rate Type:** Fixed vs Variable  

Prospects were segmented by **Bankruptcy (BK) score** (150, 200, 250), a key indicator of credit risk. The challenge was to design a test-and-rollout strategy that balanced **customer response rates** with **Customer Lifetime Value (CLV)** to maximize profits.  

**Objectives:**  
1. Understand the relationship between credit risk (BK score) and CLV.  
2. Model customer response rates to different product offers.  
3. Test allocation strategies using partial factorial design.  
4. Incorporate CLV into targeting decisions.  
5. Optimize rollout strategy to maximize profitability.  

---

## 🔍 Methodology  

### 1. Data Preparation  
- **Datasets:**  
  - Past FiTech marketing campaigns (response rates).  
  - CLV estimates for all 12 product variants across BK segments.  
- **Features considered:** APR, annual fee, fixed vs. variable, card brand, BK score.  
- **Target variable:** Customer response (yes/no).  
- Applied weights to account for different campaign sample sizes.  

---

### 2. Modeling Approach  
- **Logistic Regression:** chosen for interpretability and effectiveness given limited data.  
- Evaluated **customer response probability** based on product attributes and BK score.  
- **Metrics:** AUC = 0.661, Recall = 82%.  
- Insights aligned with intuition:  
  - Higher APRs, annual fees, and variable rates → lower response.  
  - Visa-branded cards → higher response vs MasterCard.  

---

### 3. Simulation & Strategy  
- **Round 1 (Test):** Used **partial factorial design** to distribute offers evenly across products and BK scores, ensuring broad coverage.  
- **Round 2 (Rollout):** Adjusted allocation using a **CLV-weighted response model**:  
  - Prioritized BK 150 customers (higher CLV, lower risk).  
  - Reduced offers to low-performing products.  
  - Maintained some allocation to BK 200 and 250 where response rates justified.  

**Result:** Higher profits and CLV in rollout vs test, validating the **data-driven targeting strategy**.  

---

## 🛠️ Tools & Libraries  
- **Python:** pandas, numpy, matplotlib, seaborn  
- **scikit-learn:** Logistic Regression, model evaluation  
- **Radiant (R):** experimental design and partial factorial testing  
- **Simulation:** response modeling + CLV optimization  
- **Jupyter Notebook:** analysis, visualizations, and documentation  

---

## 💡 Key Skills & Concepts  
- **Credit Risk & CLV Modeling**  
- **Logistic Regression for Response Prediction**  
- **Experimental Design (Factorial Design)**  
- **Test-and-Rollout Strategy**  
- **Profit Optimization in Marketing**  
- **Business Analytics for Fintech**  

---

## 🚀 Key Takeaways  
- CLV declines with higher **BK scores**, emphasizing the importance of risk-based segmentation.  
- No single “best product” exists — optimal offers depend on balancing **response rates vs profitability**.  
- Data-driven targeting **outperforms uniform allocation**, leading to higher campaign ROI.  
- Even simple, interpretable models (like Logistic Regression) can drive significant business impact when paired with simulation and strategic allocation.  

---
