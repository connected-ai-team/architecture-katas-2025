# ADR005 - MongoDB as Vector Database

## Status  
Accepted  

## Context and Problem Statement  
A vector database is required for AI capabilities in the SoftArch Cert System, particularly for storing embeddings used in RAG (Retrieval-Augmented Generation) and semantic search functionalities.

### Requirements  
- Scalable and reliable vector storage.

### Business and Technical Assumptions  
- MongoDB offers familiar infrastructure and vector support.

## Decision Drivers  
- Integration and reliability.

## Considered Options  

### 1. **MongoDB Atlas (Selected Option)**  
  - **Advantages:** Centralised management, reliable, familiar, scalable, strong community support, versatile for both structured and vector data, integrates well with existing infrastructure, flexible data storage, cost-effective, and horizontally scalable.  
  - **Disadvantages:** Potential single point of failure, vector operations overhead, higher memory usage, resource contention, and performance tuning challenges.

### 2. **Weaviate**  
 - **Advantages:** Specialised for vectors, optimised search performance, built-in semantic capabilities, and service-specific optimisations.  
 -  **Disadvantages:** Learning curve, integration complexity, limited ecosystem, higher costs, and increased maintenance effort.

### 3. **Other Databases**  
 -  **Advantages:** Variety of features, flexible deployment, cost options, and custom tuning.  
 - **Disadvantages:** Uncertain performance, limited support, integration challenges, complex architecture, and increased maintenance effort.

## Decision  
MongoDB Atlas will be used as the primary vector database.

## Consequences  
The trade-offs and impacts of this decision are:
- **Feature Set:** MongoDB's vector search capabilities may not be as extensive or optimised as those offered by dedicated vector databases.
- **Performance:** Dedicated vector databases might offer lower latency and higher throughput for high-performance scenarios.
- **Operational Overhead:** Managing and optimising vector search within MongoDB requires specific expertise.
- **Scalability:** Scaling MongoDB to handle increasing data volume may need additional infrastructure investment.
- **Data Security:** Adherence to data protection standards like GDPR and CCPA is essential.
- **Bias Detection & Mitigation:** Measures are required to detect and correct biases in AI-generated outputs.

## Mitigation Strategies  
To mitigate these risks, Certifiable, Inc. will:
- Implement robust monitoring and alerting systems to track vector database usage and identify potential issues.
- Establish clear data governance policies to ensure compliance with data privacy regulations.
- Investigate techniques for improving the accuracy and efficiency of vector searches in MongoDB.
- Continuously evaluate alternative vector database technologies and open-source tools to reduce dependency on a single approach.
- Create high-quality, diverse datasets to minimise bias and improve the accuracy of AI models.
- Establish expert review processes to validate the outputs of the vector database and make necessary adjustments.
- Secure AI-generated assessments and training data against unauthorised access or tampering.
- Benchmark MongoDB's vector search performance against dedicated vector databases for specific use cases.
- Optimise MongoDB's configuration and indexing strategies for vector search workloads.
