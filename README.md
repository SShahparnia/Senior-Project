# Analysis of Traffic Accidents in the US

## Overview
This project aims to identify key risk factors associated with traffic accidents across the United States and to develop a predictive model that estimates accident likelihood. By leveraging the comprehensive Kaggle "US Accidents" dataset along with complementary road network GIS data, the project conducts an in-depth exploration of how time, weather, road features, and nearby points of interest contribute to accident rates. The insights gained are intended to support urban planning, traffic safety strategies, and the advancement of autonomous vehicle technologies.

## Project Description
The project addresses several research themes through exploratory data analysis (EDA) and machine learning:

- **Temporal and Weather Patterns:**  
  Analyze accident frequency variations across different times (hours, days, seasons) and study the impact of weather conditions such as temperature, rain, and visibility on accident occurrence and severity.

- **Road Features and Urban vs. Rural Analysis:**  
  Examine how road attributes—including road types, speed limits, number of lanes, and intersection features—affect accident outcomes, comparing these dynamics between urban and rural areas.

- **Additional Factors and Clustering:**  
  Investigate the role of nearby infrastructure (e.g., speed bumps, give-way signs, railway crossings) on accident likelihood and identify geographic clusters (hotspots) where accidents occur more frequently.

- **Predictive Modeling:**  
  Develop and validate a machine learning model (for example, a random forest classifier) that leverages the aforementioned factors to estimate accident risk, providing a tool that may assist urban planners and traffic management agencies.

## Data Sources
- **US Accidents Dataset (Kaggle):**  
  Contains over 7.7 million records of traffic accidents from 2016 to 2021, featuring more than 40 columns of detailed information, including timestamps, weather conditions, road types, and geographic coordinates.  
  - [Dataset Download](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents?resource=download)
  - [Research Paper on the Dataset (arXiv)](https://arxiv.org/abs/1906.05409)
  - [ACM Digital Library Reference](https://dl.acm.org/doi/abs/10.1145/3347146.3359078)

- **Road Network GIS Data:**  
  Geospatial data from state and local transportation departments that provides additional context about road layouts, including road types, speed limits, the number of lanes, and locations of traffic signals. Additional APIs (e.g., Google Roads API) may be used to enrich this data, especially for identifying infrastructure details in metropolitan areas.

## Methodology
1. **Exploratory Data Analysis (EDA):**  
   - Analyze temporal patterns (e.g., rush hours, weekends, seasonal trends).  
   - Evaluate the impact of weather conditions on both the frequency and severity of accidents.

2. **Geospatial Analysis:**  
   - Map and identify accident hotspots using clustering techniques.  
   - Compare accident patterns in urban vs. rural settings to understand infrastructure-related risks.

3. **Predictive Modeling:**  
   - Train a machine learning model to estimate accident likelihood based on key factors (time, weather, road features).  
   - Validate and assess the performance of the model to support its application in real-world scenarios.

## Installation and Setup
1. **Clone the Repository:**

       git clone https://github.com/yourusername/traffic-accidents-analysis.git
       cd traffic-accidents-analysis

2. **Install Dependencies:**  
   It is recommended to use a virtual environment:

       python -m venv venv
       source venv/bin/activate  # On Windows: venv\Scripts\activate
       pip install -r requirements.txt

3. **Data Acquisition:**
   - Download the US Accidents Dataset from [Kaggle](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents?resource=download).
   - Place the dataset in the `data/` directory.
   - Ensure that any required GIS data is available in the appropriate directory.

4. **Run Initial Data Exploration:**

       python src/eda.py

## Usage
- **Data Exploration:**  
  Open the Jupyter notebooks in the `notebooks/` directory for interactive data analysis and visualization.

- **Model Training:**  
  Execute the training script to develop the predictive model:

       python src/train_model.py

- **Visualization:**  
  Generate charts and geospatial maps by running:

       python src/visualization.py

## Expected Outcomes
- **Temporal Patterns:** Insights into how accident frequencies vary with time and under different weather conditions.
- **Infrastructure Analysis:** Identification of road features that are strongly correlated with higher accident rates.
- **Accident Hotspots:** Mapping of high-risk areas that could benefit from targeted safety improvements.
- **Predictive Model:** A machine learning model capable of estimating accident risk, potentially aiding urban planning and the development of safer autonomous vehicle systems.

## Contributors
- **Shervan Shahparnia**
- **Nathan Cohn**

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgements
We extend our gratitude to the data providers and the research community for the valuable datasets and research papers that have made this project possible. Their contributions have laid the foundation for analyzing and improving traffic safety in the United States.
