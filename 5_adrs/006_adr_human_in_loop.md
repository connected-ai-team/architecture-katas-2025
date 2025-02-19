# ADR006 - Human-in-the-Loop vs. Fully AI Automated

## Status  
Accepted  

## Context and Problem Statement  
The AI-powered enhancements to the Certifiable, Inc. SoftArch Cert System involve several key processes such as test question generation, case study creation, short answer grading, and architecture solution evaluation.

Two primary options were considered for these processes:
- Fully AI-Automated (Human out of the loop): AI systems perform all tasks without human intervention.
- Human-in-the-Loop: AI systems perform the majority of the work, with human experts reviewing, validating, and adjusting AI-generated outputs.

Human oversight is critical to ensure quality, fairness, and compliance in these AI-generated outputs.

### Requirements  
- Expert review for AI-generated outputs.

### Business and Technical Assumptions  
- Human oversight ensures quality, fairness, and adherence to certification standards.

## Decision Drivers  
- Quality assurance, accountability, and ethical considerations.

## Considered Options  
### 1. Human-in-the-Loop (Selected Option)
- **Advantages:** Quality control, error correction, builds trust in AI decisions, ensures adherence to certification standards, bias mitigation, explainability, ethical adherence, and regulatory compliance.
- **Disadvantages:** Resource-intensive, potential bottlenecks in workflows, additional training for human reviewers, increased operational costs, and potential delays.

### 2. Fully AI Automated
- **Advantages:** Fast, cost-efficient, scalable with minimal human intervention.
- **Disadvantages:** Risk of errors, lack of human judgment, potential ethical concerns, and limited explainability.

## Decision  
The decision is to implement a Human-in-the-Loop approach as the primary method for AI-powered enhancements. Human experts will review, validate, and adjust AI-generated outputs, ensuring quality, fairness, and compliance while enabling manual overrides when necessary.

## Consequences  
The trade-offs and impacts of this decision are:
- **Expert Workload:** Requires expert time for reviewing and validating AI outputs.
- **Scalability:** May limit the scalability of AI enhancements compared to full automation.
- **Cost:** Expert involvement adds to the operational costs.
- **Turnaround Time:** Review processes may increase the time it takes to deliver results.
- **Potential Bottlenecks:** High dependency on expert availability may cause delays.

## Mitigation Strategies  
To mitigate these risks, Certifiable, Inc. will:
- Implement efficient interfaces and workflows to streamline expert review processes.
- Provide training and support to experts to effectively use AI tools.
- Continuously evaluate and refine AI models based on expert feedback to reduce manual adjustments.
- Implement monitoring and alerting systems to track AI performance and identify potential issues.
- Establish clear guidelines and rubrics for AI assessments to ensure consistency and fairness.
- Utilise confidence metrics to prioritise expert review on uncertain or ambiguous cases.
- Ensure seamless manual overrides with minimal friction for expert interventions.
- Maintain version control and logging for AI-generated outputs to enable auditing, reproducibility, and rollback if necessary.
