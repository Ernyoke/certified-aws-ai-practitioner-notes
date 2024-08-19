# Amazon Q

## Amazon Q Business

- It is a fully managed GenAI assistant for our employees
- Its knowledge is based our our company's knowledge and data
- Use cases:
    - Answer questions, provides summaries, generate content, automate tasks
    - Perform routine actions (example submit time-off requests, send meeting invites)
- Amazon Q Business is built on Amazon Bedrock, but we have less control over its implementation, we cannot choose the underlying foundation model
- **Data Connectors (fully managed RAG)**: we can connect up to 40+ popular enterprise data sources, such as 
    - AWS services: S3, RDS, Aurora, WorkDocs, etc.
    - Non-AWS services: Microsoft 365, Salesforce, GDrive, Gmail, Slack, Sharepoint, etc.
- **Plugins**: allows us to interact with 3rd party services
    - Example: create a Jira ticket
    - We can create custom plugins to connect to any 3rd party service using APIs
- To interact with Amazon Q, users must be authenticated through IAM Identity Center
- Users receive responses generated only from the documents they have access to
- IAM Identity Center can be configured to integrate with external identity providers such as Google Login, Microsoft Active Directory, etc.
- **Admin Controls**: used to control and customize responses to our organizational needs
    - Admin Controls == Bedrock Guardrails
    - We can block specific words, topics
    - We can choose for Amazon Q to respond with only internal information (vs using external knowledge)
    - We can set up controls for all type of topics and subjects or we can set up smaller topic-level controls

### Q Apps

- We can create GenAI powered apps without coding by only using natural language
- Leverages company owned internal data
- We the possibility to have plugins (example Jira)

## Amazon Q Developer

- It has 2 sides:
    - AWS apps and websites:
        - It can answer questions about AWS documentation and AWS service selection
        - It can also answer questions about resources in our AWS account
        - It can also suggest CLI commands to execute to make changes in our AWS account
        - Helps us to do bill analysis, resolve errors and troubleshooting
    - AI code companion:
        - Helps us to write code for new applications (similar to GitHub Copilot)
        - Supports many languages: Java, JavaScript, Python, TypeScript, C#, etc.
        - It can give us real-time code suggestions and security scans
        - It provides also a software agent to implement features, generate documentation and bootstrap new projects
        - Works with several IDEs, such as VSCode, JetBrain suite, Visual Studio
        - Beside all of this it can do the following:
            - Answer questions about AWS development
            - Do code completion and code generation
            - Scan code four vulnerabilities
            - Debugging, optimizations and improvements