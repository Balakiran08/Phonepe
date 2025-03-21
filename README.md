# Phonepe
PhonePe Pulse Data Analytics is an interactive dashboard analyzing India's digital payment trends using PhonePe's Pulse data. Built with Python, Streamlit, and Plotly, it offers insights into transactions, user behavior, and geographical trends, with data preprocessing for state names and pincodes. Powered by PostgreSQL.
# PhonePe Pulse Data Analytics

## Overview

This project is a comprehensive data analytics dashboard for PhonePe transactions across India. It provides insights into transaction trends, user behavior, and geographical distribution of digital payments. The dashboard is built using Python, Streamlit, and Plotly, with data stored in a PostgreSQL database. The project leverages data from PhonePe's Pulse GitHub repository to visualize and analyze transaction and user data.

## Features

- **Interactive Dashboard**: Explore transaction and user data through interactive visualizations.
- **Geographical Analysis**: Visualize transaction and user data on an India map.
- **Time Series Analysis**: Analyze trends over time with quarterly and yearly breakdowns.
- **Insights**: Gain insights into top and bottom-performing states, districts, and transaction types.
- **Data Preprocessing**: Includes data cleaning steps such as replacing state names and removing empty pincode records.

## Technologies Used

- **Python**: Primary programming language for data processing and visualization.
- **Streamlit**: Framework for building interactive web applications.
- **Plotly**: Library for creating interactive charts and maps.
- **PostgreSQL**: Database for storing and querying transaction and user data.
- **Git**: Version control for managing the project codebase.

## Installation

1. **Clone the Repository**:
   ```bash
      !git clone https://github.com/PhonePe/pulse.git
   ```

2. **Set Up PostgreSQL Database**:
   - Install PostgreSQL and create a database named `phonepe`.
   - Update the database connection details in the script:
     ```python
     mydb = psycopg2.connect(
         host='localhost',
         user='postgres',
         port='5432',
         database='phonepe',
         password='your_password'
     )
     ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
  # requirements.txt

      pandas==2.0.3
      numpy==1.24.3
      psycopg2==2.9.6
      plotly==5.15.0
      matplotlib==3.7.1
      streamlit==1.26.0

4. **Run the Streamlit App**:
   ```bash
    streamlit run Phonepe.py
   ```
## Usage

1. **Home Page**: Provides an overview of the dashboard and its features.
2. **Data Analysis**:
   - **Transaction Analysis**: Explore transaction data by state, year, and quarter.
   - **User Analysis**: Analyze user data by state, year, and quarter.
3. **Time Series Analysis**:
   - **Transaction Trends**: Analyze transaction trends over time.
   - **User Trends**: Analyze user trends over time.
4. **Insights**: Gain insights into top and bottom-performing states, districts, and transaction types.

## Data Preprocessing

The raw data from PhonePe's Pulse repository undergoes several preprocessing steps to ensure consistency and accuracy:

1. **State Name Standardization**:
   - Replace inconsistent state names with standardized versions (e.g., `andaman-&-nicobar-islands` → `Andaman & Nicobar`).
   - Handle special characters and formatting (e.g., `dadra-&-nagar-haveli-&-daman-&-diu` → `Dadra and Nagar Haveli and Daman and Diu`).

2. **Removing Empty Pincode Records**:
   - Filter out records with empty or invalid pincodes to ensure data quality.

3. **Data Cleaning**:
   - Handle missing or inconsistent data in transaction and user datasets.
   - Convert data types (e.g., string to integer) for numerical columns.

## Data Sources

- **PhonePe Pulse GitHub Repository**: The data used in this project is sourced from PhonePe's Pulse GitHub repository. The repository is cloned and processed to extract relevant data for analysis.





