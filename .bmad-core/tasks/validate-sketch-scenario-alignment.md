# validate-sketch-scenario-alignment

## Purpose

To ensure that all user scenarios defined in the PRD are properly represented in the sketch documentation and that the sketches successfully address the user driving forces identified in the trigger map. This validation task bridges the design and development phases by confirming that nothing critical has been lost in translation.

## Process

The PM will systematically review the alignment between trigger map goals, PRD scenarios, sketch documentation, and emerging epic/story requirements to ensure consistency and completeness.

### Trigger Map to PRD Validation

* **Goal Coverage**: Verify that all user driving forces from the trigger map are addressed in PRD user scenarios
* **Target Group Representation**: Confirm that scenarios cover all prioritized target user groups appropriately
* **Business Goal Alignment**: Ensure PRD scenarios support the achievement of business goals from trigger map
* **Priority Consistency**: Validate that scenario prioritization reflects trigger map insights

### PRD to Sketch Validation

* **Scenario Coverage**: Confirm that every user scenario in the PRD has corresponding sketch exploration
* **User Flow Completeness**: Verify that sketches cover complete user journeys, not just individual pages
* **Edge Case Consideration**: Check that sketches address error states and edge cases mentioned in scenarios
* **Context Accuracy**: Ensure sketches reflect the user context and motivations described in scenarios

### Sketch Documentation Quality Review

* **Synopsis Completeness**: Review all synopsis documents for completeness and clarity
* **Component Consistency**: Verify that component usage is consistent across different page sketches
* **Technical Feasibility**: Assess whether sketched interactions are technically implementable
* **Content Strategy**: Confirm that content requirements support user goals from trigger map

### Development Readiness Assessment

* **Backend Readiness**: Verify that backend epics support all data and functionality needs shown in sketches
* **UI Epic Alignment**: Ensure that planned UI epics comprehensively cover all sketched interactions
* **Dependency Management**: Confirm that dependencies between backend and UI work are properly identified
* **Quality Criteria**: Validate that acceptance criteria can verify achievement of original user goals

## Elicitation Requirements

elicit: true
format: structured-review

### Review Questions

1. **Scenario-Sketch Mapping**: "Can you trace each user scenario from the PRD to specific sketches and synopsis documents?"

2. **Goal Achievement Validation**: "Looking at the finalized sketches, will users be able to achieve their positive goals and avoid their negative goals from the trigger map?"

3. **User Experience Continuity**: "Do the sketches create a coherent user experience that flows naturally from scenario to scenario?"

4. **Technical Completeness**: "Are there any user interactions or data requirements shown in sketches that aren't covered by the planned backend epics?"

5. **Component Reusability**: "Are the identified reusable components sufficient to build all sketched pages efficiently?"

6. **Content Strategy**: "Is the content strategy clear enough to support copywriting and asset creation for all sketched elements?"

7. **Quality Assurance**: "Can the original user goals from the trigger map be used to create meaningful user acceptance tests?"

## Output

A comprehensive validation report including:

* **Alignment Matrix**: Table showing trigger map goals → PRD scenarios → sketches → epics/stories traceability
* **Gap Analysis**: Any missing connections or incomplete coverage between phases
* **Risk Assessment**: Potential issues that could impact successful achievement of user goals
* **Recommendation Summary**: Specific actions needed to address any identified gaps
* **Development Readiness Score**: Assessment of how ready the project is for development handoff

## Validation Criteria

The alignment validation is successful when:

* **Complete Traceability**: Every user goal from trigger map can be traced through to specific user stories
* **No Orphaned Work**: Every epic and story connects back to user scenarios and trigger map goals
* **Technical Feasibility**: All sketched interactions have clear implementation paths
* **User Experience Coherence**: Sketches create a logical and satisfying user experience
* **Quality Measurability**: Success can be measured against original trigger map goals

## Remediation Guidance

If gaps are identified:

* **Missing Scenarios**: Work with analyst to refine trigger map or add PRD scenarios
* **Incomplete Sketches**: Collaborate with UX Expert to address sketch gaps
* **Technical Issues**: Revise backend epics or simplify sketched interactions
* **Component Problems**: Update component library and affected synopsis documents
* **Content Gaps**: Create additional content requirements and asset specifications

## Integration with Development Handoff

* **Handoff Documentation**: This validation creates the final documentation package for development teams
* **Acceptance Criteria**: Validation insights inform user story acceptance criteria
* **Testing Strategy**: Validation report guides QA testing approach and user testing scenarios
* **Success Metrics**: Original trigger map goals become the foundation for measuring development success
