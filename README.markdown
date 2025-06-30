# Daily Transactions Analysis

## Project Overview
The **Daily Transactions Analysis** project is a data analysis initiative that explores a dataset of daily household financial transactions to uncover spending patterns, trends, and insights. Using Python in a Google Colab environment, the project performs data cleaning, exploratory data analysis (EDA), time series analysis, and correlation analysis. Visualizations such as histograms, countplots, boxplots, and heatmaps are generated to provide actionable insights for budgeting and financial planning.

### Objectives
- **Data Cleaning**: Handle missing values, convert data types, and remove duplicates.
- **Exploratory Data Analysis (EDA)**: Analyze transaction distributions, top categories, payment modes, and income vs. expense patterns.
- **Time Series Analysis**: Examine monthly and daily spending trends to identify seasonality.
- **Correlation Analysis**: Investigate relationships between transaction categories.
- **Reporting**: Summarize findings with visualizations in a comprehensive report.

### Dataset
The dataset, `Daily Household Transactions.csv`, contains 2461 transactions with the following columns:
- **Date**: Date and time of the transaction (e.g., `20/09/2018 12:04:08`).
- **Mode**: Payment method (e.g., Cash, Saving Bank account 1, Credit Card).
- **Category**: Transaction category (e.g., Food, Transportation, Household).
- **Subcategory**: Transaction subcategory (e.g., Snacks, Train, Netflix; 635 missing values).
- **Note**: Description of the transaction (e.g., "Idli medu Vada mix 2 plates"; 521 missing values).
- **Amount**: Transaction amount in INR (e.g., 30.0).
- **Income/Expense**: Type of transaction (Income, Expense, or Transfer-Out).
- **Currency**: Currency of the transaction (all INR).

**Source**: The dataset is referenced from [Kaggle](https://www.kaggle.com/datasets/path/to/daily-transactions-dataset) (replace with actual link if available).

## Prerequisites
- **Google Colab Account**: Required to run the notebook.
- **Python Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Plotly (optional for interactive visualizations).
- **Dataset**: `Daily Household Transactions.csv` (download from Kaggle or use a similar dataset).
- **Google Drive**: Optional for storing the dataset and saving outputs.

## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/daily-transactions-analysis.git
   cd daily-transactions-analysis
   ```

2. **Upload to Google Colab**:
   - Open [Google Colab](https://colab.research.google.com/).
   - Upload `Daily_Transactions.ipynb` via **File > Upload Notebook**.

3. **Install Dependencies**:
   - Most required libraries (Pandas, NumPy, Matplotlib, Seaborn) are pre-installed in Colab.
   - Install Plotly for interactive visualizations (optional):
     ```python
     !pip install plotly
     ```
   - Install `nbconvert` for PDF export:
     ```python
     !pip install nbconvert
     ```

4. **Prepare the Dataset**:
   - Download `Daily Household Transactions.csv` from Kaggle or your source.
   - Upload to Google Drive (e.g., `/MyDrive/Datasets/`) or directly to Colab's file system.
   - Update the dataset path in the notebook (e.g., `/content/drive/MyDrive/Datasets/Daily Household Transactions.csv`).

## Usage
1. **Open the Notebook**:
   - In Google Colab, open `Daily_Transactions.ipynb`.

2. **Mount Google Drive** (if using Drive for dataset storage):
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

3. **Run the Notebook**:
   - Execute cells sequentially by clicking the **Run** button or pressing `Shift + Enter`.
   - The notebook is divided into sections:
     - **Setup and Library Imports**: Imports Pandas, NumPy, Matplotlib, Seaborn.
     - **Data Loading and Inspection**: Loads the dataset and displays initial information.
     - **Data Cleaning**: Handles missing values, converts `Date` to datetime, removes duplicates.
     - **Exploratory Data Analysis (EDA)**: Generates histograms, countplots, and boxplots.
     - **Time Series Analysis**: Plots monthly and daily transaction trends.
     - **Correlation Analysis**: Creates a heatmap of category correlations.
     - **Additional Analyses**: Computes average spending, income/expense totals, and category trends.
     - **Interactive Visualizations**: Optional Plotly plots.
     - **Export**: Converts the notebook to PDF.

4. **Save Outputs**:
   - Visualizations are saved as PNG files in `/content/drive/MyDrive/Datasets/` (adjust path as needed).
   - The final report includes embedded images of visualizations.
   - Export the notebook as a PDF:
     ```python
     !jupyter nbconvert --to pdf /content/Daily_Transactions.ipynb --output /content/drive/MyDrive/Datasets/Daily_Transactions_Report.pdf
     ```

## Project Structure
- `Daily_Transactions.ipynb`: Main Jupyter notebook containing all code and analysis.
- `Daily Household Transactions.csv`: Dataset file (not included in repo; download separately).
- `/Datasets/`: Recommended folder for storing dataset and output visualizations (e.g., PNGs, HTMLs for Plotly).

## Key Findings
- **Transaction Distribution**: Amounts are right-skewed, with most transactions below INR 1000 (median ~INR 50).
- **Top Categories**: Food (37%, 907 transactions), Transportation (12%, 307), Household (7%, 176).
- **Payment Modes**: Saving Bank account 1 (50%, 1223 transactions), Cash (42%, 1046), Credit Card (7%, 162).
- **Income vs. Expense**: Expenses dominate (90%+ transactions), with income from Salary and Investments.
- **Time Series Trends**: Monthly trends show seasonal peaks (e.g., festival months like Ganesh Pujan, Diwali).
- **Correlations**: Strong relationships between Food and Household spending, indicating combined household expenses.

## Visualizations
The notebook generates the following visualizations (saved as PNGs):
1. **Distribution of Transaction Amounts**: Histogram showing right-skewed amounts.
2. **Transaction Counts by Category**: Countplot of top 5 categories (Food, Transportation, etc.).
3. **Transaction Counts by Subcategory**: Countplot of top 10 subcategories.
4. **Transaction Counts by Mode**: Countplot of top 3 payment modes.
5. **Transaction Counts by Income/Expense**: Countplot of Income vs. Expense.
6. **Transaction Amounts by Category**: Boxplot for top 5 categories.
7. **Transaction Amounts by Subcategory**: Boxplot for top 10 subcategories.
8. **Transaction Amounts by Income/Expense**: Boxplot comparing amounts.
9. **Monthly Transaction Amounts**: Line plot of total amounts per month.
10. **Daily Transaction Amounts**: Line plot of total amounts per day.
11. **Correlation Heatmap**: Heatmap of category correlations.
12. **Monthly Spending by Category** (Additional): Line plot of category-wise spending trends.

Interactive Plotly visualizations (optional) are saved as HTML files.

## Report
The final report is included in the notebook as a Markdown cell, summarizing:
- Data cleaning steps.
- EDA findings (distributions, top categories, modes).
- Time series and correlation insights.
- Embedded visualizations for easy reference.

To view the report with visualizations, run the notebook and ensure images are saved to the specified path.

## Future Improvements
- **Predictive Modeling**: Add time series forecasting (e.g., ARIMA) to predict future spending.
- **Interactive Dashboard**: Develop a Streamlit or Dash app for interactive exploration.
- **Category Segmentation**: Analyze subcategories within high-spending categories (e.g., Food).
- **Outlier Detection**: Implement methods to identify and handle extreme transaction amounts.

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make changes and commit (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

Please ensure code follows Python PEP 8 style guidelines and includes comments for clarity.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Dataset sourced from [Kaggle](https://www.kaggle.com/) (replace with actual dataset link).
- Built using Google Colab, Pandas, NumPy, Matplotlib, Seaborn, and Plotly.
- Inspired by financial data analysis tutorials and best practices.

## Contact
For questions or feedback, please open an issue on GitHub or contact gauthampre123@gmail.com.
