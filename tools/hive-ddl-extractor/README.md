# Hive DDL Extractor

## Summary

This is a PySpark utility to extract DDLs from Hive metastore. Users can use this utility to accelerate the Hive migration journey.

DDLs will be extracted to a GCS bucket and the metadata will be in a BigQuery table

## Arguments

  * `host_ip`: Hive metastore URI
  * `project`: GCP Project name
  * `hive_database`: Hive database to extract table DDLs from
  * `gcs_working_directory`: Bucket name for output of the DDLs being extracted
  * `bigquery_dataset`: BigQuery dataset for auxiliary metadata output table



## Usage

```

$ python main.py <host_ip> <project> <hive_database> <gcs_working_directory> <bigquery_dataset> 

```

## Required JAR files

This template requires the [Spark BigQuery connector](https://cloud.google.com/dataproc-serverless/docs/guides/bigquery-connector-spark-example) to be available in the Dataproc cluster.

## Example submission

```
python main.py <host_ip> <project> <database> <bucket-name> <dataset> 

```


