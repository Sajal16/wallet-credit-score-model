# 🏦 Wallet Credit Score Model

This project presents a **DeFi wallet credit scoring model** designed to analyze user wallet behavior on the blockchain and assign a credit score along with a risk label (`High Risk`, `Medium Risk`, or `Low Risk`). The scoring is based on on-chain transaction activity and wallet engagement metrics.


## 📌 Problem Statement

Given user wallet transaction data on a DeFi platform, build a **Credit Scoring System** to:
- Calculate a **credit score** based on transaction behavior.
- Classify each wallet into **risk categories**.
- Output the final result as a CSV file with `wallet`, `score`, and `risk_label`.


## 🛠️ Technologies Used

- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **Jupyter Notebook**
- **Scikit-learn** (for scaling)
- **Git/GitHub**


## 📂 Dataset Columns

| Feature               | Description                                               |
|----------------------|-----------------------------------------------------------|
| userWallet           | Wallet address (unique identifier)                        |
| tx_count             | Total transactions                                        |
| deposit_count        | Number of deposits                                        |
| borrow_count         | Number of borrows                                         |
| repay_count          | Number of repayments                                      |
| liquidation_count    | Times liquidated                                          |
| total_value_usd      | Total USD value transacted                                |
| active_days          | Days active on platform                                   |
| repay_borrow_ratio   | Ratio of repay_count to borrow_count                      |


## 🧮 Scoring Formula

```python
score = (
    repay_borrow_ratio * 400 +
    deposit_count * 0.5 +
    active_days * 2 -
    liquidation_count * 100
)


The score is then scaled to the range [0, 1000] using MinMaxScaler.

Based on the score, wallets are labeled:

Credit Score	     Risk Label
< 100	             High Risk
100–249            Medium Risk
≥ 250	             Low Risk

How to Run
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/wallet-credit-score-model.git
Open the Jupyter Notebook.

Install dependencies (if needed):

bash
Copy code
pip install pandas numpy matplotlib seaborn scikit-learn
Run all cells to generate the score and export the result CSV.

📧 Contact
For questions, contact Sajal Aggarwal at sajal162004@gmail.com.


### ✅ What to do now:
1. Go to your GitHub repo.
2. Open the `README.md`.
3. Click ✏️ (Edit).
4. Replace the current two-line description with the **above full version**.
5. Click **"Commit changes"**.
