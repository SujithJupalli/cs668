# NYC Air Quality analysis [March 2004 to February 2005]
Sai Sujith Reddy / Jupalli

* This work was realized as part of the capstone project of the MS in Data Science at Pace University
* **Abstract**:
* **Dataset**:
   * Measurements of different air pollutants and weather parameters including temperature. The measurements were recorded every hour and were obtained from AirQualityUCI dataset.
   * A few important aspects are:
      *  Air Pollutants: CO, NOx, NO2 and Benzene C6H6.
      * Sensors: Tin oxide for CO, Titania for NMHC, Tungsten oxide for NOx, and indium oxide for O3
      * Climatic Condition: temperature (T), relative humidity (RH), and absolute humidity (AH)
   * ​Size: Total number of the entries are 9357
* The dataset is available here: https://archive.ics.uci.edu/dataset/387/air+quality
* **Methodology**:
 * Data Cleaning and Preprocessing:
      * Handling Missing Values: Placeholder values for missing data (-200) are replaced with pd.NA to standardize the data for analysis.
      * Data Conversion: Date and time columns are converted to a datetime format to facilitate time-series analysis and seasonal trend identification.
      * Feature Selection: Unnecessary columns are removed to focus on relevant pollutants and environmental variables, primarily CO, NOx, Benzene, temperature,            and humidity.
 * Exploratory Data Analysis (EDA):
      * Time-Series Analysis: Pollutants (CO, NOx, Benzene) are plotted over time to observe seasonal variations, revealing a pattern of increased pollution levels         during colder months.
      * Correlation Matrix: A correlation matrix is generated to explore relationships between pollutants and environmental factors, such as temperature and                humidity. This analysis highlights inverse relationships, such as lower temperatures correlating with higher pollutant concentrations.
 * Predictive Modeling:
      * SARIMAX Model: A Seasonal Autoregressive Integrated Moving Average with Exogenous Variables (SARIMAX) model is used for time-series forecasting. This 
        statistical model captures seasonal patterns and dependencies in the data, providing short-term forecasts for pollutant levels.
      * LSTM Model: A Long Short-Term Memory (LSTM) neural network model is also developed to predict air quality indices. LSTM, a deep learning approach, is 
        capable of capturing complex temporal dependencies, enhancing forecast accuracy over longer periods.
 * Model Evaluation:
      * Both SARIMAX and LSTM models are evaluated to determine predictive accuracy. By comparing their performance, the study identifies which approach is more 
        effective for forecasting air quality in urban environments.
* **Code**:
        https://github.com/SujithJupalli/cs668/blob/cc915c4a613e8e18528ef919dfc17d6f51765b19/Capstone_Sujith_NY_AirQuality_analysis.ipynb
* **Results**:

     * CO, NOx, and Benzene show a maximum in the coldest months of the year, clearly evidencing the contribution of heating activities and typical conditions of atmospheric stability in urban areas. The correlation study points to an inverse relation of temperature with pollution levels, while the variation in humidity has mixed effects many times favorable to pollutant dispersion. Predictive modeling by SARIMAX and LSTM showed that historical data could reliably forecast the future air quality indices, capturing the seasonal pattern and complex temporal dependencies. The SARIMAX model and LSTM model Combined, these give a full understanding of the dynamics in urban air quality and its possible implications for public health.​
* **Poster**:
* ![image](https://github.com/user-attachments/assets/b698ab40-e8f8-4c87-9ff0-4b59cd2de197)


