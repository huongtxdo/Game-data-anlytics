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
