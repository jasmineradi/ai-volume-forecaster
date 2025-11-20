# Volume Forecasting Analysis Report

## Statistical Patterns Discovered

### Trend Analysis
The overall trend in the data slowly goes upward over the three years. The system also reports a daily growth rate of 0.351 units/day based on the pattern it detected in the data.

The significance is that the volume is gradually increasing over time. Even though the growth is small each day, the overall direction is positive, which is suggesting that there is a steady long-term improvement for the business overall.

### Seasonal Patterns
1. **Weekly Pattern:**  
   Weekdays are always higher than weekends. Mondays through Fridays stay around the same level, and Saturdays and Sundays drop noticeably.

2. **Monthly Pattern:**  
   Months with increases include February through May while the drops occur primarily from June to September with a slight uptick from October to December followed by another drop in January.

3. **Yearly Pattern:**  
   The data forms a repeating wave each year. Some months are always a little higher or lower in a predictable pattern. The report shows a repeating annual pattern.

### Statistical Properties
-mean: 1390.78
-standard deviation: 192.38
-Coefficient of Variation: 0.138

---

## Forecasting Methods Applied

### Moving Average
-Window size tested: 7 days
-Accuracy (MAE): 65.89

-Pros
1. It is very simple and easy to use because it just averages recent days.
2. It smooths out the data and makes short-term patterns easier to see.

-cons
1. It reacts slowly to sudden changes.
2. It cannot capture long-term patterns like seasons or trends.

### Exponential Smoothing
-alpha paramter:0.3
-accuracy(MAE): 71.99 units

-pros:
1. It reacts faster to recent changes than a normal average.
2. It is still simple and easy to apply.


-cons:
1. It still does not consider weekly or yearly patterns.
2. The results depend on choosing the right alpha value.

---

## AI/ML Concepts Applied

### From Chapter 15:
1. **Temporal Reasoning:**  
   The system looks at how values change over time and uses the history to understand how the future might behave.

2. **Markov Assumption:**  
   The forecast mostly depends on recent past data, especially the last few days.

3. **Prediction Uncertainty:**  
   The MAE numbers (around 65–72) show that predictions aren’t perfect, but they’re close enough to give a general idea of what comes next.

---

## Next Steps (Week 8 Preview)
- Implement ARIMA models  
- Add machine learning algorithms  
- Create a 13-month forecast  
- Build an interactive Excel workbook  

---

## Challenges Encountered
- The moving average accuracy calculation caused an error because the lists didn’t line up. I had to align the data so both lists were the same length.
- The statsmodels library import didn’t work at first because Python 3.13 changed the import path, so I had to update it.

---

## Learning Reflections
- I learned how to look at data over time and spot patterns like weekdays vs weekends.
- I now understand that a “forecast” is basically just a guess based on past numbers.
- Seeing the MAE helped me understand how to measure how close a prediction is.
- This project helped me get more comfortable reading the output and describing it in normal language.
