# ADR009 - Use LangFuse for Evaluation and MLOps Platform 

## Status  
Accepted  

## Context and Problem Statement  
The AI-powered enhancements to the Certifiable, Inc. SoftArch Cert System require a platform for offline evaluation to ensure that models operate as expected and to identify areas for improvement without requiring full deployment. Additionally, tracing capabilities are needed to support debugging and monitoring during development and production.  

### Requirements  
- Enable offline evaluation to validate model performance and identify improvement areas.  
- Provide robust tracing for debugging and monitoring.  
- Align with existing infrastructure for cost-effectiveness and security.  
- Allow self-hosted deployment to maintain control over sensitive data.  

### Business and Technical Assumptions  
- Offline evaluation is essential for iterative improvement without requiring deployment.  
- Tracing capabilities must integrate seamlessly with existing workflows.  
- A self-deployable solution is preferred to ensure data security and minimise operational costs.  

## Decision Drivers  
- Evaluation capabilities, tracing and monitoring, cost-effectiveness, and integration.

## Considered Options  

### 1. LangFuse (Selected Option)  
- **Advantages:** Self-deployable, cost-effective, secure, and supports robust evaluation and tracing.  
- **Disadvantages:** Requires additional effort to deploy and maintain a local instance.

### 2. Phoenix Arize  
- **Advantages:** Can be self-hosted and integrated with existing infrastructure.  
- **Disadvantages:** Less well-documented and supported, increasing implementation challenges.

### 3. LangSmith  
- **Advantages:** Highly documented, well-supported, and easy to integrate.  
- **Disadvantages:** Higher costs for advanced features and limited free tier.

## Decision  
LangFuse is selected as the evaluation and MLOps platform due to its balance of cost-effectiveness, self-deployability, and robust support for evaluation and tracing.  

## Consequences  
- **Positive Impacts:** Offline model evaluation, robust tracing, data control, and cost savings.  
- **Trade-offs and Limitations:** Requires development effort for deployment and maintenance, and may have less documentation and community support.

## Mitigation Strategies  
To address these risks, Certifiable, Inc. will:  
- Allocate resources for deploying and maintaining LangFuse locally.  
- Provide training and documentation for the team to manage LangFuse effectively.  
- Establish regular monitoring and optimisation routines for LangFuse.  
- Engage with the LangFuse community to leverage support and best practices.  
- Regularly evaluate the platform’s performance and update processes as needed.

