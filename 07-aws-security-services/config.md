# AWS Config

- Helps with auditing and recording compliance of AWS resources
- Helps record configurations and changes over time
- Provides the ability of storing the configuration data into S3 where it can be analyzed by Athena
- Problems AWS Config Solves:
    - Check if there is unrestricted SSH access to a security group
    - Check if buckets have public access
    - Find out how did an ALB configuration change over time
- We can receive alerts (SNS notifications) for any change
- AWS Config is a per region service, but it can be aggregated across regions and accounts

## AWS Config Rules

- AWS provides a set of managed config rules (over 75) which can be used by the users
- Users can also make custom config rules (a rule must be defined using AWS Lambda)
- Example of custom rules user can make:
    - Evaluate if each EBS disk is of type GP2
    - Evaluate if each EC2 instance is of type t2.micro
- Rules can be evaluated/triggered:
    - For each config change (Configuration change)
    - At regular time intervals (Periodic)
- Evaluation of rules can trigger CloudWatch events if the rule is non-compliant
- Rules can have auto remediations: if a resource is not compliant, the is an option to trigger auto remediation, example: stop instances with non-approved tags
- **AWS Config Rules do not prevent actions from happening (no deny)**
- Custom rules:
    - We can create custom rules which will be managed by us
    - In order to create a custom rule, we have to create a Lambda function which will check if a resource is compliant or not
    - Trigger types for custom rules are same as for managed rules:
        - Configuration change
        - Periodic
    - Scope of the trigger: we can define for which resource does the rule apply, example database instance, EC2 instance, etc. We can use tags as well instead of resource types

## Remediations

- Rules have a remediation action option, where we can run a SSM Automation document to address a non-compliant warning
- We can use AWS-managed automation document or create a custom automation document
- We can set Remediations Retries if the resource is still non-compliant after auto remediation

## CloudWatch vs CloudTrail vs Config

- CloudWatch
    - Performance monitoring (metrics, CPU, network, etc.) and dashboards
    - Events and alerting
    - Log aggregation and analysis
- CloudTrail
    - Record API calls made within an account
    - Define trails for specific resources
    - It is a global service
- Config
    - Record configuration changes
    - Evaluate resources against compliance rules
    - Get timeline of changes and compliance