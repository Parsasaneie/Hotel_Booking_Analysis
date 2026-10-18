# 📊 Exploratory Data Analysis (EDA) Projects

A collection of Exploratory Data Analysis projects on four real-world datasets using Python. Each notebook covers data cleaning, statistical analysis, and visualization to uncover meaningful insights.

---

## 🛠️ Tech Stack

| Tool / Library | Purpose |
|----------------|---------|
| Python | Core programming language |
| Pandas | Data loading, cleaning, and manipulation |
| NumPy | Numerical operations |
| Matplotlib | Basic plotting and chart customization |
| Seaborn | Statistical visualizations |
| Jupyter Notebook | Interactive analysis environment |

---

## 📁 Project Structure

```
EDA_Practice/
├── hotel_bookings/
│   ├── hotel_bookings_eda.ipynb
│   └── hotel_bookings.csv
├── netflix_titles/
│   ├── netflix_titles_eda.ipynb
│   └── netflix_titles.csv
├── titanic/
│   ├── titanic_eda.ipynb
│   ├── train.csv
│   ├── test.csv
│   └── gender_submission.csv
└── README.md
```

---

## 📂 Datasets

| Dataset | Rows | Columns | Topic |
|---------|------|---------|-------|
| Hotel Bookings | 119,390 | 32 | Hotel reservations and cancellations |
| Netflix Titles | 8,807 | 12 | Netflix movies and TV shows |
| Titanic | 891 | 12 | Passenger survival data |

---

## 🏨 1. Hotel Bookings

**File:** `hotel_bookings/hotel_bookings_eda.ipynb`

### Key Steps
- Missing value detection and cancellation rate analysis
- ADR (Average Daily Rate) outlier detection using boxplot
- Lead time distribution and correlation heatmap
- Group analysis: cancellation and ADR by hotel type

### Key Findings
- Compared ADR between Resort and City hotels
- Identified cancellation rate differences between hotel types
- Found correlation between lead time and cancellation

---

## 🎬 2. Netflix Titles

**File:** `netflix_titles/netflix_titles_eda.ipynb`

### Key Steps
- Missing value percentage calculation per column
- Duplicate detection and removal
- Content type split (Movies vs TV Shows)
- Top 10 countries and genres analysis
- Release year trend visualization

### Key Findings
- Analyzed Movies vs TV Shows ratio on Netflix
- Identified top 10 content-producing countries
- Explored release year growth trends over time

---

## 🚢 4. Titanic

**File:** `titanic/titanic_eda.ipynb`

### Key Steps
- Survival and gender distribution analysis
- Age distribution and fare outlier detection
- Feature engineering: created `Age_Group` column using `pd.cut()`
- Custom `survival_probability(age, pclass)` function

### Feature Engineering
```python
df['Age_Group'] = pd.cut(
    df['Age'],
    bins=[0, 12, 18, 35, 60, 100],
    labels=['Child', 'Teen', 'Young Adult', 'Adult', 'Senior']
)
```

### Custom Function
```python
def survival_probability(age, pclass):
    probability = df[
        (df['Age'] == age) & (df['Pclass'] == pclass)
    ]['Survived'].mean()
```

### Key Findings
- Women had significantly higher survival rates than men
- Found correlation between passenger class and survival
- Grouped passengers into age categories for deeper analysis

---

## 🔁 Common EDA Steps Across All Datasets

| Step | Purpose |
|------|---------|
| `df.shape` | Check number of rows and columns |
| `df.info()` | Check data types and null counts |
| `df.describe()` | Summary statistics |
| `df.isnull().sum()` | Count missing values |
| `df.duplicated().sum()` | Count duplicate rows |
| `sns.histplot()` | Distribution of numerical columns |
| `sns.boxplot()` | Detect outliers |
| `sns.heatmap(corr)` | Correlation between features |

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Parsasaneie/Hotel_Booking_Analysis.git
cd Hotel_Booking_Analysis
```

### 2. Install dependencies

```bash
python -m pip install pandas numpy matplotlib seaborn notebook
```

### 3. Launch Jupyter Notebook

```bash
python -m notebook
```

### 4. Run the notebooks

Open any `.ipynb` file from the appropriate project folder in Jupyter Notebook and run the cells sequentially.

---

**Note:** Make sure Python is installed on your system before running these commands.
## 🎓 About Me

Computer Engineering student at **Shahid Rajaee Teacher Training University, Tehran, Iran**.

## 📊 Areas of Interest

Interested in **Data Science, Data Analysis, and Algorithm Machine Learning**. Passionate about exploring data, discovering meaningful patterns, and using analytical and computational methods to solve problems.