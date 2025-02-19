# ADR007 - Implement a Custom API Gateway

## Status  
Accepted  

## Context and Problem Statement  
The AI-powered enhancements to the Certifiable, Inc. SoftArch Cert System require secure and efficient communication with multiple microservices. The challenge is to choose an approach that balances flexibility, security, performance, and cost while supporting the specific needs of the system.  

### Requirements  
- Robust security for inter-service communication.  
- Customisable routing and load balancing tailored to system architecture.  
- High performance with minimal latency.  
- Ability to integrate seamlessly with existing and future microservices.  

### Business or Technical Assumptions  
- Off-the-shelf solutions may include features that are unnecessary for the project, leading to increased costs and overheads.  
- A custom gateway can be tailored to address specific security and routing needs but will require additional development effort.  
- The system architecture will evolve, necessitating a flexible and scalable API gateway solution.  

## Decision Drivers  
- Security: The gateway must enforce strict security measures for inter-service communication.  
- Performance: Minimise latency and optimise throughput for high-frequency service calls.  
- Flexibility: Support custom routing, monitoring, and integration needs.  
- Cost-efficiency: Avoid additional costs associated with unused features in pre-built solutions.  

## Considered Options  

### 1. Off-the-Shelf API Gateways (e.g., Apigee, Kong)  
- **Advantages:** Pre-built, feature-rich, easy integration, and well-documented.  
- **Disadvantages:** May include unnecessary features, additional licensing costs, and limited flexibility for customisation.

### 2. No API Gateway  
- **Advantages:** Simplifies architecture, reduces initial setup effort.  
- **Disadvantages:** Complicates microservice communication, lacks centralised security and routing controls, increases redundancy in service handling.

### 3. Custom API Gateway (Selected Option)  
- **Advantages:** Tailored to specific security, routing, and performance needs. Fully customisable and integrates seamlessly with existing architecture.  
- **Disadvantages:** Increased development and maintenance complexity, requiring dedicated resources.

## Decision  
A custom API gateway will be developed to meet the specific integration, security, and performance needs of the Certifiable, Inc. SoftArch Cert System’s microservices.  

### Reasons  
- Provides complete control over routing, security, and monitoring tailored to Certifiable, Inc. SoftArch Cert System’s unique requirements.  
- Avoids unnecessary costs and overheads associated with off-the-shelf solutions.  
- Supports future architectural changes and scaling without dependence on third-party providers.  

## Consequences  

### Positive Impacts  
- Optimised for performance and security based on specific business requirements.  
- Greater flexibility for customisations, such as tailored routing and monitoring.  
- Ensures seamless integration with the existing and evolving microservice architecture.  

### Trade-offs and Limitations  
- Higher development and maintenance costs compared to off-the-shelf solutions.  
- Requires dedicated resources for implementation and ongoing updates.  
- Longer initial development timeline compared to pre-built solutions.

## Mitigation Strategies  
To address the identified limitations, Certifiable, Inc. will:  
- Allocate dedicated resources to manage and maintain the custom API gateway, ensuring continuous support and updates.  
- Implement robust documentation and training programs to ensure the team is well-equipped to handle development and maintenance tasks.  
- Conduct regular performance assessments and optimisation reviews to minimise latency and enhance throughput.  
- Establish a clear roadmap for gateway enhancements, ensuring scalability and flexibility as system architecture evolves.  
- Regularly evaluate and benchmark the custom gateway against industry standards and emerging technologies to maintain competitive performance and security.
