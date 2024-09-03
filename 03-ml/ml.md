# AI and Machine Learning Overview

## What is AI?

- AI is a broad field for the development of intelligent systems capable of performing tasks that typically require human intelligent, such as:
    - Perception
    - Reasoning
    - Learning
    - Problem solving
    - Decision making
- AI is an umbrella-term for various techniques
- AI use cases:
    - Computer vision for self driving cars
    - Facial recognition
    - Fraud detection
    - Intelligent Document Processing  (IDP)

## AI Components

- Data Layer: we collect a vast amount of data
- ML Framework and Algorithm Layer: data scientist and engineers work together to understand use cases, requirements and frameworks that can solve them
- Model Layer: we implement a model and train it, we have the structure, the parameters and functions (optimizer function)
- Application Layer: how to serve the model and its capabilities for our users

## What is Machine Learning (ML) ?

- ML is a type of AI for building methods that allow machines to learn
- Data is leveraged to improve computer performance on a set of tasks
- We can predictions based on data used to train the model
- Predictive modelling techniques:
    - **Regression**: the output variable is continuous and quantitative. It is used to predict a numerical value based on input data
    - **Classification**: the output variable is categorical or discrete. The goal is to assign input data into one of several predefined classes or categories
- AI != ML

## Deep Leaning

- Uses neurons and synapses (like our brain) to train a model
- With deep learning we are able to process more complex patterns in the data compared to traditional ML
- It is called deep learning because there are more then one layers of learning
- Applications of Deep Learning:
    - Computer Vision: image classification, object detection, image segmentation
    - Natural Language Processing (NLP): text classification, sentiment analysis, machine translation
- For a good model we need a large amount of data
- Training is computationally heavy, usually done with GPU (Graphical Processing Units - video cards)

## Neural Networks

- They are composed of interconnected layers of nodes (called neurons) that process and transform input data to produce an output
- Key components:
    - *Neurons (nodes)*:
        - Function: Each neuron receives one or more inputs, processes them, and produces an output This output is then passed to the next layer of neurons
        - Weights: Each input to a neuron is multiplied by a weight, which determines the importance of that input in the final output
        - Bias: A bias term is added to the weighted sum of inputs before applying the activation function. It allows the model to fit the data better by shifting the activation function
    - *Layers*:
        - Input Layer: The first layer of the network that receives the raw data. Each neuron in this layer represents one feature of the input data
        - Hidden Layers: These are the intermediate layers between the input and output layers. A network can have multiple hidden layers, and this is what makes it "deep." These layers perform computations and extract features from the input data.
        - Output Layer: The final layer of the network that produces the output. The structure of this layer depends on the task (classification, regression)
    - *Activation Functions*: introduce non-linearity into the network, allowing it to learn complex patterns. Common activation functions are: ReLU, Sigmoid, Tanh, Softmax
    - *Loss Function*:  The loss function measures how well the network’s predictions match the actual values. It provides a quantitative metric for the error in the model. Common Loss Functions: Mean Squared Error (MSE), Cross-Entropy Loss
    - *Backpropagation*: is the process of updating the weights in the network to minimize the loss function. It works by computing the gradient of the loss function with respect to each weight and adjusting the weights in the direction that reduces the error

## Transformer Models

- They are able to process sentence as a whole instead of word by word
- Allow faster and more efficient text processing (less training time)
- Concepts: 
    - Self-Attention Mechanism: allows the model to weigh the importance of different words in a sentence relative to each other. This enables the transformer to capture long-range dependencies and relationships within the input data
        - Query, Key, and Value: for each word in the input, the model computes three vectors: a query vector, a key vector, and a value vector
    - Multi-Head Attention: instead of using a single set of query, key, and value vectors, the transformer uses multiple sets (or "heads") to capture different types of relationships and patterns in the data
    - Positional Encoding: used to inject information about the position of each token in the sequence into the model
    - Encoder-Decoder Architecture:
        - Encoder: processes the input sequence and generates a set of representations (called encodings) that capture the information in the input
        - Decoder: generates the output sequence (such as a translated sentence) based on the encodings and previous outputs
- Transformer based LLMs:
    - Powerful models that can understand and generate human-like text
    - Example; Google BERT, OpenAI ChatGPT

## Diffusion Models

- Used in machine learning, particularly for generating complex data such as images, audio, and even text
- Key concepts:
    - Generative Modeling: learn the underlying distribution of a dataset and generate new data points that are similar to the training data
    - Forward Diffusion Process: the diffusion process begins by gradually adding noise to the data (e.g., an image) over a series of steps until the data is completely transformed into noise
    - Reverse Diffusion Process: generative part of the model, where the goal is to start from pure noise and iteratively remove the noise, effectively reversing the forward diffusion process, to generate new data that resembles the original training data

## Multi-Modal Models

- They do not rely on a single type of input
- They can create multiple type of output
- Example: a multi-modal model can take a mix of audio, image and text and can create output of a mix of video and text

## Training Data

- To train our model we must have "good" data
- Most critical stage to build a good model
- There are several options to model our data, which will impact the types of algorithms we can use to train our models
- **Labeled** vs **Unlabeled** data:
    - Labeled data:
        - Data includes both input features and corresponding output labels
        - Used for supervised learning to map inputs to outputs
    - Unlabeled data:
        - Data includes only input features without any output labels
        - Used for unsupervised learning where the model tried to find patterns or structures in the data
- Structured data:
    - Data is organized in a structure, often is rows and columns (Tabular Data)
    - Other type of structured data is Time Series Data, where data points are collected and recorded at successive points in time
- Unstructured data:
    - Data that does not follow a specific structure and is often text-heavy or multimedia content
    - Text data: articles, social media posts, customer reviews, etc.
    - Image data: data in the form of images, can vary widely in format and content

## Supervised Learning

- Learn a mapping function that can predict the output for new unseen input data
- Requires labeled data: very powerful, but difficult to perform on millions of data points
- Regression:
    - Used to predict a numeric value based on input data
    - The output variable is continuous, it can tale any value within range
- Classification:
    - Used to predict the categorical label of an input data
    - The output variable is discrete, it falls into a specific category or class
    - Types of classifications:
        - Binary classification: spam/not spam
        - Multiclass classification
        - Multi-label classification: assign multiple labels to the same data point
- Training/Validation/Test Set:
    - Training Set:
        - Used to train the model
        - Percentage: typically 60-80% of the dataset
    - Validation Set:
        - Used to tine model parameters and validate performance
        - Percentage: typically 10-20% of the data set
    - Test Set:
        - Used to evaluate the final performance of the model
        - Percentage: typically 10-20% of the data set
- Feature Engineering:
    - It is the process of using domain knowledge to select and transform raw data into meaningful features
    - Helps enhancing the performance of machine learning models
    - Techniques:
        - Feature Extraction: extract useful information from raw data, such as deriving age from date of birth
        - Feature Selection: select a subset of relevant features, like choosing important predictors in a regression model
        - Feature Transformation: transform data for better model performance, such as normalizing numerical data

## Unsupervised Learning

- The goal is to discover inherent patterns, structures or relationships within the the data
- The machine must uncover and create groups itself, but humans still put labels on the output groups
- Common techniques include clustering, dimensionality reduction and association rule learning
- Feature engineering cal help improve the quality of the training
- Unsupervised Learning techniques:
    - Clustering:
        - Used to group similar data points together into clusters based on their features
        - Examples: customer segmentation
        - Algorithms: K-Means Clustering
    - Association Rule Learning Technique:
        - Example: market basket analysis (identify which products are frequently bought together)
        - Algorithms: Apriori algorithm
    - Anomaly Detection:
        - Example: fraud detection
        - Algorithms: Isolation Forest

## Semi-Supervised Learning

- We can use a small amount of labeled data and a large amount of unlabeled data to train the system
- The partially trained algorithm itself labels the unlabeled data (pseud-labeling)
- The model is then re-trained on the resulting data mix without being explicitly programmed

## Reinforcement Learning (RL)

- Is a type of machine learning algorithm where an agent learns to make decisions by performing actions in an environment to maximize cumulative rewards
- Key concepts:
    - Agent: learner of decision maker
    - Environment: the external system the agent interacts with
    - Action: the choice made by the agent
    - Reward: feedback from the environment based on the agent's action
- Learning process:
    - The agent observes the current state of the environment
    - It selects an action based on its policy
    - The environment transitions to a new state and provides a reward
    - Tha agent updates its policy to improve future decisions
- Examples of use cases:
    - Robotics: Train a robot to navigate a maze
    - Gaming: teach an AI to play complex games
    - Finance: portfolio management and trading strategies
    - Healthcare: optimizing treatment plans
    - Autonomous vehicles: path planning and decision making
- Reinforcement Learning from Human Feedback (RLHF):
    - We can use human feedback to help ML models to self-learn more efficiently
    - In reinforcement learning there is a reward function, with RLHF we incorporate human feedback directly into the reward function:
        - First the model responses are compared to human responses
        - Then, a human assesses the quality of the model's responses
    - RLHF is used throughout GenAI applications including LLM models
    - RLHF significantly enhances the model performance
    - RLHF training steps:
        1. Data collection
        2. Supervised fine-tuning of a language model 
        3. Build a separate reward model (requires human intervention)
        4. Optimize the language model with reward-based model