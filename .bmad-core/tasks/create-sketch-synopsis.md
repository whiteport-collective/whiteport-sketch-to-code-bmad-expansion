# create-sketch-synopsis

## Purpose

To create comprehensive synopsis documents that translate hand-drawn conceptual sketches into detailed, development-ready specifications. This task ensures every sketch has clear narrative documentation that serves as the single source of truth for both humans and AI agents.

## Process

The UX Expert will work collaboratively with the designer to document each sketched page or storyboard, following the Whiteport methodology's documentation standards.

### 1. Sketch Analysis and Context Setting

#### **Initial Sketch Review**
- Review the hand-drawn sketch with the designer
- Understand the user scenario and context for this specific page
- Identify the business-critical elements that were the focus
- Note any areas of selective focus or "willful blindness"

#### **User Journey Context**
- Connect the sketch to the specific user scenario from the PRD
- Identify which persona's usage goals this sketch serves
- Understand where this page fits in the overall user flow
- Document the user's emotional state and context at this point

### 2. Synopsis Document Creation

#### **Structured Documentation Approach**
Using the synopsis template, create a comprehensive document that includes:

**Sketch Reference**: Direct link to the sketch image file
**Sketch Context**: User situation and page purpose in the journey
**Page Structure**: Hierarchical breakdown of all visual elements
**Referenced Components**: Links to reusable component specifications
**Interactions and Effects**: Animation and interaction requirements
**Content and Assets**: Text, image, and media specifications
**Open Questions**: Undefined or unclear design elements

#### **Detail Level Guidelines**
- **Completeness**: Every element in the sketch must be documented
- **Clarity**: Descriptions should be unambiguous for developers
- **Traceability**: Clear connection to user scenarios from PRD
- **Technical Feasibility**: Consider implementation constraints

### 3. Component Identification

#### **Reusability Assessment**
- Identify elements that appear (or will appear) on multiple pages
- Apply the "Component Rule": objects appearing twice become reusable components
- Document page-specific elements vs. reusable components
- Create links to component specifications in Docs/D. Components/

**WHITEPORT METHOD OVERRIDE**: Use alphabetized folder structure with scenarios (Docs/C. Scenarios/1. Signup/1.1 Public-start-page/, Docs/D. Components/) instead of default BMad organization.

#### **Component Documentation Protocol**
- For new components: Create component specification files
- For existing components: Update usage references
- Maintain central component library consistency
- Document component variants and states

### 4. Content and Asset Documentation

#### **Text Content Specification**
- **Headlines**: Write out feasible headlines when shown in sketch
- **Body Text**: Describe tone, length, and purpose
- **Interactive Text**: Specify button labels, links, form fields
- **Error Messages**: Define feedback and validation text

#### **Visual Asset Requirements**
- **Images**: Describe purpose, content, and dimensions using cloud symbol convention
- **Videos**: Specify functionality and content requirements
- **Icons**: Define meaning and interactive behavior
- **Brand Elements**: Note logo placement and brand consistency

### 5. Interaction and Animation Documentation

#### **Interactive Element Specification**
- **Button States**: Default, hover, active, disabled
- **Form Behavior**: Validation, feedback, submission flow
- **Navigation Elements**: Linking behavior and states
- **Dynamic Content**: Loading states, updates, real-time changes

#### **Animation and Transition Requirements**
- **Page Transitions**: How users move between views
- **Micro-interactions**: Hover effects, click feedback
- **Loading States**: Progress indicators and skeleton screens
- **Error States**: How problems are communicated visually

### 6. Responsive and Accessibility Considerations

#### **Responsive Design Documentation**
- **Breakpoint Behavior**: How layout adapts to different screen sizes
- **Content Priority**: What elements are most important on smaller screens
- **Touch Interactions**: Mobile-specific interaction requirements
- **Cross-Platform Consistency**: Alignment with web and mobile platforms

#### **Accessibility Requirements**
- **Alt Text**: Descriptions for all images and visual elements
- **Keyboard Navigation**: Tab order and keyboard accessibility
- **Screen Reader Support**: ARIA labels and semantic structure
- **Color and Contrast**: Accessibility compliance requirements

### 7. Quality Assurance and Validation

#### **Synopsis Review Checklist**
- [ ] Every sketch element is documented
- [ ] Component references are accurate and complete
- [ ] Content specifications are detailed enough for implementation
- [ ] Interactions are clearly defined with all states
- [ ] Technical implementation is feasible
- [ ] Connection to user scenarios is clear

#### **Cross-Document Consistency**
- [ ] Terminology follows Whiteport standards
- [ ] Component references match central library
- [ ] User scenario alignment is maintained
- [ ] Technical constraints are respected

## Output

A complete synopsis document that includes:
- **Comprehensive Documentation**: Every sketch element explained
- **Component Integration**: Links to reusable component library
- **Development Specifications**: Technical requirements and constraints
- **User Context**: Clear connection to scenarios and usage goals
- **Quality Validation**: Reviewed and validated documentation

## Integration with Whiteport Workflow

### **Connection to User Scenarios**
- Synopsis documents directly support the scenarios defined in the PRD
- Each sketch serves specific persona usage goals
- Documentation enables traceability from trigger map to implementation

### **Component Library Development**
- Synopsis creation identifies and documents reusable components
- Central component library grows organically through sketch documentation
- Component specifications provide single source of truth

### **Development Handoff Preparation**
- Synopsis documents serve as primary development specifications
- Clear technical requirements enable accurate story creation
- Quality documentation reduces development ambiguity

### **PM Coordination**
- Synopsis documents inform UI epic and story creation
- Technical specifications guide development planning
- Component documentation supports development estimation

## Best Practices

### **Collaborative Documentation**
- Work directly with the designer during synopsis creation
- Ask clarifying questions about sketch intentions
- Validate understanding before finalizing documentation
- Iterate based on designer feedback and clarification

### **Technical Feasibility**
- Consider platform constraints during documentation
- Validate that interactions are technically possible
- Note any areas requiring technical consultation
- Plan for graceful degradation when necessary

### **Documentation Quality**
- Use clear, unambiguous language throughout
- Provide specific rather than generic descriptions
- Include examples and clarifications when helpful
- Maintain consistency with established terminology

This task ensures that the designer's creative vision, captured in hand-drawn sketches, is accurately translated into actionable development specifications while maintaining the collaborative spirit of the Whiteport methodology.
