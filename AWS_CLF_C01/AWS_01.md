# What is cloud computing?

## How do websites work?
---

Client will use network to route packets to server and it will reply send the information back. In order to view a website

In order to find the server and the server to find you, they use an IP address. This is similar to a physical mailing address, it gives it a location for it to route to your destination. 

A server is composed of a CPU and RAM - Compute + MEmory = BAsically together they make a brain. 

Storage: Data -> Files
More structured = Database: Stores data in a structured way.

Traditionally, people would start by making a server in a garage. It would grow then you'd move to an office and then you'd have a data center.

Problems with this is that you have to pay rent, pay for power, cooling, and maintenance. 
Adding and removing Servers takes time.
Scaling becomes limited.
You need to hire a 24/7 team to monitor infrastructure.

How do we solve this -> Cloud computing. 

### What actually is cloud computing?
---

Cloud computing is the on-demand delivery of computational power, database storage, applications, and other IT services.

It has a Pay-as you go pricing.

Since it scales, you provision only exactly what you need. You can even access all these servers you can gain access to them instantly. It provides a simple way to access servers,storage, databases, and a set of applications services. 

AWS owns and maintains the network connected hardware required for these application services, while you only use/provision what you need via a web application. 

Example of clud services:
1. Gmail
2. Dropbox -> Cloud Storage Sservice built on originally AWS
3. Netflix -> Completely built on AWS

### Deployment models

- Private: Cloud services are used only by a single ORG and are not exposed to the public. They have complete control. Much better security for ssensitive applications, and are typically designed for specific business needs. 
- Public:
  1. Azure
  2. Google Cloud
  3. AWS
- Hybrid Cloud: Keeps some servers on premises, to keep some assests private. But keep public 

### 5 Characteristics of Cloud Computing

1. On Demand Service - Users can provision resources and use them without human interaction
2. Broad Network Access - Resources available over the network, and can be accessed by diverse client platforms.
3. Multi-tenancy and Resource Pooling - Multiple customers can share the same infrastructure and applications without compromising security and privacy. Multiple customers are served froma  single resource.
4. Rapid Elasticity and Scalability - Automatically and quickly acquire and dispose resources when neccessary. this also allows us to quickly scale based strictly on demand.
5. Measured service - Only pay for what is actually used.

### 6 Advantages of Cloud computing

1. Trade capital expenses for operational expenses.
  - Pay on demand
  - Reduced Total cost of Ownership
2. Benefit from massive economies of scale.
3. Stop guessing capacity 
  - Scale based on actual measured usage
4. Increased Speed and Agility
5. No more money spent on Maintenance

### Different types of Cloud computing

- IAAS - Infrastructure as a service
  - Provide building blocks for cloud IT
  - Provides networking, computers, data storage and space
  - Highet level of flexability
  - Easy paralell with traditionall on-site IT
- PaaS - Platform as a Service
  - Remove the need for your organization to manage the underlying structure
  - Focus on the deployment and managment of your applications
- SaaS
  - completed product managed by service provider

### AWS Cloud Use Cases

Applicable in a  diverse set of industries

### AWS Regions

- AWS has regions around the world represented by a name us-west-1
- They are cluster of data centers

If you need to launch a new applictaion where do you deploy.

- Compliance with data governance and legal requirements: Data never leaves region without your explicit permission
- Proximity - Reduced latency for users
- Available service within a region: New services and new features are not automatically available in every region
- Pricing - Varies from region to region.

- Availability zones
  - Each region has many availability zones 
    - usually 3, min 2, max 6
  - Each one is isolated from disasters to prevent cascading faiure

- AWS of points of presence
  - has 216 points of presence
  - Not all resources and services available in all locations