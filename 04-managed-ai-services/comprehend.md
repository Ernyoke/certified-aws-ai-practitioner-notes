# Amazon Comprehend

- It is a natural language processing and text analytics engine
- It accepts input documents which can come from a wide area of sources such as: social media, email, web pages, raw documents, transcripts, medical records (Comprehend Medical)
- Uses machine learning to find insights and relationships in text:
    - Extracts key phrases, entities, sentiment, language, syntax, topics, and document classification
    - It can do events detection (mainly about companies)
    - It can identify PII data and redact it
    - It can do targeted sentiment analysis for specific entities
    - Automatically organizes a collections of text files by topic
- We can train it on our own data

## Custom Classification

- We can organize documents into categories that we define
- Example: categorize customer emails so that we can provide guidance based on the type of the customer request
- Supports different types of documents (txt, PDF, Word, images)
- It can do real-time analysis on single documents on a synchronous way
- It can do asynchronous analysis on a batch of documents

## Custom Entity Recognition

- We can analyze text for specific terms and noun-based phrases
- Can be used to extract terms like policy numbers or phrases that imply a customer escalation, or anything specific to our business
- We can train the model with custom data such as a list of entities and documents that contain them
- It can do real-time or async analysis