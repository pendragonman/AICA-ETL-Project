# AICA Data Engineering - ETL Project

This project is a submission for the AICA Data Engineering track. It is an ETL (Extract, Transform, Load) pipeline written in Python that merges data from a local CSV file with live data from the World Bank API.

## Project Tasks

The pipeline performs all 5 required tasks:
1.  **Extract:** Fetches data from the World Bank API (`raw_api_data.json`).
2.  **Transform:** Cleans both the `all_countries.csv` file and the API data.
3.  **Merge:** Merges the two datasets together based on country name.
4.  **Store (JSON):** Saves the raw, extracted API data.
5.  **Store (CSV):** Saves the final, transformed, and merged data (`transformed_country_data.csv`).

## Data Sources

* **Local File:** `all_countries.csv`
* **API:** World Bank V2 API - Countries endpoint (`https://api.worldbank.org/v2/country?format=json&per_page=300`)

## How to Run

1.  Make sure you have `pandas` and `requests` installed:
    ```bash
    pip install pandas requests
    ```
2.  Ensure `all_countries.csv` is in the same folder as the script.
3.  Run the main script:
    ```bash
    python etl_pipeline.py
    ```

The script will run the full ETL process and create the `raw_api_data.json` and `transformed_country_data.csv` files.
