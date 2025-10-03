# Documentation Review and Quality Standards

## Purpose

Establish comprehensive quality assurance standards for documentation review, progress tracking, and content example development based on learnings from real-world documentation projects.

## Documentation Review Excellence

### MANDATORY PRE-DOCUMENTATION REVIEW
**CRITICAL REQUIREMENT**: ALL Whiteport Agents MUST perform comprehensive documentation review before creating, modifying, or editing ANY document. This is NON-NEGOTIABLE.

#### **Required Review Process for ALL Agents**
1. **WPS2C Standards Review**: Read complete WPS2C documentation standards
2. **Project Context Review**: Read project brief, trigger map, and existing scenarios
3. **Naming Conventions Check**: Verify Title-Case-With-Dashes requirements
4. **Component Linking Standards**: Confirm proper clickable header and arrow link patterns
5. **Bilingual Requirements**: Verify SE/EN content format when applicable
6. **File Structure Standards**: Ensure fidelity-based folder organization

#### **Component Linking Compliance Check**
Before ANY component reference work, verify:
- ✅ Component headers use clickable format: `### [Component Name](path)`
- ✅ Navigation lists use arrow format: `→ [Component Name](path)`
- ✅ Referenced Components sections are properly structured
- ✅ All relative paths are correct and tested

### Critical Success Principles

**Content Format Decision Framework**:
- **Human Review Required**: Use clean, readable formatting without code blocks
- **Technical Implementation**: Use code blocks only when showing actual code syntax  
- **Mixed Context**: Prioritize readability while maintaining technical accuracy
- **User-Centric Design**: Always prioritize user needs over technical convenience

### Systematic Review Process

Before finalizing any documentation, perform these quality checks:

1. **Link Integrity Verification**
   - Test all markdown links to ensure they point to existing files
   - Verify relative paths are correct after any file reorganization
   - Check that image references and assets are accessible

2. **Naming Consistency Audit**
   - Ensure consistent capitalization throughout (e.g., "ProductName", not "productname")
   - Verify consistent terminology and component naming
   - Check for spelling errors and typos

3. **Formatting Standards Check**
   - Review markdown syntax for proper bold/italic usage
   - Verify heading hierarchy follows logical structure
   - Ensure list formatting is consistent
   - Check code block formatting and syntax highlighting

4. **File Reference Accuracy**
   - Confirm all image references point to existing files
   - Verify file paths are correct after component reorganization
   - Test that all cross-references work properly

5. **Content Structure Validation**
   - Ensure examples follow established patterns and specifications
   - Verify multi-language content is consistent when required
   - Check that content matches documented structure requirements

## Progress Tracking Excellence

### Accurate Status Management
- **Update Page To-Do Lists**: Reflect actual completion status, removing finished items and adding newly discovered requirements
- **Documentation Progress Tracking**: Update project README and overview files to show real accomplishments vs. outstanding work
- **Component Status Management**: Track which components are fully documented vs. need additional work
- **Example Integration Status**: Monitor which pages have complete, realistic content examples

### To-Do List Best Practices
- Remove completed items immediately after finishing work
- Add newly discovered requirements to appropriate sections
- Categorize outstanding work by type (sketches, specifications, examples)
- Maintain realistic scope and priority in task descriptions

## Content Example Development Standards

### Comprehensive Example Strategy
When creating content examples:

1. **Follow Specification Patterns**
   - Ensure examples match documented structures exactly
   - For articles: 3 paragraphs + bullet list + conclusion structure
   - For metadata: "Date, time | Location | Source | Reading time" format

2. **Realistic Context**
   - Use authentic scenarios relevant to the project domain
   - Provide context-appropriate content for different page types
   - Include proper geographic and cultural references when relevant

3. **Complete Metadata**
   - Include full publication information in documented formats
   - Provide reading time estimates for user planning
   - Show source attribution and geographic context

4. **Multi-language Consistency**
   - Provide bilingual content when project requirements specify it
   - Maintain consistent translation quality and cultural appropriateness
   - Follow established language patterns from project brief

5. **Integration Value**
   - Show how examples fit within larger content ecosystem
   - Demonstrate component usage in realistic scenarios
   - Connect examples to user journey context

## Navigation Pattern Optimization

### Usability Best Practices
Apply web-standard navigation patterns:

- **Clickable Headings**: Use `### [Component Name](link)` for component definitions (most intuitive for users)
- **Arrow Navigation**: Use `→ [Link]` patterns for navigation lists and cross-references
- **Consistent Linking**: Maintain standard patterns throughout documentation for predictable user experience

### Link Pattern Guidelines

**For Component Definitions**:
```markdown
### [Component Name](path/to/component.md)
**State**: Component state information
**Purpose**: Component role and function
```

**For Navigation Lists**:
```markdown
- → [Page A](path/to/a.md) - Brief description
- → [Component B](path/to/b.md) - Brief description
```

## Systematic Documentation Review Patterns

**Context**: These review patterns emerged from comprehensive documentation quality work. Use them as a checklist to catch common issues before they become problems.

### Comprehensive Review Approach

Some teams find it helpful to conduct periodic comprehensive reviews of project documentation. Here's one approach that has proven effective:

#### **1. Cross-Reference Validation**

Check that all component and page references actually exist:

**Review Pattern**:
- Read through scenario documents and list all referenced components
- Check if each referenced component has a corresponding `.md` specification file
- Verify all internal links point to existing files
- Test markdown links to ensure no broken paths

**Common Issues to Catch**:
- References to `Button-Secondary-Small` when only `Button-Secondary` exists
- Component links pointing to wrong folder depths (`../../` vs `../../../`)
- Scenario references to components not yet specified
- Placeholder links that were never completed

**Quick Check Method**:
```
1. Search for all markdown links: `\[.*\]\(.*\.md\)`
2. Extract file paths from matches
3. Verify each file exists at that location
```

#### **2. Duplicate Content Detection**

Look for unintentional duplication that creates maintenance burden:

**What to Look For**:
- Identical feature descriptions in different sections
- Copy-pasted content with slight variations
- Duplicate component specifications
- Repeated user stories or scenarios

**Example from Practice**:
- Found "Feature 6: Performing Walk" that was identical to "Feature 2: Walk Verification"
- Both described the same functionality with same details
- Consolidation improved maintainability and reduced confusion

**Review Technique**:
- Read each major feature/component description
- Note key phrases and compare to other sections
- Question when two things seem very similar
- Verify if duplication is intentional (repeated for context) or accidental

#### **3. Naming Consistency Check**

Ensure consistent terminology and capitalization throughout:

**Patterns to Verify**:
- Component names match across all references
- Capitalization is consistent (e.g., always "Walk Booking" not "walk booking")
- Abbreviations used consistently (e.g., "UI" vs "U.I." vs "ui")
- File names match documentation titles

**Common Inconsistencies**:
- `Button-Primary-Large` in code, `Primary Large Button` in docs
- `LanguageSelector` vs `Language Selector` vs `language-selector`
- Mixed use of feature numbers (Feature 6 vs Feature Six vs F6)

**Quick Audit**:
- List all component names found in documentation
- Check variations in capitalization and formatting
- Standardize to one canonical form
- Update all references to use canonical form

#### **4. Missing Specification Detection**

Identify components mentioned but not fully specified:

**Discovery Method**:
- Scan scenario documents for component references
- Create list of all mentioned components
- Check Design System folder for matching `.md` files
- Flag missing specifications for creation

**Components Often Missed**:
- Form inputs (checkboxes, radio buttons, text areas)
- Navigation elements (breadcrumbs, pagination)
- Feedback components (loading spinners, success messages)
- Modal dialogs and overlays

**Documentation Gap Pattern**:
```
Referenced in scenarios: Checkbox, Toggle, PhoneInput, LanguageSelector
Found in Design System: Toggle, PhoneInput
Missing specs: Checkbox ✗, LanguageSelector ✗
```

#### **5. Content Accuracy & Typo Review**

Catch small errors that undermine professional quality:

**What to Review**:
- Spelling errors in body text
- Grammatical mistakes in descriptions
- Incorrect terminology or technical terms
- Factual errors in specifications

**Example Catches**:
- "Never ask who's time it is" → "Never ask whose turn it is"
- "auth" vs "authentication" inconsistency
- Swedish market references using American spellings
- Incorrect accessibility contrast ratios

**Review Aid**:
- Read content aloud to catch awkward phrasing
- Use spell-check but verify suggested corrections
- Have domain knowledge available for technical terms
- Cross-check facts (contrast ratios, dimensions) with sources

### When to Conduct Comprehensive Reviews

**Good Timing**:
- Before major milestones or stakeholder presentations
- After rapid documentation creation phases
- When team members notice inconsistencies
- Before transitioning from design to development
- Periodically during long projects (monthly/quarterly)

**Signs You Need a Review**:
- Team members reporting confusion about component names
- Developers unable to find referenced specifications
- Duplicate work happening due to missed documentation
- Stakeholders asking about inconsistencies

### Balancing Thoroughness and Progress

**Remember**: Perfect documentation on day one isn't the goal—*useful, maintainable documentation* is:

- Don't let review paralysis stop forward progress
- Document well enough to move forward, refine later
- Focus reviews on high-impact areas (core components, main scenarios)
- Accept that some rough edges are okay in early drafts
- Schedule dedicated review time rather than constant perfection

**Review Effort Guidelines**:
- **Quick pass** (30 min): Check for broken links, major typos
- **Standard review** (2-3 hours): Cross-references, naming, missing specs
- **Comprehensive audit** (full day): Everything above plus content accuracy, duplicate detection

Choose the review depth that matches your project phase and needs.

---

## Implementation Workflow

### Pre-Finalization Checklist
- [ ] All markdown links tested and working
- [ ] Naming consistency verified across all files
- [ ] Formatting standards applied consistently
- [ ] File references accurate after any reorganization
- [ ] Content examples follow specification patterns
- [ ] Progress tracking reflects actual completion status
- [ ] Navigation patterns optimized for usability

### Quality Gates
- No broken links allowed in final documentation
- All content examples must be complete and realistic
- Progress tracking must accurately reflect completion status
- Documentation must pass systematic review process

This framework ensures documentation maintains professional quality standards while providing maximum value to project stakeholders and development teams.
