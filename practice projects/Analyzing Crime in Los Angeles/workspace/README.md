
# Analyzing Crime in Los Angeles

Analyze LAPD crime records to uncover patterns that can help allocate resources more effectively.

## Objective

Answer three questions using the provided `crimes.csv` dataset:

1. Which hour has the highest frequency of crimes?
2. Which area has the largest frequency of night crimes (10 PM to 3:59 AM)?
3. How many crimes were committed against victims in different age groups?

## Source

- Practice project and provided dataset source (DataCamp): https://app.datacamp.com/learn/projects/1876

## Dataset

The analysis uses a modified version of Los Angeles Open Data.

**File:** `crimes.csv`

**Columns used in this project** (from the dataset):

- `TIME OCC`: Time of occurrence in 24-hour military time (e.g., `1345` = 1:45 PM)
- `AREA NAME`: Geographic area / patrol division name
- `Vict Age`: Victim age in years

Other columns exist in the dataset (e.g., `DR_NO`, dates, crime descriptions, etc.) but are not required for the three questions above.

## Notebook

The full analysis is in:

- `01_main.ipynb`

It includes:

- Loading and inspecting the dataset
- Creating a derived `hour` column from `TIME OCC`
- Filtering night-time crimes using the derived hour
- Creating victim age groups via binning (`pd.cut`)
- Visualizations using Matplotlib + Seaborn

## Approach (What the notebook does)

### 1) Peak crime hour

- Convert `TIME OCC` into an hour-of-day feature:
	- `hour = TIME OCC // 100`
- Compute the most frequent hour with `value_counts()`
- Plot crime counts by hour

### 2) Area with most night crimes

- Filter to crimes occurring between **10 PM and 3:59 AM**:
	- `hour >= 22` or `hour < 4`
- Compute the most frequent `AREA NAME`
- Plot night crime counts by area

### 3) Crimes by victim age group

- Bin `Vict Age` into these groups:
	- `0–17`, `18–25`, `26–34`, `35–44`, `45–54`, `55–64`, `65+`
- Count crimes per age group
- Plot the distribution

## Results (From the notebook)

These are the results recorded in the notebook output:

- **Peak crime hour:** **12** with **13,663** occurrences
- **Night crime hotspot (10 PM–3:59 AM):** **Central** with **3,312** occurrences
- **Victim age group distribution:**
	- `0–17`: 4,528
	- `18–25`: 28,291
	- `26–34`: 47,470
	- `35–44`: 42,157
	- `45–54`: 28,353
	- `55–64`: 20,169
	- `65+`: 14,747

## How to run

### Option A: Run in VS Code (recommended)

1. Open `01_main.ipynb`
2. Ensure you have a Python environment selected
3. Install dependencies (if needed):

```bash
pip install pandas numpy matplotlib seaborn
```

4. Run cells top-to-bottom

### Option B: Run with Jupyter

```bash
pip install notebook pandas numpy matplotlib seaborn
jupyter notebook
```

Then open `01_main.ipynb` and run all cells.

## Project structure

```text
workspace/
	01_main.ipynb
	crimes.csv
	README.md
```

## Notes

- The notebook assumes `crimes.csv` is in the same folder as `01_main.ipynb`.
- Visualizations use Seaborn palettes; you can change palettes without affecting the analysis logic.

