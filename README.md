# Project README: RetailPulse Project

## Project Overview

This project analyzes sales trends and evaluates the effectiveness of marketing campaigns using advanced data analysis techniques. The project leverages Python for data preprocessing, analysis, visualization, and forecasting while incorporating methods for measuring campaign performance and predicting future sales. The project is designed to provide actionable insights into customer behavior, sales patterns, and campaign impact.

---

## Key Features

1. **Sales Data Aggregation**:

   - Monthly sales data is aggregated and cleaned for analysis.
   - Missing or irregular data points are handled to ensure accuracy.

2. **Campaign Effectiveness Analysis**:

   - Sales metrics such as total sales, average sales, and unique customers are calculated for periods before and after marketing campaigns.
   - A reusable module (`analyze_campaign_effectiveness`) is implemented to automate the analysis process.

3. **Forecasting Sales**:

   - Exponential Smoothing is used to forecast sales for the next 12 months.
   - Seasonal trends and patterns are identified and incorporated into the forecasts.

4. **Data Visualization**:

   - Interactive visualizations, including bar charts and time-series plots, are created to display sales trends and forecast results.

5. **Tableau Visualizations**:

   - A Tableau workbook (`sales_visualizations.twbx`) contains detailed dashboards and visualizations for deeper insights into sales and campaign data.

6. **Project Documentation**:

   - The project documentation (`project_documentation.docx`) provides a detailed overview of methodologies, assumptions, and insights generated during the analysis.

---

## Technologies and Tools

- **Programming Language**: Python
- **Libraries**:
  - Data Analysis: `pandas`, `numpy`
  - Visualization: `matplotlib`, `seaborn`
  - Time Series Forecasting: `statsmodels`
- **Tools**:
  - Jupyter Notebook
  - Tableau (for dashboards and visualizations)
  - Microsoft Word (for documentation)

---

## File Structure

```
Sales_Project/
│
├── dashboard/
│   └── RetailPulse.twbx                # Tableau workbook with dashboards
│
├── data/
│   ├── city_to_coords.json             # JSON file mapping cities to coordinates
│   ├── filtered_sales_data.csv         # Filtered sales dataset
│   ├── merged_sales_holidays.csv       # Merged sales and holidays dataset
│   ├── publicHolidays.csv              # Public holidays dataset
│   ├── RetailPulse Project.ipynb       # Jupyter notebook for RetailPulse analysis
│   ├── sales_heatmap.html              # Sales heatmap visualization
│   ├── Sample - Superstore.csv         # Sample dataset (Superstore)
│   ├── updated_sales_with_coordinates.csv # Updated sales dataset with coordinates
│   ├── weather_data.csv                # Full weather dataset
│   ├── weather_data_partial.csv        # Partial weather data
│
├── previous_weather_data.csv           # Archived weather data
│
└── Retail Pulse.docx                   # Project documentation
```

---

## Steps to Run the Project

1. Clone the repository and navigate to the project folder:
   ```bash
   git clone https://github.com/ParagTippannawar/RetailPulse
   cd project-folder
   ```
2. Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the Jupyter Notebook to execute the project:
   ```bash
   jupyter notebook data/RetailPulse Project.ipynb 
   ```
4. jupyter notebook notebooks/sales\_analysis.ipynbFollow these steps in the notebook:
   - **Step 1**: Load the dataset and preprocess it.
   - **Step 2**: Analyze the effectiveness of marketing campaigns using the provided module.
   - **Step 3**: Generate forecasts using Exponential Smoothing.
   - **Step 4**: Visualize the results (campaign analysis and sales forecasts).
5. Open the Tableau workbook (`sales_visualizations.twbx`) to explore interactive dashboards.
6. Refer to the project documentation (`project_documentation.docx`) for detailed explanations and insights.
7. Use the outputs in the `outputs/` folder for further insights and reporting.

---

## Limitations

- This project planned to integrate Apache Airflow for workflow orchestration, but it was not feasible due to the technical limitations of the system. Windows 11 Home lacks support for WSL2 (Windows Subsystem for Linux 2), which is required to run Airflow natively or via Docker. These features, such as Hyper-V and Virtual Machine Platform, are only available on Windows 11 Pro or higher editions, limiting the automation capabilities of the data pipeline that was intended to be included.

- The project aimed to incorporate weather data for enhanced analysis using a free Weather API. However, due to the limitations of the free subscription, retrieving data at scale was challenging. Workarounds such as batch API calls were implemented, but the API provided insufficient data points for accurate analysis. To maintain accuracy, the weather data was excluded from the final analysis. The code for ingesting data from the Weather API is still included in the Python notebook for reference.

