# ADR008 - Use LangGraph as the Language Model Orchestration Framework

## Status  
Accepted  

## Context and Problem Statement  
The AI-powered enhancements to the Certifiable, Inc. SoftArch Cert System require a robust framework for orchestrating natural language processing (NLP) tasks. The framework must allow for defining and managing complex workflows involving multi-step interactions, conditional logic, and advanced contextual handling. The challenge is to choose a framework that supports these needs while ensuring scalability and efficient implementation.

### Requirements  
- Support for structured orchestration of language model interactions.  
- Flexibility to define complex workflows with conditional logic and branching.  
- Scalability to manage increasing complexity and volume of tasks.  
- Familiarity among team members for efficient adoption and use.

### Business or Technical Assumptions  
- Workflow orchestration is critical for managing the system’s multi-step, conditional tasks.  
- Knowledge graphs are not a focus; the framework must manage the structure and flow of language model operations.  
- The team has prior experience with LangGraph, reducing onboarding time and implementation effort.

## Decision Drivers  
- Workflow management, scalability, team familiarity, and efficient development.

## Considered Options  

### 1. CrewAI  
- **Advantages:** Tools for collaborative AI workflows.  
- **Disadvantages:** Lacks robust support for structuring complex orchestration tasks.

### 2. AutoGen  
- **Advantages:** Strong automation features for task management.  
- **Disadvantages:** Limited flexibility for user-defined, structured workflows.

### 3. Haystack  
- **Advantages:** Open-source and flexible for NLP tasks.  
- **Disadvantages:** Focuses on search pipelines, lacking native support for structured orchestration.

### 4. LangGraph (Selected Option)  
- **Advantages:** Designed for structured language model orchestration, supporting complex workflows with branching and conditional logic. Team familiarity accelerates implementation. Strong community support (LangChain, LangSmith, LangServe).  
- **Disadvantages:** More complex than other options, requiring additional learning and effort.

## Decision  
LangGraph is selected as the language model orchestration framework due to its support for structured workflows, advanced contextual handling, and alignment with team expertise.

## Consequences  
- **Positive Impacts:** Improved management of complex workflows, accelerated implementation due to team familiarity, enhanced scalability for future demands.  
- **Trade-offs and Limitations:** Requires additional development effort for designing and implementing complex workflows.

## Mitigation Strategies  
To address the identified risks, Certifiable, Inc. will:  
- Provide comprehensive training and documentation to minimise the learning curve associated with LangGraph.  
- Allocate dedicated resources for the development and maintenance of complex workflows.  
- Implement iterative testing and feedback loops to refine workflow design and ensure reliability.  
- Regularly review and optimise workflows to enhance performance and scalability.  
- Leverage community support and best practices from LangGraph’s ecosystem to stay updated with improvements and solutions
