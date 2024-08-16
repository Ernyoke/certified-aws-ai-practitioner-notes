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

