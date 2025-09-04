# analyze-codebase-impact

## Task Description
Perform comprehensive codebase analysis after task completion to explore potential dependencies and bugs in other related parts of the codebase, ensuring implementation doesn't introduce issues elsewhere.

## Purpose
Maintain codebase integrity by identifying ripple effects, dependency conflicts, and potential issues in related components that may be affected by the current implementation.

## Key Analysis Areas

### 1. Dependency Impact Assessment
- **Direct Dependencies**: Analyze components that directly import or use modified code
- **Indirect Dependencies**: Identify components that may be affected through shared state, context, or utilities
- **Circular Dependencies**: Check for potential circular dependency issues introduced by changes
- **Package Dependencies**: Verify no version conflicts or missing dependencies for new features

### 2. Shared State and Context Analysis
- **Global State**: Analyze impact on React Context, Redux stores, or other global state management
- **Props Flow**: Check component prop changes don't break parent-child relationships
- **Event Handlers**: Verify event bubbling and handling still functions correctly
- **Shared Utilities**: Ensure utility function changes don't affect other consumers

### 3. Integration Point Verification
- **API Endpoints**: Verify API calls and data structures remain compatible
- **Route Changes**: Check URL structure changes don't break navigation or deep linking
- **Configuration Files**: Ensure config changes don't affect other features
- **Build Process**: Verify build pipeline and deployment aren't negatively affected

### 4. Cross-Component Compatibility
- **Styling Dependencies**: Check CSS/styling changes don't affect other components
- **Animation Conflicts**: Verify new animations don't interfere with existing ones
- **Event Conflicts**: Ensure new event handlers don't conflict with existing ones
- **Performance Impact**: Assess performance implications on other components

### 5. Accessibility and Standards Compliance
- **ARIA Relationships**: Verify ARIA labels and relationships remain intact
- **Keyboard Navigation**: Check tab order and keyboard navigation flow
- **Screen Reader Compatibility**: Ensure changes don't break screen reader functionality
- **Focus Management**: Verify focus management remains consistent

## Analysis Process

### Step 1: Component Graph Analysis
1. Map all components that import or reference modified files
2. Identify shared dependencies and utilities
3. Create dependency tree to understand impact scope
4. Document potential risk areas

### Step 2: Code Pattern Verification
1. Search for similar patterns that might need updating
2. Check for consistent implementation across related features
3. Verify naming conventions and code standards compliance
4. Identify opportunities for refactoring or standardization

### Step 3: Integration Testing Review
1. Test critical user flows that may be affected
2. Verify all related features still function correctly
3. Check responsive behavior across different screen sizes
4. Test browser compatibility for affected functionality

### Step 4: Performance Impact Assessment
1. Measure bundle size impact and loading performance
2. Check for memory leaks or performance regressions
3. Verify smooth animations and transitions
4. Assess impact on Core Web Vitals metrics

## Documentation Requirements

### Impact Analysis Report
Document findings in the story's Dev Agent Record:
- **Components Analyzed**: List all reviewed components and files
- **Dependencies Identified**: Map direct and indirect dependencies
- **Risk Assessment**: Identify potential issues and mitigation strategies
- **Performance Impact**: Report any performance implications
- **Recommended Actions**: Suggest any additional changes or monitoring

### Regression Testing Notes
- **Test Scenarios**: Document what should be tested
- **Critical Paths**: Identify user flows that require verification
- **Browser Testing**: Note any browser-specific concerns
- **Accessibility Testing**: Highlight a11y verification needs

## Success Criteria
- ✅ All dependent components identified and analyzed
- ✅ No breaking changes in related functionality
- ✅ Performance impact assessed and documented
- ✅ Accessibility compliance maintained across affected components
- ✅ Clear documentation of analysis findings
- ✅ Recommended testing scenarios provided

## Professional Standards
- **Thoroughness**: Don't assume isolated changes - analyze comprehensively
- **Documentation**: Record findings for future reference and team knowledge
- **Proactive Communication**: Flag potential issues before they become problems
- **Quality Assurance**: Ensure implementation excellence extends beyond immediate scope

## Integration with WPS2C Methodology
This task ensures that sketch-driven development and brownfield excellence extend beyond individual components to maintain system-wide integrity and professional implementation standards.
