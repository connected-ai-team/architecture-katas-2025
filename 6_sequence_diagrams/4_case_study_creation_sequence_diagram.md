# Case Study Creation Sequence Diagram

## Description
This sequence diagram outlines the process of creating and modifying case studies using contextual retrieval, feedback generation, and AI-assisted improvements.

![Case Study Creation Sequence Diagram](../images/sequence_diagrams/case_study_seq.png)

## Steps
1. **Initiate Case Study:** The Case Study Creation Admin starts the process.
2. **Request Context:** The Context Orchestrator requests contextual information about the case study topic.
3. **Data Extraction:** Content RAG extracts information from the internet and stores it.
4. **Retrieve Data:** The system queries stored data for relevant case study context.
5. **Provide Feedback:** Context Orchestrator requests feedback based on previous case studies.
6. **User Feedback Retrieval:** Relevant user feedback is retrieved and provided for improvements.
7. **Generate Case Study:** The system generates a case study based on a tailored prompt.
8. **Critique and Improve:** Feedback is generated and used for refining the LLM-generated case study.
9. **Store Critique:** Expert feedback is stored for future model improvements.
