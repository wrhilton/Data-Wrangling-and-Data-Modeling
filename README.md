Project provided by Udacity in the Data Analytics Nanodegree program. Work is my own.

# Project: Exploring US Bikeshare Data

## Overview

This project performs an exploratory data analysis on bikeshare usage data from three major US cities: Chicago, New York City, and Washington. The goal is to uncover patterns in usage by calculating descriptive statistics and identifying trends related to time, popular stations, trip durations, and user demographics.

The analysis is interactive, prompting the user to choose a city and apply filters for month and day of the week to explore the data dynamically.

## Data Source

The data used in this analysis covers bike share usage for the first six months of 2017 for the following cities:

* Chicago (Divvy)
* New York City (Citi Bike)
* Washington (Capital Bikeshare)

Data is provided by Motivate International Inc. and made available through Udacity. The datasets include information such as trip start/end times, stations, duration, user types, and demographic details (where available).

## Methodology

The analysis follows these key steps within the script/notebook:

1.  **Data Loading:** Loading datasets for Chicago, New York City, and Washington using Pandas.
2.  **User Input:** Gathering user preferences for:
    * City of interest.
    * Time filters (specific month, specific day of the week, or no filter).
3.  **Data Filtering:** Applying the selected month and day filters to the chosen city's dataset.
4.  **Descriptive Statistics Calculation:** Computing various statistics based on the filtered data, including:
    * Most frequent month of travel.
    * Most frequent day of the week.
    * Most frequent start hour.
    * Most popular start station.
    * Most popular end station.
    * Most frequent combination of start and end stations.
    * Total travel time.
    * Average travel time.
    * Counts of different user types (e.g., Subscriber, Customer).
    * Counts of gender (for NYC and Chicago).
    * Earliest, most recent, and most common year of birth (for NYC and Chicago).
5.  **Results Display:** Printing the calculated statistics clearly to the console.
6.  **Raw Data Display:** Offering an option to display chunks of the raw filtered data upon user request.

## Key Findings (Examples derived from analysis)

The analysis reveals insights such as:

* Peak usage times (common months, days, hours).
* Most frequented start and end locations, highlighting popular routes.
* Average trip durations.
* Breakdown of user types (e.g., subscribers vs casual riders).
* Basic demographic patterns where data is available (gender, age distribution).

*(Refer to the code and outputs in the `Explore_bikeshare_data.html` file or the original `.ipynb` notebook for specific statistical results based on different filter selections.)*

## Technologies & Libraries Used

* Python 3
* Pandas (for data manipulation and analysis)
* NumPy (for numerical operations)
* time (for calculating durations)
* Jupyter Notebook (as the development environment)

## How to Run

1.  **Prerequisites:** Ensure you have Python 3 installed along with the Pandas and NumPy libraries.
    ```bash
    pip install pandas numpy
    ```
2.  **Get the Code:** Download the original Jupyter Notebook (`.ipynb` file - **recommended to add this to the repo!**) associated with the `Explore_bikeshare_data.html` file.
3.  **Get the Data:** Download the corresponding city bikeshare `.csv` files (e.g., `chicago.csv`, `new_york_city.csv`, `washington.csv`) and place them in the same directory as the notebook/script.
4.  **Execute:** Run the Python script or the Jupyter Notebook. The script will prompt you for city and filter choices to perform the analysis.

## File Structure

* `Explore_bikeshare_data.ipynb` (Recommended): The original Jupyter Notebook containing the Python code and analysis steps.
* `Explore_bikeshare_data.html`: An HTML export of the notebook, viewable in a web browser.
* `chicago.csv`, `new_york_city.csv`, `washington.csv` (Data files - not included in this repo, must be obtained separately).
* `README.md`: This file.

Remember to upload the actual .ipynb file to your GitHub repository alongside this README for the best experience for anyone visiting your profile! Let me know if you'd like any adjustments.


Sources and related content
Your saved info
Info you asked Gemini to save





wrangle_report
PDF

twitter_ar...ive_master
CSV

twitter-ar...e-enhanced
CSV

twitter-api
PY

tweet_json
TXT

image-predictions
TSV

wrangle_report.ipynb
IPYNB

wrangle_act.ipynb
IPYNB

act_report.ipynb
IPYNB


create me a readme file for github based on my attached files



Show thinking
Okay, based on the files you've provided (wrangle_act.ipynb, act_report.ipynb, wrangle_report.pdf, data files, etc.), here is a draft README file for your GitHub repository detailing the WeRateDogs data wrangling and analysis project.

Markdown

# Project: WeRateDogs Twitter Data Wrangling and Analysis

## Overview

This project focuses on gathering, assessing, cleaning, and analyzing tweet data from the popular Twitter account WeRateDogs (@dog_rates). The goal is to practice data wrangling skills on real-world data from multiple sources and then derive insights through analysis and visualization. The project demonstrates a typical data science workflow, transforming messy data into a clean dataset ready for exploration.

## Data Sources

The analysis utilizes data gathered from three distinct sources:

1.  **WeRateDogs Twitter Archive (`twitter-archive-enhanced.csv`):** A CSV file containing basic tweet data (tweet ID, timestamp, text, dog stage columns, etc.) for thousands of WeRateDogs tweets. Provided directly.
2.  **Image Prediction Data (`image-predictions.tsv`):** A TSV file hosted online, containing predictions of dog breeds based on the tweet images, generated by a neural network. This data was downloaded programmatically using the `requests` library.
3.  **Twitter API Data (`tweet_json.txt`):** Additional tweet details, primarily retweet counts and favorite counts, were gathered by querying Twitter's API using the tweet IDs from the archive. The `tweepy` library was used via the `twitter-api.py` script, and results were stored line by line as JSON objects.

## Project Workflow

The project follows these main stages, primarily executed within the `wrangle_act.ipynb` Jupyter Notebook:

1.  **Data Gathering:** Loading the Twitter archive CSV, downloading the image predictions TSV, and querying the Twitter API for engagement data.
2.  **Data Assessing:** Programmatically and visually inspecting the gathered dataframes to identify data quality issues (e.g., missing values, incorrect data types, inconsistent values) and structural (tidiness) issues (e.g., multiple columns representing the same variable like dog stages). Findings are documented in `wrangle_report.pdf` / `wrangle_report.ipynb`.
3.  **Data Cleaning:** Addressing the issues identified during assessment. This involved:
    * Handling missing data.
    * Correcting data types (e.g., timestamps).
    * Extracting and correcting rating information (numerator/denominator).
    * Filtering out retweets and replies.
    * Standardizing dog names where appropriate (e.g., 'a', 'an').
    * Merging the datasets into a single master dataframe (`twitter_archive_master.csv`).
    * Restructuring data (e.g., consolidating dog stage columns into one).
4.  **Data Analysis & Visualization:** Exploring the cleaned dataset (`twitter_archive_master.csv`) to uncover insights. This included:
    * Identifying the most common dog breeds based on image predictions.
    * Investigating the relationship between tweet ratings and engagement (retweets, favorites).
    * Visualizing findings, such as the distribution of top predicted breeds using Matplotlib and Seaborn. Key insights are documented in `act_report.ipynb`.

## Key Findings & Insights (Summary)

* The analysis identified popular dog breeds frequently featured and predicted in the tweets (e.g., Golden Retriever, Labrador Retriever, Pembroke Welsh Corgi).
* A positive correlation was observed between the rating given to a dog and the tweet's popularity (retweet and favorite counts).
* Various data quality and tidiness issues were successfully addressed, resulting in a clean dataset suitable for analysis.

*(Refer to the `wrangle_act.ipynb` and `act_report.ipynb` notebooks for detailed analysis code, visualizations, and discussion.)*

## Technologies & Libraries Used

* Python 3
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Requests
* Tweepy
* JSON
* Regular Expressions (`re`)

## File Structure

* `wrangle_act.ipynb`: Main Jupyter Notebook containing the entire workflow (gathering, assessing, cleaning, analysis, visualization).
* `act_report.ipynb`: Jupyter Notebook focusing on the analysis insights and visualizations report.
* `wrangle_report.ipynb` / `wrangle_report.pdf`: Report detailing the data wrangling efforts (gathering, assessing, cleaning).
* `twitter_archive_master.csv`: The final, cleaned master dataset produced by the wrangling process.
* `twitter-archive-enhanced.csv`: Original Twitter archive data.
* `image-predictions.tsv`: Downloaded image prediction data.
* `tweet_json.txt`: Raw JSON data retrieved from the Twitter API.
* `twitter-api.py`: Python script used to query the Twitter API (requires credentials).
* `README.md`: This file.

## How to Run

1.  **Prerequisites:** Ensure you have Python 3 and the required libraries installed.
    ```bash
    pip install pandas numpy matplotlib seaborn requests tweepy jupyter
    ```
2.  **Twitter API Credentials:** To run the data gathering step involving the Twitter API (`twitter-api.py` or the equivalent section in `wrangle_act.ipynb`), you will need valid Twitter API credentials (consumer key, consumer secret, access token, access secret) and insert them into the script/notebook.
3.  **Execute Notebook:** Open and run the `wrangle_act.ipynb` Jupyter Notebook. This notebook contains the full process from gathering (including the API query if credentials are provided) through cleaning and analysis.
4.  **Data:** Ensure the necessary input data files (`twitter-archive-enhanced.csv`, `image-predictions.tsv`) are available in the same directory or path specified in the notebook. Note that `tweet_json.txt` is generated by the API query step. `twitter_archive_master.csv` is generated by the cleaning process.
