🛍️ Customer Shopping Behavior Analysis

A data analytics project that explores customer shopping patterns, purchasing habits, and behavioral trends using Python, PostgreSQL, and Jupyter Notebook.

📌 Project Overview

This project analyzes a customer shopping behavior dataset to uncover meaningful insights about:
- Customer demographics (age, gender, location)
- Purchase patterns (category, amount, season, frequency)
- Payment preferences and shipping types
- Subscription status and discount usage
- Review ratings and customer loyalty indicators

 📁 Dataset Features

| Column | Description |
|---|---|
| customer_id | Unique customer identifier |
| age | Customer age |
| gender | Customer gender |
| item_purchased | Item bought |
| category | Product category |
| purchase_amount | Amount spent |
| location | Customer location |
| size | Product size |
| color | Product color |
| season | Season of purchase |
| review_rating | Customer review score |
| subscription_status | Subscribed or not |
| shipping_type | Shipping method |
| discount_applied | Whether discount was used |
| previous_purchases | Number of past purchases |
| payment_method | Mode of payment |
| frequency_of_purchases | How often customer buys |
| age_group | Derived age group category |
| purchase_frequency_days | Days between purchases |

 🛠️ Tech Stack

- Python 3 (Jupyter Notebook)
- Pandas – Data manipulation and cleaning
- SQLAlchemy – Database ORM
- psycopg2 – PostgreSQL adapter
- PostgreSQL / pgAdmin 4– Database storage and management
- Matplotlib / Seaborn – Data visualization

 ⚙️ Setup Instructions

1. Clone the Repository
bash
git clone https://github.com/madhu-03-art/Customer_behavior_analysis.git
cd Customer_behavior_analysis

2. Install Dependencies
bash
pip install pandas sqlalchemy psycopg2-binary

3. Set Up PostgreSQL
- Install PostgreSQL and pgAdmin 4
- Create a database named customer_behavior
- Note your username, password, host, and port

 4. Configure Database Connection
In the notebook, update the connection details:
python
from sqlalchemy import create_engine
from urllib.parse import quote_plus

username = "postgres"
password = quote_plus("your_password")  # quote_plus handles special characters
host = "localhost"
port = "5432"
database = "customer_behavior"

engine = create_engine(f"postgresql+psycopg2://{username}:{password}@{host}:{port}/{database}")

 5. Run the Notebook
Open Customer_Shopping_Behavior_Analysis.ipynb in Jupyter and run all cells.

 📊 Key Analysis Steps

1. *Data Loading* – Import CSV dataset into a Pandas DataFrame
2. *Data Cleaning* – Handle duplicates, drop redundant columns, fix data types
3. *Exploratory Data Analysis (EDA)* – Understand distributions and relationships
4. *Feature Engineering* – Create age_group, purchase_frequency_days
5. *Database Export* – Push cleaned data to PostgreSQL via SQLAlchemy
6. *Insights & Visualization* – Identify trends in purchasing behavior


🗄️ Loading Data into PostgreSQL

python
table_name = "customer"
df.to_sql(table_name, engine, if_exists="replace", index=False)
print(f"Data successfully loaded into table '{table_name}' in database '{database}'.")

 📂 Project Structure

Customer_behavior_analysis/
│
├── Customer_Shopping_Behavior_Analysis.ipynb   
├── customer_shopping_behavior.csv              
└── README.md                                   

 🔍 Sample Insights

- Customers who use discounts tend to have higher purchase frequency
- Certain seasons show spikes in specific product categories
- Subscription customers have significantly more previous purchases
- Payment method preferences vary across age groups

 👩‍💻 Author

Madhu– [GitHub Profile](https://github.com/madhu-03-art)
