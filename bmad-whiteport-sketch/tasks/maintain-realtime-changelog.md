# Maintain Real-Time Change Log

## Purpose
Establish and maintain live documentation of specification changes during active sessions to prevent team confusion and ensure all agents understand evolving standards and decisions.

## When to Use
- During any session that modifies existing specifications
- When making decisions that affect other team members or agents
- After implementing changes that alter established patterns
- When discovering new best practices or standards

## Real-Time Change Log Protocol

### Immediate Documentation Rule
**CRITICAL**: Document significant changes as they happen, not at session end.

### Change Categories
- **STANDARD**: New or modified documentation standards
- **STRUCTURE**: File/folder organization changes  
- **NAVIGATION**: Link structure or flow modifications
- **CONTENT**: Specification content updates
- **TEMPLATE**: Template or format changes
- **PROCESS**: Workflow or methodology updates

### Entry Format
```
YYYY-MM-DD HH:MM: [CATEGORY] - Brief description
Impact: [High/Medium/Low] - Affected areas/team members
Files: [List of changed files with links]
Rationale: Why this change was made
Next Actions: What others need to do (if any)
```

### Impact Levels

**High Impact**: 
- Changes that affect multiple team members
- Modifications to established templates or standards
- Structural changes that break existing links
- New mandatory requirements

**Medium Impact**:
- Content updates that change specifications
- Navigation improvements
- New optional standards or recommendations

**Low Impact**:
- Minor content corrections
- Cosmetic improvements
- Individual file updates without broader implications

## Implementation Steps

### Step 1: Identify Change Significance
Before making any change, assess:
- Does this affect other team members?
- Will this change existing patterns or standards?
- Could this create confusion if not documented?
- Does this establish a new precedent?

### Step 2: Document Immediately
Add entry to CHANGELOG.md immediately after implementing change:
- Use consistent format above
- Include specific file paths and line numbers when relevant
- Explain the business or technical rationale
- Note any follow-up actions required

### Step 3: Update Session Learnings
For significant discoveries, also update:
- `data/session-learnings-professional-documentation.md`
- Relevant template files if standards changed
- Agent instructions if workflow modified

### Step 4: Communicate Impact
If High Impact change:
- Explicitly mention affected team members
- Include clear next actions
- Update relevant templates or checklists
- Consider updating agent instructions

## Example Entries

### High Impact Example
```
2025-08-30 14:30: [STANDARD] - Implemented link-first documentation standard for all external document references
Impact: High - Affects all agents and team members creating documentation
Files: README.md, 00-User-Scenarios.md, all scenario overview files
Rationale: Improves navigation and follows Whiteport excellence standards
Next Actions: All future documentation must use "## → [Title](path)" format for external links
```

### Medium Impact Example
```
2025-08-30 15:15: [STRUCTURE] - Reorganized README with executive-first flow
Impact: Medium - Changes stakeholder presentation approach
Files: README.md, CHANGELOG.md (created)
Rationale: Executive feedback indicated need for business-first structure
Next Actions: Apply same structure to other project READMEs
```

### Low Impact Example
```
2025-08-30 16:00: [CONTENT] - Fixed navigation links in start page scenario
Impact: Low - Corrects broken internal links
Files: 1.1-Start-Page.md
Rationale: Links pointed to renamed folder
Next Actions: None
```

## Quality Assurance

### Before Session End
- Review all change log entries for completeness
- Ensure impact levels are accurate
- Verify all affected files are listed
- Check that rationales are clear

### Session Summary
- Count total changes by impact level
- Identify any patterns or themes
- Note lessons learned for future sessions
- Update expansion pack documentation if needed

## Integration with Agents

### Agent Awareness
All agents should:
- Check CHANGELOG.md at session start
- Understand recent changes before making recommendations
- Follow established patterns from recent entries
- Ask for clarification on unfamiliar standards

### Agent Responsibilities
When agents make changes:
- Follow this same protocol
- Document their changes immediately
- Assess impact on other agents
- Update relevant templates or standards

---

**This protocol ensures continuous documentation quality and prevents specification drift during collaborative sessions.**
