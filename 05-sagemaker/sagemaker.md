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

## SageMaker Feature Store

- Can ingest features from a variety of sources
- In Feature Store we get on overview of all our features that we saved
- Offers the ability to define the transformation of data into feature from with Feature Store
- We can also publish directly from Data Wrangler into Feature Store
- Feature are discoverable within SageMaker Studio

## SageMaker Clarify

- With Clarify we can evaluate and compare Foundational Models
- Clarify will evaluate human-factors such as friendliness or humor
- To evaluate a model we need human intervention. We can leverage an AWS-managed team or bring our own employees
- To evaluate models we can use a builtin dataset or we can bring our own data
- We can have builtin metrics and algorithms to choose from
- SageMaker Clarify is Part of SageMaker Studio

### SageMaker Clarify - Model Explainability

- Provides a set of tools to help explain how machine learning models work and make predictions
- We can understand model characteristics as a whole prior to deployment
- We can also debug predictions provided by the model after it is deployed
- Detect Bias:
    - Ability to detect and explain biases in our datasets and models
    - It can measure bias using statistical metrics
    - We can specify an input feature and the bias will be automatically detected

## SageMaker Ground Truth

- Based on RLHF - Reinforcement Learning from Human Feedback
- We use it to review models, customizations and do evaluations based human feedback
- We align models to human preferences
- Human feedback for ML:
    - We can rely on human feedback to create and evaluate models
    - We can use human workforce to generate or annotate data (example: create labels)
- Reviewers: can be Amazon Mechanical Turk workers, our employees or third-party vendors

## ML Governance

- SageMaker Model Cards:
    - It is a way for us to gather essential model information in one place
    - Example: we want to document the model's intended uses, risk rating and training details
- SageMaker Model Dashboards:
    - Centralized repository of our models
    - We can get information and insights for all our models about risk ratings, model quality, data quality, etc.
- SageMaker Role Manager:
    - We define roles for and permissions for employees within SageMaker
    - Example: we can have data scientists, MLOps engineers

## SageMaker Model Dashboards

- It is a centralized portal where we can view, search and explore all our models
- For example: track which models are deployed for inference
- Can be accessed from SageMaker Console directly
- Helps us to find models that violate threshold we set for data quality, model quality, bias, explainability, etc.

## SageMaker Model Monitor

- Monitors the quality for our models that are deployed in production
- It can run continuously or on-schedule
- Alerts for deviations in the model quality => we could then fix and retrain the model
- Example: loan model starts giving loans to people who don't have the correct credit score (drift)

## SageMaker Model Registry

- Centralized repository that allows us to track, manage and version ML models
- We can catalog models, manage model versions and associate metadata with a model
- We can manage the approval status of a model: automate model deployment, share models

## SageMaker Pipelines

- Allows us to create workflows that automate the process of building, training and deploying ML models
- Similar to a Continuous Integration and Continuous Delivery (CI/CD) but for ML
- Helps us to easily build, train, test and deploy 100s of models automatically
- We can iterate faster, reduce errors (no manual steps), have a repeatable mechanism
- Pipelines are composed of Steps and each Step can perform a specific task (example data preprocessing, model training)
- Supported task types:
    - Processing: for data preprocessing
    - Training: for training a model
    - Tuning: for hyperparameter tuning
    - AutoML: automatically train a model
    - Model: create or register a SageMaker model
    - ClarifyCheck: perform drift check against the baseline (data bias, model bias, model explainability)
    - QualityCheck: perform drift checks against the baseline (data quality, model quality)