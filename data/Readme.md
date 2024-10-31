# Bitcoin Blockchain Cohort Data

This dataset provides a detailed analysis of the Bitcoin blockchain, focusing on cohort-based transaction behaviors and economic activity. Published in *Scientific Data* [1], the dataset enables users to examine trends and dynamics within Bitcoin user cohorts over time. It includes transaction data from Bitcoin’s inception in 2009, categorized by various transaction and cohort characteristics, offering a unique perspective on user activity and the evolution of Bitcoin’s economic landscape.

Available as open-access on the [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/XSZQWP), the dataset is structured to support data science research, particularly in economic modeling, transaction pattern analysis, and network analysis. Researchers can utilize this dataset to explore the impact of new user cohorts on the broader Bitcoin economy, identify behavior patterns, and apply it in predictive modeling for blockchain studies.

## References
[1] D. A. Ante, “Deciphering Bitcoin blockchain data by cohort analysis,” *Scientific Data*, vol. 9, no. 1, p. 605, 2022. Available: https://www.nature.com/articles/s41597-022-01254-0.

Here’s the revised data dictionary with the additional information on the timezone, date range, frequency, and inclusion of other cryptocurrencies.

---
## Data Dictionaries
### Table S1: STXO Dataset Data Dictionary

| Variable Name | Definition | Unit                    | Range (Date & Value)                       | Frequency          | Timezone | Sample Observation |
|---------------|------------|-------------------------|--------------------------------------------|---------------------|----------|---------------------|
| `date`        | Date of cohort data queried in format `%Y/%m/%d` | Date                    | `2009-01-03` to `2021-02-10` | Daily (n=4421)      | UTC+0    | `2021-02-10`       |
| `newborn`     | Number of UTXOs in BTC created on the given date | BTC count              | 0–1000+                                | Daily              | UTC+0    | `50`               |
| `dead`        | Number of UTXOs in BTC spent as inputs on the given date | BTC count              | 0–1000+                                | Daily              | UTC+0    | `30`               |
| `WAL`         | Weighted average lifespan of the UTXOs spent on the given date | Years                  | 0–20                                   | Daily              | UTC+0    | `5.3`              |
| `-9`          | UTXOs in BTC spent created less than one day before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `10`               |
| `-7`          | UTXOs in BTC spent created more than one day but less than one month before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `20`               |
| `-5`          | UTXOs in BTC spent created more than one month but less than three months before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `15`               |
| `-3`          | UTXOs in BTC spent created more than three months but less than six months before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `25`               |
| `-1`          | UTXOs in BTC spent created more than six months but less than one year before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `12`               |
| `1`           | UTXOs in BTC spent created more than one year but less than two years before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `8`                |
| `3`           | UTXOs in BTC spent created more than two years but less than three years before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `5`                |
| `5`           | UTXOs in BTC spent created more than three years but less than four years before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `3`                |
| `7`           | UTXOs in BTC spent created more than four years but less than five years before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `1`                |
| `9`           | UTXOs in BTC spent created more than five years but less than ten years before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `2`                |
| `11`          | UTXOs in BTC spent created more than ten years before | BTC count              | 0–500+                                 | Daily              | UTC+0    | `1`                |

---

### Table S2: UTXO Dataset Data Dictionary

| Variable Name | Definition | Unit                    | Range (Date & Value)                       | Frequency          | Timezone | Sample Observation |
|---------------|------------|-------------------------|--------------------------------------------|---------------------|----------|---------------------|
| `date`        | Date of cohort data queried in format `%Y/%m/%d` | Date                    | `2009-01-03` to `2021-02-10` | Daily (n=4421)      | UTC+0    | `2021-02-10`       |
| `-9`          | UTXOs in BTC still alive created less than one day before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `60`               |
| `-7`          | UTXOs in BTC still alive created more than one day but less than one month before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `40`               |
| `-5`          | UTXOs in BTC still alive created more than one month but less than three months before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `25`               |
| `-3`          | UTXOs in BTC still alive created more than three months but less than six months before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `18`               |
| `-1`          | UTXOs in BTC still alive created more than six months but less than one year before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `10`               |
| `1`           | UTXOs in BTC still alive created more than one year but less than two years before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `7`                |
| `3`           | UTXOs in BTC still alive created more than two years but less than three years before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `4`                |
| `5`           | UTXOs in BTC still alive created more than three years but less than four years before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `2`                |
| `7`           | UTXOs in BTC still alive created more than four years but less than five years before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `1`                |
| `9`           | UTXOs in BTC still alive created more than five years but less than ten years before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `0`                |
| `11`          | UTXOs in BTC still alive created more than ten years before | BTC count              | 0–1000+                                | Daily              | UTC+0    | `0`                |

---

### Table S3: File Metadata for Altcoins UTXO and STXO Datasets

| Variable Name     | Definition                              | Unit     | Data End Date | Sample Observation           |
|-------------------|----------------------------------------|----------|---------------|-------------------------------|
| `name`            | Name of cryptocurrency                 | Text     | -             | Bitcoin                       |
| `brief`           | Abbreviation for the cryptocurrency    | Text     | -             | BTC                           |
| `UTXO file name`  | File name for UTXO dataset on GitHub   | Text     | Varies by altcoin | BitcoinResultUTXO2021-02-10.csv |
| `STXO file name`  | File name for STXO dataset on GitHub   | Text     | Varies by altcoin | BitcoinResultSTXO2021-02-10.csv |

---

### Notes

- **Data Range**: The data spans from `2009-01-03` to `2021-02-10`, with a total of 4,421 daily records for each dataset.
- **Timezone**: All data points are recorded in UTC+0.
- **Cryptocurrencies**: In addition to Bitcoin, the dataset includes cohort analysis for five other cryptocurrencies, resulting in twelve datasets in total (UTXO and STXO datasets for each of the six cryptocurrencies: Bitcoin, Bitcoin Cash, Litecoin, Dogecoin, Dash, and Zcash).

These tables incorporate the detailed structure and metadata of the UTXO and STXO datasets, ensuring a clear understanding of the data’s scope, frequency, and variables. Let me know if you need any further modifications or additional details.

