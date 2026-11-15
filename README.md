
📓 View full notebook here (GitHub preview bug): https://nbviewer.org/github/Dathan-Quraisch/supermarket-vegetable-analysis/blob/main/supermarket_vegetable_analysis.ipynb

# Supermarket Vegetable Sales Analysis

## Business Question
A Chinese supermarket wanted to know: Which vegetables should we order more, which are wasting money, and is the business growing or dying?

## Dataset
- 878,000+ transactions, Jul 2020 - Jun 2023
- 242 vegetable products
- Fields: Date, Item Name, Quantity Sold, Revenue, Cost, Profit, Loss Rate

## Key Findings

### 1. Business is Stable + Seasonal, Not Dying
| Year | Revenue | Profit | Margin |
| :--- | :--- | :--- | :--- |
| 2021 | 1,101,976 | 390,477 | 35.4% |
| 2022 | 1,039,726 | 398,648 | 38.4% |

Revenue dropped in 2022 due to COVID, but profit INCREASED because margin improved from 35.4% to 38.4% and volume grew from 137k to 161k kilos.
2023 H1 (563k revenue) is on track to beat 2021.

Seasonality: Huge spike every Jan/Feb for Chinese New Year (180k in Jan 2021), then crash in March.

### 2. Low Waste = High Profit
Top products:
- Broccoli: 90,256 profit, 9.26% loss
- Xixia Mushroom: 71,574 profit, 13.82% loss
- Net Lotus Root: 62,412 profit, 5.54% loss
- Wuhu Green Pepper: 61,455 profit, 5.70% loss

### 3. Decision Engine
I built a simple rule to classify all 242 products:
- STAR - Order more: 17 products
- KEEP BUT FIX STORAGE: 5 products
- DELETE: 2 products
- KEEP - Normal: 218 products

**Fix Storage:** Chinese Cabbage (25,895 profit, 22.27% loss, loses 5,767 RMB to waste), Honghu Lotus Root, High Melon (29.25% loss), Foreign Garland Chrysanthemum, Dongmenkou Xiaobaicai

**Delete:** Chuncai (75 RMB profit in 3 years, 29% loss), Purple Cabbage (80 RMB profit, 25.53% loss)

## Recommendation
Don't cut the assortment. Fix storage for the 5, delete the 2 dead products, and never run out of Stars in January.

## Tools
Python, Pandas, Matplotlib, Jupyter Notebook
