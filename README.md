# spotify-end-to-end-etl-pipeline
## Introduction
This project was made to create a ETL pipeline using AWS, to retrieve Spotify's Top 100 songs data via spotify API, transform it and store in AWS database.

## architecture
![architecture diagram](https://github.com/rana1505/spotify-end-to-end-etl-pipeline/blob/main/spotify_api_end_to_end_pipeline_flow.png)

## About Databas/API
The data contains Top 100 songs playlist fetched from Spotify using the spotify web API - [Spotify API](https://developer.spotify.com/documentation/web-api)

### services used:
1. S3 simple storage service
2. AWS Lambda compute function
3. Cloud Watch
4. AWS Glue Crawler
5. Data Catalog
6. Amazon Athena

## Installed Packages
1. pip install pandas
2. pip install numpy
3. pip install spotipy

## Project Execution
Extract data from API -> Lambda Trigger (every 1 hr) -> Run extract code -> Store Raw Data -> Trigger Transform Function -> Transform Data and load it -> Query using athena.
