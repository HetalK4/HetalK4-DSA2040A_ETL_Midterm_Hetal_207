
## Project Title: ETL Pipeline (Extract -> Transform -> Load)

### 1. Project Overview:

A hands-on mini-project that extracts data, applies useful transformations, and loads it into a structured format.

### 2. ETL Phases:

#### a.) Extract: Description of '1_etl_extract.ipynb' and tasks done

- Loads and previews source data ('raw_data.csv' and 'incremental_data.csv').
- Inspects the data structure (.head(), .info()) of each dataset.
- Makes important observations such as:
    - identifies missing values (isnull().sum())
    - identifies suspicious rows (checking if each record is unique)
    - identifies duplicate rows (duplicated().sum())
- Saves raw copies to '1_data/' directory.


#### b.) Transfrom: Description of '2_etl_transform.ipynb' and tasks done

- Applied atleast 4 transformations to both data sets (raw_data.csv' and 'incremental_data.csv'):
    - Cleaning: handled missing values (numerical columns were filled with their corresponding mean and categorical columns were filled with their corresponding mode), removed duplicates.
    - Enrichment: Added and derived a new column 'total_price' (total_price = quantity * unit_price).
    - Structural: Converted data types (converted the data type for 'order_date' to a datetime format).
    - Filtering: Dropped irrelevant columns ('customer_name' if unused).
- Saved the transformed files to '2_transformed/' folder as CSV

#### c.) Load: Description of '3_etl_load.ipynb' and tasks done

- Loads both transformed files into Parquet (using pandas.to parquet())
- Previews the stored results (using pd.read_paraquet() then .head())
- Saves the outputs in the '3_loaded/' folder.
- Create a bar chart to visualize the total sales for each product.

### 3. Tools Used:

- Python, Jupyter Notebook, Pandas, PyArrow.

### 4. How to Run the Project:

- Ensure you have the necessary libraries installed (`pip install pandas pyarrow jupyter`)
- Clone the repository
- Follow the notebooks in order (1_etl_extract.ipynb -> 2_etl_transform.ipynb -> 3_etl_load.ipynb)
- Verify the outputs by checking '1_data/', '2_transformed/', and '3_loaded/' folders.

### 5. Screenshot of the bar chart:
- `Total_sales_by_Product.png`: the bar chart






