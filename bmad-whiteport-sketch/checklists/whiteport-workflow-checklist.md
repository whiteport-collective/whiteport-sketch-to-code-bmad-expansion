# Whiteport Workflow Checklist

## Pre-Sketch Phase (PM Tasks)

### Foundation Documents (Analyst Entry Point)
- [ ] Product brief is completed by Analyst (Step 1 - foundational vision and strategy)
  - [ ] Project vision and strategic direction defined
  - [ ] High-level business goals and success metrics established
  - [ ] Platform architecture and development approach outlined
- [ ] Trigger map is created based on product brief (Step 2 - detailed user-business mapping)
  - [ ] Business goals from product brief are detailed and connected to user needs
  - [ ] Target user groups identified and prioritized
  - [ ] User driving forces (positive/negative goals) mapped to business outcomes
  - [ ] User-business goal alignment documented
- [ ] Trigger map visualization created (Step 3 - stakeholder communication)
- [ ] Individual personas developed (Step 4 - detailed user research)
  - [ ] Detailed persona profiles with rich backgrounds
  - [ ] Personal context and relationship to core activity
- [ ] Foundation documents provide complete strategic and user context

### PRD Creation from Product Brief
- [ ] PRD created using sketch-driven-prd-tmpl.yaml based on product brief
- [ ] Core user scenarios extracted and formalized from product brief
- [ ] Each scenario connects to trigger map user goals via product brief
- [ ] Technical constraints from product brief are documented
- [ ] Success metrics defined and measurable

### Backend Foundation & Epic Creation (Parallel Process)
- [ ] Backend requirements identified from product brief and scenarios
- [ ] Technology stack defined (React/TypeScript, Node.js, PostgreSQL, etc.)
- [ ] Platform architecture documented (three-platform approach)
- [ ] Data models and API endpoints defined
- [ ] Authentication and authorization requirements specified
- [ ] Integration points with external systems documented (Google Workspace, Microsoft 365)
- [ ] Backend epics prioritized by dependency and value
- [ ] Backend user stories created with clear acceptance criteria
- [ ] Technical constraints and performance requirements documented

## During Scenario Outline & Sketching Phase (PM Parallel Work + Monitoring)

### Step 5: Scenario Outline Phase
- [ ] UX Expert creates detailed scenario outlines for sketching
- [ ] PM validates scenarios align with backend capabilities
- [ ] Technical feasibility confirmed for each scenario
- [ ] Cross-platform considerations documented

### Step 6: Step-by-Step Sketching Phase

### Scenario-Sketch Alignment
- [ ] All user scenarios have corresponding sketch exploration
- [ ] Sketches address the core user driving forces from trigger map
- [ ] Complex user flows are properly broken down in sketches
- [ ] Edge cases and error scenarios are considered in sketches

### Documentation Quality
- [ ] Synopsis documents are created for each sketched page
- [ ] Component library is maintained and updated
- [ ] Reusable patterns are identified and documented
- [ ] Content and asset requirements are captured

## Post-Sketch Phase (PM Tasks)

### UI Epic Creation
- [ ] All sketched pages have corresponding user stories
- [ ] Component development stories are created
- [ ] Interaction and animation requirements are specified
- [ ] Responsive design requirements are documented
- [ ] Content creation stories are included

### Development Readiness
- [ ] Backend APIs are ready to support UI development
- [ ] Component library provides clear development specifications
- [ ] User acceptance criteria include design review checkpoints
- [ ] Technical feasibility of all sketched interactions is validated

### Quality Assurance
- [ ] Visual design testing criteria are defined
- [ ] Responsive testing requirements are specified
- [ ] Accessibility requirements are included
- [ ] User testing plan connects back to trigger map goals

## Handoff Validation

### Documentation Completeness
- [ ] All user scenarios are covered by epics and stories
- [ ] Traceability from trigger map → PRD → sketches → stories is clear
- [ ] Component specifications are complete and consistent
- [ ] Content and asset requirements are fully documented

### Development Team Readiness
- [ ] Backend team can begin work immediately
- [ ] Frontend team has clear design specifications
- [ ] QA team has testable acceptance criteria
- [ ] All dependencies between teams are identified and managed

## Success Criteria

The Whiteport workflow is successful when:
- [ ] Every user goal from trigger map is addressed in final stories
- [ ] Sketches successfully guide development without ambiguity
- [ ] Backend and UI work can proceed in parallel efficiently
- [ ] Final product can be validated against original trigger map goals
