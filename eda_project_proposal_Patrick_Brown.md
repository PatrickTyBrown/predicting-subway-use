### EDA Project Proposal

# Covid Rates and Subway Use

## **Case**
- The NYC Health Department was tasked to evaluate the effectiveness of COVID related guidance throughout the pandemic. The department has decided to focus on public transport use. Therefore, they have partnered with the MTA. In order to ensure nonbiased reporting, they have contracted an independent Analyst to perform the evaluation.

## **Question**
- Was subway use related to Covid 19 rates?
- Were specific neighborhoods/boroughs disproportionately affected?
- Can changes in COVID case numbers be predicted by subway use?
## **Data**
- MTA Turnstile [Data](http://web.mta.info/developers/turnstile.html)
    - Focus on January 2019 - PRESENT
    - Calculated Metrics will include counts for Entries and Exits and the average of those with the number of Subway Lines at a given Station as a proxy for density of persons
    - An individual sample will include DAY | STATION | LINES | ENTRIES | EXITS | DENSITY
- Daily Rates Covid 19 [Data](https://data.cityofnewyork.us/Health/COVID-19-Daily-Counts-of-Cases-Hospitalizations-an/rc75-m7u3) 
    - Whole Dataset from January 2019 - PRESENT
    - Calculated metrics will include total counts across all boroughs
    - An individual sample will include DAY | BOROUGH | POSITIVE | HOSPITALIZED | DEATHS
- *Challenges*
    - Boroughs need to be identified for each station
    - Calculate Standardized Counts by station / borough
- *Extra*
    - Additional COVID Data can be used for [outcomes](https://data.cityofnewyork.us/Health/COVID-19-Outcomes-by-Testing-Cohorts-Cases-Hospita/cwmx-mvra) and [antibodies](https://data.cityofnewyork.us/Health/DOHMH-COVID-19-Antibody-by-Borough/x98t-3bbk).
## **Tools**
- SQL for early table work and aggregation
- SQLAlchemy for bringing MTA Data to Python
- Pandas for joining datasets EDA
- Matplotlib and Plotly for Visualization
- Map for Borough Visualization
- *Possibly* python for further analysis (correlation, regression)

## **MVP**
- Line Chart showing Subway Use vs Covid Rates
- Table with averages of metrics for different boroughs