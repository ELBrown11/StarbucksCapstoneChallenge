# Starbucks Capstone - Customer Behavior Analysis | Udacity - Data Science Nanodegree
## Overview
## Datasets
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
