# ADR012 - Define Continuous Integration and Continuous Deployment (CI/CD) Pipeline

## Status  
Accepted  

## Context and Problem Statement  
A robust CI/CD pipeline is essential for rapid development, consistent testing, and reliable deployment of AI-powered services within the Certifiable, Inc. SoftArch Cert System. The challenge is to select tools and practices that ensure automated testing, seamless deployment, and scalability.

### Requirements  
- Automate testing to ensure code quality and reliability.  
- Enable continuous delivery for fast, reliable deployments.  
- Support scalable integration with existing development workflows.

### Business and Technical Assumptions  
- Development is hosted on Git-based platforms.  
- The team has prior experience with CI/CD tools like GitHub Actions and Jenkins.

## Decision Drivers  
- Automation, code quality, rapid iteration, and scalability.

## Considered Options  

### 1. GitHub Actions (Selected Option)
- **Advantages:** Integrated with GitHub repositories, easy to configure, and supports scalable workflows.  
- **Disadvantages:** Limited flexibility if using non-GitHub repositories.

### 2. Jenkins  
- **Advantages:** Open-source, highly customisable, and widely adopted.  
- **Disadvantages:** Requires significant setup, maintenance, and dedicated resources.

### 3. GitLab CI/CD  
- **Advantages:** Integrated with GitLab, robust pipeline management.  
- **Disadvantages:** Less flexible when working with non-GitLab repositories.

## Decision  
GitHub Actions will be implemented for CI/CD pipelines due to its seamless integration with GitHub-hosted repositories and familiarity within the team. Offline evaluation of AI components against ground truth datasets will be included in the CI/CD process.

## Consequences  
- **Positive Impacts:** Streamlined development, consistent automated testing, and reliable deployments.  
- **Trade-offs and Limitations:** Dependence on GitHub, reduced flexibility if moving to other platforms.

## Mitigation Strategies  
To address these risks, Certifiable, Inc. will:  
- Regularly review and optimise CI/CD workflows for performance and reliability.  
- Provide training to ensure the team can manage and enhance CI/CD pipelines effectively.  
- Implement fallback processes for migrating CI/CD to alternative platforms if required.  
- Integrate monitoring and alerting for pipeline failures and performance bottlenecks.  
- Maintain version control for CI/CD scripts to ensure rollback capabilities and consistency.

