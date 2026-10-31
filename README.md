# 💰 AI Expense Tracker

A Python and Jupyter Notebook project that helps categorize expenses, analyze monthly spending, monitor budgets, identify unusual transactions, and export financial reports.

> **Privacy note:** The notebook uses synthetic demo transactions by default. If you use real financial records, keep them private and never commit bank statements or personal financial information to a public GitHub repository.

## ✨ Features

- 🤖 Automatic expense categorization
- 🧠 TF-IDF and Logistic Regression classification demo
- 📊 Monthly spending summaries
- 📈 Category-wise expense visualization
- 💰 Configurable budget tracking
- 🚨 Overspending alerts
- 🔍 Unusual transaction detection
- 💬 Simple natural-language spending queries
- 📁 CSV report export
- 🔒 Local-first execution without an API key

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Transaction data processing |
| NumPy | Numerical calculations |
| Matplotlib | Spending visualizations |
| Scikit-learn | Text classification |
| TF-IDF | Transaction description vectorization |
| Logistic Regression | Expense category prediction |
| Jupyter Notebook | Interactive development |

## 📁 Project Structure

```text
ai-expense-tracker/
│
├── ai_expense_tracker.ipynb
├── README.md
├── requirements.txt
├── .env.example
└── .gitignore
```

## ⚙️ Requirements

- Python 3.10 or later
- Jupyter Notebook or Google Colab
- Basic knowledge of Python and data analysis

No API key is required to run the included demonstration.

## 🚀 Getting Started

### 1. Clone the repository

Replace `YOUR_USERNAME` with your GitHub username.

```bash
git clone https://github.com/YOUR_USERNAME/ai-expense-tracker.git
```

### 2. Navigate to the project directory

```bash
cd ai-expense-tracker
```

### 3. Create a virtual environment

**Windows PowerShell**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS/Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Launch Jupyter Notebook

```bash
jupyter notebook ai_expense_tracker.ipynb
```

Run the notebook cells from top to bottom.

## 🧠 How It Works

### 1. Transaction Data Processing

The project loads transaction records containing:

- Transaction date
- Transaction description
- Transaction amount
- Category label for the demo dataset

It validates the data and identifies income and expenses.

Positive amounts represent income, while negative amounts represent expenses.

### 2. Automatic Expense Categorization

The notebook first uses explainable keyword rules to categorize transactions into groups such as:

- Groceries
- Dining
- Transport
- Housing
- Utilities
- Shopping
- Healthcare
- Entertainment
- Income
- Other

These rules provide a simple baseline that can be inspected and customized.

### 3. Machine Learning Classification

The notebook demonstrates a text classification pipeline using:

- TF-IDF vectorization
- Logistic Regression
- Training and test data
- Classification metrics

The classifier learns patterns from the labeled synthetic transaction descriptions.

**Important:** The included dataset is small and intended for demonstration. Its classification performance should not be interpreted as production-level accuracy.

### 4. Monthly Spending Analysis

The tracker calculates total expenses for each month.

It creates a chart that helps compare spending between months and identify changes in expenditure.

### 5. Category-Wise Expense Analysis

Transactions are grouped by category to calculate total spending.

A bar chart helps identify the categories accounting for the largest share of expenses.

### 6. Budget Monitoring

Users can define spending limits for individual categories.

For example:

```python
budgets = {
    "Groceries": 6000,
    "Dining": 2500,
    "Transport": 3000,
    "Shopping": 4000,
    "Utilities": 3500,
    "Entertainment": 1500,
    "Healthcare": 2500,
    "Housing": 12000,
    "Other": 2000
}
```

These amounts are illustrative examples. Customize them to suit your circumstances.

The budget report shows:

- Category budget
- Actual spending
- Remaining budget
- Budget status

When spending exceeds a category's limit, the report marks it as `OVER BUDGET`.

### 7. Unusual Expense Detection

The project uses a robust statistical threshold based on the median and median absolute deviation to flag potentially unusual expenses.

These flags can help identify transactions that deserve closer inspection.

They do not prove fraud, financial misconduct, or incorrect transactions.

### 8. Natural-Language Spending Queries

The notebook includes a simple rule-based question-answering function.

Example questions include:

```text
What are my total expenses?
Which category has the highest spending?
How much did I spend on groceries?
What is my total income?
```

The function recognizes only a limited set of question patterns. It is a demonstration of basic natural-language query handling, not a general-purpose conversational AI assistant.

### 9. Report Export

The notebook exports categorized transactions, budget reports, and unusual-expense review results as CSV files.

Generated reports are saved in:

```text
expense_tracker_exports/
```

Avoid committing private financial exports to a public repository.

## 📊 Example Output

The notebook produces:

- Total income
- Total expenses
- Net cash flow
- Monthly spending summaries
- Category-wise spending charts
- Budget monitoring reports
- Unusual transaction review tables
- Categorized transaction CSV files

The exact values depend on the transactions provided.

## 🔐 Privacy and Security

The project uses synthetic data by default and does not send financial records to an external API.

Before using real financial records:

- Keep bank statements and exports in a private location.
- Remove unnecessary personal and account information.
- Never upload API keys or private financial records to a public GitHub repository.
- Restrict access to generated reports.
- Review transaction categories and unusual-expense alerts manually.

## ⚠️ Limitations

- The demo dataset is synthetic.
- The classification model uses a small set of labeled examples.
- Expense categories may be incorrect.
- Unusual-expense flags require human review.
- Natural-language queries support only a limited set of patterns.
- The project does not connect directly to a bank.
- It is not a financial adviser or a fraud-detection system.

## 🔮 Future Enhancements

Potential improvements include:

- CSV and Excel bank statement import
- Interactive Streamlit dashboard
- Manual transaction editing and category correction
- Recurring payment and subscription detection
- Receipt scanning with OCR
- Better classification using user-reviewed transaction labels
- Secure database storage
- Authentication and user-specific budgets
- Optional LLM-powered financial summaries
- Automated monthly expense reports

## 🎯 Learning Outcomes

By completing this project, you will gain experience with:

- Python data analysis
- Financial transaction processing
- Text classification using machine learning
- Data visualization
- Budget tracking
- Statistical anomaly detection
- CSV report generation
- Building a reproducible Jupyter Notebook project

## 📄 License

Choose a license before publishing this repository publicly. MIT is one option for an open-source portfolio project.

---

**Built as an Applied AI and Machine Learning portfolio project.**
