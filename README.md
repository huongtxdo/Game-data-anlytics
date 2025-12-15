# Game-data-anlytics

Dataset info

Link: https://www.kaggle.com/datasets/debs2x/gamelytics-mobile-analytics-challenge/data

1. User Registration Data (reg_data.csv)
Records: 1,000,000
Columns:
    reg_ts: Registration time (Unix time, int64)
    uid: Unique user ID (int64)
Description: This dataset contains user registration timestamps and IDs. It is clean and contains no missing data.

2. User Activity Data (auth_data.csv)
Records: 9,601,013
Columns:
    auth_ts: Login time (Unix time, int64)
    uid: Unique user ID (int64)
Description: This dataset captures user login timestamps and IDs. It is clean and contains no missing data.

3. A/B Testing Data (ab_test.csv)
Records: 404,770
Columns:
    user_id: Unique user ID (int64)
    revenue: Revenue (int64)
    testgroup: Test group (object)
Description: This dataset provides insights into A/B test results, including revenue and group allocation for each user. It is clean and ready for analysis.

# Project goals
1. Determine the overall retention rate of different milestones and the retention rate of daily cohorts from the datasets of players' registration and login dates.

2. Determine the better-performing promotional offer from the dataset of A/B testing data.

3. Define some metrics to test the success of an in-game event.

# Data cleaning & analysis process
The csv-format datasets are loaded into pandas dataframes, cleaned and saved as 2 copies of csv and pkl files. The detailed steps are presented in 01_data_cleaning.ipynb

The first 2 goals are analyzed in 02_exploration.ipynb.

The last goal is discussed in 03_event_success_metrics.ipynb.

# Result & Insight
1. The game has quite low retention rates, with most return in around 1 week after their registration dates. 

2. If the game manages to keep players logging in after 50 days, it will likely be able to retain the players after one year.

3. For the cohort of August 2020 as an example, players starting around the end of the month have lower retention rates than those who started earlier. Other cohorts can be visualized by adjusting the reg_ts mask. 

# Steps to reproduce
1. Download the datasets from the link above and place them in the data/raw
2. Set up the project environemtn
   ```
   python -m venv venv
   ```
3. Activate it
    ```
    venv\Scripts\activate
    ```
4. Install packages
    ```
    pip install pandas numpy jupyter matplotlib
    ```
5. Run notebooks
