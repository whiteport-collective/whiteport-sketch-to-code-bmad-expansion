# analyze-existing-code

## Task Description
Perform comprehensive analysis of existing codebase to understand dependencies, integration points, potential risks, existing patterns, performance considerations, and breaking change potential before implementing new features.

## Purpose
Ensure brownfield development excellence by respecting existing implementations, identifying potential risks, and maintaining architectural consistency when adding new features.

## Steps

### 1. Component Architecture Analysis
- Identify existing component patterns and structures
- Map component hierarchies and relationships
- Document naming conventions and organizational patterns
- Identify reusable components and utilities that should be leveraged

### 2. State Management Analysis
- Analyze existing state management patterns (Context, Redux, local state)
- Identify data flow patterns and state dependencies
- Map existing state structures that new features must integrate with
- Document state update patterns and side effects

### 3. Styling System Analysis
- Identify existing CSS/styling approaches and frameworks
- Document class naming conventions and styling patterns
- Analyze existing responsive design patterns
- Identify theme systems and design tokens in use

### 4. Integration Points Analysis
- Map API integration patterns and data fetching approaches
- Identify existing utility functions and helper libraries
- Document routing patterns and navigation structures
- Analyze existing error handling and validation patterns

### 5. Performance Analysis
- Identify existing performance optimizations that must be preserved
- Analyze bundle structure and import patterns
- Document existing lazy loading and code splitting approaches
- Identify performance-critical components that should not be disrupted

### 6. Dependency Analysis
- Map external dependencies and their usage patterns
- Identify internal dependencies between components and modules
- Document shared utilities and common functionality
- Analyze potential conflicts with new feature requirements

### 7. Risk Assessment
- Identify potential breaking changes that new implementation might cause
- Document components or functionality that might be affected
- Assess performance impact of new feature integration
- Identify accessibility features that must be preserved or enhanced

## Output Requirements
- **Architecture Documentation**: Clear documentation of existing patterns and structures
- **Integration Plan**: Specific plan for how new features will integrate with existing code
- **Risk Mitigation**: Identified risks and mitigation strategies
- **Pattern Compliance**: Confirmation that new implementation will follow existing excellent patterns
- **Performance Impact**: Assessment of how new features will affect existing performance

## Success Criteria
- ✅ Complete understanding of existing codebase architecture
- ✅ Clear integration plan that respects existing patterns
- ✅ Identified and documented all potential risks
- ✅ Confirmed approach maintains or enhances existing excellent implementations
- ✅ Performance impact assessment completed

## WPS2C Compliance
- Maintain Zero Tolerance Parentheses Policy in all documentation
- Respect existing excellent implementations rather than replacing them
- Ensure new implementations enhance rather than disrupt existing quality
- Document patterns for future development consistency
