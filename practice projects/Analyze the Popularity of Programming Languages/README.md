# 📊 Analyze the Popularity of Programming Languages


## 📝 Project Overview

This project analyzes the popularity of programming languages over time using Stack Overflow question data. By examining trends in the number of questions asked for different programming language tags, we can gain insights into which technologies are growing, declining, or maintaining steady interest in the developer community.

## 🎯 Objectives

The main goals of this analysis are to answer:

1. **What was the percentage of R questions for 2020?**
2. **Which five programming language tags had the highest total number of questions asked between 2015 and 2020 (inclusive)?**

## 📚 Data Source

- **Project Source:** [DataCamp - Analyze the Popularity of Programming Languages](https://app.datacamp.com/learn/projects/2557)
- **Dataset:** `stack_overflow_data.csv`
- **Data Origin:** Stack Overflow question statistics

### Dataset Description

| Column | Description |
|--------|-------------|
| `year` | The year the questions were asked |
| `tag` | The programming language/technology tag |
| `num_questions` | Number of questions asked for that tag in that year |
| `year_total` | Total questions asked across all tags for that year |

## 🔧 Technologies Used

- **Python 3.x** - Core programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical data visualization
- **Jupyter Notebook** - Interactive development environment

## 📈 Key Findings

### 1. R Language Popularity (2020)
- Questions related to the **R programming language** accounted for approximately **0.97%** of total Stack Overflow questions in 2020.

### 2. Top 5 Programming Languages (2015-2020)
The five programming language tags with the highest total number of questions:

| Rank | Programming Language | Total Questions |
|------|---------------------|-----------------|
| 1 | JavaScript | Highest |
| 2 | Python | 2nd |
| 3 | Java | 3rd |
| 4 | Android | 4th |
| 5 | C# | 5th |

## 📊 Visualizations

The notebook includes several visualizations:
- 📉 Growth of R questions over the years
- 📉 Growth of R questions percentage over the years
- 📉 Comparative growth of top 5 programming languages
- 📉 Percentage trends for top 5 programming languages

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Running the Analysis
1. Clone this repository
2. Navigate to the project directory
3. Open the Jupyter notebook:
   ```bash
   jupyter notebook 01_main.ipynb
   ```
4. Run all cells to reproduce the analysis

## 📁 Project Structure

```
Analyze the Popularity of Programming Languages/
│
├── 01_main.ipynb          # Main analysis notebook
├── stack_overflow_data.csv # Dataset
└── README.md              # Project documentation
```

## 🔍 Analysis Workflow

1. **Data Loading** - Import the Stack Overflow dataset
2. **Data Inspection** - Examine structure, types, and missing values
3. **Data Cleaning** - Handle missing values in the 'tag' column
4. **Exploratory Data Analysis** - Answer key research questions
5. **Visualization** - Create insightful charts and graphs
6. **Conclusion** - Summarize findings

## 👤 Author

**Haseeb**

## 📜 License

This project is for educational purposes as part of the DataCamp learning platform.

## 🙏 Acknowledgments

- [DataCamp](https://www.datacamp.com/) for providing the project and dataset
- [Stack Overflow](https://stackoverflow.com/) for the original data

---

*This project was completed as part of learning data analytics with Python.*
