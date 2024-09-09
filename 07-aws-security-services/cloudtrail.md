# AWS CloudTrail

- Provides governance, compliance and audit for an AWS account
- CloudTrail is enabled by default!
- Provides a history of events/API calls made within an AWS account
- It can put logs into CloudWatch Logs or S3
- A trail can be applied to All Regions (default) or a single Region
- In case of a resource deletion, to investigate it (who did it), we have to look inside CloudTrail first
- The default UI only shows create, modify and delete events
- CloudTrail Trail features:
    - Provides detailed list of all events
    - Ability to store these events in S3 for further analysis
    - It can be region specific or global
- CloudTrail logs are encrypted with SSE-S3 encryption by default when they are stored into S3. There is a possibility to use SSE-KMS encryption
- A CloudTrail log entry contains information about:
    - Who made the request
    - When was the request made and from where
    - What was requested
    - What was the response
- CloudTrail may have a 15 minutes delay to deliver log files into the S3 bucket

## CloudTrail Events

- Management Events:
    - Operations that are performed on resources in our AWS account
    - Example: `AttachRolePolicy`, `CreateSubnet`, `CreateTrail`
    - By default trails are configured to log management events no mather what
    - We can separate Read Events (that don't modify resources) from Write Events (that modify resources)
- Data Events:
    - By default data events are not logged (because high volume of operations)
    - Data events are: 
        - S3 object-level activity (`GetObject`, `DeleteObject`, `PutObject`)
        - AWS Lambda function execution activity
- CloudTrail Insights Events:
    - If enabled, it will analyze events to detect unusual activity in our account. Examples:
        - Inaccurate resource provisioning
        - Hitting service limits
        - Bursts of AWS IAM actions
        - Gaps in periodic maintenance activity
    - CloudTrail Insights analyzes normal management events to create a baseline and then continuously analyzes write events to detect unusual patterns
    - Insights events will appear in CloudTrail console
    - They are also sent to S3 (if enabled)
    - An EventBridge event is generated (for automation needs)