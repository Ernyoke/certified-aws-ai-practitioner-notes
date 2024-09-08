# Compliance for AI

## Regulated Workloads

- Some industries will require extra level of compliance. Such industries are:
    - Financial services
    - Healthcare
    - Aerospace
- If we need to comply with regulatory frameworks (audit, archival, special security requirements), then we have a regulated workload

## AI Standard Compliance Challenges

- Complexity and Opacity: it is very challenging to audit how AI systems make decisions
- Dynamism and Adaptability: AI systems change over time, they are not static
- Emergent Capabilities: unintended capabilities a system may have
- Unique Risks: algorithmic bias, privacy violations and misinformation
    - Algorithmic bias: if the data is biased the model can perpetuate the bias
    - Human bias: the humans who create the AI system can also introduce bias
- Algorithm Accountability: algorithms should be transparent and explainable
    - Regulations in the EU "Artificial Intelligence Act" and US (several state and cities)
    - Promote fairness, non-discrimination and human rights

# AWS Compliance

- AWS supports are over 140 security standards and compliance certifications
- Examples:
    - National Institute of Standards and Technology (NIST)
    - European Union Agency for Cybersecurity (ENISA)
    - International Organization for Standardization (ISO)
    - AWS System and Organization Controls (SOC)
    - Health Insurance Portability and Accountability Act (HIPAA)
    - General Data Protection Regulation (GDPR)
    - Payment Card Industry Data Security Standard (PCI DSS)

## Model Cards

- Standardized format for documenting the key details about an ML model
- For GenAI models it can include source citations and data origin documentation
- Details about the dataset used, their sources, licenses and any known biases or quality issues in the training data
- Helpful to support audit activities
- AWS AI Service Cards are examples