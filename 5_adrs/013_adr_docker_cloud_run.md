# ADR013 - Use Containerisation with Docker for Cloud Run Deployment

## Status  
Accepted  

## Context and Problem Statement  
Containerising applications using Docker ensures consistent deployments by encapsulating application dependencies and environments. Google Cloud Run, a fully managed serverless platform, simplifies the orchestration and deployment of containerised applications, removing the need for managing Kubernetes clusters.

### Requirements  
- Consistent application deployment across development, staging, and production environments.  
- Scalable and serverless orchestration for containerised services.  
- Minimise operational overhead for managing infrastructure.  
- Ensure compatibility with existing development workflows.

### Business and Technical Assumptions  
- Docker will be used to containerise applications, packaging all dependencies into a single artefact.  
- Cloud Run will handle the orchestration, scaling, and deployment of containerised services.

## Decision Drivers  
- Deployment consistency, scalability, operational simplicity, and cost efficiency.

## Considered Options  

### 1. Docker with Cloud Run (Selected Option)  
- **Advantages:** Simplifies deployment with a serverless model, ensuring scalability and reliability without managing clusters.  
- **Disadvantages:** Limited control over infrastructure configuration compared to self-managed solutions like Kubernetes.

### 2. Docker with Kubernetes (GKE)  
- **Advantages:** Full control over orchestration, supports complex workloads.  
- **Disadvantages:** Overkill for the project's needs, increases operational complexity.

### 3. Traditional Deployment Without Containers  
- **Advantages:** Simpler for small-scale applications without dynamic scaling needs.  
- **Disadvantages:** Lacks consistency, scalability, and flexibility provided by containerisation.

## Decision  
Docker will be used for containerising applications, creating artefacts for deployment on Google Cloud Run. This ensures deployment consistency while leveraging the scalability and simplicity of a serverless orchestration platform.

## Consequences  
- **Positive Impacts:** Simplified deployment, scalable architecture, consistent application behaviour, improved developer productivity.  
- **Trade-offs and Limitations:** Limited control compared to Kubernetes, restrictions on non-HTTP workloads, potential vendor lock-in.

## Mitigation Strategies  
To address these risks, Certifiable, Inc. will:  
- Provide training on Docker and Cloud Run for the development team.  
- Implement fallback plans for workloads unsuited to Cloud Run.  
- Regularly update Docker images for security and performance.  
- Establish monitoring and logging for containerised services.  
- Periodically review hosting options to avoid long-term vendor lock-in.
  

