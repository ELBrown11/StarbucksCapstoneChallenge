# Starbucks Capstone - Customer Behavior Analysis | Udacity - Data Science Nanodegree
## Overview
This project utilizes a simulated dataset from the Starbucks Rewards app, comprising three JSON files: `portfolio`, `profile`, and `transcript`. These files are integrated to create a unified dataset for analysis. The portfolio file contains metadata on promotional offers, including offer type, delivery channel, reward threshold, difficulty, and duration. The profile file includes customer demographic information such as age, membership start date, income, and gender. The transcript file logs customer interactions with the app, including events related to offers (e.g., received, viewed, completed) and associated metadata. By joining these datasets, we can analyze user behavior from the Starbucks app to understand which types of promotional offers perform best across different demographic groupings. This is analyzed via rule-based heuristics. The resulting insights can be used to inform both user engagement strategies and targeted marketing efforts.
## Libraries
- pandas
- numpy
- math
- json
- matplotlib
- seaborn
- gc (garbage collector
## Datasets
The three datasets are provided by Udacity and Starbucks as JSON files. The data was collected during a 30-day test period and was likley derived through distinct methods aligned with their intended purpose and structure:
- **Portfolio Data:** The data was likely sourced via content management system (CMS). It contain offer meta data (eg. offer type, duration, difficulty) defined by the marketing or product team in charge of the campaign design.  This is static throughout the 30-day test period and was likely ingested prior to the experiment starting. 
- **Profile Data:** Customer profile data was likely collected at the time of app registration (eg. age, gender, etc) and automatically logged system metadata (eg. account creation timestamp). Some attributes like income might have been inferred or appended through demographic enrichment services which summate based on zip code or other indirect information. 
- **Transcript Data:** This data was likely collected through backend event logging and client-side instrumentation integrated with the mobile app. Each record represented a user activity generated event (eg. “offered viewed”, “transaction”) and time-stamped relative to the beginning of the experiment. 

### `portfolio.json` 

| Column Name | Data Type        | Description                                           |
|-------------|------------------|-------------------------------------------------------|
| `id`        | `string`         | Offer ID                                              |
| `offer_type`| `string`         | Type of offer (e.g., BOGO, discount, informational)   |
| `difficulty`| `int`            | Minimum required spend to complete an offer           |
| `reward`    | `int`            | Reward given upon completing an offer                 |
| `duration`  | `int`            | Time for offer to be open, in days                    |
| `channels`  | `list of strings`| Channels where the offer is available (e.g. web, email, mobile, social) |

### `profile.json` 

| Column Name       | Data Type         | Description                                  |
|-------------------|-------------------|----------------------------------------------|
| `age`             | `int`             | Age of the customer                          |
| `became_member_on`| `date`            | Date when customer created an app account    |
| `gender`          | `str` (categorical)| Gender of the customer                       |
| `id`              | `str`             | Customer ID                                   |
| `income`          | `float`           | Customer’s income                            |

### `transcript.json`

| Column Name | Data Type            | Description                                                                          |
|-------------|----------------------|--------------------------------------------------------------------------------------|
| `event`     | `str`                | Record description (e.g., transaction, offer received, offer viewed)                |
| `person`    | `str`                | Customer ID                                                                          |
| `time`      | `int`                | Time in hours since start of test                                                   |
| `value`     | `dictionary of strings`  | Contains either an offer ID or transaction amount depending on the type of record   |

## Files
- [Data Cleaning Notebook](https://github.com/ELBrown11/StarbucksCapstoneChallenge/blob/main/Starbucks_Capstone_notebook_DataPrep.ipynb)
- [Rule-Based Heuristics and Data Analysis Notebook](https://github.com/ELBrown11/StarbucksCapstoneChallenge/blob/main/Starbucks_Capstone_Heuristics.ipynb)
