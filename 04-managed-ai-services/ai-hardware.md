# Hardware for AI

## Amazon EC2

- EC2 is one of the most popular offering from AWS
- EC2 = Elastic Compute Cloud => IaaS
- EC2 service mainly consists of the following capabilities:
    - Renting virtual machines (EC2 Instances)
    - Storing data of virtual drives (EBS - Elastic Block Storage)
    - Distribute load across machines (ELB - Elastic Load Balancing)
    - Scaling the services using auto-scaling groups (ASG)
- EC2 configurations:
    - Operating System (OS): Linux, Windows, MacOS
    - Compute power and cores (CPU)
    - Random-access memory (RAM)
    - Storage space for EBS or Instance Store
    - Network card: speed of the card, Public IP address
    - Firewall rules (Security Group)
    - Bootstrap script (configure the instance at launch) - EC2 User Data

## Amazon's HW for AI

- AWS provides GPU based EC2 instances (P3, P4, P5, G3, G6, etc.)
- AWS Trainium:
    - ML chip built to perform Deep Learning on 100B+ parameter models
    - Trn 1 instance has for example 16 Trainium Accelerators
    - We can get 50% cost reduction when training a model
- AWS Inferentia:
    - ML chip built to deliver inference at high performance and low cost