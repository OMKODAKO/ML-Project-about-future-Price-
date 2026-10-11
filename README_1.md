# 📊 მაღაზიის მოგების პროგნოზირება — ML Pipeline

> **ლექცია #10** — Gradient Boosting & მოდელების შედარება  
> BTU · Python · Jupyter Notebook

---

## 🎯 პროექტის მიზანი

რეალური ტრანზაქციური მონაცემებიდან (**10,674 ტრანზაქცია**, 2025-03 → 2026-05) **შემდეგი 30 დღის მოგების** პროგნოზირება Machine Learning-ის გამოყენებით.

---

## 📁 სტრუქტურა

```
├── lecture_10_gradient_boosting.ipynb   # მთავარი ნოუთბუქი
├── merged.xlsx                          # მონაცემები (არ ატვირთო!)
├── requirements.txt                     # ბიბლიოთეკები
└── README.md
```

---

## 🤖 შედარებული მოდელები

| მოდელი | MAE | MAPE | R² |
|--------|-----|------|----|
| **Random Forest** ⭐ | **2.18 GEL** | **1.6%** | **0.9983** |
| Ensemble (შეწონილი) | 2.96 GEL | 1.7% | 0.9928 |
| Ridge Regression | 4.37 GEL | 3.3% | 0.9949 |
| Gradient Boosting | 4.59 GEL | 2.1% | 0.9504 |
| LightGBM | 4.80 GEL | 3.6% | 0.9932 |

---

## 📓 ნოუთბუქის შინაარსი

1. **EDA** — მონაცემების შესწავლა და NULL-ების შემოწმება  
2. **Data Cleaning** — ანომალიები, Data Leakage-ის პრევენცია  
3. **Feature Engineering** — Lag features, Rolling statistics, Time features  
4. **სტატისტიკური ანალიზი** — საფასო კატეგორიები, საკომისიოები, ტრენდები  
5. **4 მოდელის გაწვრთნა** — Ridge, Gradient Boosting, Random Forest, LightGBM  
6. **შედარება** — MAE / RMSE / MAPE / R² + TimeSeriesSplit CV  
7. **30-დღიანი პროგნოზი** — Recursive forecasting + ვიზუალიზაცია  

---

## ⚙️ გაშვება

```bash
# 1. დააინსტალირე ბიბლიოთეკები
pip install -r requirements.txt

# 2. გახსენი ნოუთბუქი
jupyter notebook lecture_10_gradient_boosting.ipynb
```

---

## 🔑 მთავარი პრინციპები

- **Data Leakage პრევენცია** — `settlement amount` და `commission` feature-ებიდან სრულად ამოღებულია  
- **TimeSeriesSplit CV** — Random split დაუშვებელია time series-ზე  
- **Dependency-free** — XGBoost-ის ნაცვლად `sklearn.GradientBoostingRegressor` (macOS-თავსებადი)  
- **Ensemble** — ოთხი მოდელის შეწონილი საშუალო უფრო მდგრად შედეგს იძლევა  

---

## 📚 წყაროები

- [Gradient Boosting — Explained.AI](https://explained.ai/gradient-boosting/)
- [TimeSeriesSplit — sklearn](https://scikit-learn.org/stable/modules/cross_validation.html#time-series-split)
- [Feature Engineering for Time Series](https://machinelearningmastery.com/basic-feature-engineering-time-series-data-python/)
- [Data Leakage in ML](https://machinelearningmastery.com/data-leakage-machine-learning/)

---

## 👩‍💻 ავტორი

**Omiko** · BTU Student  
ML & Web Development
