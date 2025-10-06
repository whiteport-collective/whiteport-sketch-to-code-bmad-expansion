# Validate Sketch Components

## Task Overview
This validation task helps ensure all components identified in sketches are properly documented and integrated into the design system before prototype creation. This systematic approach maintains consistency and prevents incomplete implementations.

## Task Purpose
- **Prevent Incomplete Prototypes**: Ensure all sketch elements have corresponding design system components
- **Maintain Design System Integrity**: Keep design system as single source of truth
- **Enforce Systematic Approach**: Prevent ad-hoc component creation during prototype development
- **Quality Assurance**: Verify component specifications are complete and consistent

## When to Use
- **Before** creating any prototype from sketches to ensure complete specifications
- **Before** generating frontend code to maintain design system integrity
- **After** analyzing sketches for component identification to validate completeness
- **When** user requests prototype creation to follow systematic approach

## Task Steps

### Step 1: Analyze Sketch Components
- **Identify All Elements**: List every UI element, icon, button, input, text style, etc. in the sketch
- **Categorize Components**: Classify each element as atomic, molecular, or organism
- **Check Existing Design System**: Verify which components already exist in design system
- **Identify Missing Components**: List components that need to be created or documented

### Step 2: Validate Component Completeness
- **Check Component Specifications**: Please ensure each component has proper documentation for consistency
- **Verify Design Tokens**: Please confirm components use foundation design tokens to maintain visual consistency
- **Validate Usage Guidelines**: Please check that components have clear usage instructions for team reference
- **Ensure Accessibility**: Please verify components meet accessibility standards for inclusive design

### Step 3: Create Missing Components
- **Document New Components**: Create specifications for missing components
- **Follow Atomic Design**: Organize components in proper atomic/molecular/organism structure
- **Use Consistent Naming**: Follow established naming conventions
- **Include All States**: Document all component states and variants

### Step 4: Update Design System Guide
- **Add to Interactive Showcase**: Include new components in Design System Guide
- **Update Navigation**: Ensure components are accessible via navigation
- **Test Component Display**: Verify components render correctly in showcase
- **Update Component Links**: Ensure all components are properly linked

### Step 5: Final Validation
- **Complete Component List**: Verify all sketch elements have design system counterparts
- **Test Component Integration**: Ensure components work together properly
- **Validate Design Consistency**: Check that all components follow design system patterns
- **Confirm Ready for Prototype**: Verify design system is complete for prototype creation

## Success Criteria
- **100% Component Coverage**: Every sketch element has corresponding design system component
- **Complete Documentation**: All components have proper specifications and usage guidelines
- **Design System Integration**: All components are integrated into Design System Guide
- **Consistency Validation**: All components follow established design system patterns
- **Accessibility Compliance**: All components meet accessibility standards

## Error Handling
- **Missing Components**: Please create missing components before proceeding to ensure complete specifications
- **Incomplete Specifications**: Please complete component documentation to maintain quality standards
- **Design Inconsistencies**: Please fix inconsistencies before prototype creation to ensure visual coherence
- **Integration Issues**: Please resolve design system integration problems to maintain system integrity

## Output
- **Component Validation Report**: List of all components and their status
- **Missing Components List**: Components that need to be created
- **Design System Updates**: Changes made to design system
- **Validation Confirmation**: Confirmation that design system is ready for prototype creation

## Related Commands
- `*analyze-sketch-components`: Identify components in sketches
- `*create-component-specification`: Document new components
- `*update-design-system-guide`: Update Design System Guide
- `*enforce-design-system-first`: Ensure design system is updated first

## Dependencies
- **Design System Structure**: Must have proper atomic design structure
- **Component Specifications**: Must have component documentation templates
- **Design System Guide**: Must have interactive showcase for validation

## Quality Assurance
- **Systematic Validation**: Every sketch element must be validated
- **No Exceptions**: No prototype creation without complete component validation
- **Design System Integrity**: Maintain design system as single source of truth
- **Consistency Enforcement**: Ensure all components follow established patterns

---

*This task is part of the Whiteport Sketch-to-Code (WPS2C) methodology, designed to maintain design system integrity and prevent incomplete prototype creation.*
