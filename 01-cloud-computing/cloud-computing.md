# Cloud Computing

## IT Terminology

- Network: cables, routers and servers connected with each other
- Router: a network device that forwards the data packets between computer networks. A router knows where to send our packets over the internet
- Switch: send the packet to the correct client on the network

## Problems with Traditional IT

- Pey for the rent for the data center
- Pay for power supply, cooling, maintenance
- Adding and replacing hardware takes time
- Scaling is limited
- We need to hire a 24/7 team to monitor the infrastructure
- How to deal with disasters (power outage, fire, etc.) ?

## What is Cloud Computing?

- Cloud computing is the on-demand delivery of computer power, database storage, applications and other IT resources
- Through a cloud service platform we get a pay-as-we-go pricing
- We can provision exactly the right type and size of computing resources we need
- We can access as many resources as we need almost instantly
- Provides a simple way to access servers, storage, databases and a set of application services
- Amazon Web Services (AWS) owns and maintains the network-connected hardware required for these application services, while we provision and use what we need via a web application

## Deployment Models of the Cloud

- Private Cloud: 
    - Cloud services used by a single organization not exposed to the public
    - We have complete control over it
    - We have more security for sensitive applications which may meet some specific business needs
- Public Cloud:
    - 3 famous public cloud providers are Amazon Web Services (AWS), Microsoft Azure and Google Cloud (GCP)
    - The cloud resources are owned and operated by a third party cloud service provider and delivered over the internet
- Hybrid Cloud:
    - We keep some services on-premises and extend some capabilities to the public cloud

## Five Characteristics of Cloud Computing

- On-demand self service:
    - Users can provision resources and use them without human interaction form the service provider
- Broad network access:
    - Resources are available over the network and can be accessed by diverse client platforms
- Multi-tenancy and resource pooling:
    - Multiple customers can share the same infrastructure and applications with security and privacy
    - Multiple customers are serviced from the same physical resources
- Rapid elasticity and scalability:
    - Automatically and quickly acquire and dispose resources when needed
    - Quickly and easily scale based on demand
- Measured service:
    - Usage is measured, users pay for what they use

## Six Advantages of Cloud Computing

- We trade capital expense (CAPEX) for operational expense (OPEX):
    - We pay on-demand, we don't own the hardware
    - Results in reduced Total Cost of Ownership (TCO) and Operational Expense (OPEX)
- We benefit for massive economies of scale:
    - Prices are reduces as AWS is more efficient due to large scale
- Stop guessing capacity
    - We can scale automatically based on actual measured usage
- Increased speed and agility
- We stop spending money running and maintaining data centers
- We can go global in minutes

## Problems Solved by the Cloud

- Flexibility: we can change resource type when we need it
- Cost-Effectiveness: we pay as we go for what we use
- Scalability: can can accommodate large loads by making hardware stronger or adding additional nodes
- Elasticity: we have the ability to scale out and scale in when we need
- High-Availability and Fault Tolerance: we can rely on multiple data centers around the world
- Agility: we can rapidly develop, test and launch software applications

## Types of Cloud Computing

- Infrastructure as a Service (IaaS):
    - Provides building blocks for cloud IT
    - Provides networking, computers, data storage space
    - Has the highest level of flexibility
    - Can be used with ease in parallel with traditional on-premises
- Platform as a Service (PaaS):
    - Removes the need for our organization to manage the underlying infrastructure
    - We can focus on the deployment and management of our application
- Software as a Service:
    - Complete product that is run and managed by the service provider
- Examples of services for each type:
    - IaaS:
        - Amazon EC2 (on AWS)
        - Azure VMs, Digital Ocean, Linode
    - Platform as a Service:
        - Elastic Beanstalk (on AWS)
        - Heroku, Google App Engine (on GCP), Azure App Service
    - Software as a Service:
        - Many AWS services (ex. Rekognition for ML)
        - Google Apps (Gmail), Dropbox, Zoom, etc.

## Pricing

- AWS has 3 pricing fundamentals:
    - Compute: we pay for the compute time
    - Storage: we pay for data stored in the cloud
    - Networking: we pay for data which leaves the cloud, data transfer inside the cloud is free