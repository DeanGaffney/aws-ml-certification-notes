# aws-ml-certification-notes
Notes for the AWS Machine Learning Specialty Certification

# Data Engineering

## Amazon S3
### Overview
* Amazon S3 allows people to store objects in buckets
* Buckets must be globally unique
* Objects have a key, the key is the full path
* Max Object size is 5TB
#### AWS S3 for ML
* Object Tags are useful for life cycle and security purposes
* Backbone for many AWS ML services (example Sagemaker)
* Create a "Data Lake"
    * Infinite size, no  provisioning
    * 99.99999999% durability
    * Decoupling of storage to compute
* Centralized Architecture
* Object storage => supports any file format
* Common formats for ML:
    * CSV
    * JSON
    * Parquet
    * ORC
    * AVRO
    * Protobuf
#### AWS S3 Data Partitioning
* Pattern for speeding up range queries (ex: AWS Athena)
* By Date `s3://bucket/my-data-set/year/month/day/hour/data_00.csv`
* By Product `s3://bucket/my-data-set/product_id/data_32.csv`
* You can define whatever partitioning strategy you like!
* Data partitioning will be handled by some tools we use (eg. AWS Glue)