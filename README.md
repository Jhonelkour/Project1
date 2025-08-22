# Weather Dataset Analysis Project

## Overview
This project performs comprehensive exploratory data analysis on a weather dataset using Python and pandas. The analysis includes data exploration, statistical calculations, filtering operations, and answering specific questions about weather patterns and conditions.

## Project Structure
```
Project1/
├── Project1.ipynb                    # Main Jupyter notebook with analysis
├── Project_ 1_Weather Dataset.csv    # Weather dataset (CSV format)
├── README.md                         # This file
└── .vscode/                         # VS Code configuration
```

## Dataset Information
The weather dataset contains the following columns:
- **Date/Time**: Timestamp of weather observations
- **Temp_C**: Temperature in Celsius
- **Dew Point Temp_C**: Dew point temperature in Celsius
- **Rel Hum_%**: Relative humidity percentage
- **Wind Speed_km/h**: Wind speed in kilometers per hour
- **Visibility_km**: Visibility in kilometers
- **Press_kPa**: Atmospheric pressure in kilopascals
- **Weather_Condition**: Weather condition description (originally named 'Weather')

## Prerequisites
- Python 3.x
- Jupyter Notebook or JupyterLab
- Required Python packages:
  - pandas
  - numpy (implicitly used with pandas)

## Installation
1. Clone or download this project to your local machine
2. Install required packages:
   ```bash
   pip install pandas jupyter
   ```
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Open `Project1.ipynb`

## Analysis Overview

### Data Exploration
The notebook begins with comprehensive data exploration including:
- Loading the dataset using pandas
- Displaying first and last few rows (`head()`, `tail()`)
- Checking dataset shape and structure
- Examining data types and column information
- Identifying unique values and null values

### Key Questions Answered

#### 1. **Unique Wind Speed Analysis**
- Finds all unique wind speed values in the dataset
- Counts the number of distinct wind speed measurements

#### 2. **Clear Weather Analysis**
- Counts instances when weather condition is exactly "Clear"
- Uses value counting and filtering techniques

#### 3. **Specific Wind Speed Analysis**
- Identifies all instances when wind speed was exactly 4 km/h
- Demonstrates precise filtering capabilities

#### 4. **Data Quality Assessment**
- Identifies all null values in the dataset
- Provides data completeness statistics

#### 5. **Data Cleaning**
- Renames the 'Weather' column to 'Weather_Condition' for clarity
- Demonstrates data preprocessing techniques

#### 6. **Statistical Analysis**
- Calculates mean visibility across all observations
- Provides descriptive statistics for visibility data

#### 7. **Pressure Variability**
- Computes standard deviation of atmospheric pressure
- Assesses pressure variability in the dataset

#### 8. **Humidity Analysis**
- Calculates variance of relative humidity
- Measures humidity distribution spread

#### 9. **Snow Event Detection**
- Identifies all instances when snow was recorded
- Uses both exact matching and string pattern matching

#### 10. **Complex Filtering**
- Finds instances with wind speed > 24 km/h AND visibility = 25 km
- Demonstrates compound logical operations

#### 11. **Grouped Statistics**
- Calculates mean values for each column grouped by weather condition
- Provides insights into weather pattern relationships

#### 12. **Extreme Value Analysis**
- Finds minimum and maximum values for each weather condition
- Identifies weather-specific ranges for all variables

#### 13. **Fog Analysis**
- Extracts all records where weather condition is fog
- Focuses on specific weather phenomena

#### 14. **OR Logic Filtering**
- Finds instances where weather is clear OR visibility > 40 km
- Demonstrates logical OR operations

#### 15. **Complex Multi-condition Analysis**
- Combines multiple conditions with AND/OR logic
- Advanced filtering: (Clear weather AND humidity > 50%) OR (visibility > 40 km)

## Key Features

### Data Analysis Techniques Used
- **Data Loading**: CSV file reading with pandas
- **Data Exploration**: Shape, info, describe, head/tail analysis
- **Data Cleaning**: Column renaming, null value handling
- **Statistical Analysis**: Mean, standard deviation, variance calculations
- **Filtering**: Single and multi-condition filtering
- **Grouping**: GroupBy operations for categorical analysis
- **String Operations**: Pattern matching for text data

### Programming Concepts Demonstrated
- Pandas DataFrame operations
- Boolean indexing and filtering
- Logical operators (AND, OR)
- String methods and pattern matching
- Statistical functions
- Data aggregation and grouping

## Sample Usage
```python
# Load the dataset
import pandas as pd
df = pd.read_csv("Project_ 1_Weather Dataset.csv")

# Basic exploration
df.head()
df.info()
df.describe()

# Example filtering
clear_weather = df[df['Weather_Condition'] == 'Clear']
high_wind = df[df['Wind Speed_km/h'] > 24]
```

## Results Summary
The analysis reveals insights about:
- Weather pattern distributions
- Statistical properties of meteorological variables
- Frequency of specific weather conditions
- Relationships between different weather parameters
- Data quality and completeness

## Learning Outcomes
This project demonstrates:
- Fundamental pandas operations for data analysis
- Data exploration and quality assessment techniques
- Statistical analysis of real-world datasets
- Complex filtering and querying operations
- Best practices for data science workflows

## Future Enhancements
Potential improvements could include:
- Data visualization with matplotlib/seaborn
- Time series analysis of weather patterns
- Correlation analysis between variables
- Predictive modeling for weather forecasting
- Geographic analysis if location data is available

## Contributing
Feel free to fork this project and submit improvements or additional analysis questions.

## License
This project is for educational purposes. Please check the dataset license for commercial use.

---
*Last updated: August 2025*
