# Amazon Bedrock

- A service is AWS that can be used to build GenAI applications
- It is a fully managed service
- We keep control of all the data we use, data will not leave the account 
- It has a pay-per-use pricing model
- Offers an unified standardized API
- Leverages a wide array of foundation models
- Offers out-of-the box features such as RAG, LLM Agents
- We get security, privacy, governance and responsible AI features

## Foundation Models

- Amazon Bedrock offers access to the modes from the following companies:
    - AI21labs:
    - Cohere
    - stability.ai
    - Amazon
    - Anthropic
    - Models from Meta
    - Mistral AI
- Amazon Bedrock makes a copy of the foundation model (FM). This will be only available to use. We can further fine-tune it with our data
- None of our data is sued to train the FM
- How to chose a foundation model?
    - There can be a lot of different factors we might want to take into consideration, such as: performance, requirements, capabilities, constraints, compliance
    - Level of customization, model size, inference options, license agreements, context windows, latency
    - Multimodal models in case of varied types onf input and output
    - Smaller models are most cost-effective
- Amazon Titan:
    - It is the high-performing FM from AWS
    - It is multimodal, can accept image, text
    - Can be customized with our own data

## Fine-Tuning a Model

- We can adapt a copy of a foundation model with our own data
- Fine-tuning will change to weights of the base foundation model
- Training data must:
    - Adhere to a specific format
    - Be stored in Amazon S3
- We can either fine tune once of do continued pre-training
- To use a fine-tuned model we must use **Provisioned Throughput**
- Note: some models can be fine-tuned, some cannot be
- Fine-tuning use cases:
    - We want to create a chatbot designed with a particular persona or tone geared towards a specific purpose (example assisting customers, advertising)
    - We want to train using more up-to-date information than what the language model previously accessed
    - We want to train the model with our own exclusive data
    - Targeted use cases: categorization, assessing accuracy

## Evaluating Foundation Models

- Automatic Evaluation:
    - Used to evaluate a model for quality control
    - Built-in task types:
        - Text summarization
        - Question and answer
        - Text classification
        - Open-ended text generation
    - We have to add a prompt dataset to do evaluation, or we can use the built-in curated prompt dataset
    - Scores are calculated automatically
    - There are different ways to calculate this grading score suing various statistical methods (example BERTScore, F1 score)
- Human Evaluation:
    - We can chose a work team to evaluate a model
    - This work team can be employees of our company or subject-matter experts (SMEs)
    - We define metrics and how to evaluate a model: thumbs up/down, ranking, etc.
    - We can chose from built-in task types (same as with automatic evaluation) or add custom task types
- We can have business metrics top evaluate a model on:
    - Uses Satisfaction: gather use feedback and asses their satisfaction with the model responses
    - Average Revenue Per Use (ARPU): we can compute the average revenue per user attributed to the GenAI app (monitor ecommerce user base revenue)
    - Cross-Domain Performance: measure the model's ability to perform cross different domain tasks (example monitor multi-domain ecommerce platforms)
    - Conversion Rate: generate recommended desired outcomes such as purchases
    - Efficiency: evaluate the model's efficiency in computation, resource utilization

## RAG and Knowledge Bases

- RAG =  Retrieval-Augmented Generation
- Allows a foundation model to reference a data source outside of its training data
- This data source is usually stored in a **vector database**
- Bedrock takes care of creating vector embeddings in the vector database of choice based on our data

## Vector Databases

- Vector databases on AWS can be of several kind
- There are 2 AWS services that can be used as vector database with Bedrock: OpenSearch and Aurora. By default Bedrock will use OpenSearch
- There are 3 other options for databases that can be used with Bedrock: MongoDB, Redis and Pinecone
- Embedding models: there are used to convert date (text, images) into vectors
- Available embedding models for Bedrock are Amazon Titan and cohere
- The embedding model and the foundation model can be different
- Documents are split into chunks before storing them as embeddings in vector databases
- The outcome if this procedure is that the data (vectors) are easily searchable and we can de similarity queries
- RAG data sources for Bedrock can be the following:
    - Amazon S3
    - Confluence
    - Microsoft SharePoint
    - Salesforce
    - Web pages (our website, social media, etc.)
- Use cases for RAG:
    - Customer service chatbot:
        - Knowledge base: products, features, specs, troubleshooting, etc.
        - RAG application: chatbot that can answer customer queries
    - Legal Research and Analysis:
        - Knowledge base: laws, regulations, case precedents, legal opinions and expert analysis
        - RAG application: chatbot that can provide relevant information for specific legal queries
    - Healthcare Question-Answering
        - Knowledge base: diseases, treatments, clinical guidelines, research papers
        - RAG application: chatbot that can answer complex medical queries

## Guardrails

- Allows us to control the interaction between users and the foundation model
- It can be used ot filter undesirable and harmful content
- It can be used ro remove Personally Identifiable Information (PII) and enhance privacy
- It can be used to reduce hallucinations
- We can create multiple (multiple level) Guardrails and monitor and analyze user input that can violate the Guardrails

## Bedrock - Other Features

- Bedrock Studio:
    - It is an UI that we can provide to our team so they can create AI powered applications easily
- Watermark detection:
    - Check if an image was generated by Amazon Titan Generator
- Agents:
    - We can create agents that will fulfill users' requests, invoke specific APIs automatically based on the needs
    - They can leverage external data sources when needed

## Pricing

- On-Demand:
    - We pay-as-we-go (no commitment)
    - Text models: we are charged for every input/output token processed
    - Embedding models: we are charged for every input token processed
    - Image models: we are charged for every image we generate
    - On-demand works for Base models only
- Provisioned Throughput
    - We can purchase model units for a certain period of time (1 months, 6 months, etc.)
    - Throughput: we define max number of input/output tokens we want to process per minute
    - Works with Base, Fine-tuned and Custom Models