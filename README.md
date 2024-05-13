# TweetFlow - Automating Twitter Data Pipelines with Apache Airflow

## Overview
TweetFlow leverages Apache Airflow to automate the extraction, processing, and analysis of Twitter data. This project utilizes Tweepy for fetching tweets and pandas for data manipulation, orchestrating the entire pipeline on AWS to provide real-time insights into Twitter data.

## Project Files

- **twitter_dag.py**: Defines the Airflow Directed Acyclic Graph (DAG) that orchestrates the workflow for the pipeline. This includes scheduling and managing tasks such as tweet extraction, data transfer, and analysis.
- **twitter_etl.py**: Contains the ETL script for extracting tweets using the Tweepy library.
- **README.md**: Provides a comprehensive overview of the project, including setup instructions and usage guidelines.

## Setup Instructions

1. **Install Requirements**:
   - Ensure Apache Airflow and the required Python libraries (Tweepy, pandas) are installed on your system or AWS cloud instance.
2. **Clone the Repository**:
   - `git clone [[repository-url](https://github.com/vinayvaida27/TweetFlow-Automating-Twitter-Data-Pipelines-with-Apache-Airflow/tree/main)]` - Clone this repository to your local machine or cloud instance.
3. **Configure Apache Airflow**:
   - Set up Apache Airflow on AWS or your preferred cloud service. Detailed instructions can be found in the official [Airflow Documentation](https://airflow.apache.org/docs/).
4. **DAG Setup**:
   - Place `twitter_dag.py` and `twitter_etl.py` in the Airflow DAGs directory.
   - Configure Airflow to execute the DAG on a regular schedule, such as daily.
5. **API Credentials**:
   - Ensure that your Twitter API credentials are correctly configured to allow tweet extraction.
6. **Start Airflow Services**:
   - Begin the Airflow scheduler and web server to monitor and manage the pipeline.

## Usage

- **DAG Execution**:
  - The Airflow DAG, defined in `twitter_dag.py`, automatically triggers tasks according to the defined schedule.
  - The `twitter_etl` task extracts tweets from the Twitter API and stores the data in a specified location for further processing.
- **Data Analysis**:
  - Use pandas within subsequent tasks or separate scripts to analyze the tweet data and derive insights.

## Contributing

We welcome contributions to TweetFlow! If you have suggestions for improvements, or if you want to request features or report bugs, please fork the repository, make changes, and submit a pull request. We appreciate feedback and engagement from the community.

## Acknowledgments

Special thanks to the Apache Airflow, Tweepy, and pandas communities for their invaluable resources and contributions to the open-source community.

## License

This project is open-source and available under the MIT License. See the LICENSE file for more details.
