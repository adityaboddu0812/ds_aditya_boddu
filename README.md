# Trading Performance Analysis: Fear vs Greed Sentiment

This project analyzes cryptocurrency trading performance in relation to market sentiment, specifically comparing trading behavior and outcomes during "Fear" and "Greed" market conditions using the Fear & Greed Index.

## Project Overview

The analysis examines how trading metrics (PnL, volume, win rate) differ between periods of market fear and greed, providing insights into trading behavior patterns and performance across different market sentiment conditions.

## Google Colab Notebooks

- **Notebook 1 (Main Analysis):**  
  https://colab.research.google.com/drive/1L5PM4_c0mgvQ4EWPr7lYVkzCUq0nw467?usp=sharing
   

## Data Files
Due to GitHub file size limitations, large CSV files are not stored in this repository.
All cleaned and processed datasets are generated via the Google Colab notebooks and stored in Google Drive.

## Project Structure

The project is stored in Google Drive at `/content/drive/MyDrive/ds_aditya_boddu/`:

```
ds_aditya_boddu/
├── notebook_1.ipynb                   # Main analysis notebook (run in Google Colab)
├── csv_files/                         # Processed data files
│   ├── cleaned_trades.csv             # Cleaned trading data
│   ├── sentiment_daily.csv            # Daily Fear & Greed Index data
│   ├── daily_trading_metrics.csv      # Aggregated daily trading metrics
│   └── merged_trading_sentiment.csv   # Merged trading and sentiment data
├── outputs/                           # Generated visualizations
│   ├── pnl_fear_vs_greed.png          # PnL comparison chart
│   ├── volume_fear_vs_greed.png       # Volume comparison chart
│   └── winrate_fear_vs_greed.png      # Win rate comparison chart
├── ds_report.pdf                      # Project report
└── README.md                          # This file
```

## Data Sources

1. **Historical Trading Data** (`historical_data.csv`)
   - Contains 211,224 trading records
   - Includes: account, coin, execution price, size, PnL, timestamps, and trade metadata

2. **Fear & Greed Index** (`fear_greed_index.csv`)
   - Contains 2,644 daily sentiment records
   - Includes: timestamp, value, classification (Fear/Greed), and date

## Analysis Steps

### Step 1: Data Loading & Understanding
- Load and explore trading and sentiment datasets
- Understand data structure and quality

### Step 2: Data Cleaning & Standardization
- Standardize column names (lowercase, snake_case)
- Convert timestamps to datetime format
- Extract trade dates for merging
- Remove unnecessary columns

### Step 3: Feature Engineering
- Create profitability indicator (`is_profitable`)
- Calculate trade volume metrics
- Aggregate daily trading metrics:
  - Total PnL
  - Average PnL
  - Total trading volume
  - Trade count
  - Win rate

### Step 4: Data Merging
- Merge daily trading metrics with Fear & Greed sentiment data
- Align data by date for correlation analysis

### Step 5: Exploratory Analysis
- Compare trading performance metrics between Fear and Greed periods
- Generate visualizations for:
  - Average Daily PnL
  - Average Trading Volume
  - Average Win Rate

## Key Metrics Analyzed

1. **Average Daily PnL**: Profit and loss comparison between sentiment periods
2. **Average Trading Volume**: Trading activity volume in USD
3. **Average Trades per Day**: Trading frequency
4. **Average Win Rate**: Percentage of profitable trades

## Visualizations

The project generates three comparison charts saved in the `outputs/` directory:
- `pnl_fear_vs_greed.png`: PnL performance comparison
- `volume_fear_vs_greed.png`: Trading volume comparison
- `winrate_fear_vs_greed.png`: Win rate comparison

## Requirements

To run this analysis, you'll need:
- Google Colab account
- Google Drive (for storing project files)
- Python 3.x (provided by Colab)
- pandas (pre-installed in Colab)
- matplotlib (pre-installed in Colab)

## Usage

1. Upload the project to your Google Drive in the `ds_aditya_boddu` folder

2. Ensure you have the required data files in your Colab environment:
   - `historical_data.csv`
   - `fear_greed_index.csv`

3. Open `notebook_1.ipynb` in Google Colab

4. The notebook will:
   - Mount your Google Drive
   - Process and clean the data
   - Generate daily metrics
   - Merge with sentiment data
   - Create visualizations
   - Save outputs to Google Drive in the respective directories (`csv_files/` and `outputs/`)

## Output Files

All processed data and visualizations are automatically saved:
- Cleaned datasets in `csv_files/`
- Visualization charts in `outputs/`

## Author

Aditya Boddu





