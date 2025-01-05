# solar_flare_analysis
This project analyzes solar flare data from SpaceWeatherLive and NASA. It uses Python to scrape and clean data, combines datasets, and visualizes trends like flare intensity and timing. The goal is to better understand solar activity and its impacts.



# Long Story - Solar Flare Data Analysis and Integration

Solar flares are highly energetic events on the Sun that release vast amounts of radiation, impacting space weather and potentially affecting satellites, astronauts, and power grids on Earth. This project aims to analyze and integrate data from SpaceWeatherLive.com and NASA's Wind/WAVES Type II Burst Catalog to provide enriched insights into solar flare activity.

---

## Project Objectives
1. Scrape and process solar flare data from SpaceWeatherLive and NASA datasets.
2. Integrate and clean the datasets to ensure usability and consistency.
3. Analyze and visualize key patterns and trends in solar activity.
4. Provide actionable insights for better understanding solar flare characteristics.

---

## Data Sources
- **SpaceWeatherLive**: Top 50 solar flares ranked by intensity ([link](https://www.spaceweatherlive.com/en/solar-activity/top-50-solar-flares)).
- **NASA Wind/WAVES Type II Burst Catalog**: Data on radio-loud CMEs observed by the Wind spacecraft ([link](http://cdaw.gsfc.nasa.gov/CME_list/radio/waves_type2.html)).

---

## Methodology

### 1. Data Scraping
- Extracted data using Python libraries (`BeautifulSoup` and `pandas`) from:
  - SpaceWeatherLive’s top 50 solar flares table.
  - NASA’s Type II Burst catalog.
- Parsed raw HTML to structured dataframes.

### 2. Data Cleaning and Preparation
- Combined date and time fields into `datetime` objects for consistency.
- Handled missing values (`NaN`) and recoded non-numeric fields like "Halo" in CME angles.
- Standardized column formats for easier analysis and integration.

### 3. Integration and Matching
- Matched entries between the SpaceWeatherLive and NASA datasets using similarity criteria.
- Annotated NASA data with SpaceWeatherLive rankings for richer analysis.

### 4. Analysis and Visualization
- Reproduced the SpaceWeatherLive top 50 solar flare rankings using NASA data.
- Visualized trends such as flare intensity, frequency, and CME speed over time.
- Assessed the relationship between flare attributes, such as Halo CMEs and flare rankings.

---

## Key Findings
- SpaceWeatherLive rankings closely align with NASA data, confirming dataset reliability.
- High-intensity solar flares are associated with faster and wider CMEs, indicating potential risks.
- Halo CMEs are prevalent among the top-ranked solar flares, highlighting their large-scale impact.
- Temporal clustering of flares suggests periods of heightened solar activity.

---

## Technologies Used
- **Data Scraping**: `BeautifulSoup`, `requests`
- **Data Manipulation**: `pandas`, `numpy`
- **Visualization**: `matplotlib`, `seaborn`
- **Documentation**: Jupyter Notebook, HTML rendering

---

## How to View the Project
1. **HTML File**: The project is rendered into a user-friendly HTML format for easy viewing.
2. **Jupyter Notebook**: For those who wish to explore the code interactively, the `.ipynb` file is also available.

---

## Future Enhancements
- Automate data updates to include the latest solar flare information.
- Expand analysis to include lower-ranked flares and their potential impacts.
- Develop predictive models using historical data for forecasting solar activity.
