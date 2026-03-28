# Trader Performance vs Market Sentiment
**Primetrade.ai — Data Science Intern Assignment**  
**Analyst:** Priyanshu Tamboli



## Objective
Analyze how Bitcoin market sentiment (Fear/Greed Index) influences trader behavior 
and performance on Hyperliquid, and derive actionable trading strategy insights.



## Datasets
 Bitcoin Fear/Greed Index | 2,644 | 4 | Feb 2018 – May 2025 |
 Hyperliquid Trader Data | 211,224 | 16 | May 2023 – May 2025 |

---

## Setup
## Setup
1. Download datasets from the links provided in the assignment email
2. Place both CSV files in the same folder as the notebook
3. Install dependencies:
```
   pip install pandas numpy matplotlib seaborn scipy
```
4. Open and run all cells in `analysis.ipynb`

---

## Methodology
- Merged both datasets on date after normalizing timestamps to daily level
- Engineered trader-day level features: daily PnL, win rate, trade frequency, 
  avg trade size, long/short ratio
- Segmented 32 unique traders into: Small/Medium/Large (position size), 
  Infrequent/Moderate/Frequent (activity), Losing/Neutral/Winning (performance)
- Analyzed behavior and performance metrics across all 5 sentiment categories

---

## Key Insights
1. **Panic creates opportunity for skilled traders** — Extreme Fear days have 
   the second highest median PnL ($218) but Losing traders hit their lowest 
   win rate (21%) on those same days. Skill gap widens during panic.

2. **Extreme Greed is the best environment across all segments** — Highest 
   median PnL ($418), Winning traders at ~100% win rate, even Neutral traders 
   cross 50% win rate.

3. **Moderate traders overtrade during panic** — Trade frequency spikes to 
   55/day on Extreme Fear vs 18/day on Extreme Greed. More trades, worse outcomes.

---

## Strategy Recommendations
1. **Losing/Neutral traders should reduce activity on Extreme Fear days** — 
   cut trade frequency and size by at least 30%. Data shows these segments 
   underperform most severely during panic.

2. **Winning traders should size up on Extreme Greed days** — their edge 
   holds across all sentiments but PnL peaks during euphoria. Momentum 
   amplifies their alpha.

---
