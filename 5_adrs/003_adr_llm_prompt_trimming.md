# ADR003 - Use LLM for Prompt Trimming

## Status  
Accepted  

## Context and Problem Statement  
The AI-powered enhancements to the Certifiable, Inc. SoftArch Cert System rely on Large Language Models (LLMs) for various tasks. Effective prompt management is crucial for optimising LLM performance and cost. Three primary options were considered:
- Huge Prompts: Sending large prompts without trimming.
- Manual Prompt Trimming: Manually reviewing and shortening prompts.
- LLM-based Trimming: Using LLMs to trim and summarise prompts automatically.

### Requirements  
- Automated prompt trimming for large prompts.  
- Consistent, context-aware reductions with cost optimisation.

### Business and Technical Assumptions  
- LLM-based trimming ensures efficiency, consistency, scalability, and cost optimisation.

## Decision Drivers  
- Automation, cost savings, and improved LLM performance.

## Considered Options  

### 1. LLM-based Prompt Trimming (Selected Option)  
- **Advantages:** Automated, scalable, consistent, reduces human workload, ensures context maintenance, improves performance, and optimises costs.
- **Disadvantages:** Token usage costs, potential for nuanced detail loss, added latency, dependency on LLM provider.

### 2. Manual Prompt Trimming  
- **Advantages:** Full human control, domain-specific tailoring.
- **Disadvantages:** Time-consuming, labour-intensive, prone to error.

### 3. No Trimming  
- **Advantages:** Simplicity, no processing.
- **Disadvantages:** High token costs, performance issues.

## Decision  
Prompts will be sent to an LLM for automatic trimming and summarisation before processing by the primary LLM. Future enhancements may explore caching and alternative models.

## Consequences  
- Added latency, dependency on LLM providers, cost considerations, data security, and explainability challenges.

## Mitigation Strategies  
To mitigate these risks, Certifiable, Inc. will:
- Implement monitoring for LLM usage.
- Establish data governance for privacy compliance.
- Investigate explainability techniques.
- Explore caching to reduce latency and costs.
- Continuously evaluate LLM providers.
- Create diverse datasets for accuracy.
- Maintain expert reviews.
- Provide explainable AI feedback.
