# VOIS_AICTE_Oct2025_chandrasekharj
# Airbnb Open Data Analysis

This project performs an exploratory data analysis (EDA) on the Airbnb Open Data dataset. The goal is to clean the data, uncover insights, and visualize patterns related to listings, pricing, host behavior, and geographical distribution in New York City.

 📈 Project Overview

The analysis starts with a raw dataset and applies several data cleaning and preprocessing techniques to make it suitable for analysis. Following the cleaning phase, various visualizations are generated to answer key questions about the Airbnb market in the analyzed region.

 💾 Dataset

The analysis uses the `Airbnb_Open_Data.csv` file. This dataset contains comprehensive information about Airbnb listings, including:
- Host details (ID, name, verification status)
- Listing location (neighborhood, latitude, longitude)
- Room type and pricing (price, service fee)
- Booking policies (minimum nights, cancellation policy)
- Review metrics (number of reviews, review rate)

 🧹 Data Cleaning and Preprocessing

To prepare the data for analysis, the following steps were performed:

- **Dropped irrelevant columns:** Columns with a high percentage of missing values (`house_rules`, `license`) were removed.
- **Removed duplicate records:** All duplicate rows were identified and dropped.
- **Cleaned and converted numeric columns:** The `price` and `service_fee` columns were cleaned by removing `$` and `,` characters, then converted to a numeric (float) type.
- **Standardized column names:** All column names were converted to lowercase and snake_case (e.g., `service fee` became `service_fee`).
- **Handled outliers:** Records with illogical data, such as an `availability_365` value greater than 365, were removed.
- **Removed missing values:** All remaining rows containing any `NaN` values were dropped to ensure a complete dataset for visualization.

 📊 Key Analysis and Visualizations

The Jupyter Notebook explores several questions, visualized through various plots:

1.  **Distribution of Room Types:** A count plot shows the frequency of different room types (`Entire home/apt`, `Private room`, etc.).
2.  **Listings by Neighbourhood Group:** A bar chart illustrates the number of listings in each neighborhood group (e.g., Brooklyn, Manhattan).
3.  **Average Price by Neighbourhood Group:** This visualization compares the average listing price across different neighborhood groups.
4.  **Construction Year vs. Price:** A line plot shows the trend of average listing prices based on the property's construction year.
5.  **Top 10 Hosts:** A bar chart identifies the hosts with the highest number of listings.
6.  **Host Verification and Reviews:** Analysis of the average review rate based on whether a host's identity is verified.
7.  **Price and Service Fee Correlation:** A regression plot demonstrates the strong positive correlation between the listing price and the service fee.
8.  **Host Listings vs. Availability:** A regression plot explores the relationship between a host's total listings count and the property's availability throughout the year.

 🛠️ Libraries Used

This analysis relies on the following Python libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `plotly`
