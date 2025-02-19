# ADR011 - Host Backend Services on GCP and Frontend on Firebase Deploy & Cloud Run

## Status

Accepted

## Context and Problem Statement

The AI-powered enhancements to the Certifiable, Inc. SoftArch Cert System require robust and scalable platforms for both backend and frontend components. The challenge is to select hosting solutions that align with the system’s scalability, simplicity, and integration needs while minimising complexity and maintenance overhead.

### Requirements

- Backend hosting must support scalable, efficient APIs and integrate seamlessly with existing tools and development pipelines.
- Frontend hosting must efficiently manage static content and support dynamic content through serverless functions, provide real-time updates, and simplify deployment.
- The solutions should balance cost, scalability, and ease of maintenance.

### Business and Technical Assumptions

- Backend services need high scalability and seamless integration with cloud-based tools used by the team.
- The frontend will primarily serve static content and handle dynamic operations via Firebase Cloud Functions.
- GCP is favoured due to existing infrastructure and team expertise.

## Decision Drivers

- Integration, scalability, simplicity, and cost-efficiency.

## Considered Options

### Backend Hosting

1. **AWS**

   - **Advantages:** Industry standard, scalable.
   - **Disadvantages:** Less alignment with existing infrastructure.

2. **Azure**

   - **Advantages:** Integrates well with Microsoft tools.
   - **Disadvantages:** Less synergy with current tools.

3. **GCP (Selected Option)**

   - **Advantages:** Aligns with existing infrastructure, scalable, integrates with development pipelines.
   - **Disadvantages:** Requires GCP expertise.

### Frontend Hosting

1. **Firebase Deploy with Cloud Run (Selected Option)**

   - **Advantages:** Developer-friendly, efficient for static content, supports dynamic operations through Cloud Run, easy maintenance.
   - **Disadvantages:** Requires managing Cloud Run for dynamic needs.

2. **Cloud Run**

   - **Advantages:** Dynamic scaling.
   - **Disadvantages:** Overkill for frontends.

3. **Heroku**

   - **Advantages:** Easy to deploy.
   - **Disadvantages:** Designed for dynamic apps.

4. **Self-hosted**

   - **Advantages:** Full control.
   - **Disadvantages:** Increased complexity.

## Decision

Backend will be hosted on GCP for scalability, integration, and existing expertise. Frontend will be hosted on Firebase Deploy with Cloud Run for simplicity, ease of maintenance, and support for both static and dynamic content.

## Consequences

- **Positive Impacts:** Scalable backend, seamless integration, efficient frontend hosting with dynamic support through Cloud Run.
- **Trade-offs:** Separate platforms require distinct monitoring and cost management.

## Mitigation Strategies

To address these risks, Certifiable, Inc. will:

- Allocate resources for managing GCP and Firebase environments.
- Provide team training on GCP tools, Firebase management, and Cloud Run development.
- Implement unified monitoring tools for both platforms.
- Regularly review costs and optimise resource usage.
- Establish fallback strategies for complex dynamic content needs in the future.
