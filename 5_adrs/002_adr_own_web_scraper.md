# ADR002 - Develop Own Web Scraping Service for Question Leakage Detection

## Status  
Accepted  

## Context and Problem Statement  
The AI Aptitude Test Creation & Modification service requires a mechanism to detect potential question leakage on the internet. Three primary options were considered:
- Developing our own web scraping service: Creating custom scripts to crawl the web and identify instances where test questions may have been exposed.
- Using an enterprise web scraping service (e.g., Jina or Firecrawl): Leveraging a third-party service to automate web crawling and leakage detection.
- Hybrid approach: Combining an in-house scraper for critical data with an enterprise service for large-scale scraping tasks.

### Requirements  
- Reliable, tailored scraping solutions.  
- Performance considerations (e.g., low latency for real-time detection).  
- Security measures for handling scraped data securely.  
- Compliance with ethical and legal constraints (e.g., GDPR, robots.txt adherence).  
- Scalability to accommodate growing test content and sources.

### Business and Technical Assumptions  
- In-house scraping ensures control, customisation, and cost-efficiency.  
- Enterprise solutions provide scalability but may introduce dependency risks and higher costs.  
- Hybrid solutions may balance control with scalability but introduce integration complexity.

## Decision Drivers  
- Control, reliability, flexibility, cost savings, and availability of tools.  
- Legal compliance (e.g., ensuring ethical scraping practices).  
- Real-time detection vs. batch processing trade-offs.  
- Security and privacy requirements for handling scraped data.

## Considered Options  

### 1. Own Web Scraping Service (Selected Option)  
- **Advantages:**  
  - Full control, tailored solutions, flexible updates, data security, cost-effective, and adaptable to changes in web structures.  
- **Disadvantages:**  
  - Development effort, ongoing maintenance, scalability challenges, and legal considerations.  

### 2. Use Enterprise Web Scraping Service (e.g., Jina or Firecrawl)  
- **Advantages:**  
  - Quick setup, reduced initial effort, scalable infrastructure, compliance with legal and ethical scraping guidelines.  
- **Disadvantages:**  
  - Limited control, higher costs with frequent use, dependency on external providers, potential limitations in customisation.  

### 3. Hybrid Approach (In-House + Enterprise Scraping)  
- **Advantages:**  
  - Balances control with scalability.  
  - Reduces infrastructure overhead for large-scale scraping tasks.  
  - Allows prioritization of resources for sensitive, high-value data collection.  
- **Disadvantages:**  
  - Increased complexity in integration and orchestration.  
  - Requires careful management of when to use which service.  

## Decision  
An in-house web scraping service will be developed. Future enhancements may explore enterprise solutions for additional scalability or automation, or a hybrid approach where appropriate.

## Consequences  
- Development and maintenance overhead, scalability requirements, legal and ethical considerations, data security adherence, and bias detection.  
- Possible integration challenges if transitioning to a hybrid or enterprise-based solution in the future.  
- Ongoing monitoring of regulatory changes affecting web scraping practices.

## Mitigation Strategies  
To mitigate these risks, Certifiable, Inc. will:
- Implement monitoring systems for scraping activity.  
- Establish data governance for privacy compliance.  
- Improve accuracy and efficiency continuously.  
- Evaluate alternative scraping technologies and hybrid options.  
- Create diverse datasets for AI accuracy.  
- Maintain expert review processes.  
- Secure assessments and data from unauthorised access.  
- Implement strategies for handling blocked scrapers (e.g., user-agent rotation, proxying).  
- Establish legal review mechanisms to ensure compliance with data usage policies.  
- Plan for rate-limiting policies in enterprise services to prevent excessive API costs.  
