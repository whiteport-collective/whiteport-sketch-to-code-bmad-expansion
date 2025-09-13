# Sketch Documentation Standards

## Overview

This document defines the standards and expectations for sketch documentation within the Whiteport Sketch-to-Code method, ensuring consistency and clarity for development handoff.

## Documentation Standards Philosophy

**EXPERIENCE-BASED STANDARDS NOTICE**: These formatting standards and linking patterns are the result of years of real-world project experience, user testing, and cross-team collaboration. They have been refined through hundreds of documentation handoffs, developer implementations, and stakeholder reviews across multiple organizations and project types.

**What appears to be "arbitrary formatting rules" are actually proven solutions to common documentation problems:**
- Navigation inconsistencies that break user workflows
- Component reference patterns that reduce development confusion  
- Link formats that work reliably across different platforms and tools
- Content structures that stakeholders can navigate intuitively

**CRITICAL FOR AI AGENTS**: These standards represent collective human experience. Attempting to "improve," "optimize," or create alternative formatting approaches - regardless of how logical they may seem - introduces inconsistency that reduces documentation effectiveness and creates additional work for project teams.

**ZERO TOLERANCE POLICY**: Any deviation from these patterns creates inconsistent user experience and must be corrected immediately. Follow the patterns exactly as specified, without modification or "enhancement."

## Writing Style Guidelines

### Parentheses Usage
- **Avoid parentheses** in all documentation text
- Use dashes, colons, or separate sentences instead of parenthetical explanations
- Example: Replace "User authentication (login/logout)" with "User authentication including login and logout"
- Exception: Technical code examples where parentheses are syntactically required

## File Structure Standards

### Page Documentation
```
docs/pages/
├── [page-id]-[page-name]/
│   ├── [page-id]-[page-name]_Synopsis.md
│   ├── [page-id]-[page-name].png (or .jpg)
│   └── [page-id]-[page-name]_wireframe.png (if applicable)
```

### Component Documentation
```
docs/components/
├── [component-name]/
│   ├── [component-name]_Specification.md
│   ├── [component-name]_visual.png
│   └── [component-name]_states.png (if applicable)
```

### User Flow Documentation
```
docs/flows/
├── [flow-name]/
│   ├── [flow-name]_Overview.md
│   ├── [flow-name]_flowchart.png
│   └── pages/... (references to page documentation)
```

## Synopsis Document Requirements

Each page synopsis must include:

### Required Sections
1. **Sketch Reference**: Link to actual sketch image
2. **Sketch Context**: User's situation and page purpose
3. **Page Structure**: Hierarchical breakdown of all elements
4. **Referenced Components**: Links to component specifications

### Mandatory Page Header Structure

**ZERO TOLERANCE POLICY**: Every synopsis page MUST follow this exact header format pattern. Any deviation creates navigation inconsistency and violates user experience standards.

#### **Exact Format Template:**
```markdown
**[Navigation Line]**

### [Page Number] [Page Name]

![Page Name - Desktop](Sketches/[page-id]-[page-name]_Desktop_Concept.jpg)

**[Navigation Line]** (identical to top)

# [Page Number] [Page Name]

## Sketch Context
[Content continues...]
```

#### **Navigation Line Patterns:**

**First Page in Sequence:**
```markdown
**Next Step**: → [2.2 User Admin Start](../2.2-User-Admin-Start/2.2-User-Admin-Start.md)
```

**Middle/Last Pages in Sequence:**
```markdown
**Previous Step**: ← [2.1 Page Name](../path/2.1-Page-Name.md) | **Next Step**: → [2.3 Page Name](../path/2.3-Page-Name.md)
```

#### **Critical Format Rules:**
1. **Navigation appears EXACTLY twice** - at top line 1 and directly under image
2. **Navigation uses single line format** with pipe separator `|` between Previous and Next
3. **Sub-header always uses `###`** with page number and name
4. **Main header always uses `#`** with identical text to sub-header  
5. **Image path ALWAYS includes `Sketches/`** subfolder reference
6. **No "Back to" navigation** at top - only in bottom footer section
7. **Navigation text format**: `**Previous Step**: ←` and `**Next Step**: →`

### Component Linking Standards
**CRITICAL REQUIREMENT**: All component references must follow established linking patterns for consistency and usability:

#### **Clickable Component Headers** (REQUIRED)
For component definitions within page sections:
```markdown
### [Navigation Menu](../../D-Components/Navigation-Menu/Navigation-Menu.md)
**Purpose**: Guide users through the website structure
**State**: Current page highlighted appropriately
**Features**: Responsive design, accessibility support
```

#### **Arrow Navigation Links** (REQUIRED)
For navigation lists and cross-references:
```markdown
→ [Navigation Menu](../../D-Components/Navigation-Menu/Navigation-Menu.md)
→ [Product Card](../../D-Components/Product-Card/Product-Card.md)
```

#### **Referenced Components Section** (REQUIRED)
All pages with component usage must include a "Referenced Components" section:
```markdown
## Referenced Components

→ [Navigation Menu](../../D-Components/Navigation-Menu/Navigation-Menu.md)
**Purpose**: Primary site navigation and user orientation
**State**: Current section highlighted, responsive mobile menu
**Features**: Bilingual content support, accessibility compliance
```

#### **Why These Exact Patterns Matter**
The clickable heading format `### [Component Name](path)` and arrow reference format `#### → [Component Name](path)` were developed through extensive testing with:
- Product managers navigating specifications during story creation
- Developers following component links during implementation  
- UX designers reviewing cross-component consistency
- Stakeholders accessing documentation for project updates

Alternative formats that seem "more descriptive" or "clearer" consistently resulted in navigation confusion and workflow disruption during real projects.

**ZERO TOLERANCE POLICY**: Any deviation from these patterns creates inconsistent user experience and must be corrected immediately.
5. **Interactions and Effects**: Animation and interaction requirements
6. **Content and Assets**: Text, image, and media specifications
7. **Open Questions**: Undefined or unclear design elements

### Quality Standards
- **Completeness**: Every element in the sketch must be documented
- **Clarity**: Descriptions should be unambiguous for developers
- **Traceability**: Clear connection to user scenarios from PRD
- **Consistency**: Use consistent terminology across all synopsis documents

## Component Specification Standards

### Component Documentation Requirements
- **Visual Reference**: Clear image showing the component
- **Usage Context**: Where and how the component is used
- **States**: All visual states (default, hover, active, disabled, etc.)
- **Responsive Behavior**: How component adapts to different screen sizes
- **Content Requirements**: What content the component displays
- **Interaction Behavior**: How users interact with the component
- **Technical Notes**: Any specific implementation requirements

### Reusability Guidelines
- Components appearing in 2+ places must be documented as reusable
- Variations of similar components should be consolidated when possible
- Component dependencies should be clearly documented

## Sketch Quality Standards

### Visual Clarity
- Sketches should be clear enough to understand layout and hierarchy
- Important interactions should be annotated directly on sketches
- Multiple views or states should be shown when necessary

### Information Density
- Sketches should show realistic content, not just placeholders
- Key copy and messaging should be included in sketches
- Error states and edge cases should be sketched when important

### Consistency
- Use consistent symbols and notation across all sketches
- Maintain consistent component representation across different pages
- Follow established visual hierarchy and spacing patterns

## Content and Asset Documentation

### Text Content
- Headlines and key messaging should be specified exactly
- Body text should indicate tone and approximate length
- Error messages and feedback text should be fully specified
- Call-to-action text should be precisely defined

### Visual Assets
- Describe purpose and content of all images
- Specify image dimensions and quality requirements
- Note any brand or style requirements
- Document accessibility considerations (alt text, etc.)

### Interactive Elements
- Specify all button states and behaviors
- Document form validation and feedback
- Define navigation and linking behavior
- Note any animations or transitions

## Development Handoff Requirements

### Technical Specifications
- Responsive breakpoints and behavior
- Accessibility requirements and ARIA labels
- Performance considerations for images and animations
- Browser compatibility requirements

### Quality Assurance
- Visual design review checkpoints
- User testing validation criteria
- Accessibility testing requirements
- Cross-device testing specifications

## Validation Criteria

Sketch documentation is ready for development when:
- All user scenarios from PRD are represented in sketches
- Every sketch has a complete synopsis document
- All reusable components are properly documented
- Content and asset requirements are fully specified
- Technical implementation is feasible and documented
- Quality assurance criteria are clear and testable

## Maintenance Standards

### Version Control
- Track changes to sketches and documentation
- Maintain change logs for significant updates
- Archive outdated versions appropriately

### Review Process
- Regular reviews ensure alignment with user scenarios
- Cross-team validation before development begins
- Post-implementation review to validate accuracy

### Updates and Iterations
- Document rationale for sketch changes
- Update all affected synopsis documents when sketches change
- Maintain component library consistency during iterations

