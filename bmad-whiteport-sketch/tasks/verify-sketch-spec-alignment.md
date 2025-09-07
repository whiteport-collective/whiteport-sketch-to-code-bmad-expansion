# Verify Sketch-Spec Alignment Task

## Purpose
Actively identify each interface element in the sketch and confirm design and outline against specifications before development begins, ensuring perfect coherence between visual design intent and documented requirements.

## When to Use
- Before starting any UI development work
- After receiving sketches and specifications for a feature
- When sketches or specifications have been updated during development
- As part of mandatory WPS2C development methodology verification

## Core Principle
**Sketch and specifications must make coherent sense together before implementation begins.** The developer must understand exactly what to build by confirming every interface element exists in both visual design and written specifications.

## Verification Process

### Step 1: Sketch Analysis - Interface Element Identification
**Systematically identify every interface element in the sketch**:
- [ ] **Navigation elements** - menus, breadcrumbs, back buttons, tab bars
- [ ] **Content elements** - headings, text blocks, images, videos, cards
- [ ] **Interactive elements** - buttons, links, form fields, toggles, sliders
- [ ] **Feedback elements** - loading indicators, error messages, success states
- [ ] **Layout elements** - containers, grids, spacing, visual hierarchy
- [ ] **Data elements** - lists, tables, charts, dynamic content areas

### Step 2: Specification Cross-Reference
**For each identified interface element, confirm in specifications**:
- [ ] **Element purpose** - What does this element do and why is it needed?
- [ ] **Content requirements** - What text, images, or data does it display?
- [ ] **Interaction behavior** - How does the user interact with this element?
- [ ] **Visual specifications** - Colors, fonts, sizing, spacing requirements
- [ ] **Responsive behavior** - How does it adapt to different screen sizes?
- [ ] **Accessibility requirements** - ARIA labels, keyboard navigation, screen reader support

### Step 3: Coherence Validation
**Ensure sketch and specifications make sense together**:
- [ ] **No missing elements** - Every sketch element has specification coverage
- [ ] **No orphaned specifications** - Every specification has visual representation
- [ ] **Interaction clarity** - User interaction patterns are clear and consistent
- [ ] **Content alignment** - Specified content fits designated visual spaces
- [ ] **Technical feasibility** - Specified functionality can be implemented as designed

### Step 4: Gap Identification and Designer Consultation
**If discrepancies are found, describe to designer and request guidance**:

#### Missing from Sketch
- Document specification requirements that lack visual representation
- Request sketch updates or clarification on visual design intent
- Confirm whether missing elements should be added to sketch

#### Missing from Specifications
- Document interface elements visible in sketch but not specified
- Request specification updates covering interaction behavior and requirements
- Confirm design intent for unspecified elements

#### Inconsistencies Between Sketch and Specifications
- Document where visual design conflicts with written requirements
- Present both versions to designer for clarification
- Request resolution ensuring both sketch and specifications align

## Exceptions to Verification Requirement

### Backend Functionality
- Database operations, API integrations, data processing
- Server-side logic, authentication flows, background tasks
- Infrastructure setup, deployment configurations

### Explicit Designer Requests
- When designer explicitly asks developer to propose UI solution
- When designer requests developer creativity for specific elements
- When designer delegates design decisions to developer expertise

### Data-Only Features
- Database schema modifications, data migration scripts
- Configuration files, environment variables
- Non-user-facing technical implementation

## Escalation Protocol

### When to Flag as Blocker
- **Major missing elements** - Core functionality lacks visual design
- **Conflicting requirements** - Sketch and specifications contradict each other
- **Unclear interaction patterns** - User experience flow is ambiguous
- **Technical impossibility** - Specified design cannot be implemented as shown

### Designer Communication Format
```
**Sketch-Spec Alignment Issue Identified**

**Element**: [Specific interface element name]
**Issue Type**: Missing from [sketch/specifications] | Conflicting requirements | Unclear interaction

**Details**: [Specific description of what is missing or conflicting]

**Impact**: [How this affects implementation and user experience]

**Request**: [Specific guidance needed from designer]
```

## Completion Criteria
- [ ] Every interface element in sketch has been identified and catalogued
- [ ] Every identified element has corresponding specification coverage
- [ ] All discrepancies have been documented and presented to designer
- [ ] Designer guidance has been received and incorporated
- [ ] Perfect coherence achieved between sketch and specifications
- [ ] Clear understanding of exactly what to implement and how

## Quality Standards
- **Comprehensive Coverage**: No interface element overlooked or assumed
- **Clear Communication**: Discrepancies presented professionally and specifically
- **Designer Partnership**: Collaborative resolution ensuring design intent preservation
- **Implementation Readiness**: Complete understanding before development begins
- **Documentation Quality**: All clarifications captured in specifications

## Success Indicators
- Developer can explain every interface element and its purpose
- No assumptions needed to bridge gaps between sketch and specifications
- Designer confirms alignment meets design intent
- Implementation can proceed with confidence and clarity
- Future developers can understand requirements from documentation alone
