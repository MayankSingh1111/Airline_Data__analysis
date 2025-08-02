# ✈️ Flight Price Analysis with Python

This project analyzes flight pricing data to uncover trends in how various features such as airline, travel class, number of stops, and booking window impact ticket prices. It includes data cleaning, exploratory analysis, and visualization using Python in Jupyter Notebook.

---

## 📁 Dataset Overview

The dataset contains **300,153** domestic flight records in India. It includes the following key columns:

| Column            | Description                                          |
|------------------|------------------------------------------------------|
| `airline`        | Name of the airline                                  |
| `flight`         | Flight number (removed during cleaning)              |
| `source_city`    | Departure city                                       |
| `departure_time` | Time of departure (Morning, Evening, etc.)           |
| `stops`          | Number of stops (e.g., zero, one)                    |
| `arrival_time`   | Time of arrival                                      |
| `destination_city` | Destination city                                   |
| `class`          | Travel class (Economy or Business)                   |
| `duration`       | Flight duration in hours                             |
| `days_left`      | Days left from booking to travel date                |
| `price`          | Ticket price in INR                                  |

---

## 🧹 Data Cleaning Steps

Performed in `01_data_cleaning.ipynb`:

- Removed irrelevant columns: `index`, `flight`
- Converted `stops` from categorical (e.g., "zero") to numeric values
- Checked and confirmed absence of missing values
- Exported a cleaned dataset for analysis

---

## 📊 Exploratory Data Analysis

Conducted in `02_exploratory_analysis.ipynb`. Key insights and visualizations:

### 1. 🎯 Price Distribution
- Most ticket prices are between ₹3,000 and ₹15,000.
- A few business class tickets go above ₹50,000.

### 2. 🏢 Average Price by Airline
- Vistara and Air India tend to have higher prices on average.
- Low-cost carriers like AirAsia and SpiceJet offer cheaper fares.

### 3. 💼 Travel Class vs Price
- Business class tickets are significantly more expensive than economy (2.5–4x higher).

### 4. ✈️ Stops vs Price
- Non-stop flights are usually more expensive.
- 1-stop and multi-stop flights are cheaper, often due to inconvenience.

### 5. 📅 Days Left vs Price
- Prices increase as `days_left` decreases.
- Booking early (10+ days in advance) helps save money.

### 6. ⏱️ Duration vs Price

```python
sns.scatterplot(data=df, x='duration', y='price')
plt.title("Duration vs Price")
```

- There's a moderate positive trend: longer flights often cost more, but it's not linear.
- Business class inflates prices even for shorter durations.

---

## 📌 Key Takeaways
- Booking early and choosing economy class significantly reduces flight cost.
- Airline choice and number of stops greatly influence the final ticket price.
- Longer flights tend to cost more, but not always—route and airline also matter.

---

## 🧰 Tech Stack
- Python 3
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook

---

## ✅ Future Work
- Add machine learning to predict ticket prices
- Add clustering to segment customer pricing tiers
- Deploy the project on Streamlit as an interactive dashboard

---

## 🧑‍💻 Author
- Mayank Singh – Data Science Learner & Project Builder  
- GitHub: [github.com/mayanksingh1111](https://github.com/mayanksingh1111)
