# Security and Privacy for AI

## Security

- Thread Detection:
    - Examples: detect when fake content is generated, data is manipulated, attacks are being automated
    - We can deploy an AI-based thread detection system
    - We can analyze the network traffic, user behavior and other relevant data sources
- Vulnerability Management:
    - The way of identifying vulnerabilities in AI systems. Vulnerabilities can be: software bugs, model weakness, etc.
    - Conduct security assessments, penetration testing and code reviews
    - Have strong processes in place for patch management and update processes
- Infrastructure Protection:
    - Secure the cloud computing platform, edge devices and data stores
    - Implement access controls, network segmentation and have encryption in place for data
    - We must ensure we can stand system failures
- Prompt Injection:
    - Manipulate input prompts to generate malicious or undesirable content
    - To prevent prompt injection we need to implement guardrails: prompt filtering, sanitization, validation
- Data Encryption:
    - Encrypt data at rest and in transit
    - Manage encryption keys properly and make sure they are protected against unauthorized access

## Monitoring AI Systems

- Performance Metrics:
    - Model Accuracy: ratio of positive predictions
    - Precision: ratio of true positive predictions
    - Recall: ratio of true positive predictions compared to actual positive predictions
    - F1 score: average of precision and recall
    - Latency: time taken by a model to make a prediction
- Infrastructure monitoring - to catch bottlenecks and failures:
    - Compute resources (CPU/GPU usage)
    - Network performance
    - Storage
    - System logs
- Bias and Fairness, Compliance and Responsible AI

## AWS Shared Responsibility Model

- AWS responsibility - security of the cloud
    - Protect infrastructure (hardware, software, facilities and networking) that runs all the AWS services
- Customer responsibility - security in the cloud
    - Customer is responsible for data management, access controls, setting up guardrails, etc.
- Shared Controls:
    - Patch management, configuration management, awareness and training

## Best Practices for Secure Data Engineering

- Assess data quality:
    - Completeness: diverse and comprehensive range of scenarios
    - Accuracy: accurate, up-to-date and representative
    - Timeliness: age of the data in a data store
    - Consistency: maintain coherence and consistency in the data lifecycle
    - Data profiling and monitoring
    - Data lineage
- Privacy-Enhancing technologies:
    - Data masking, data obfuscation to minimize the risk of data breaches
    - Encryption, tokenization to protect data during processing and usage
- Data Access Control:
    - Comprehensive data governance framework with clear policies
    - Role-based access control and fine-grained permissions to restrict access
    - Implement single sign-on, multi-factor authentication, identity and access management solutions
    - Monitor and log all data access activities
    - Regularly review and update access rights based on least privilege principles
- Data Integrity:
    - Data is complete, consistent and free from errors and inconsistencies
    - Have a robust data backup and recovery strategy
    - Maintain data lineage and audit trails
    - Monitor and test the data integrity controls to ensure effectiveness