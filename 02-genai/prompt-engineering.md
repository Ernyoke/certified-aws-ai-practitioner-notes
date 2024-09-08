# Prompt Engineering

- Prompt Engineering: developing, designing and optimizing prompts to enhance the output of foundation models for our needs
- Improved prompting techniques consist of:
    - *Instructions*: a task for the model to do (description, how the model should perform)
    - *Context*: external information to guide the model
    - *Input data*: the input for which we want a response
    - *Output indicator*: the output type or format

## Negative Prompting

- A technique where we explicitly instruct the model on what not to include or do in its response
- Negative prompting helps to:
    - Avoid unwanted content: we explicitly state what not to include, reducing the chances of irrelevant or inappropriate content
    - Maintain focus: helps the model to stay on topic and not stray into areas that are not useful or desired
    - Enhanced clarity: prevents the use of complex terminology or details data, making the output clearer and more desirable

## Prompt Performance Optimization

- *System Prompts*: prompts given by the developer to the model, specifies how the system should behave and reply
- *Temperature*: value between 0 to 1. Defines the creativity of the output:
    - Low value: outputs are more conservative, repetitive and focused on mot likely response
    - High value: outputs are more diverse, create and unpredictable, maybe less coherent
- *Top P*: value between 0 to 1:
    - Low P (example 0.25): only consider the 25% most likely words. The model will provide most coherent responses
    - High P (example 0.99): consider a broad range of possible words, possibility to be more creative and have a diverse output
- *Top K*: it is a number. limits the number of probable words
    - Low K (example 10): more coherent responses
    - High K (example 500): more probable words, more diverse and creative responses
- *Length*: maximum length of the answer
- *Stop Sequences*: tokens that signal the model to stop generating output

## Prompt Engineering Techniques

- **Zero-Shot Prompting**:
    - Present a task to the model without providing any examples or explicit training for that specific task
    - We rely fully on the model's general knowledge
    - The larger and more capable the model, the more likely we get good results
- **Few-Shots Prompting**:
    - We provide examples of a task to the model to guide its output
    - We provide a "few shots" to the model to perform the task
    - If we provide only one example, this technique is called **One-Shot Prompting**
- **Chain of Thought Prompting**:
    - Divide the task into a sequence of reasoning steps, leading to more structure and coherence
    - Using a sequence like "Think step by steps" helps
    - Helpful when solving a problem as a human usually requires several steps
    - Can be combined with Zero-Shot or Few-Shots prompting
- **Retrieval-Augmented Generation (RAG)**:
    - Combine the model's ability with external data sources to generate a more informed and contextual rich response
    - The initial prompt is then augmented with external information