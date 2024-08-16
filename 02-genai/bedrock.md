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