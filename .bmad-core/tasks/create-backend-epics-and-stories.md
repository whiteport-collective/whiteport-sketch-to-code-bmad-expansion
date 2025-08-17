# create-backend-epics-and-stories

## Purpose

To create comprehensive epics and user stories for backend infrastructure, API development, and non-visual system components that support the sketch-driven user interface. This task focuses on the foundational technical work that must be completed before or alongside UI development.

## Process

The PM will analyze the PRD and trigger map to identify all backend requirements that are not directly tied to visual user interactions but are essential for the product's functionality.

### Identify Backend Requirements

* **Data Models & Database Design**: Review the trigger map and PRD to identify all data entities, relationships, and storage requirements
* **API Endpoints**: Determine what API endpoints will be needed to support the user scenarios and sketch interactions
* **Authentication & Authorization**: Define user management, security, and access control requirements
* **Integration Points**: Identify external services, third-party APIs, or enterprise system integrations
* **Business Logic**: Extract complex business rules and calculations that happen server-side
* **Performance Requirements**: Identify caching, optimization, and scalability needs

### Create Backend Epics

For each major backend domain, create epics that group related functionality:

* **Epic Structure**: Each epic should have a clear business value statement connecting back to user goals from the trigger map
* **Acceptance Criteria**: Define what "done" means for each epic in terms of functionality and quality
* **Dependencies**: Identify dependencies between backend epics and connections to future UI work
* **Technical Scope**: Include infrastructure, database, API, and service layer components

### Break Down into User Stories

* **Technical User Stories**: Create stories from the perspective of the system, other services, or developers who will consume the APIs
* **API-First Design**: Structure stories to define clear API contracts that will support the future UI development
* **Data Flow**: Ensure stories cover the complete data flow from input validation to storage to retrieval
* **Error Handling**: Include stories for error scenarios, validation, and edge cases

### Prioritization and Sequencing

* **Foundation First**: Prioritize infrastructure and core data models that other components depend on
* **API Readiness**: Sequence development so APIs are ready when UI development begins
* **Risk Mitigation**: Tackle complex integrations and technical unknowns early
* **Value Delivery**: Balance technical foundation with early value delivery opportunities

## Elicitation Requirements

elicit: true
format: structured-interview

### Questions to Ask

1. **Data Requirements**: "Based on the user scenarios, what data does the system need to store, process, and retrieve?"

2. **Integration Needs**: "What external systems, services, or APIs does this product need to connect with?"

3. **Performance Expectations**: "What are the expected user loads, response times, and scalability requirements?"

4. **Security Requirements**: "What are the authentication, authorization, and data protection requirements?"

5. **Business Logic**: "What complex calculations, validations, or business rules need to happen server-side?"

6. **Technical Constraints**: "Are there existing systems, databases, or architectural constraints we need to work within?"

## Output

A comprehensive set of backend epics and user stories organized by:

* **Epic Priority**: Ranked by dependency and business value
* **Story Details**: Each story includes acceptance criteria, technical requirements, and API specifications
* **Dependency Map**: Clear visualization of how backend components relate to each other and to future UI work
* **Development Sequence**: Recommended order of implementation that supports the overall project timeline

## Integration with Sketch-Driven Development

* **API-First Approach**: Backend stories should define clear API contracts that will support the sketch-based UI development
* **Data Modeling**: Ensure data models support all the interactions and scenarios depicted in the conceptual sketches
* **Service Architecture**: Structure backend components to efficiently support the user flows emerging from the sketch documentation process

## Success Criteria

The backend epics and stories are successful when:
* All data and API requirements for the sketched user scenarios are covered
* Technical dependencies are clearly identified and sequenced appropriately
* Development teams can begin backend work immediately while UI sketching continues
* APIs will be ready to support UI development when sketch documentation is complete
