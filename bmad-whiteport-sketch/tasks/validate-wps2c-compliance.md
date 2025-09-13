# validate-wps2c-compliance

## Purpose

To perform comprehensive WPS2C standards validation across all documentation, identify compliance violations, and generate actionable reports for systematic fixes. This task ensures documentation maintains A+ WPS2C compliance grade before proceeding with any new work.

## Process

The UX Expert systematically validates all documentation against WPS2C standards and provides detailed compliance assessment with specific remediation steps.

### 1. Header Format Validation

#### **Scenario Page Header Compliance Check**
- Scan all scenario pages for exact header format compliance
- Verify mandatory double navigation pattern (top line 1 and directly under image)
- Check for correct **Previous Step**: ← and **Next Step**: → format
- Validate navigation text uses proper display names
- Identify any deviations from WPS2C Zero Tolerance Policy

#### **Required Header Format Template**
```markdown
**Previous Step**: ← [Page Name](../path/page.md) | **Next Step**: → [Page Name](../path/page.md)

### [Page Number] [Page Name]

![Page Name - Desktop](Sketches/page-name_Desktop_Concept.jpg)

**Previous Step**: ← [Page Name](../path/page.md) | **Next Step**: → [Page Name](../path/page.md)

# [Page Number] [Page Name]
```

### 2. Component Organization Validation

#### **Atomic/Molecular/Organism Structure Check**
- Verify all components are organized in proper WPS2C structure:
  - **Atomic**: buttons, inputs, icons, cards (basic building blocks)
  - **Molecular**: forms, navigation, modals (combinations of atoms)
  - **Organism**: headers, layouts, dashboards (complex combinations)
- Identify components in wrong locations or flat structure
- Check for proper folder hierarchy and naming conventions

#### **Component Classification Criteria**
- **Atomic Components**: Single-purpose, reusable building blocks
- **Molecular Components**: Combinations of 2-3 atomic components
- **Organism Components**: Complex combinations with multiple molecules/atoms

### 3. Path Validation and GitHub Compatibility

#### **Absolute Path Compliance Check**
- Scan all component references for path format
- Identify relative paths (../../D-Components/) that break GitHub web interface
- Verify absolute paths (/docs/D-Components/) are used consistently
- Test component link functionality in GitHub web viewer context

#### **Link Integrity Validation**
- Verify all component paths point to existing files
- Check for broken links or incorrect path references
- Validate component linking standards compliance:
  - Component headers: `### [Component Name](/docs/D-Components/category/Component/Component.md)`
  - Navigation lists: `→ [Component Name](/docs/D-Components/category/Component/Component.md)`

### 4. Documentation Standards Compliance

#### **Zero Tolerance Parentheses Policy Check**
- Scan all documentation for parentheses usage
- Identify violations and suggest dash/colon alternatives
- Verify professional language standards compliance

#### **Title-Case-With-Dashes Naming Validation**
- Check all folder and file names for URL-safe naming
- Identify spaces, special characters, or case-sensitive issues
- Verify consistency across entire documentation structure

#### **Bilingual Content Format Check**
- Validate SE/EN content follows established patterns
- Check for proper indentation and structure
- Verify consistency with project bilingual requirements

### 5. Compliance Report Generation

#### **Comprehensive Assessment Report**
Create detailed report including:
- **Overall Compliance Grade**: A+ to F scale with specific score
- **Critical Issues**: Header format violations, broken component organization
- **Major Issues**: Path format problems, component linking violations
- **Minor Issues**: Naming convention inconsistencies, formatting deviations
- **Remediation Plan**: Prioritized list of specific fixes needed

#### **Actionable Fix List**
For each issue identified:
- **Issue Type**: Critical/Major/Minor classification
- **Location**: Specific file and line number
- **Current State**: What exists now
- **Required Fix**: Exact correction needed
- **Impact**: How this affects stakeholder navigation/functionality

### 6. Systematic Fix Recommendations

#### **Priority-Based Remediation**
1. **Critical (Fix Immediately)**: Header format violations, broken component paths
2. **Major (Fix Before New Work)**: Component organization, path format issues
3. **Minor (Fix During Maintenance)**: Naming conventions, formatting consistency

#### **Batch Processing Recommendations**
- Suggest use of *batch-update-paths for path corrections
- Recommend *organize-components-systematically for structure fixes
- Propose *standardize-all-headers for header format corrections

## Output

A comprehensive WPS2C compliance report that includes:
- **Executive Summary**: Overall compliance status and grade
- **Detailed Issue Inventory**: Complete list of violations with locations
- **Remediation Roadmap**: Prioritized fix plan with specific commands
- **Quality Gate Status**: Pass/Fail determination for proceeding with new work
- **GitHub Compatibility Assessment**: Web interface navigation functionality

## Integration with Whiteport Workflow

### **Pre-Work Validation Protocol**
- MANDATORY execution before any documentation work begins
- Blocks new work if compliance issues exist
- Ensures consistent A+ documentation quality

### **Quality Assurance Integration**
- Provides systematic validation framework
- Enables proactive issue prevention
- Supports professional stakeholder experience

### **Continuous Improvement Support**
- Identifies patterns in compliance violations
- Informs process improvements and training needs
- Maintains documentation excellence over time

## Best Practices

### **Systematic Approach**
- Follow validation checklist methodically
- Document all findings with specific locations
- Provide actionable remediation steps for each issue

### **Stakeholder Focus**
- Prioritize issues that affect navigation and usability
- Consider GitHub web interface user experience
- Ensure professional presentation standards

### **Prevention-Oriented**
- Identify root causes of compliance violations
- Recommend process improvements to prevent recurrence
- Build quality into documentation workflow from start

This task ensures that WPS2C compliance becomes a systematic, measurable aspect of documentation quality rather than an ad-hoc concern, supporting professional stakeholder experience and seamless cross-platform functionality.
