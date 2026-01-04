# Root Cause Analysis: E-commerce "Add-to-Cart" Friction

## 📌 Project Overview
This project investigates a significant bottleneck in the conversion funnel of a multi-category e-commerce store. Initial data exploration revealed a paradox: **Purchase events are outnumbering Add-to-Cart (ATC) events**, and the vast majority of product categories show zero cart activity. 

The goal of this analysis is to determine whether these discrepancies are caused by technical bugs, tracking failures, or specific user UI/UX behaviors (like "Buy It Now" features).

---

## 📊 Key Data Insights
Based on the analysis of 500,000 events from October 2019:

### 1. The Conversion Funnel

The funnel shows a massive drop-off between viewing a product and adding it to the cart.

| Event Type | Total Count | Conversion Rate | Unique Users |
| :--- | :--- | :--- | :--- |
| **View** | 481,833 | 96.37% | 89,108 |
| **Purchase** | 9,758 | 1.95% | 7,362 |
| **Cart** | 8,409 | 1.68% | 4,441 |

*Data Source:*

### 2. The "Cart" Paradox
* **User Discrepancy:** There are **7,362 unique purchasers** but only **4,441 unique users** who added items to a cart.
* **Category Gap:** Out of **540 unique categories** viewed, only **89 categories** recorded an "Add to Cart" event.

---

## 🔍 Root Cause Investigation Strategy
The following structured checks have been identified to uncover the source of the friction:

### Technical Functionality Audit
* **Button Rendering:** Investigate if the "Add to Cart" button is failing
