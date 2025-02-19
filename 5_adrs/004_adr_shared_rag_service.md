# ADR004 - Shared vs. Separate RAG Service

## Status  
Accepted  

## Context and Problem Statement  
The AI-powered enhancements to the Certifiable, Inc. SoftArch Cert System rely on Retrieval-Augmented Generation (RAG) for various services, including test question generation, case study creation, and short answer grading.

Two primary options were considered:
- **Separate RAG service for each AI service:** Independent RAG services for each enhancement.
- **Shared RAG service:** A single, shared RAG service used by all AI-powered enhancements.

### Requirements  
- Centralized observability, responsible AI checks, efficiency, security, and consistency.
- Scalable and resilient architecture to handle increasing AI workloads.

### Business and Technical Assumptions  
- A shared RAG service reduces redundancy, cost, and simplifies management.
- A single RAG service can be optimized for **performance and fault tolerance**.
- Future growth may require a **hybrid model** where certain workloads are offloaded to separate RAG instances.

## Decision Drivers  
- **Efficiency**: Reduces duplication of infrastructure and models.
- **Cost Optimization**: Shared resources minimize infrastructure expenses.
- **Consistency**: Ensures uniform responses and governance across AI enhancements.
- **Simplified Architecture**: Reduces operational complexity and overhead.

## Considered Options  

### 1. **Shared RAG Service (Selected Option)**  
- **Advantages:**  
  - Centralized management, lower cost, unified observability.  
  - Consistent data usage across services.  
  - Easier maintenance and governance.  
  - Code reuse and cost savings.  
  - Improved model quality with a single, well-tuned instance.  
- **Disadvantages:**  
  - **Single point of failure** (unless mitigated with redundancy).  
  - Potential **resource contention** across different AI services.  
  - **Scalability challenges** if demand spikes.  

### 2. **Separate RAG Services**  
- **Advantages:**  
  - Service-specific optimizations and model tuning.  
  - Better resource isolation to avoid performance bottlenecks.  
- **Disadvantages:**  
  - **Higher costs** due to duplicated infrastructure.  
  - **Complex architecture** with multiple RAG instances.  
  - **Increased maintenance effort** to manage multiple pipelines.  

### 3. **Hybrid Approach (Not Selected, but Considered for Future Growth)**  
- **Description:**  
  - A **shared RAG service** is used for most AI-powered enhancements.  
  - **Dedicated RAG instances** are deployed for high-traffic or critical services requiring **custom tuning or guaranteed performance**.  
- **Advantages:**  
  - Balances **cost savings** with **custom optimizations**.  
  - Provides **isolation for critical services**.  
- **Disadvantages:**  
  - Adds **complexity** in determining which services warrant dedicated RAG instances.  

## Decision  
A shared RAG service will be implemented for all AI-powered enhancements, with future scalability and performance optimizations. The **hybrid approach may be revisited** if performance issues arise.

## Consequences  
- **Management Complexity**: Requires careful monitoring and optimization.  
- **Scalability Needs**: Must ensure efficient load balancing and auto-scaling.  
- **Data Security**: Centralized RAG service requires **strict access controls**.  
- **Performance Risks**: Single service may experience **bottlenecks** if demand is not well-distributed.  
- **Bias Mitigation**: Needs consistent evaluations to avoid RAG-driven bias across services.  

## Mitigation Strategies  
To mitigate these risks, Certifiable, Inc. will:
- **Implement monitoring** for RAG usage and performance.  
- **Establish redundancy and failover mechanisms** to prevent single points of failure.  
- **Optimize caching and pre-fetching** to reduce load times.  
- **Establish rate limiting** to prevent overloading the shared RAG service.  
- **Ensure data governance** for privacy compliance and fairness.  
- **Improve RAG accuracy and efficiency** through periodic review.  
- **Evaluate alternative RAG scaling options** (e.g., hybrid approach if needed).  
- **Secure data and enforce strict access controls** to prevent unauthorized use.  
- **Conduct periodic audits** to assess bias and fairness.  
