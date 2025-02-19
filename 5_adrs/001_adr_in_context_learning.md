# ADR001 - In-Context Learning vs. Fine-Tuning Approaches - Use In-Context Learning for AI-Powered Capabilities in SoftArch Cert System

## Status  
Accepted  

## Context and Problem Statement  
The AI-powered enhancements to the Certifiable, Inc. SoftArch Cert System require a mechanism for generating and processing text for various tasks such as test question generation, case study creation, and feedback generation. Three primary options were considered:
- Using in-context learning with commercial Large Language Models (LLMs) like OpenAI, Claude, or Gemini.
- Applying LoRA (Low-Rank Adaptation) fine-tuning on pre-trained models.
- Performing full Supervised Fine-Tuning (SFT) on pre-trained models.

The decision is to utilise in-context learning with commercial LLMs due to flexibility, performance, reduced development time, and access to cutting-edge technology. Future enhancements may explore fine-tuning approaches when enough golden data is available.

### Requirements  
- Seamless integration with existing workflows.  
- Support for manual overrides and expert reviews.  
- Explainable AI outputs with justification for grading and feedback.

### Business and Technical Assumptions  
- In-context learning offers flexibility and quick iterations.  
- Commercial LLMs provide high performance and reduce development time.

## Decision Drivers  
- Flexibility, performance, and reduced development time.

## Considered Options  

### 1. In-Context Learning with Pre-Trained Models (Selected Option)  
- **Advantages:**  
  - Fast iterations, cost-effective, adaptable, easy maintenance, access to advanced AI technology.  
  - Flexibility to adapt to evolving tasks.  
  - High performance of commercial models.  
  - Reduced development time.  
  - Access to cutting-edge AI without in-house development effort.  
  - Future potential to explore fine-tuning approaches when sufficient data is available.  
- **Disadvantages:** Dependency on external providers, potential cost scaling, data security concerns.

### 2. LoRA Fine-Tuning on Pre-Trained Models  
- **Advantages:**  
  - Lower computational cost compared to full fine-tuning.  
  - Ability to adapt the model to domain-specific needs while retaining general capabilities.  
- **Disadvantages:**  
  - Requires expertise in fine-tuning techniques.  
  - Still involves model training infrastructure.  
  - May require periodic updates as tasks evolve.  

### 3. Full Supervised Fine-Tuning (SFT) on Pre-Trained Models  
- **Advantages:**  
  - Highly tailored to specific tasks and domains.  
  - Can provide the highest level of performance when sufficient data is available.  
- **Disadvantages:**  
  - High development time and costs.  
  - Requires significant computing resources.  
  - Risk of overfitting to training data.  

## Decision  
In-context learning with commercial LLMs will be used, with future consideration for fine-tuning approaches as more data becomes available.

## Consequences  
- **Dependency on External Providers:** Risks related to pricing, availability, and data privacy.  
- **Cost Considerations:** Costs may scale with usage, but LLM inference gateways offer flexibility.  
- **Data Security:** Adherence to data privacy standards is crucial, with secure pipelines for sensitive data.  
- **Explainability and Bias:** Efforts required to ensure fairness, bias mitigation, and explainable feedback.  
- **Latency:** Initial latency acceptable but caching mechanisms will be explored as usage grows.  

## Mitigation Strategies  
To mitigate these risks, Certifiable, Inc. will:
- Implement robust monitoring and alerting systems to track LLM usage and identify potential issues.  
- Establish clear data governance policies to ensure compliance with data privacy regulations.  
- Investigate techniques for improving the explainability and fairness of commercial LLMs.  
- Explore caching mechanisms to reduce latency and costs.  
- Continuously evaluate alternative LLM providers and open-source models to reduce dependency on a single provider.  
- Create high-quality, diverse datasets to minimize bias and improve accuracy of AI models.  
- Establish expert review processes to validate AI-generated outputs and make necessary adjustments.  
- Provide explainable AI feedback, detailing why a specific score was assigned to enhance transparency.  
