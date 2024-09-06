# Amazon SageMaker

- Fully managed service for developers/data scientists to build ML models
- Typically, it is difficult to do all the process in one place, and also provision servers
- SageMaker offers a set of built-in ML algorithms:
    - Supervised Algorithms:
        - Linear regression and classification
        - KNN algorithms (for classification)
    - Unsupervised Algorithms:
        - Principal Component Analysis (PCA) - reduce the number of features for a dataset
        - K-means: find grouping in data
        - Anomaly Detection
    - Textual Algorithms (NLP, summarization)
    - Image Processing (classification, detection)

## Automatic Model Tuning (AMT)

- We define the objective metric => AMT will automatically choose hyperparameter ranges, search strategy, maximum runtime of a tuning job and early stop condition

## Model Deployment and Inference

- We can deploy models from SageMaker with "one-click"
- We get automatic scaling and no servers to manage => reduced overhead
- Model deployment types:
    - Real-time:
        - We get an endpoint for one prediction at a time
        - Uses EC2 instances under the hood
    - Serverless:
        - We can have idle periods between traffic spikes, we are not charged when there is no traffic
        - Downside of this is that we should be able to tolerate initial startup latency (cold start)
    - Asynchronous:
        - For large payload sizes up to 1 GB, payload is stored in an S3 bucket
        - Supports long processing times
        - Good for near-real time latency requirements
        - Responses are also stored in S3
    - Batch:
        - Recommended for predictions for entire datasets (multiple predictions)
        - Requests and responses are in S3 buckets

## SageMaker Studio

- End-to-end ML development for an unified interface
- Supports team collaboration
- Offers an interface for tuning and debugging and deploying ML models
- We can also create automatic workflows from SageMaker Studio

## Data Wrangler

- Part of SageMaker Studio
- Can be used to prepare tabular and image data for machine learning
- We can do data preparation, transformations and feature engineering
- From a single interface we can do data selection, cleansing, exploration, visualizations and data processing
- Offers SQL support
- We can also analyze the quality of our data with Data Quality tool
- When we use Data Wrangler we would want to create ML features:
    - Features are inputs to ML models used during training and used for inference
    - It is important to have high quality features across our datasets in our company for reuse

## Feature Store

- Can ingest features from a variety of sources
- In Feature Store we get on overview of all our features that we saved
- Offers the ability to define the transformation of data into feature from with Feature Store
- We can also publish directly from Data Wrangler into Feature Store
- Feature are discoverable within SageMaker Studio